<template >
  <section class="section" @scroll="handleScroll">
    <main class="main" >
      <article class="cards-block" id="cardsBlock" >
        <div class="card greetings" id="greetings"></div>
        <div class="card skills" id="skills"></div>
        <div class="card scroll-down" id="scrollDown"></div>
      </article>
    </main>
  </section>
</template>
<script setup>
  import { onMounted, ref, watch } from 'vue'

  onMounted(() => {
    height.value = cardsBlock.style.height = document.documentElement.clientHeight + 'px';
  })
  const height = ref(null)
  const scroll = ref(null)
  const greetingsCount = ref(0)
  const skillsCount = ref(0)
  const scrollDownCount = ref(0)
  const checkScrollHeight = ref(null)

  const handleScroll = () => {
    scroll.value = window.scrollY
    checkScrollHeight.value = parseInt(height.value) - ( parseInt(height.value) * 0.3 )
  }
  window.addEventListener("scroll",handleScroll)
  window.addEventListener('beforeunload', () => {
    window.scrollTo(0,0)
  })
  
  watch(() => scroll.value , (newScroll, oldScroll) => {
    if (newScroll > oldScroll && newScroll < checkScrollHeight.value){
      greetingsCount.value += 3
      console.log('ВНИЗ', greetingsCount.value)
      greetings.style.top = greetingsCount.value + 'px'
    }
    else if (newScroll < oldScroll && newScroll > checkScrollHeight.value){
      greetingsCount.value += 3
      console.log('ВНИЗ', greetingsCount.value)
      greetings.style.top = greetingsCount.value + 'px'
    }
    else{
      greetingsCount.value -= 3
      greetings.style.top = greetingsCount.value + 'px'
      console.log('ВВЕРХ', greetingsCount.value)
    }
  })
</script>
<style scoped>
.section{
  width: 100%;
  height: 2000px;
  /* background-attachment: fixed; */
  background-color: #42b983;
  
}
.main{
  width: 90%;
  height: 100%;
  margin: 0 auto;
  /* position: fixed; */
  background-color: rgba(250, 235, 215, 0.493);
  /* background-attachment: scroll ; */
  z-index: 2;
}
.cards-block{
  position: relative;
  }
.card{
  width: 50%;
  height: 30%;
  position: fixed;
  top: 0;
  left: 0;
}
.greetings{
  background-color: pink;
  z-index: 3;
}
.skills{
  background-color: rgba(0, 255, 242, 0.582);
  z-index: 2;
}
.scroll-down{
  background-color: rgba(238, 255, 0, 0.753);
  z-index: 1;
}
</style>