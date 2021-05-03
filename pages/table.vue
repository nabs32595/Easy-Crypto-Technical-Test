<template>
  <div id="app">
    <section class="ec-section has-wave-top has-wave-bottom ec-section-light-gray">
      <div class="container is-max-widescreen">
        <!--        <div class="columns mobile-margin">-->
        <!--          <div class="column">-->
        <!--            <div class="level pb-0 pt-3">-->
        <!--              <div class="level-left level-item">-->
        <!--                <div class="level-item">-->
        <!--                  <h2 class="title is-4">-->
        <!--                    All Rates-->
        <!--                  </h2>-->
        <!--                </div>-->
        <!--              </div>-->
        <!--            </div>-->
        <!--          </div><div class="column is-4 has-text-align-right">-->
        <!--            <div class="field is-grouped">-->
        <!--              <div class="control is-expanded has-icons-left">-->
        <!--                <input debounce-events="input" type="search" placeholder="Filter list" class="input is-small"><span class="icon is-small is-left"><i class="fa fa-search" /></span>-->
        <!--              </div><div class="field is-grouped">-->
        <!--                <label class="switch is-rounded"><input type="checkbox" true-value="true" value="false"><span class="check" /><span class="control-label">USD</span></label>-->
        <!--              </div>-->
        <!--            </div>-->
        <!--          </div>-->
        <!--        </div>-->
        <b-table
          ref="multiSortTable"
          :data="data"
          :paginated="true"
          :per-page="20"
          :current-page.sync="currentPage"
          :pagination-position="paginationPosition"
          :default-sort-direction="defaultSortDirection"
          :sort-icon="sortIcon"
          :mobile-cards="false"
          checkable
          checkbox-position="right"
          header-checkable="false"
          :checked-rows.sync="checkedRows"
        >
          <b-table-column v-slot="props" label="Name" sortable searchable>
            {{ props.row.name }}
          </b-table-column>

          <b-table-column v-slot="props" label="Symbol" sortable entered>
            {{ props.row.symbol }}
          </b-table-column>

          <b-table-column v-slot="props" field="symbol" label="Sell" sortable centered>
            {{ props.row.symbol }}
          </b-table-column>

          <b-table-column v-slot="props" field="symbol" label="Buy" sortable centered>
            {{ props.row.symbol }}
          </b-table-column>

          <b-table-column v-slot="props" field="symbol" label="Symbol" sortable centered>
            {{ props.row.symbol }}
          </b-table-column>

          <b-table-column v-slot="props" field="symbol" label="24h" sortable centered>
            {{ props.row.symbol }}
          </b-table-column>

          <b-table-column>
            <b-button type="is-success" rounded centered label="buy" />
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
      data: [],
      defaultSortDirection: 'asc',
      sortIcon: 'arrow-up',
      paginationPosition: 'bottom',
      currentPage: 1,
      perPage: 20,
      rates: []
    }
  },
  mounted () {

  },
  created () {
    this.$axios.$get('https://r.easycrypto.nz/json/backenddb.json').then((res) => {
      this.data = Object.entries(res).map(e => e[1])
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
