<template>
    <div>
        <v-card class='banner-img elevation-0 d-flex align-center' height='100vh'>          
            <v-container>
                <svg class='blob1' viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'>
                    <path d='M36.5,-38.9C50.2,-22.9,66.1,-11.4,66.3,0.2C66.4,11.8,50.9,23.6,37.2,38.9C23.6,54.3,11.8,73.3,-2.1,75.5C-16.1,77.6,-32.1,62.9,-48.1,47.5C-64.2,32.1,-80.1,16.1,-77.7,2.5C-75.2,-11.1,-54.3,-22.3,-38.3,-38.3C-22.3,-54.4,-11.1,-75.3,0.1,-75.4C11.4,-75.5,22.9,-54.9,36.5,-38.9Z' transform='translate(100 100)' />
                </svg>
                <svg class='blob2 text-start' viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'>
                    <path d='M40.6,-56C48,-50.6,46.2,-32.5,47,-18.1C47.8,-3.7,51.2,7,50.5,18.6C49.8,30.2,44.9,42.7,35.8,48C26.7,53.4,13.4,51.6,2,48.9C-9.4,46.1,-18.8,42.4,-32,38.4C-45.3,34.4,-62.6,30.2,-65.6,21.2C-68.6,12.3,-57.5,-1.4,-50.6,-14.5C-43.7,-27.7,-41.1,-40.3,-33.4,-45.7C-25.7,-51.1,-12.8,-49.2,1.9,-51.8C16.6,-54.4,33.2,-61.5,40.6,-56Z' transform='translate(100 100)' />
                </svg>
                <svg class='blob3 align-end' viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                    <path d='M52,-43.1C63.6,-27,66.5,-5.6,63,16.2C59.4,37.9,49.5,60,33.7,66.3C17.8,72.5,-3.9,62.8,-14.8,50.1C-25.6,37.4,-25.7,21.6,-34.4,2.5C-43.1,-16.7,-60.4,-39.3,-56.1,-53.8C-51.8,-68.2,-25.9,-74.5,-2.8,-72.2C20.2,-70,40.4,-59.2,52,-43.1Z' transform='translate(100 100)' />
                </svg>
                <v-row>
                    <v-col cols='12' lg='6'>                      
                        <div>
                            <v-card-text class='pa-0'>
                                <v-card-title 
                                class='primaryFont--text text-lg-h1 text-md-h2 text-h4 font-weight-bold' 
                                style='opacity: 0.15;'
                                z-index='1'>
                                Software Engineer
                                </v-card-title>
                                <v-card-title 
                                class='primaryFont--text text-lg-h3 text-md-h4 text-h5 font-weight-bold mx-4 mt-n14 mx-lg-12 mt-lg-n16' 
                                absolute>
                                Vladislav Rumyantsev
                                </v-card-title>
                                <p class='tertiaryFont--text mx-4 mt-lg-0 mt-0 text-lg-subtitle-1 text-caption'>
                                    Welcome to the portfolio page! Here you can find several home projects.
                                </p>                     
                            </v-card-text>                    
                            <v-card-actions class='mx-2'>
                                <v-btn 
                                class='secondary primaryFont--text rounded-pill font-weight-bold pa-lg-6 mt-lg-6 mt-4 pa-5' 
                                depressed text>
                                Let's Start
                                    <v-icon 
                                    class='ml-lg-16 ml-8 mr-lg-n6 mr-n6 tertiary tertiaryFont--text rounded-r-pill pa-lg-3 pa-2'>
                                    mdi-arrow-right
                                    </v-icon>
                                </v-btn>
                            </v-card-actions>
                        </div>
                    </v-col>
                    <v-col cols='12' lg='6' class='d-lg-flex d-none justify-end'>
                        <div>
                            <v-card-text class="pa-0">
                                <v-img class='' src='/Server.svg' width='350' cover></v-img>
                            </v-card-text>
                        </div>
                    </v-col>
                </v-row>
            </v-container>
            <div class='custom-shape-divider-bottom-1692457725'>
                <svg data-name='Layer 1' xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1200 120' preserveAspectRatio='none'>
                    <path d='M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z' class='shape-fill'></path>
                </svg>
            </div>
        </v-card>

        <v-card class='my-4 elevation-0 d-flex align-center'>
            <v-container>
                <div class="text-center">
                    <h2 class="primaryFont--text mt-2">Projects</h2>
                    <v-divider class="tertiary mx-auto mt-4 mb-8" width="40"></v-divider>
                </div>
                <v-row class="my-4">
                    <v-col v-for='(w, index) in webSites' :key="index" lg='4'>
                        <v-card 
                        class='mx-auto pa-3 rounded-xxl'
                        style='box-shadow: rgba(0, 0, 0, 0.1) 0px 10px 50px;'>
                            <v-img
                            class='rounded-xl'
                            height='200'
                            :src='w.img'
                            cover
                            >
                            </v-img>
                            <v-card-title class='primaryFont--text'>{{ w.title }}</v-card-title>
                            <v-card-subtitle class='secondaryFont--text pt-'>{{ w.category }}</v-card-subtitle>
                            <v-card-text>
                                <div>{{ w.description }}</div>
                            </v-card-text>
                            <v-card-actions>
                                <v-btn color='primary' :href="w.visitSite" depressed>Explore</v-btn>
                            </v-card-actions>
                        </v-card>
                    </v-col>
                </v-row>
            </v-container>
        </v-card>  
    </div>
</template>

<script>
export default {
    name: 'IndexLayout',
    data() {
        return {
            webSites: [
                {
                    img: 'project_screen_1.png',
                    title: 'Musix',
                    category: 'Music Player',
                    description: 'Classic audio player made by VUE.JS with own design.',
                    visitSite: 'https://musix-audio.netlify.app',
                }
            ]
        }
    },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montaga&family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

.name {
    font-family: 'Montaga', serif;
}
.blob1 {
    position: absolute;
    width: 400px;
    top: 45%;
    left: 0%;
    z-index: 0;
    path {
        fill: #2d3520;
        opacity: 0.15;
    }
}
.blob2 {
    position: absolute;
    width: 400px;
    left: 80%;
    top: 20%;
    z-index: 0;
    path {
        fill: #748ac7;
        opacity: 0.15;
    }
}
.blob3 {
    position: absolute;
    width: 400px;
    left: 40%;
    top: 0%;
    z-index: 0;
    path {
        fill: #3b5570;
        opacity: 0.15;
    }
}
.banner-img {
    background: rgb(116,138,199);
    background: linear-gradient(150deg, rgba(116,138,199,1) 0%, rgba(158,174,207,1) 30%, rgba(200,192,197,1) 100%);
}
.custom-shape-divider-bottom-1692457725 {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    overflow: hidden;
    line-height: 0;
    transform: rotate(180deg);
}
.custom-shape-divider-bottom-1692457725 svg {
    position: relative;
    display: block;
    width: calc(150% + 1.3px);
    height: 100px;
}
.custom-shape-divider-bottom-1692457725 .shape-fill {
    fill: #FFFFFF;
}

/* Mobiles */
@media only screen and (max-width: 600px) {
    .custom-shape-divider-bottom-1692457725 svg {
        height: 50px;
    }
    .blob1 {
        width: 200px;
        top: 50%;
    }
    .blob2 {
        width: 200px;
        left: 55%;
        top: 20%;
    }
    .blob3 {
        width: 200px;
        left: 20%;
        top: 0%;
    }

    
    
}
/* Tablets anf Laptops */
@media only screen and (min-width: 600px) {

}
</style>