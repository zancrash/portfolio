<template>
    <section id="projects-section">
    <div id="project-holder">
        <h2 class="section-title">Projects</h2>
        <div v-for="(project, index) in projects" :key="project.key" id="project-row" :index="project.id" >
            <div id ="project-main" v-bind:class="{ reverse: !( index % 2 != 0) }">
                <div id="project-img">
                    <img :src="project.img" alt="image"/>
                </div>
                <div id="project-details" >
                    <h3 id ="project-name">{{project.name}}</h3>
                    <p>{{project.details}}</p>
                </div>
            </div>
        </div>
    </div>
    </section>
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
    .reverse{
        /* order: 1; */
        flex-direction: row-reverse;
    }
    #projects-section{
        display: flex;
        justify-content: center;
        /* flex-direction: column; */
        margin: 0 0 100px 0;
    }
    #project-holder{
        width: 80%;
        max-width: 1344px;
    }
    #project-row{
        margin: 100px 0 0 0;
    }
    .section-title{
        color: #fff;
        font-size: 3rem;
    }
    #project-img{
        display: block;
        width: 50%;
    }
    #project-img img{
        width: 100%;
    }
    #project-details{
        /* display: flex;
        flex-direction: column;
        justify-content: space-between; */
        width: 50%;
        padding: 0 2% 0 2%;
    }
    #project-name{
        margin: 0;
        color: #5dedcd;
        font-size: 2em;
    }
    /* #links-holder{
        width: 100px;
        height: 20px;
        align-self: flex-end;
        background-color: grey;
    } */
    #project-main{
        display: flex;
        /* justify-content: center; */
        width: 100%;
        text-align: left;
    }
    #project-main p{
        color: #fff;
        font-size: 18px;
    }

/* 1024px wide or less */
@media screen and (max-width: 1024px) {
    .section-title{
        font-size: 2.5rem;
    }
}

/* 800px wide or less */
@media screen and (max-width: 800px) {
    #project-main{
        flex-direction: column;
    }
    #project-details{
        width: 100%;
    }
    #project-img{
        width: 100%;
    }

}

/* 600px wide or less */
@media screen and (max-width: 600px) {
}

/* 450px wide or less */
@media screen and (max-width: 450px) {
}

</style>