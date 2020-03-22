<template>
    <div id="skills">
        <div class="layer">
            <b-container>
            <b-img class="img-fluid" src="../assets/cv.jpg" alt="cv"/>
            </b-container>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{

        }
    },
    components:{

    },
    head(){
        return{
            title: 'Hany | C.V'
        }
    }    
}
</script>

<style lang='scss' scoped>
    #skills{
        background-image: linear-gradient( var(--fourth-color),var(--primary-color) ,var(--tertiary-color) );
        background-size: cover;
        position: absolute;
        width: 100%;
        height: 1750px;

        @media(max-width: 1200px){
        height: 1500px;
        }

        @media(max-width: 991px){
        height: 1100px;
        }

        @media(max-width:767px) {
        height: 900px;
        }

        @media(max-width: 600px){
            height: 875px;
        }


        .layer{
            position: relative;
            top: 0;
            left: 0;
            width: 100%;
            background-color: rgba(91, 0, 156,0.1);
            height: 100%;

            img{
                box-shadow: -50px 50px 50px #111;
                margin-top: 100px;
            }
        }
    }
</style>