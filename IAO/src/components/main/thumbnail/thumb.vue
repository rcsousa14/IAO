<template>
   <section class="header-row">
            <div class="column">
                <div class="thumbnail-column"></div>
            </div>
            <div class="column">
                <div class="intro-column">

                    <h1>De Web a Mobile Apps, Aprenda a Desenvolver para Produção.</h1>
                </div>
            </div>
        </section>
</template>

<script>
export default {

}
</script>

<style>
.header-row {
     display: flex;
     flex-direction: row;
     flex-wrap: wrap;
     width: 100%;
     justify-content: space-between;
 }
  .column {
     display: flex;
     flex-direction: column;
     flex-basis: 100%;
     flex: 1;
 }
 .info-column {
     font-size: -0.5rem;
     text-align: center;
     margin: 3rem;
     display: flex;
     flex-direction: column;
     justify-content: center;
 }
 
 .thumbnail-column {
     background-color: gray;
     height: 20rem;
     margin: 0.5rem;
 }
 
 .intro-column {
     
      margin: 0.5rem;
 }
 
 .intro-column h1 {
     font-size: 2.6rem;
 }
 @media only screen and (max-width: 600px) {
     .header-row {
         display: flex;
         flex-direction: column-reverse;
         flex-wrap: wrap;
         width: 100%;
         justify-content: space-between;
     }
     .intro-column h1 {
         font-size: 2.45rem;
     } 
     .thumbnail-column {
         height: 15rem;
         margin-top: 0.5rem;
     }
     .intro-column {
         height: 15rem;
         margin-bottom: 0.5rem;
     }
 }
 @media only screen and (min-width: 600px) and (max-width: 900px) {
     .header-row {
         display: flex;
         flex-direction: column-reverse;
         flex-wrap: wrap;
         width: 100%;
         justify-content: space-between;
     }
     .intro-column h1 {
         font-size: 2.4rem;
     }
      .thumbnail-column {
         height: 15rem;
         margin-top: 0.5rem;
     }
     .intro-column {
         height: 15rem;
         margin-bottom: 0.5rem;
     }
     
 }
 @media only screen and (min-width: 900px) and (max-width: 1080px) {
   .intro-column h1 {
         font-size: 2.3rem;
     } 
 }

</style>