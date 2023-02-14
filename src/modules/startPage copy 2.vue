<template>
  <section class="section" @scroll="handleScroll">
    <main class="main">
      <article class="cards-block" id="cardsBlock" >
        <div class="card greetings" id="greetings"></div>
        <div class="card skills" id="skills"></div>
        <div class="card scroll-down" id="scrollDown"></div>
        <div class="action">
          <h1>Проскроль</h1>
          <p>=)</p>
        </div>
      </article>
      <article>
        <h1>Проекты</h1>
        <div class="project"></div>
      </article>

    </main>
  </section>
</template>
<script setup>
 import { onMounted, ref, watch } from 'vue'
 onMounted(() => {
    height.value = cardsBlock.style.height = document.documentElement.clientHeight + 'px';
  })
 const scroll = ref(null)
 const height = ref(null)
 const greetingsCount = ref(0)
 const greetingsDown = ref(false)
 const skillsCount = ref(0)
 const skillsDown = ref(false)
 const scrollDownCount = ref(0)
 const scrollInDown = ref(false)
 const checkScrollHeight = ref(null)

 const handleScroll = () => {
    scroll.value = (window.scrollY)
    checkScrollHeight.value = parseInt(height.value) - ( parseInt(height.value) * 0.3 ) + 120
  }
  window.addEventListener("scroll",handleScroll)
  window.addEventListener('beforeunload', () => {
    window.scrollTo(0,0)
  })
  
  watch(() => scroll.value , (newScroll, oldScroll) => {
    if(scroll.value < checkScrollHeight.value){
      greetingsDown.value = false
      if (newScroll > oldScroll){
            greetings.style.top = newScroll - 100 + 'px'
            console.log('DOWN',newScroll, oldScroll)
          }
      else{
        greetings.style.top = newScroll - 100 + 'px'
            console.log('UP',newScroll, oldScroll)
      }
    }
    else{
      greetingsDown.value = true
      greetings.style.zIndex = 1

    }}
  )
  watch(() => scroll.value , (newScroll, oldScroll) =>{
    if(greetingsDown.value && (scroll.value < checkScrollHeight.value * 3)){
      skillsDown.value = false
      if (newScroll > oldScroll){
        skillsCount.value += newScroll/2 - oldScroll/2 
        skills.style.top = skillsCount.value - 120 + 'px'
      }
      else{
        skillsCount.value += newScroll/2 - oldScroll/2
        skills.style.top = skillsCount.value - 120 + 'px'
      }
    }
    else{
      skillsDown.value = true
    }
  })
  watch(() => scroll.value , (newScroll, oldScroll) =>{
    if(skillsDown.value && greetingsDown.value && (scroll.value < checkScrollHeight.value * 5)){
      scrollInDown.value = false
      if (newScroll > oldScroll){
        scrollDownCount.value += newScroll/2 - oldScroll/2 
        scrollDown.style.top = scrollDownCount.value - 120 + 'px'
        scrollDown.style.zIndex = 3
      }
      else{
        scrollDownCount.value += newScroll/2 - oldScroll/2
        scrollDown.style.top = scrollDownCount.value - 120 + 'px'
      }
    }
    else{
      scrollInDown.value = true
    }
  })
  watch(() => scroll.value , (newScroll, oldScroll) =>{
    if(newScroll == 0  &&  skillsDown.value){
      // location.reload()
    }
    else if (greetingsDown.value && skillsDown.value && scrollInDown.value)
    {
      console.log('123')
    }
  })
</script>
<style scoped>
.section{
  width: 100%;
  height: 5000px;
  /* background-attachment: fixed; */
  background-color: #42b983;
}
/* .cards-block{
  position: relative;
  width: 100%;
  } */
.card{
  width: 50%;
  height: 30%;
  position: fixed;
  left: 25%;
}
.greetings{
  background-color: pink;
  z-index: 3;
  top: -120px;
}
.skills{
  background-color: rgba(0, 255, 242, 0.582);
  z-index: 2;
  top: -120px;
}
.scroll-down{
  background-color: rgb(238, 255, 0);
  z-index: 1;
  top: -120px;
}
.action{
  position: fixed;
  top:50%;
  left: 45%;
  text-align: center;
}
</style>