<template>
<div>
  <TheHeader @sidenavToggle="displaySidenav = !displaySidenav"/>
  <TheSidenav
  :show="displaySidenav"
  @close="displaySidenav=false"/>
  <Nuxt />

  <div class="home-page">
    <section class="intro">
      <h1>  Get the latest tech news!</h1>
      </section>
    <section class="featured-posts">
      <PostPreview
      id="1"
      thumbnail="https://previews.123rf.com/images/yewkeo/yewkeo1707/yewkeo170700003/82436195-technique-abstraite-génie-technique-bleu-.jpg" 
      title="Hello There!"
      previewText="This is my post "
      />
      <PostPreview 
       id="2"
      thumbnail="https://imageio.forbes.com/specials-images/imageserve/61d52d4e3a76ed81ac034ea8/0x0.jpg?format=jpg&width=1200" 
      title="Hello There second post !"
      previewText="This is my post "/>
      <PostPreview 
       id="3"
      thumbnail="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSj-JoV27CJHCIL6Mem7d9D8VMaqMZ30Y0KiCZjDoJK9VlRyDNRDC66q43eO5-NDps3UHc&usqp=CAU" 
      title="Hello There third post!"
      previewText="This is my post "/>
      <PostPreview  id="4"
      thumbnail="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTXULZZr6exCchMn-nWO1ZBE2XwInhClTs2t3G2EeZGLRdOnoEQoC_651sTNvFynbmFtXo&usqp=CAU" 
      title="Hello There forth post!"
      previewText="This is my post "/>

    </section>
  </div>
  </div>
</template>


<script>

import PostPreview from '@/components/Posts/PostPreview'
import TheHeader  from '@/components/Navigation/TheHeader'
import TheSidenav  from '@/components/Navigation/TheSidenav'

export default {
  components: {
    PostPreview,  
    TheHeader,
TheSidenav
  },
  data() {
  return {
    displaySidenav:false 
  }
}
  
}
</script>

<style scoped>  /* scoped means that these styles will be applied only to this component  */

.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image:url('~/pages/images/main-page-background.jpg');
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}

.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}


</style>
