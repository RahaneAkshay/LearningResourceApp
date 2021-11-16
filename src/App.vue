<template>
<learning-resource></learning-resource>
    <ul v-for="(item,index) in storedResources" :key="index">
        <li >{{item.id}}</li>
         <li >{{item.title}}</li>
          <li >{{item.description}}</li>
           <li >{{item.link}}</li>
    </ul>
</template>
<script>
import LearningResource from './components/learning-resources/LearningResource.vue'
export default {
    components:{
        'learning-resource':LearningResource
    },
    data(){
        return{
            storedResources:[{
                id:'vue',
                title:'vue official guide',
                description:'Use vue docs',
                link:'https://v3.vuejs.org/'
            },
            {
                id:'Google',
                title:'Google',
                description:'Google for help',
                link:'https://www.google.co.in/'
            }]
        }
    }
}
</script>