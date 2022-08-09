<template>
    <ul class="iframe__list__mrx">
        <li class="iframe__item__mrx" v-for="(iframe,index) in iframes" :key="index" @click="$emit('video',iframe.link)">
           <video class="iframe__video" :src="iframe.link" muted></video>
           <h2 class="iframe__title">{{iframe.title}}</h2>
        </li>
    </ul>
</template>

<script>
export default {
    emits:['video'],
    props:['iframes'],
}
</script>

<!-- <iframe width="1280" height="720" src="https://www.youtube.com/embed/FJkflaK6gcc" title="ПЕСНИ ОТ КОТОРЫХ НАХЛЫНУТ ВОСПОМИНАНИЯ | Песни Нашей Юности  | Подростковые Песни | Песни на вечер" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->