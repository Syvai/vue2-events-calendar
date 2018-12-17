<template>
  <div id="app">
    <h1>vue-event-calendar</h1>
    <h2 class="t-center">Default template</h2>
    <vue-event-calendar
      :events="demoEvents"
      @day-changed="handleDayChanged"
      @month-changed="handleMonthChanged"
    ></vue-event-calendar>
    <h2 class="t-center">Custom template</h2>
    <vue-event-calendar :events="demoEvents">
      <template scope="props">
        <div v-for="(event, index) in props.showEvents" class="event-item">
          <!-- In here do whatever you want, make you owner event template -->
          {{event}}
        </div>
      </template>
    </vue-event-calendar>
  </div>
</template>

<script>
let today = new Date()
export default {
  name: 'app',
  data () {
    return {
      demoEvents: [{
        date: `${today.getFullYear()}/${today.getMonth() + 1}/${today.getDate()}`,
        title: 'Title-1',
        desc: 'longlonglong description',
        icon: 'icon1.png'
      },{
        date: `${today.getFullYear()}/${today.getMonth() + 1}/${today.getDate()}`,
        title: 'Title-1',
        desc: 'longlonglong description',
        icon: ''
      },{
        date: `${today.getFullYear()}/${today.getMonth() + 1}/${today.getDate()}`,
        title: 'Title-1',
        desc: 'longlonglong description',
        icon: ''
      },{
        date: `${today.getFullYear()}/${today.getMonth() + 1}/${today.getDate()}`,
        title: 'Title-1',
        desc: 'longlonglong description',
        icon: ''
      },{
        date: `${today.getFullYear()}/${today.getMonth() + 1}/${today.getDate()}`,
        title: 'Title-1',
        desc: 'longlonglong description',
        icon: ''
      },{
        date: `${today.getFullYear()}/${today.getMonth() + 1}/${today.getDate()}`,
        title: 'Title-1',
        desc: 'longlonglong description',
        icon: 'icon3.png'
      },{
        date: '2018-12-15 00:00:00',
        title: 'Title-1',
        desc: 'longlonglong description',
        icon: 'icon1.png'
      },{
        date: `2018-12-24: 00:00:00`,
        title: 'Title-2',
        icon: 'icon2.png'
      },{
        date: `${today.getFullYear()}/${today.getMonth() === 11 ? 1 : today.getMonth() + 2}/06`,
        title: 'Title-3',
        desc: 'description',
        icon: ''
      }]
    }
  },
  methods: {
    handleDayChanged (data) {
    },
    handleMonthChanged (data) {
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 30px;
}

h1, h2, h3 {
  font-weight: normal;
  margin: 0;
  padding: 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
.t-center{
  text-align: center;
  margin: 20px;
}
</style>
