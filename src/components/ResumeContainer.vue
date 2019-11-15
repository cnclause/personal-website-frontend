<template>
    <div class="resume">
        <h1> Technical Skills </h1>
        <ul class="skills-list">
            <!-- <li> Ruby </li> -->
                <img src='../images/ruby.png' alt="ruby" />
            <!-- <li> Rails </li> -->
                <img src='../images/rails.png' alt="rails" />
            <!-- <li> Node.js </li> -->
                <img src='../images/node.png' alt="node" />
            <!-- <li> SQL </li> -->
                <img src='../images/sql.png' alt="sql" />
            <!-- <li> ActiveRecord </li>
                <img src='../images/ruby.png' alt="ruby" /> -->
            <!-- <li> Postgresql </li> -->
                <img src='../images/postgresql.png' alt="postgresql" />
            <!-- <li> JavaScript </li> -->
                <img src='../images/javascript.png' alt="javascript" />
            <!-- <li> HTML </li> -->
                <img src='../images/html.png' alt="html" />
            <!-- <li> CSS </li> -->
                <img src='../images/css.png' alt="css" />
            <!-- <li> React </li> -->
                <img src='../images/react.png' alt="react" />
            <!-- <li> Vue </li> -->
                <img src='../images/vue.png' alt="vue" />
        </ul>
        <div class="employment">
            <h1> Employment History </h1>
            <div class= "employment-card">
                <h3> Executive Director, Timoun Kontan </h3>
                <h4> Port-au-Prince, Haiti </h4>
                <h4> July 2017 - Present </h4>
                <ul>
                    <li> Timoun Kontan exists to empower communities through education </li>
                    <li> Coordinated and implemented a scholarship program, mentorship program, and yoga program  </li>
                    <li> Currently supporting the education of 9 children </li>
                </ul>
            </div>
            <div class= "employment-card">
                <h3> Barista, Copper Door Coffee Roaster </h3>
                <h4> Denver, CO </h4>
                <h4> August 2018 - August 2019 </h4>
                <ul>
                    <li> Responsible for managing shop alone, making drinks and exceptional customer service
                    </li>
                </ul>
            </div>
            <div class= "employment-card">
                <h3> Lead Program Coordinator, World in Conversation </h3>
                <h4> State College, PA </h4>
                <h4> June 2015 - June 2018 </h4>
                <ul>
                    <li> Manages practicum course requirements for 35 students per semester; creates and upheld scheduling systems that fosters distinct pedagogical approach including environment where students learn by working in partnerships that take into account different social demographics including race, class, gender; train students on google applications, create a safe and diverse work environment
                    </li>
                    <li> Manages Excel sheets that monitor daily program analytics, including registration rates, attendance rates, and annual program projections; Supervises an average of 10 undergraduate student interns per semester; create weekly schedules, monitors data entry 
                    </li>
                    <li> Research for NATO Grant, COIL Grant, Climate Change Initiative, International Chinese Student Engagement Initiative 
                    </li>
                    <li> Proficient with data collection and survey applications: Qualtrics, SurveyMonkey, Google Forms
                    </li>
                </ul>
            </div>
        </div>
        <div class="education">
            <h1> Education </h1>
            <div class="education-card">
                <h2> Flatiron School, Denver </h2>
                <h4> 2019 </h4>
                <li> Bootcamp Full Stack Web Development, Ruby on Rails, JavaScript, and React fully immersive program </li>
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
        width: 6rem;
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