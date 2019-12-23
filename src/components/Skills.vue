<template>
  <div class="skills">
    <div class="row">
      <div class="col-md-6 offset-md-3 mt-5">
        <form  class="from-group" @submit.prevent="addSkill">
        <input class="form-control bg-dark text-white" type="text" v-model="skill" placeholder="Add Skill here...">
        </form>
      </div>     
    </div>
    <div class="row">   
      <div class="col-md-6 offset-md-3 mt-3">
              <ul  class="list-group">
                <li class="list-group-item" v-for="(data,index) in skills" :key="index">{{data.skill}}</li>
            </ul> 
      </div>       
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data(){
    return {
      skill:'',
      skills:[
        {'skill':'vue.js'},
        {'skill':'Frontend Dev'}        
      ]
    }
  },
  methods:{
    addSkill(){
      this.skills.push({'skill':this.skill});
      this.skill = '';
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
