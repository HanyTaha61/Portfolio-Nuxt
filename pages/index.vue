<template>
  <div class="main">
    <home/>
  </div>
</template>

<script>
import home from '../components/home'
export default {
  components:{home},
  methods:{

  },
  head(){
    return{
      script:[
        {src: ''}
      ]
    }
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Abril+Fatface|Lobster|Quicksand");
@import 'https://use.fontawesome.com/releases/v5.11.2/css/all.css';


  body{
    /* colors */
		--primary-color: #c44569;
    --primary-hexa: 196, 69, 105;
		--secondary-color: rgb(34, 166, 179);
    --secondary-hexa: 34, 166, 179;
    --tertiary-color: rgb(99, 205, 218);
    --fourth-color: rgb(34, 112, 147);
    --fourth-hexa: 34, 112, 147;
    /*--------*/
    
    color: #ccc;
  }
  .routerView{
    position: absolute !important;
    width: 100%
  }
</style>
