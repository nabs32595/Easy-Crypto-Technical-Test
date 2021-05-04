<template>
  <div id="app">
    <section class="has-text-centered ec-section ec-section-purple">
      <div class="container">
        <div class="columns is-variable is-4">
          <div class="column is-6 is-offset-3">
            <h1 class="title is-1 is-size-2-mobile has-text-white">
              Crypto Live Rates
            </h1>
          </div>
        </div>
      </div>
    </section>

    <section class="ec-section ec-section-light-gray">
      <div class="container is-max-widescreen column">
        <div v-if="favCoin.length>0">
          <div class="columns mobile-margin">
            <div class="column">
              <div class="level pb-0">
                <div class="level-left level-item">
                  <div class="level-item">
                    <h2 class="title is-4">
                      Favourite Coins
                    </h2>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <b-table
            ref="multiSortTable"
            class="mb-5 box box-shadow"
            :data="favCoin"
            :mobile-cards="false"
            checkable
            checkbox-position="right"
            :checked-rows.sync="checkedRows"
            header-checkable:false
          >
            <b-table-column v-slot="props" sortable field="symbol">
              <figure class="control image is-32x32">
                <img :src="`https://static.easycrypto.nz/img/coins/${props.row.symbol}.png`" :alt="props.row.name">
              </figure>
            </b-table-column>

            <b-table-column v-slot="props" field="name" label="Name" sortable>
              {{ props.row.name }}
            </b-table-column>

            <b-table-column v-slot="props" field="symbol" cell-class="has-text-left" label="Symbol" sortable>
              {{ props.row.symbol }}
            </b-table-column>

            <b-table-column v-slot="props" field="rate" cell-class="has-text-left" label="Rate" sortable>
              {{ props.row.rate ? props.row.rate: " " }}
            </b-table-column>

            <b-table-column v-slot="props" field="rate" cell-class="has-text-left" label="Buy">
              ${{ props.row.rank }}
            </b-table-column>

            <b-table-column v-slot="props" field="rate" cell-class="has-text-left" label="Sell">
              ${{ props.row.rank }}
            </b-table-column>

            <b-table-column v-slot="props">
              <b-button size="is-small" type="is-success" rounded label="Buy" @click="snackbar(props.row.rank)" />
            </b-table-column>
          </b-table>
        </div>
      </div>
    </section>

    <section class="ec-section ec-section-white">
      <div class=" container is-max-widescreen  column">
        <topCoinOfTheWeek />
      </div>
    </section>

    <section class="ec-section ec-section-light-gray">
      <div class="container is-max-widescreen column">
        <div class="columns mobile-margin">
          <div class="column">
            <div class="level">
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
              </div>
            </div>
          </div>
        </div>

        <b-table
          ref="multiSortTable"
          class="box box-shadow"
          :data="filter"
          :paginated="true"
          :per-page="20"
          :current-page.sync="currentPage"
          :pagination-position="paginationPosition"
          :mobile-cards="false"
          checkable
          checkbox-position="right"
          :checked-rows.sync="checkedRows"
          default-sort="symbol"
          header-checkable:false
        >
          <b-table-column v-slot="props" sortable field="symbol">
            <figure class="control image is-32x32">
              <img :src="`https://static.easycrypto.nz/img/coins/${props.row.symbol}.png`" :alt="props.row.name">
            </figure>
          </b-table-column>

          <b-table-column v-slot="props" field="name" label="Name" sortable>
            {{ props.row.name }}
          </b-table-column>

          <b-table-column v-slot="props" field="symbol" cell-class="has-text-left" label="Symbol" sortable>
            {{ props.row.symbol }}
          </b-table-column>

          <b-table-column v-slot="props" field="rate" cell-class="has-text-left" label="Rate" sortable>
            {{ props.row.rate }}
          </b-table-column>

          <b-table-column v-slot="props" field="rate" cell-class="has-text-left" label="Buy">
            ${{ props.row.rank }}
          </b-table-column>

          <b-table-column v-slot="props" field="rate" cell-class="has-text-left" label="Sell">
            ${{ props.row.rank }}
          </b-table-column>

          <b-table-column v-slot="props">
            <b-button size="is-small" type="is-success" rounded label="Buy" @click="snackbar(props.row.rank)" />
          </b-table-column>
        </b-table>
      </div>
    </section>
  </div>
</template>

<script>

import TopCoinOfTheWeek from '../components/topCoinOfTheWeek'

export default {
  name: 'Table',
  components: { TopCoinOfTheWeek },
  data () {
    return {
      favCoin: [],
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
  watch: {
    checkedRows () {
      localStorage.setItem('favCoin', JSON.stringify(this.checkedRows))
      if (this.favCoin) {
        this.favCoin = this.checkedRows
      }
    }
  },
  created () {
    this.$axios.$get('https://r.easycrypto.nz/json/backenddb.json').then((res) => {
      this.rates = Object.entries(res).map(e => e[1])
    })
  },
  mounted () {
    this.favCoin = JSON.parse(localStorage.getItem('favCoin') || '[]')
  },
  methods: {
    snackbar (payload) {
      this.$buefy.snackbar.open({
        type: 'is-success',
        message: `$${payload} has been transferred to your account 😀`
      })
    }
  }
}
</script>

<style scoped>
.ec-section {
  position: relative;
  padding: 50px 0;
}

.ec-section-light-gray {
  background-color: #f6f9fd;
}

.ec-section-purple {
  background: url('http://easycrypto.ai/assets/images/purple.jpg') top center no-repeat #3c0e9b;
  background-size: cover;
}

</style>
