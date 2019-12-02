<template>
  <li>
    {{ config.title }}
    <ul>
      <Folder
        v-for="(child, index) in config.children"
        :key="index" 
        :config="child">
        {{ child.title }}
      </Folder>
    </ul>
  </li>
</template>

<script>
export default {
  name: 'Folder',
  props: {
    config: {
      type: Object,
      default: () => ({
        title: '',
        children: []
      })
    }
  }
}
</script>

<style scoped>
  ul > li {
    color: #343aeb;
    text-align: left;
  }
  ul > li:only-of-type {
    opacity: 0.9;
  }
</style>