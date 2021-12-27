<template>
  <div id="project-holder">
    <h1>Projects</h1>
    <div v-for="project in projects" :key="project.key">
        <h2>
            {{project.name}}
        </h2>
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
        fetch('https://farzan-dev-server.herokuapp.com/projects')
            .then(res => res.json())
            .then(data => this.projects = data)
            .catch(err => console.log(err.message))
    }
}
</script>

<style scoped>
    #project-holder h1{
        color: #fff;
    }
    #project-holder h2{
        color: #fff;
    }
</style>