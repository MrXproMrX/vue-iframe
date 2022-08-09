<template>
    <section class="container">
      <div class="iframe">
        <div class="iframe__list">

          <div class="iframe__video__mrx">
            <video :src="videoIfrome" controls muted></video>
          </div>

          <div class="iframe__item">
            <Iframelist :iframes="iframes" @video="video"></Iframelist>
          </div>
        </div>
      </div>
    </section>
</template>

<script>
import Iframelist from '@/components/Iframelist.vue';
import IframeJs from '@/data/IframeJs'
export default {
  components:{
    Iframelist
  },

  data(){
    return{
      iframes:IframeJs,
      videoIfrome:IframeJs[0].link
    }
  },

  methods:{
    video(link){
      this.videoIfrome = link
    }
  }
}
</script>
