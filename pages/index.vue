<template>
  <main>
    <section class="self-center flex flex-col flex-1 items-center justify-center">
      <div style="max-width: 800px; margin: 0 auto">
        <img :src="indexBanner" class="max-w-full h-auto border shadow transition-shadow rounded-lg"/>
      </div>
      <h1 class="title text-center m-2">Welcome to Mech OEM</h1>
      <p style="max-width: 800px; margin: 0 auto">Mech OEM was founded in 1994, is located in the most happiness city in Yuyao of Zhejiang province. The company is a professional automotive and motorcycle parts manufacturer. Adhere to the development policy of  “pragmatic innovation, pioneering and enterprising”. adhere to the tenet of “technology update, tighter quality,  users are more satisfied”. The company has high-quality team, perfect organization system, excellent technology and advanced equipment. The company provides high quality products and efficient service.</p>
    </section>
  </main>
</template>

<script>
import indexBanner from '../static/img/indexBanner.png'
export default {
  data () {
    return {
      indexBanner
    }
  }
}
</script>