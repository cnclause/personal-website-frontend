<template>
    <div class="resume">
        <h1> Technical Skills </h1>
        <ul class="skills-list">
                <img src='../images/ruby.png' alt="ruby" />
                <img src='../images/rails.png' alt="rails" />
                <img src='../images/node.png' alt="node" />
                <img src='../images/express.png' alt="express" />
                <img src='../images/knex.png' alt="knex" />
                <img src='../images/sql.png' alt="sql" />
                <img src='../images/postgresql.png' alt="postgresql" />
                <img src='../images/javascript.png' alt="javascript" />
                <img src='../images/html.png' alt="html" />
                <img src='../images/css.png' alt="css" />
                <img src='../images/react.png' alt="react" />
                <img src='../images/vue.png' alt="vue" />
                <img src='../images/vuex.png' alt="vuex" />
        </ul>
        <div class="employment">
            <h1> Employment History </h1>
            <div class= "employment-card">
                <h3> Executive Director, Timoun Kontan </h3>
                <h4> Port-au-Prince, Haiti </h4>
                <h4> July 2017 - Present </h4>
                <ul>
                    <li> Analyzed our research results to design relevant community programs to address 50% of children not being in school and over 30% of the families requesting assistance with health and wellness </li>
                    <li> Established framework of implementing mentorship program during political unrest to keep children safe and educated, in collaboration with the Haitian team </li>
                    <li> Implemented a multi-faceted model that encompasses a scholarship, mentorship, and health and wellness program </li>
                    <li> Created and executed community programs from the ground up, using social media campaigns, fundraisers, corporate sponsorships, and reaching out to donors </li>
                    <li> Curated an art exhibit using local artists to bring awareness and funding to the organization and local art community </li>
                    <li> Built a model automating the calculations of funding and expenses within excel to make budget oversight more efficient</li>
                </ul>
            </div>
            <div class= "employment-card">
                <h3> Lead Program Coordinator, World in Conversation </h3>
                <h4> State College, PA </h4>
                <h4> June 2015 - June 2018 </h4>
                <ul>
                    <li> Data analytics for NATO Grant, COIL Grant, Climate Change Initiative, International Chinese Student Engagement Initiative 
                    </li>
                    <li> Proficient with data collection and survey applications: Qualtrics, SurveyMonkey, Google Forms
                    </li>
                    <li>Delivered solutions for logistical efficiency by designing excel sheets that monitor daily program analytics</li>
                    <li> Managed practicum course requirements for 35 students per semester</li>
                    <li> Created and upheld scheduling systems that fosters distinct pedagogical approach including environment where students learn by working in partnerships that take into account different social demographics including race, class, gender</li>
                    
                </ul>
            </div>
        </div>
        <div class="education">
            <h1> Education </h1>
            <div class="education-card">
                <h2> Flatiron School, Denver </h2>
                <h4> 2019 </h4>
                <li> Full Stack Software Engineering Program</li>
                <li> 15 week immersive program</li>
                <li> Volunteered for beginners’ code day</li>
                <li> Lead multiple team trainings on LinkedIn and white-boarding</li>
                <li> Facilitated development, mission, and vision for local women’s meetup</li>
            </div>
            <div class="education-card">
                <h2> The Pennsylvania State University, University Park </h2>
                <h4> 2016 </h4>
                <li> Bachelors: Honors in Sociology and Criminology</li>
            </div>
        </div>
    </div>
</template>

<script>

</script>

<style scoped lang="scss">

    .resume{
        display: flex;
        flex-flow: column;
        align-items: center;
        padding-top: 3rem;
    }

    .skills-list{
        display: flex;
        flex-flow: wrap;
        max-width: 50%;
        justify-content: center;
        list-style-type: none;
        padding: 1rem;
        line-height: 30px;
    }

    .skills-list img{
        max-width: 8rem;
        height: 6rem;
        margin: 1rem;
    }

    .employment, .education{
        display: flex;
        flex-direction: column;
        align-items:center;

    }

    .education-card{
        list-style-type: none;
    }

    .education-card h2{
    color: 	#38C3FF;
    font-size: 17pt;
   
    }

   .employment-card li:before {
    content: "+";
    }

   .education-card li:before {
    content: "+";
    }

    .employment-card, .education-card {
        line-height: 30px;
        max-width: 60%;
        padding: 1rem;
    }
    .employment-card h3{
        line-height: 30px;
        color: #38C3FF;
        font-size: 17pt;
    }

    h1 {
        color: #1955Fa;
        font-size: 25pt;
    }

</style>