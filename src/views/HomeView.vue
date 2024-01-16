<template>
  <div>
    <MenuNavbar></MenuNavbar>
  </div>
</template>

<script>
import MenuNavbar from '../components/MenuNavbar.vue'
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
export default {
  name: 'HomeView',
  data () {
    return {
      firstname: 'dffsdfsdfsdf',
      age: 25
    }
  },
  components: {
    MenuNavbar
  }
}
</script>
