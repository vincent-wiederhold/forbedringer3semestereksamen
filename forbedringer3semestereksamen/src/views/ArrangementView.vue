<script setup>
import Arrangement from '@/components/Arrangement.vue';
import FooterBottom from '@/components/FooterBottom.vue';
import Navbar from '@/components/Navbar.vue';
</script>


<template>
  <Navbar/>
  <div class="hero arrangementer-hero">
    <h1 class="hero-text">Arrangementer</h1>
  </div>
  <div class="section-wrapper">
    <h2>Se udvalget af Krus og kopperne herunder</h2>
    <p>De keramiske krus og kopper er hos os speciallavet kunsthåndværk, flere forskellige slags kan ses an i butikken</p>
    <Arrangement/>
  </div>
  <FooterBottom/>
</template>
<style scoped lang="scss">

        
    .arrangementsection{
        width: 90%;
        margin: 80px auto;
        .row{
            display: flex;
            flex-wrap: wrap;
            margin: 40px 0px 20px 0px;

            .individualarrangements{
                width: 400px;
                display: flex;
                flex-direction: column;
                margin: 20px auto;
                .arrangementbillede {
                    height: 245px;
                }

                p{
                    padding: 20px 0px;
                }
            }
        }
    }

    @media (min-width: 800px) {

      .arrangementsection{
        margin: 80px 0px;
        .row{
            display: flex;
            flex-wrap: wrap;
            margin: 40px 0px 20px 0px;

            .individualarrangements{
                width: 400px;
                display: flex;
                flex-direction: column;
                margin: 20px auto;
                .arrangementbillede {
                    height: 245px;
                }

                p{
                    padding: 20px 0px;
                }
            }
        }
    }
    }




</style>