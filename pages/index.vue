<template>
  <div>
    <section class="has-text-centered mb-6 ec-section has-wave-bottom ec-hero-page ec-section-purple">
      <div class="container">
        <div class="columns is-variable is-4">
          <div class="column is-6 is-offset-3">
            <h1 class="title is-1 is-size-2-mobile has-text-white">
              Crypto Live Rates
            </h1><!---->
          </div>
        </div>
      </div><!----><svg
        width="1440px"
        height="37px"
        viewBox="0 0 1440 37"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        class="ec-wave-bottom"
      ><g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"><g transform="translate(0.000000, -2010.000000)" fill="#FFFFFF" fill-rule="nonzero"><g transform="translate(0.000000, 1380.000000)"><g transform="translate(0.000000, 630.000000)"><path d="M0,0 L48,3.7 C96,7.4 192,14.8 288,18.5 C384,22.2 480,22.2 576,19.725625 C672,17.34375 768,12.25625 864,8.625625 C960,4.85625 1056,2.54375 1152,4.925625 C1248,7.4 1344,14.8 1392,18.5 L1440,22.2 L1440,37 L1392,37 C1344,37 1248,37 1152,37 C1056,37 960,37 864,37 C768,37 672,37 576,37 C480,37 384,37 288,37 C192,37 96,37 48,37 L0,37 L0,0 Z" /></g></g></g></g></svg>
    </section>

    <section class="ec-section has-wave-top has-wave-bottom ec-section-light-gray">
      <div class="container">
        <div class="columns mobile-margin">
          <div class="column">
            <div class="level pb-0 pt-3">
              <div class="level-left">
                <div class="level-item">
                  <h2 class="title is-4">
                    All Rates
                  </h2>
                </div><div class="level-item">
                  <div class="ml-4 is-size-6">
                    <a href="/nz/vote" class="">Vote for a new listing!
                      <span class="icon"><i class="fas fa-check" /></span></a>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="column is-4 has-text-align-right">
            <div class="field is-grouped">
              <div class="control is-expanded has-icons-left">
                <input debounce-events="input" type="search" placeholder="Filter list" class="input is-small"><span class="icon is-small is-left"><i class="fa fa-search" /></span>
              </div><div class="field is-grouped">
                <label class="switch is-rounded"><input type="checkbox" true-value="true" value="false"><span class="check" /><span class="control-label">USD</span></label>
              </div>
            </div>
          </div>
        </div>
        <div class="b-table">
          <div class="table-wrapper">
            <table class="table">
              <thead>
                <tr>
                  <th class="is-current-sort is-sortable is-unselectable">
                    <div class="th-wrap">
                      <span class="is-relative">   <span class="icon sort-icon is-small is-desc"><i class="fas fa-arrow-up" /></span></span>
                    </div>
                  </th><th class="is-sortable is-unselectable">
                    <div class="th-wrap">
                      <span class="is-relative"> Name <span class="icon sort-icon is-small is-desc is-invisible"><i class="fas fa-arrow-up" /></span></span>
                    </div>
                  </th><th class="is-sortable is-unselectable">
                    <div class="th-wrap">
                      <span class="is-relative"> Symbol <span class="icon sort-icon is-small is-desc is-invisible"><i class="fas fa-arrow-up" /></span></span>
                    </div>
                  </th><th class="is-sortable is-unselectable">
                    <div class="th-wrap is-numeric">
                      <span class="is-relative"> Sell <span class="icon sort-icon is-small is-desc is-invisible"><i class="fas fa-arrow-up" /></span></span>
                    </div>
                  </th><th class="is-sortable is-unselectable">
                    <div class="th-wrap is-numeric">
                      <span class="is-relative"> Buy <span class="icon sort-icon is-small is-desc is-invisible"><i class="fas fa-arrow-up" /></span></span>
                    </div>
                  </th><th class="is-sortable is-unselectable">
                    <div class="th-wrap is-numeric">
                      <span class="is-relative"> 24h <span class="icon sort-icon is-small is-desc is-invisible"><i class="fas fa-arrow-up" /></span></span>
                    </div>
                  </th><th class="">
                    <div class="th-wrap is-numeric">
                      <span class="is-relative"> Last 48 hours <span class="icon sort-icon is-small is-desc is-invisible"><i class="fas fa-arrow-up" /></span></span>
                    </div>
                  </th>
                  <th class="">
                    <div class="th-wrap">
                      <span class="is-relative">   <span class="icon sort-icon is-small is-desc is-invisible"><i class="fas fa-arrow-up" /></span></span>
                    </div>
                  </th>
                </tr>
              </thead>
              <tbody>
                <tr draggable="false" class="">
                  <td data-label=" " class="">
                    <figure class="control image is-32x32">
                      <img src="https://static.easycrypto.nz/img/coins/BTC.png" alt="Bitcoin">
                    </figure>
                  </td>
                  <td data-label="Name" class="">
                    <span>
                      Bitcoin
                    </span><div class="dropdown dropdown-menu-animation is-top-right is-hoverable is-mobile-modal">
                      <div role="button" aria-haspopup="true" class="dropdown-trigger">
                        <span class="icon has-text-grey-lighter"><i class="fa fa-info-circle" /></span>
                      </div><div aria-hidden="true" class="background" style="display: none;" /><div aria-hidden="true" class="dropdown-menu" style="display: none;">
                        <div role="list" class="dropdown-content">
                          <div tabindex="0" class="content dropdown-item">
                            <div>
                              <span class="icon"><i class="fas fa-globe-americas" /></span><b>Website:</b><br><a href="https://bitcoin.org/" target="_blank">https://bitcoin.org/</a>
                            </div><br><div>
                              <span class="icon"><i class="fas fa-wallet" /></span><b>Wallet:</b><div>
                                <a href="https://www.exodus.io" target="_blank">https://www.exodus.io</a>
                              </div><div>
                                <a href="https://www.jaxx.io" target="_blank">https://www.jaxx.io</a>
                              </div><div>
                                <a href="https://edge.app" target="_blank">https://edge.app</a>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </td>
                  <td data-label="Symbol" class="">
                    BTC
                  </td>
                  <td data-label="Sell" class="has-text-right">
                    $80,25437
                  </td>
                  <td data-label="Buy" class="has-text-right">
                    <span>$83,620.51</span>
                  </td>
                  <td data-label="24h" class="has-text-right">
                    <span class="has-text-weight-medium"><span class="has-text-success no-break">+1.4%</span></span>
                  </td>
                  <td data-label="Last 48 hours" class="has-text-right">
                    <div class="graph" style="">
                      <svg width="150" height="28" stroke-width="2" class="sparkline-up"><path class="sparkline--fill" d="M4 13.41 L 4 13.41 L 7.086956521739131 11.63 L 10.173913043478262 11.7 L 13.26086956521739 14.44 L 16.347826086956523 16.31 L 19.434782608695652 14.81 L 22.52173913043478 14.15 L 25.608695652173914 14.98 L 28.695652173913043 12.39 L 31.782608695652172 13.03 L 34.869565217391305 14.43 L 37.95652173913044 14.39 L 41.04347826086956 12.63 L 44.130434782608695 13.06 L 47.21739130434783 16.23 L 50.30434782608695 14.49 L 53.391304347826086 14.68 L 56.47826086956522 21.04 L 59.565217391304344 19.4 L 62.65217391304348 20 L 65.73913043478261 20.66 L 68.82608695652173 22.53 L 71.91304347826087 4 L 75 4 L 78.08695652173913 20.71 L 81.17391304347827 18.29 L 84.26086956521739 21.12 L 87.34782608695652 20.69 L 90.43478260869566 21.73 L 93.52173913043478 22.35 L 96.6086956521739 21.74 L 99.69565217391305 21.12 L 102.78260869565217 20.79 L 105.8695652173913 20.22 L 108.95652173913044 19.54 L 112.04347826086956 20.83 L 115.13043478260869 24 L 118.21739130434783 16.83 L 121.30434782608695 11.84 L 124.39130434782608 10.87 L 127.47826086956522 10.83 L 130.56521739130434 12.61 L 133.65217391304347 11.49 L 136.7391304347826 11.47 L 139.82608695652175 5.17 L 142.91304347826087 4.18 L 146 5.09 V 28 L 4 28 Z" stroke="none" /><path class="sparkline--line" d="M4 13.41 L 4 13.41 L 7.086956521739131 11.63 L 10.173913043478262 11.7 L 13.26086956521739 14.44 L 16.347826086956523 16.31 L 19.434782608695652 14.81 L 22.52173913043478 14.15 L 25.608695652173914 14.98 L 28.695652173913043 12.39 L 31.782608695652172 13.03 L 34.869565217391305 14.43 L 37.95652173913044 14.39 L 41.04347826086956 12.63 L 44.130434782608695 13.06 L 47.21739130434783 16.23 L 50.30434782608695 14.49 L 53.391304347826086 14.68 L 56.47826086956522 21.04 L 59.565217391304344 19.4 L 62.65217391304348 20 L 65.73913043478261 20.66 L 68.82608695652173 22.53 L 71.91304347826087 4 L 75 4 L 78.08695652173913 20.71 L 81.17391304347827 18.29 L 84.26086956521739 21.12 L 87.34782608695652 20.69 L 90.43478260869566 21.73 L 93.52173913043478 22.35 L 96.6086956521739 21.74 L 99.69565217391305 21.12 L 102.78260869565217 20.79 L 105.8695652173913 20.22 L 108.95652173913044 19.54 L 112.04347826086956 20.83 L 115.13043478260869 24 L 118.21739130434783 16.83 L 121.30434782608695 11.84 L 124.39130434782608 10.87 L 127.47826086956522 10.83 L 130.56521739130434 12.61 L 133.65217391304347 11.49 L 136.7391304347826 11.47 L 139.82608695652175 5.17 L 142.91304347826087 4.18 L 146 5.09" fill="none" /><line
                        class="sparkline--cursor"
                        x1="-1000"
                        x2="-1000"
                        y1="0"
                        y2="28"
                        stroke-width="2"
                      /><circle class="sparkline--spot" cx="-1000" cy="-1000" r="2" /><rect width="150" height="28" style="fill: transparent; stroke: transparent" class="sparkline--interaction-layer" /></svg><span class="tooltip" />
                    </div>
                  </td>
                  <td data-label=" " class="">
                    <div class="no-break">
                      <button class="mr-4 button is-size-7 is-rounded is-success">
                        Buy
                      </button><span class="cursor has-text-grey-lighter"><span class="icon"><i class="far fa-star" /></span></span>
                    </div>
                  </td>
                </tr>
                <tr draggable="false" class="">
                  <td data-label=" " class="">
                    <figure class="control image is-32x32">
                      <img src="https://static.easycrypto.nz/img/coins/BTC.png" alt="Bitcoin">
                    </figure>
                  </td>
                  <td data-label="Name" class="">
                    <span>
                      Bitcoin
                    </span><div class="dropdown dropdown-menu-animation is-top-right is-hoverable is-mobile-modal">
                      <div role="button" aria-haspopup="true" class="dropdown-trigger">
                        <span class="icon has-text-grey-lighter"><i class="fa fa-info-circle" /></span>
                      </div><div aria-hidden="true" class="background" style="display: none;" /><div aria-hidden="true" class="dropdown-menu" style="display: none;">
                        <div role="list" class="dropdown-content">
                          <div tabindex="0" class="content dropdown-item">
                            <div>
                              <span class="icon"><i class="fas fa-globe-americas" /></span><b>Website:</b><br><a href="https://bitcoin.org/" target="_blank">https://bitcoin.org/</a>
                            </div><br><div>
                              <span class="icon"><i class="fas fa-wallet" /></span><b>Wallet:</b><div>
                                <a href="https://www.exodus.io" target="_blank">https://www.exodus.io</a>
                              </div><div>
                                <a href="https://www.jaxx.io" target="_blank">https://www.jaxx.io</a>
                              </div><div>
                                <a href="https://edge.app" target="_blank">https://edge.app</a>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </td>
                  <td data-label="Symbol" class="">
                    BTC
                  </td>
                  <td data-label="Sell" class="has-text-right">
                    $80,25437
                  </td>
                  <td data-label="Buy" class="has-text-right">
                    <span>$83,620.51</span>
                  </td>
                  <td data-label="24h" class="has-text-right">
                    <span class="has-text-weight-medium"><span class="has-text-success no-break">+1.4%</span></span>
                  </td>
                  <td data-label="Last 48 hours" class="has-text-right">
                    <div class="graph" style="">
                      <svg width="150" height="28" stroke-width="2" class="sparkline-up"><path class="sparkline--fill" d="M4 13.41 L 4 13.41 L 7.086956521739131 11.63 L 10.173913043478262 11.7 L 13.26086956521739 14.44 L 16.347826086956523 16.31 L 19.434782608695652 14.81 L 22.52173913043478 14.15 L 25.608695652173914 14.98 L 28.695652173913043 12.39 L 31.782608695652172 13.03 L 34.869565217391305 14.43 L 37.95652173913044 14.39 L 41.04347826086956 12.63 L 44.130434782608695 13.06 L 47.21739130434783 16.23 L 50.30434782608695 14.49 L 53.391304347826086 14.68 L 56.47826086956522 21.04 L 59.565217391304344 19.4 L 62.65217391304348 20 L 65.73913043478261 20.66 L 68.82608695652173 22.53 L 71.91304347826087 4 L 75 4 L 78.08695652173913 20.71 L 81.17391304347827 18.29 L 84.26086956521739 21.12 L 87.34782608695652 20.69 L 90.43478260869566 21.73 L 93.52173913043478 22.35 L 96.6086956521739 21.74 L 99.69565217391305 21.12 L 102.78260869565217 20.79 L 105.8695652173913 20.22 L 108.95652173913044 19.54 L 112.04347826086956 20.83 L 115.13043478260869 24 L 118.21739130434783 16.83 L 121.30434782608695 11.84 L 124.39130434782608 10.87 L 127.47826086956522 10.83 L 130.56521739130434 12.61 L 133.65217391304347 11.49 L 136.7391304347826 11.47 L 139.82608695652175 5.17 L 142.91304347826087 4.18 L 146 5.09 V 28 L 4 28 Z" stroke="none" /><path class="sparkline--line" d="M4 13.41 L 4 13.41 L 7.086956521739131 11.63 L 10.173913043478262 11.7 L 13.26086956521739 14.44 L 16.347826086956523 16.31 L 19.434782608695652 14.81 L 22.52173913043478 14.15 L 25.608695652173914 14.98 L 28.695652173913043 12.39 L 31.782608695652172 13.03 L 34.869565217391305 14.43 L 37.95652173913044 14.39 L 41.04347826086956 12.63 L 44.130434782608695 13.06 L 47.21739130434783 16.23 L 50.30434782608695 14.49 L 53.391304347826086 14.68 L 56.47826086956522 21.04 L 59.565217391304344 19.4 L 62.65217391304348 20 L 65.73913043478261 20.66 L 68.82608695652173 22.53 L 71.91304347826087 4 L 75 4 L 78.08695652173913 20.71 L 81.17391304347827 18.29 L 84.26086956521739 21.12 L 87.34782608695652 20.69 L 90.43478260869566 21.73 L 93.52173913043478 22.35 L 96.6086956521739 21.74 L 99.69565217391305 21.12 L 102.78260869565217 20.79 L 105.8695652173913 20.22 L 108.95652173913044 19.54 L 112.04347826086956 20.83 L 115.13043478260869 24 L 118.21739130434783 16.83 L 121.30434782608695 11.84 L 124.39130434782608 10.87 L 127.47826086956522 10.83 L 130.56521739130434 12.61 L 133.65217391304347 11.49 L 136.7391304347826 11.47 L 139.82608695652175 5.17 L 142.91304347826087 4.18 L 146 5.09" fill="none" /><line
                        class="sparkline--cursor"
                        x1="-1000"
                        x2="-1000"
                        y1="0"
                        y2="28"
                        stroke-width="2"
                      /><circle class="sparkline--spot" cx="-1000" cy="-1000" r="2" /><rect width="150" height="28" style="fill: transparent; stroke: transparent" class="sparkline--interaction-layer" /></svg><span class="tooltip" />
                    </div>
                  </td>
                  <td data-label=" " class="">
                    <div class="no-break">
                      <button class="mr-4 button is-size-7 is-rounded is-success">
                        Buy
                      </button><span class="cursor has-text-grey-lighter"><span class="icon"><i class="far fa-star" /></span></span>
                    </div>
                  </td>
                </tr>
                <tr draggable="false" class="">
                  <td data-label=" " class="">
                    <figure class="control image is-32x32">
                      <img src="https://static.easycrypto.nz/img/coins/BTC.png" alt="Bitcoin">
                    </figure>
                  </td>
                  <td data-label="Name" class="">
                    <span>
                      Bitcoin
                    </span><div class="dropdown dropdown-menu-animation is-top-right is-hoverable is-mobile-modal">
                      <div role="button" aria-haspopup="true" class="dropdown-trigger">
                        <span class="icon has-text-grey-lighter"><i class="fa fa-info-circle" /></span>
                      </div><div aria-hidden="true" class="background" style="display: none;" /><div aria-hidden="true" class="dropdown-menu" style="display: none;">
                        <div role="list" class="dropdown-content">
                          <div tabindex="0" class="content dropdown-item">
                            <div>
                              <span class="icon"><i class="fas fa-globe-americas" /></span><b>Website:</b><br><a href="https://bitcoin.org/" target="_blank">https://bitcoin.org/</a>
                            </div><br><div>
                              <span class="icon"><i class="fas fa-wallet" /></span><b>Wallet:</b><div>
                                <a href="https://www.exodus.io" target="_blank">https://www.exodus.io</a>
                              </div><div>
                                <a href="https://www.jaxx.io" target="_blank">https://www.jaxx.io</a>
                              </div><div>
                                <a href="https://edge.app" target="_blank">https://edge.app</a>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </td>
                  <td data-label="Symbol" class="">
                    BTC
                  </td>
                  <td data-label="Sell" class="has-text-right">
                    $80,25437
                  </td>
                  <td data-label="Buy" class="has-text-right">
                    <span>$83,620.51</span>
                  </td>
                  <td data-label="24h" class="has-text-right">
                    <span class="has-text-weight-medium"><span class="has-text-success no-break">+1.4%</span></span>
                  </td>
                  <td data-label="Last 48 hours" class="has-text-right">
                    <div class="graph" style="">
                      <svg width="150" height="28" stroke-width="2" class="sparkline-up"><path class="sparkline--fill" d="M4 13.41 L 4 13.41 L 7.086956521739131 11.63 L 10.173913043478262 11.7 L 13.26086956521739 14.44 L 16.347826086956523 16.31 L 19.434782608695652 14.81 L 22.52173913043478 14.15 L 25.608695652173914 14.98 L 28.695652173913043 12.39 L 31.782608695652172 13.03 L 34.869565217391305 14.43 L 37.95652173913044 14.39 L 41.04347826086956 12.63 L 44.130434782608695 13.06 L 47.21739130434783 16.23 L 50.30434782608695 14.49 L 53.391304347826086 14.68 L 56.47826086956522 21.04 L 59.565217391304344 19.4 L 62.65217391304348 20 L 65.73913043478261 20.66 L 68.82608695652173 22.53 L 71.91304347826087 4 L 75 4 L 78.08695652173913 20.71 L 81.17391304347827 18.29 L 84.26086956521739 21.12 L 87.34782608695652 20.69 L 90.43478260869566 21.73 L 93.52173913043478 22.35 L 96.6086956521739 21.74 L 99.69565217391305 21.12 L 102.78260869565217 20.79 L 105.8695652173913 20.22 L 108.95652173913044 19.54 L 112.04347826086956 20.83 L 115.13043478260869 24 L 118.21739130434783 16.83 L 121.30434782608695 11.84 L 124.39130434782608 10.87 L 127.47826086956522 10.83 L 130.56521739130434 12.61 L 133.65217391304347 11.49 L 136.7391304347826 11.47 L 139.82608695652175 5.17 L 142.91304347826087 4.18 L 146 5.09 V 28 L 4 28 Z" stroke="none" /><path class="sparkline--line" d="M4 13.41 L 4 13.41 L 7.086956521739131 11.63 L 10.173913043478262 11.7 L 13.26086956521739 14.44 L 16.347826086956523 16.31 L 19.434782608695652 14.81 L 22.52173913043478 14.15 L 25.608695652173914 14.98 L 28.695652173913043 12.39 L 31.782608695652172 13.03 L 34.869565217391305 14.43 L 37.95652173913044 14.39 L 41.04347826086956 12.63 L 44.130434782608695 13.06 L 47.21739130434783 16.23 L 50.30434782608695 14.49 L 53.391304347826086 14.68 L 56.47826086956522 21.04 L 59.565217391304344 19.4 L 62.65217391304348 20 L 65.73913043478261 20.66 L 68.82608695652173 22.53 L 71.91304347826087 4 L 75 4 L 78.08695652173913 20.71 L 81.17391304347827 18.29 L 84.26086956521739 21.12 L 87.34782608695652 20.69 L 90.43478260869566 21.73 L 93.52173913043478 22.35 L 96.6086956521739 21.74 L 99.69565217391305 21.12 L 102.78260869565217 20.79 L 105.8695652173913 20.22 L 108.95652173913044 19.54 L 112.04347826086956 20.83 L 115.13043478260869 24 L 118.21739130434783 16.83 L 121.30434782608695 11.84 L 124.39130434782608 10.87 L 127.47826086956522 10.83 L 130.56521739130434 12.61 L 133.65217391304347 11.49 L 136.7391304347826 11.47 L 139.82608695652175 5.17 L 142.91304347826087 4.18 L 146 5.09" fill="none" /><line
                        class="sparkline--cursor"
                        x1="-1000"
                        x2="-1000"
                        y1="0"
                        y2="28"
                        stroke-width="2"
                      /><circle class="sparkline--spot" cx="-1000" cy="-1000" r="2" /><rect width="150" height="28" style="fill: transparent; stroke: transparent" class="sparkline--interaction-layer" /></svg><span class="tooltip" />
                    </div>
                  </td>
                  <td data-label=" " class="">
                    <div class="no-break">
                      <button class="mr-4 button is-size-7 is-rounded is-success">
                        Buy
                      </button><span class="cursor has-text-grey-lighter"><span class="icon"><i class="far fa-star" /></span></span>
                    </div>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
          <div class="top level">
            <div class="level-left" /><div class="level-right">
              <div class="level-item">
                <nav class="pagination">
                  <a role="button" href="#" disabled="disabled" class="pagination-link pagination-previous"><span class="icon" aria-hidden="true"><i class="fas fa-angle-left" /></span></a><a role="button" href="#" class="pagination-link pagination-next"><span class="icon" aria-hidden="true"><i class="fas fa-angle-right" /></span></a><ul class="pagination-list">
                    <li><a role="button" href="#" aria-current="true" class="pagination-link is-current ">1</a></li><li><a role="button" href="#" class="pagination-link">2</a></li><li><span class="pagination-ellipsis">…</span></li><li><a role="button" href="#" class="pagination-link">5</a></li>
                  </ul>
                </nav>
              </div>
            </div>
          </div>
        </div>

        <div class="content is-size-7 has-text-left has-text-weight-light" style="margin: 1em;">
          <p class="has-text-weight-light has-text-centered">
            Want to list a new coin?
            <a href="/nz/vote" class="link-white">Click here to vote!</a>
          </p><p>Rates updated Monday 3, 18:18:54.</p><p>The rate you are quoted on our main page is inclusive of ALL fees. This means all currency exchange fees, all mining fees, all gas prices, and all withdrawal fees – everything!</p><p>As some exchange fees are fixed price vs percentage, the rate will change with the size of your order. Larger orders are most cost-effective as the fixed fees are a smaller part of the order. Rates displayed here are the price per 1 coin or $2000. For an exact quote, please click the Buy button and fill in an amount.</p>
        </div>
      </div>
      <svg
        width="1440px"
        height="37px"
        viewBox="0 0 1440 37"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        class="ec-wave-top"
      ><g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"><g transform="translate(0.000000, -1380.000000)" fill="#FFFFFF" fill-rule="nonzero"><g transform="translate(0.000000, 1380.000000)"><g transform="translate(720.000000, 18.500000) scale(-1, -1) translate(-720.000000, -18.500000) "><path d="M0,0 L48,3.7 C96,7.4 192,14.8 288,18.5 C384,22.2 480,22.2 576,19.725625 C672,17.34375 768,12.25625 864,8.625625 C960,4.85625 1056,2.54375 1152,4.925625 C1248,7.4 1344,14.8 1392,18.5 L1440,22.2 L1440,37 L1392,37 C1344,37 1248,37 1152,37 C1056,37 960,37 864,37 C768,37 672,37 576,37 C480,37 384,37 288,37 C192,37 96,37 48,37 L0,37 L0,0 Z" /></g></g></g></g></svg>
      <svg
        width="1440px"
        height="37px"
        viewBox="0 0 1440 37"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        class="ec-wave-bottom"
      ><g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"><g transform="translate(0.000000, -2010.000000)" fill="#FFFFFF" fill-rule="nonzero"><g transform="translate(0.000000, 1380.000000)"><g transform="translate(0.000000, 630.000000)"><path d="M0,0 L48,3.7 C96,7.4 192,14.8 288,18.5 C384,22.2 480,22.2 576,19.725625 C672,17.34375 768,12.25625 864,8.625625 C960,4.85625 1056,2.54375 1152,4.925625 C1248,7.4 1344,14.8 1392,18.5 L1440,22.2 L1440,37 L1392,37 C1344,37 1248,37 1152,37 C1056,37 960,37 864,37 C768,37 672,37 576,37 C480,37 384,37 288,37 C192,37 96,37 48,37 L0,37 L0,0 Z" /></g></g></g></g></svg>
    </section>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data () {
    return {
      rate: {}
    }
  },
  mounted () {
    this.$axios.$get('https://r.easycrypto.nz/json/backenddb.json').then((res) => {
      this.rate = res
    })
  }

}
</script>
