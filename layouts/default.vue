<template>
  <div class="wrapper">
    <Header />
    <nuxt />
    <footer>
      <div class="flex">
        <div class="w-1/2">
          No. 40, Zhenxing Road, Lianghui Development Zone, Yuyao City, Zhejiang Province
          <br>
          Mobile:13486438318
          <br>
          Tel:0574-62315300
          <br>
          Fax:0574-62315988
          <br>
          E-mail:sales@yyxinghe.com
        </div>
        <div class="w-1/4"></div>
        <div class="w-1/4 ">
          <nuxt-link to="/products/auto_parts" class="block">Auto Parts</nuxt-link>
          <nuxt-link to="/products/moto_parts" class="block">Motor Parts</nuxt-link>
          <nuxt-link to="/products/precision" class="block">Precision Equipments</nuxt-link>
        </div>
      </div>
    </footer>
  </div>
</template>

<style lang="postcss" scoped>
footer {
  background-color: #111111;
  color: white;
  width: 100%;
  min-height: 150px;
}
footer > div {
  max-width: 980px;
  margin: 0 auto;
  padding: 14px 0;
}
</style>