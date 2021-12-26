<template>
  <div id="project-holder">
    <h1>Projects</h1>
    <div v-for="project in projects" :key="project.id">
        <h2>
            {{project.name}}
        </h2>
        <!-- <img :src="project.img" alt="image"/> -->
        <img :src="project.img" alt="image" width="400"/>

    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            projects: []
            // projects: [
            //     {name: "Circulr", id: 1, details: "lorem"},
            //     {name: "Muspace", id: 2, details: "lorem"},
            //     {name: "KDJ", id: 3, details: "lorem"}
            // ]
        }
    },
    mounted() {
        fetch('http://localhost:3000/projects')
            .then(res => res.json())
            .then(data => this.projects = data)
            .catch(err => console.log(err.message))
    }
}
</script>

<style scoped>
    #project-holder{
        /* background-color: #000; */
    }
    #project-holder h1{
        color: #fff;
    }
    #project-holder h2{
        color: #fff;
    }
</style>