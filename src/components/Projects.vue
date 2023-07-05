<template>
    <section id="projects-section">
    <div id="project-holder">
        <h2 class="section-title">Projects</h2>
        <div v-for="(project, index) in projects" :key="project.key" id="project-row" :index="project.id" >
            <div v-if="project" id ="project-main" v-bind:class="{ reverse: !( index % 2 != 0) }">
                <div id="project-img">
                    <img :src="project.img" alt="image"/>
                </div>
                <div id="project-details" >
                    <h3 id ="project-name">{{project.name}}</h3>
                    <div id="project-tags">
                        <span v-for="tag in project.tags" :key="tag">{{tag}}</span>
                    </div>
                    <p v-html="project.details"></p>
                    <div id="project-links" v-html="project.links"></div>

                </div>
            </div>
            <div v-else>
                <p id="loading">Loading Projects...</p>
            </div>
        </div>
    </div>
    </section>
</template>

<script>

export default {
    data() {
        return {
            projects: [
                {
                    name: "Circulr", 
                    id: 1, img:"https://i.imgur.com/BKBfzOo.png", 
                    tags:[
                        "Mobile",
                        "iOS",
                        "Android",
                        "Flutter",
                        "Dart",
                        "Firebase",
                        "STRIPE",
                    ], 
                    links: "<a href='https://apps.apple.com/ca/app/circulr-reuse/id1605639496' target='_blank'>App Store</a> <a href='https://play.google.com/store/apps/details?id=com.circulrshop.circulr' target='_blank'>Play Store</a> <a href='https://github.com/zancrash/Circulr' target='_blank'>Github</a>",
                    details: "Circulr is a cross-platform mobile application developed using the Flutter framework. Circulr helps its users to track products purchased from participating businesses so they they can return used containers and encourage reuse. The app uses a firebase back-end for user authentication and data storage, as well as the STRIPE API to make payments."
                },
                {
                    name: "MuSpace", 
                    id: 2, 
                    img:"https://i.imgur.com/H15ueAB.png", 
                    tags:[
                        "ReactJS",
                        "Javascript",
                        "Firebase",
                        "Social Media"
                    ], 
                    links: "<a href='https://github.com/SherRao/MuSpace/' target='_blank'>Github</a>",
                    details: "MuSpace is a music sharing platform with the goal of connecting with similar listeners. My classmates and I built MuSpace as a project for our software engineering course. MuSpace uses the ReactJS framework for the user-facing side, and Firebase to store and serve data."
                },
                {
                    name: "UFCW", 
                    id: 3, 
                    img:"https://i.imgur.com/g6JnOW0.png", 
                    tags:[
                        "HTML",
                        "CSS",
                        "JS",
                        "WordPress"
                    ], 
                    links: "<a href='https://www.ufcw175.com/' target='_blank'>Website</a>",
                    details: "A website developed for the UFCW Local 175 & 633 labour union. The site was built using HTML, CSS, and JS, and uses the Wordpress CMS to serve content. I collaborated closely with the union representatives to understand their needs and goals, as well as my own team. UFCW was the largest client we took on during my time at Firefly Creative Inc."
                },
                {
                    name: "KDJ", 
                    id: 4, 
                    img:"https://i.imgur.com/ejl9sSi.png", 
                    tags:[
                        "HTML",
                        "CSS",
                        "JS",
                        "WordPress"
                    ],
                    links: "<a href='https://kellyjordanfamilylaw.com/' target='_blank'>Website</a>",
                    details: "Website built for the KDJ Family Law Firm. I used HTML, CSS, and JS with the WordPress CMS to allow for blog hosting and profile pages. I also utilized the ScrollMagic JavaScript library to integrate web animations. The site allows potential clients to gain information regarding their family law needs, and see which member of the KDJ team would be best suited for their needs."
                },
                {
                    name: "Rutherford & Mathews", 
                    id: 5, 
                    img:"https://i.imgur.com/gKSx5yk.png", 
                    tags:[
                        "HTML",
                        "CSS",
                        "JS",
                        "WordPress"
                    ], 
                    links: "<a href='https://rutherfordmathews.com/' target='_blank'>Website</a>",
                    details: "R&M is a condominium law firm, the website I built for them is created using the WordPress CMS to allow for quick content updates and blogs, as well as allowing users to sign up for newsletters using Mailchimp integration. The site was coded with HTML, CSS, and JS. "
                }
            ]
            
        }
    },
    // mounted() {
    //     fetch('https://farzan-dev-server.herokuapp.com/projects')
    //         .then(res => res.json())
    //         .then(data => this.projects = data)
    //         .catch(err => console.log(err.message))
    // }
}
</script>

<style>
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
        /* background-color: #272336; */

    }
    .section-title{
        color: #5dedcd;
        font-size: 4em;
    }
    #loading{
        color: #5dedcd;
        font-family: 'Roboto Mono', monospace;
        font-size: 3em;
    }
    #project-img{
        display: flex;
        width: 50%;
    }
    #project-img img{
        width: 100%;
        align-self: center;
    }
    #project-details{
        width: 50%;
        padding: 0 2% 0 2%;
    }
    #project-name{
        margin: 0;
        color: #fff;
        font-size: 3em;
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
    #project-details p{
        color: #fff;
        font-size: 18px;
    }
    #project-links{
        display: flex;
    }
    #project-links a{
        text-decoration: none;
        margin: 0 25px 0 0;
        font-weight: bold;
        color: #5dedcd;
    }
    #project-links a p{
        color: #5dedcd;
        background-color: #003328;
    }
    #project-tags span{
        font-size: 1em;
        margin: 10px 15px 0 0;
        /* color: #000; */
        background-color: #47415c;
        padding: 5px 10px 5px 10px;
        display: inline-flex;
        /* border-radius: 5px; */
        color: #5dedcd;
        font-family: 'Roboto Mono', monospace;
    }


/* 1024px wide or less */
@media screen and (max-width: 1024px) {
    .section-title{
        font-size: 3.5rem;
    }
}

/* 800px wide or less */
@media screen and (max-width: 800px) {
    #project-main{
        flex-direction: column;
    }
    #project-name{
        margin: 20px 0 0 0;
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