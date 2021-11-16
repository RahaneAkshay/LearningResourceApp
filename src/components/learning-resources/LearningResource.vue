<template>
    <div class="container-fluid, m-3 ">  <ul v-for="(item,index) in resources" :key="index">
       <div class="card">
        <h5 class="card-header text-warning bg-dark">{{item.id}}</h5>
        <div class="card-body bg-info text-dark">
          <p>Desciption: {{item.description}}</p>
           <p>Url: <a :href="item.link">{{item.title}}</a></p>
           </div>
           <h5 class="card-footer bg-dark"><button type="button" @click="removeResource(item.index)" class="btn btn-outline-danger">Delete</button></h5>
    </div></ul></div>
</template>
<script>
export default {
    props:["storedResources"],
    data(){
        return{
            resources:this.storedResources
        }
    },
    methods:{
        removeResource(index){
            this.resources.splice(index,1)
        }
    }
}
</script>