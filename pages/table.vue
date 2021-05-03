<template>
  <div id="app">
    <section class="ec-section has-wave-top has-wave-bottom ec-section-light-gray">
      <div class="container is-max-widescreen">
        <b-table
          v-if="checkedRows.length > 0"
          ref="multiSortTable"
          class="mb-5"
          :data="checkedRows"
          :mobile-cards="false"
        >
          <b-table-column v-slot="props" field="name" label="Name" sortable>
            {{ props.row.name }}
          </b-table-column>

          <b-table-column v-slot="props" field="symbol" cell-class="has-text-left" label="Symbol" sortable>
            {{ props.row.symbol }}
          </b-table-column>

          <b-table-column v-slot="props" field="rate" cell-class="has-text-left" label="Rate" sortable>
            {{ props.row.rate }}
          </b-table-column>
        </b-table>

        <div class="columns mobile-margin">
          <div class="column">
            <div class="level pb-0 pt-3">
              <div class="level-left level-item">
                <div class="level-item">
                  <h2 class="title is-4">
                    All Rates
                  </h2>
                </div>
              </div>
            </div>
          </div>
          <div class="column is-4 has-text-align-right">
            <div class="field is-grouped">
              <div class="control is-expanded has-icons-left">
                <b-input
                  v-model="filterName"
                  placeholder="Filter list"
                  icon="magnify"
                  icon-clickable
                  icon-right-clickable
                  icon-right="close-circle"
                  @icon-right-click="filterName = []"
                />
              </div><div class="field is-grouped">
                <label class="switch is-rounded"><input type="checkbox" value="false"><span class="check" /><span class="control-label">USD</span></label>
              </div>
            </div>
          </div>
        </div>

        <b-table
          ref="multiSortTable"
          class="my-2 box"
          :data="filter"
          :paginated="true"
          :per-page="20"
          :current-page.sync="currentPage"
          :pagination-position="paginationPosition"
          :mobile-cards="false"
          checkable
          checkbox-position="right"
          header-checkable="false"
          :checked-rows.sync="checkedRows"
        >
          <b-table-column v-slot="props" field="name" label="Name" sortable>
            {{ props.row.name }}
          </b-table-column>

          <b-table-column v-slot="props" field="symbol" cell-class="has-text-left" label="Symbol" sortable>
            {{ props.row.symbol }}
          </b-table-column>

          <b-table-column v-slot="props" field="rate" cell-class="has-text-left" label="Rate" sortable>
            {{ props.row.rate }}
          </b-table-column>
        </b-table>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Table',
  data () {
    return {
      checkedRows: [],
      defaultSortDirection: 'asc',
      sortIcon: 'arrow-up',
      paginationPosition: 'bottom',
      currentPage: 1,
      perPage: 20,
      rates: [],
      filterName: ''
    }
  },
  computed: {
    filter () {
      const filter = new RegExp(this.filterName, 'i')
      const data = []
      this.rates.forEach((item, index) => {
        if (this.rates[index].name.match(filter) || this.rates[index].symbol.match(filter) || String(this.rates[index].rate).match(filter)) {
          data.push(this.rates[index])
        }
      })
      return data
    }
  },
  // watch: {
  //   checkedRows () {
  //     const starCoin = []
  //     this.checkedRows.forEach((item, index) => {
  //       starCoin.push(this.rates[index])
  //     })
  //   }
  // },
  created () {
    this.$axios.$get('https://r.easycrypto.nz/json/backenddb.json').then((res) => {
      this.rates = Object.entries(res).map(e => e[1])
    })
  },
  methods: {}
}
</script>

<style scoped>

.ec-section.has-wave-bottom {
  padding-bottom: 110px;
}
.ec-section.has-wave-top {
  padding-top: 110px;
}
.ec-section-light-gray {
  background-color: #F6F9FE;
}
.ec-section {
  position: relative;
  padding: 70px 0;
}
</style>
