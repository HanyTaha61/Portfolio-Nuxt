<template>
  <div id="projects">
    <b-container class="main">
      <b-row class="row">
        <div class="col-md-4 project rounded" v-for="(project,index) in projects" :key="index">
          <h2 class="text-center my-3 mb-5 py-3 rounded text-light">
            <a target="_blank" :href= project.url>{{(index)+1}}. {{project.name}}</a>
          </h2>
          <a :href= project.url target="_blank" class="mb-4">
            <img class="img-fluid" :src="require(`../assets/projects/${project.src}`)" :alt= project.name> 
          </a>
          <ol class="list d-block px-2 h2 mr-1 py-3 rounded mb-2"><p>Technologies Used:</p>
            <li class="tech mb-2 pb-2" v-for="(tech, i) in project.technology" :key="i">
              {{tech}}
            </li>
          </ol>
          <h4 class="bg-dark mb-5 p-2">Publish Date: {{project.date}}</h4>
        </div>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  data(){
      return{
          projects:[

            {
              name: 'Vuetify Project Manager',
              src: "vuetify project manager.png",
              url: 'https://serial-depot.netlify.app/',
              technology: ['Vue.js', 'Vuetify'],
              date: 'Oct. 2021'
            },
            {
              name: 'Serial Depot',
              src: "serial depot.jpg",
              url: 'https://serial-depot.netlify.app/',
              technology: ['Nuxt.js', 'Vuetify'],
              date: 'Aug. 2020'
            },            
            {
              name: 'Five for Health',
              src: "54health.png",
              url: 'https://five4health.netlify.app/',
              technology: ['Nuxt.js', 'bootstrap-vue'],
              date: 'June 2020'
            },            
            {
              name: 'My Portfolio',
              src: "portfolio.png",
              url: 'https://hany-portfolio.netlify.app/',
              technology: ['Nuxt.js', 'bootstrap-vue'],
              date: 'Mar. 2020'
            },            
            {
              name: 'Syrian Chicken House',
              src: "Syrian Chicken House.png",
              url: 'https://syrian-chicken-house.netlify.app/',
              technology: ['Vue.js', 'Bootstrap-vue'],
              date: 'Nov. 2019'
            },
            {
              name: 'Dallas Business School',
              src: "dbs.jpg",
              url: 'https://dallas-bussiness-school.netlify.app/',
              technology: ['Bootstrap 4', 'jQuery'],
              date: 'Mar. 2019'
            }
            
          ]
      }
  },
  head(){
    return{
      title: 'Hany | Projects'
    }
  }
}
</script>

<style lang='scss'>
  #projects{
    background-color: #e2e2e2;
    

    .main{
      padding-top: 100px;
        
      .project{
        // box-shadow: -50px 30px 50px #111;
        margin-bottom: 100px;
        background-color: #fff;

        h2{
          font-family: 'Abril Fatface';
          background-color: var(--primary-color);
          text-shadow: 7px 7px 10px #333;
          font-size: 1.5em;

          // @media(max-width: 991px){
          //   font-size: 3.5em;
          // }

          // @media(max-width: 767px){
          //   font-size: 2.4em;
          // }
          

          &:hover a{
            transform: scale(1.1);
            color: #fff;
          }
        }
        a{
          color: #fff;
          overflow: hidden;
          display: block;
          transition: 0.25s;
          text-decoration: none !important;
          
          &:hover img{
            transform: scale(1.2);
          }
          img{
            transition: 0.5s;
            display: block;
          }
        }
        .list{
          font-weight: bold;
          background-color: var(--secondary-color);

          @media(max-width: 767px){
            font-size: 1.5em;
          }

          p{
            width: fit-content;
            padding-bottom: 5px;
            border-bottom: 5px solid #000;
          }

          .tech{
            margin-left: 75px;
            text-decoration: none !important;
            font-weight: normal;
            color: #f9f9f9;
            text-shadow: 3px 3px 3px #000;
          }
        }
      }
    }
  }
</style>