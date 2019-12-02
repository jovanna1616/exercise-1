<template>
  <div id="app">
    <ul>
      <li>Root component - independed content</li>
      <Folder :config="config"></Folder>
    </ul>
  </div>
</template>

<script>
import Folder from './components/Folder.vue'

export default {
  name: 'app',
  components: {
    Folder
  },
  data () {
    return {
      config: {
        title: 'It\'s shocking what you can find in stores now days.',
        children: [{
          title: 'Especially in outlet malls. They do have their positives and negatives, but overall they strike a bad cord with me.',
          children: [{
            title: 'I never found anything hot there, mostly just neutral staff.',
            children: [{
              title: 'Plus most stores just charge too much. I miss Circuit City.',
              children: [{
                title: 'I came here so I could feel grounded.',
                children: [{
                  title: 'Those are all painfull old. Don\'t you know any current pouns?',
                  children: [{
                    title: 'Ohm my God. Will you guys cut it out?',
                    children: [{
                      title: 'Ouch, that hz.',
                      children: [{
                        title: 'C-C-C-CITCUIT BREAKER',
                        children: []
                      }]
                    }]
                  }]
                }]
              }]
            }]
          }]
        }]
      }
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
ul {
  list-style: none;
}
</style>
