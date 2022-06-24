<template>
  <q-page padding>
    <div class="row">
      <div class="col-md-8 col-sm-12 col-xs-12">
        <trade-overview />

        <div class="row">
          <div class="col-12 q-pt-md">
            <q-btn
              color="info"
              label="Depositar"
              class="text-bold"
              rounded
              unelevated
            />
            <q-btn
              color="info"
              label="Buscar Ativo"
              class="text-bold q-ml-md"
              rounded
              unelevated
            />
          </div>
        </div>
      </div>

      <div class="col-md-4 col-sm-12 col-xs-12">
        <scroll-page>
          <!-- <list-wealth-product />
          <my-wealth />
          <list-wealth-latest-moves />
          <list-help-options :items="items"> </list-help-options> -->
        </scroll-page>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageTrade',
  components: {
    TradeOverview: () => import('src/components/TradeOverview'),
    // BarWealthOverview: () => import('src/components/charts/BarWealthOverview'),
    // ListWealthProduct: () => import('src/components/lists/ListWealthProduct'),
    // ListWealthLatestMoves: () =>
    //   import('src/components/lists/ListWealthLatestMoves'),
    // ListHelpOptions: () => import('src/components/lists/ListHelpOptions'),
    // MyWealth: () => import('src/components/MyWealth'),
    ScrollPage: () => import('src/components/scroll/ScrollPage')
  },
  data () {
    return {
      items: [
        {
          color: 'warning',
          icon: 'mdi-help',
          title: 'Dúvidas',
          route: '/test'
        }
      ]
    }
  }
}
</script>
