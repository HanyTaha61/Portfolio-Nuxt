<template>
<div class="home">
  <div class="layer">
    <div class="container">
      <div class="title">
        <h1 class=" text-light">Hi, I'm</h1>   
        <h2 class="">Hany Taha</h2>
        <p class=" text-light">
          Front-End Engineer
          <span class="d-block px-2">
            &lt; Vue developer /&gt;
          </span>
        </p>
        <div class="typer_dev">
          <p>
            <p class="help">I Can help in:</p>
            <span class="typer"
            data-delay="50"
            data-words="Optimizing web pages for maximum speed and scalability,Determining the structure and design of web pages,Striking a balance between functional and aesthetic design,Maintaining working websites, Working in a team using latest technology"
            data-delete-delay="1500">
            </span>
            <span class="cursor" data-owner="first-typer" data-cursor-display='|'></span>
          </p>
        </div>
      </div>
    </div>
  </div>  
</div>
</template>

<script>
// import vueTyper from 'vue-typer'

export default {
  components:{
    // vueTyper
  },
  head(){
      return{
        title: 'Hany | Home Page',
        script:[
          {src: 'https://unpkg.com/typer-dot-js@0.1.0/typer.js'}
        ]
      }
    }    
  }
</script>

<style lang='scss' scoped>
.home{
  background: url('../assets/home.jpg') no-repeat center center;
  background-size: cover;
  position: absolute;
  width: 100%;

  .layer{
    padding-top: 100px;
    position: relative;
    top: 0;
    left: 0;
    width: 100%;
    background-color: rgba(0,0,0, 0.1);
  }

  .title {
    padding-top: 150px;
    height: 837px;

    @media (max-width: 705px) {
    height: 820px;
    }
    
    
  .typer_dev{

    .cursor{
      font-size: 3em;
      color: var(--primary-color)
   }

    p{
      font-size: 2.5em;
      color: var(--tertiary-color);
    }
    .typer{
      background-color: rgba(0,0,0,0.5);
      margin-top: -20px !important;
      padding: 5px 10px;
      color: var(--primary-color) !important;
      font-size: 2em;
      
      @media (max-width: 705px) {
      font-size: 1.5em;
      }    
    }
  }


    h1{
      font-size: 7rem !important;
      @media (max-width: 705px) {
        font-size: 3rem !important;
      }
    }

    h2{
      width: fit-content;
      padding: 5px;
      border-radius: 5px;

      @media (max-width: 992px) {
          font-size: 3rem !important;
      }
    }

    p{
      font-family: 'Quicksand';
      font-size: 3rem;
      color: #ccc;

      @media (max-width: 705px) {
        font-size: 2rem !important;
      }

      span{
        color: var(--primary-color);
        background: rgba(1, 1, 1, 0.4);
        width: fit-content;
      }
    }

    h1, h2{
      color: var(--secondary-color);
      font-size: 7rem;
      font-family: 'Abril Fatface';
    }

    h1, p{
      color: #ccc;
    }
  }
}


</style>