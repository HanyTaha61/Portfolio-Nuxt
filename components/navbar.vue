<template>
    <div class="categories container-fluid" id="categories">
        <div class="container-fluid cats">
            <b-navbar toggleable="lg" type="dark" id="navbar" fixed="top">
                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
                <b-collapse id="nav-collapse" is-nav>
                    <b-navbar-nav class="links">
                        <b-nav-item class="ml-5">
                            <nuxt-link exact to="/">Home</nuxt-link>
                        </b-nav-item>
                        <b-nav-item class="ml-5">
                            <nuxt-link to="/about">About Me</nuxt-link>
                        </b-nav-item>
                        <b-nav-item class="ml-5">
                            <nuxt-link to="/cv">My C.V</nuxt-link>
                        </b-nav-item>
                        <b-nav-item class="ml-5">
                            <nuxt-link to="/projects">My Projects</nuxt-link>
                        </b-nav-item>
                        <b-nav-item class="ml-5">
                            <nuxt-link to="/contact">Contact Me</nuxt-link>
                        </b-nav-item>
                    </b-navbar-nav>
                </b-collapse>
            </b-navbar>
        </div>
    </div>
</template>

<script>


export default {
    data(){
        return{
            
        }
    },
    // methods:{
    //     // increase navbar Opacity on scroll
    //     //----------------------------------
    //     navbar_opacity: function navbar_opacity(){
    //     let nav_bar = document.getElementById('navbar')
    //     window.addEventListener('scroll', function(){           
    //         if(window.pageYOffset > 250){
    //             if(window.innerWidth < 991){
    //                 nav_bar.style.backgroundColor = 'rgba(1,1,1, 0.9)'
    //             }else{
    //                 nav_bar.style.backgroundColor = 'rgba(0,0,0,0.75)'
    //             }
    //         }
    //         else{
    //             if(window.innerWidth < 991){
    //                 nav_bar.style.backgroundColor = 'rgba(1,1,1, 0.9)'
    //             }else{
    //                 nav_bar.style.backgroundColor = 'rgba(var(--secondary-hexa),0.5)'
    //             }
    //         }
    //     })
    //     }
    //     // ----------------------------------------------          
    // },
    // mounted(){
    //     // this.navbar_opacity()
    // },    
}
</script>

<style scoped lang='scss'>
.navbar-dark .navbar-toggler{
    background-color: #111;
}
.cats{
    margin-left: -15px;
}
.cats .navbar{
    z-index: 1111;
    background-color: rgba(var(--secondary-hexa), 0.5);
    margin-left: -15px;
    margin-right: -45px;
    transition: 0.3s;

    @media (max-width: 991px) {
        background-color: rgba(1,1,1, 0.9);        
    }

}
.cats .nuxt-link-active{
    background-color:  var(--primary-color);
    color: #fff;
    border-radius: 5px;
    padding: 10px 20px;
    margin-top: 10px;
    font-family: 'Quicksand', sans-serif;
}
.cats a{
    margin-top: 10px;
    font-size: 1.2em;
    font-family: 'Lobster', sans-serif;
    text-decoration: none;
    border-radius: 5px;
    color: #111;
    text-align: center;
    padding: 10px 20px;
    transition: 0.3s;
    color: #fff;

    @media (max-width: 991px) {
    }
}

.navbar .links a:hover{
transform: scale(1.1)
}
</style>
