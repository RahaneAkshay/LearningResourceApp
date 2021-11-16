<template>
  <div class="container-fluid">
      <div class="row">
         <div class="col-12">
             <the-header></the-header>
         </div>
      </div>
    <div class="row">
      <div class="col-6"><add-resource></add-resource></div>
      <div class="col-6">
        <learning-resource
          :stored-resources="storedResources"
        ></learning-resource>
      </div>
    </div>
  </div>
</template>
<script>
import LearningResource from './components/learning-resources/LearningResource.vue';
import AddResource from './components/learning-resources/AddResource.vue'
import TheHeader from './components/Layout/TheHeader.vue'
export default {
  components: {
    'learning-resource': LearningResource,
    'add-resource':AddResource,
    'the-header':TheHeader
  },
  data() {
    return {
      storedResources: [
        {
          id: 'vue',
          title: 'vue official guide',
          description: 'Use vue docs',
          link: 'https://v3.vuejs.org/',
        },
        {
          id: 'Google',
          title: 'Google',
          description: 'Google for help',
          link: 'https://www.google.co.in/',
        },
      ],
    };
  },
};
</script>
