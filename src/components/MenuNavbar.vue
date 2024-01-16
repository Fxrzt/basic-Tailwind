<template>
  <nav class="py-5 px-2 bg-orange-500">
    <div
      class="max-w-screen-xl flex flex-wrap items-center justify-between pl-12"
    >
      <a href="#" class="flex items-center space-x-3 rtl:space-x-reverse">
        <span
          class="sty_logo self-center text-2xl font-semibold whitespace-nowrap text-white"
          >Gavyn Miles</span
        >
      </a>
      <div class="hidden w-full md:block md:w-auto">
        <ul
          class="font-medium flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700"
        >
          <li v-for="(item,index) in menubar" :key="index">
            <a
              href="#"
              class="topic_text_TH block py-2 px-3 text-white bg-blue-700 rounded md:bg-transparent md:text-blue-700 md:p-0 dark:text-white md:dark:text-blue-500"
              aria-current="page"
              v-if="index == 0"
              @click="fn_getName"
              >{{ item }}</a
            >
            <a
              v-else
              href="#"
              class="topic_text_TH block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent"
              >{{ item }}</a
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'MenuNavbar',
  data () {
    return {
      nameGame: 'game',
      toggleMenu: false,
      menubar: ['Home', 'Service', 'About', 'Contact']
    }
  },
  methods: {
    fn_getName () {
      return console.log(`${this.nameGame}`)
    }
  }
}
</script>

<style scoped>
.topic_text_TH{
    font-weight: 600;
    font-size: 23px;
}
</style>
