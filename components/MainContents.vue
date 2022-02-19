<template>
  <div>
    <hooper :settings="hooperSettings">
      <slide class="contents">
        <nuxt-link to="/countapp" >
          CountApp
        </nuxt-link>
      </slide>
      <slide>
        slide 2
      </slide>
      <slide>
        slide 3
      </slide>
      <slide>
        slide 4
      </slide>
      <slide>
        slide 5
      </slide>
      <slide>
        slide 6
      </slide>
      <hooper-navigation slot="hooper-addons"></hooper-navigation>
    </hooper>
  </div>
</template>
<script>
import { 
  Hooper,
  Slide,
  Navigation as HooperNavigation
   } from 'hooper';
import 'hooper/dist/hooper.css';

export default {
  name: 'App',
  components: {
    Hooper,
    Slide,
    HooperNavigation
  },
  data() {
      return {
        hooperSettings: {
          itemsToShow: 1,
          infiniteScroll: true,
          wheelControl: false,
          autoPlay: false,
          playSpeed: 2000,
          transition: 800,
          breakpoints: { // breakpointを用いたいときはsettingsでまとめないとうまく渡せない
          768: {
            itemsToShow: 2 // 小数点以下の値も指定できる
          },
        }
        },
      }
    }
};
</script>

<style scoped>
/deep/ .hooper-slide {
    background-color: #62caaa;
    padding: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
    border: 2px solid #fff;
    font-size: 30px;
    border-radius: 10px;
  }
a{
  color: white;
}
</style>