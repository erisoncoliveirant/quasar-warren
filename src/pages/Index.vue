<template>
  <q-page padding>
    <div class="row">
      <div class="col-md-8 col-sm-12 col-xs-12">
        <overview />
        <line-overview />

        <div class="row">
          <div class="col-12 q-pt-xl">
            <q-btn
              color="primary"
              label="Fazer Transação"
              class="text-bold"
              rounded
              unelevated
            />
          </div>
        </div>
      </div>

      <div class="col-md-4 col-sm-12 col-xs-12">
        <scroll-page>
          <list-section />
          <list-product />
          <list-latest-moves />
          <list-help-options :items="items"></list-help-options>
        </scroll-page>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  components: {
    Overview: () => import('src/components/Overview.vue'),
    LineOverview: () => import('src/components/charts/LineOverview.vue'),
    ScrollPage: () => import('src/components/scroll/ScrollPage.vue'),
    ListSection: () => import('src/components/lists/ListSection.vue'),
    ListProduct: () => import('src/components/lists/ListProduct.vue'),
    ListLatestMoves: () => import('src/components/lists/ListLatestMoves.vue'),
    ListHelpOptions: () => import('src/components/lists/ListHelpOptions.vue')
  },
  data () {
    return {
      items: [
        {
          color: 'primary',
          icon: 'mdi-clock-outline',
          title: 'Históricos de rendimentos',
          route: '/history'
        },
        {
          color: 'primary',
          icon: 'mdi-help',
          title: 'Dúvidas',
          route: '/test'
        }
      ]
      // thumbStyle: {
      //   // display: 'none'
      //   width: '10px'
      // },
      // barStyle: {
      //   // display: 'none'
      //   width: '20px'
      // }
    }
  }
}
</script>
