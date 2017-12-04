<template>
  <div>
    <app-header v-bind:title="title" v-on:changeTitle="updateTitle($event)"></app-header>
    <app-ninjas v-bind:ninjas="ninjas"></app-ninjas>
    <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
import header from './components/header.vue';
import footer from './components/footer.vue';
import ninjas from './components/ninjas.vue';


export default {
  components: {
    'app-header': header,
    'app-footer': footer,
    'app-ninjas': ninjas
  },
  data () {
    return {
      ninjas: [
        {name: 'Ryu', speciality: 'vue components', show: false},
        {name: 'Crystal', speciality: 'HTML Widzary', show: false},
        {name: 'Hitoshi', speciality: 'Click events', show: false},
        {name: 'Tango', speciality: 'Conditionals', show: false},
        {name: 'Kami', speciality: 'Webpack', show: false},
        {name: 'Yoshi', speciality: 'Data Diggin', show: false},
      ],
      title: "Vue ninjas"
    }
  },
  methods: {
    updateTitle: function(updateTitle){
      this.title = updateTitle;
    }
  }
}
</script>

<style scoped>


</style>
