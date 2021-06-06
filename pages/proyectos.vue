<template>
  <div>
    
      
       <div class="menu ">
    <div class="menuitems flex fx-space-between">
      <NuxtLink class="links" to="/">INICIO</NuxtLink>
      <NuxtLink class="links" to="sobremi">SOBRE MÍ</NuxtLink>
      <NuxtLink class="links selected" to="proyectos">PROYECTOS</NuxtLink>
      <NuxtLink class="links" to="fotografia">FOTOGRAFÍA</NuxtLink>
      <NuxtLink class="links" to="contacto">CONTACTO</NuxtLink>
     
      
    </div>
       </div>
  
 <div class="container">

        <h1 class="title">
          Proyectos
        </h1>
        <br>
         <div id="revelar" class="subtitle">
          Estos son algunos de mis últimos proyectos
        </div>
    </div>

   <div class="container_proj">
    <section id="revelar" class="flex fx-space-between">
          <div class="mi-proj relative">
           <NuxtLink to="bimbo" class="full absolute ease">
             <div class="absolute full bg-dark hover-cover flex fx-align-center fx-justify-center">
               <h2 class="text-white">ANUNCIO BIMBO</h2>
             </div>
            <img src="../img/proyecto_bimbo.jpeg">
          </NuxtLink>

          </div>
          <div class="mi-proj relative">
           <NuxtLink to="book" class="full absolute ease">
             <div class="absolute full bg-dark hover-cover flex fx-align-center fx-justify-center">
               <h2 class="text-white">BOOK TRAILER</h2>
             </div>
            <img src="../img/proyecto_trailer.jpeg">
          </NuxtLink>
          </div>
          
          </section>

           <section id="reveal1" class="flex fx-space-between">
          <div class="mi-proj relative">
           <NuxtLink to="vet" class="full absolute ease">
             <div class="absolute full bg-dark hover-cover flex fx-align-center fx-justify-center">
               <h2 class="text-white">ANUNCIO VET</h2>
             </div>
            <img src="../img/proyecto_vet.jpeg">
          </NuxtLink>

          </div>
          <div class="mi-proj relative">
           <NuxtLink to="fitness" class="full absolute ease">
             <div class="absolute full bg-dark hover-cover flex fx-align-center fx-justify-center">
               <h2 class="text-white">VIDEO INTRO BUSINESS GYM</h2>
             </div>
            <img src="../img/proyecto_bus.jpeg">
          </NuxtLink>
          </div>
          
          </section>

         
       
  </div>
  <footer class="bg-darkness">
    <div class="container-box flex fx-justify-center fx-space-between">
      <div class="info align-center">
        <h4 class="text-white">Hablemos de tu proyecto</h4> <br>
        <p class="text-white">Mejora tu identidad corporativa para adaptarla a los nuevos tiempos. Una gran decisión, que acarreará muy buenos beneficios.</p>
      </div>


       <div class="info align-center">
        <h4 class="text-white">¿Quieres una animación?</h4> <br>
        <p class="text-white">Ponte en contacto conmigo en el apartado de contacto.</p>
      </div>
    </div>
    <h4 class="text-white align-center" style="font-size:30px">antonio.duran.hat@gmail.com</h4> <br>
  </footer>
    
   
  </div>
  

</template>

<script>
export default {
  mounted(){

 const controller = new this.$scrollmagic.Controller();
    
    new this.$scrollmagic.Scene({
						
						
							duration: "200%", // hide 10% before exiting view (80% + 10% from bottom)
							offset: 50 // move trigger to center of element
						})
						.setClassToggle("#reveal1", "visible") // add class to reveal
						// add indicators (requires plugin)
						.addTo(controller);


      var sceneC = new this.$scrollmagic.Scene({
						
						
							duration: "200%", // hide 10% before exiting view (80% + 10% from bottom)
							offset: 0 // move trigger to center of element
						})
						.setClassToggle("#revelar", "visibility") // add class to reveal
						// add indicators (requires plugin)
						.addTo(controller);

  }
}
</script>

<style lang="scss">
.info h4{
  font-size: 30px;
}
.info p{
  font-size: 20px;
}

#reveal1 {
		opacity: 0;
		-webkit-transform: scale(0.9);
			 -moz-transform: scale(0.9);
				-ms-transform: scale(0.9);
				 -o-transform: scale(0.9);
						transform: scale(0.9);
		-webkit-transition: all 1s ease-in-out;
			 -moz-transition: all 1s ease-in-out;
				-ms-transition: all 1s ease-in-out;
				 -o-transition: all 1s ease-in-out;
						transition: all 1s ease-in-out;
	}
	#reveal1.visible {
		opacity: 1;
		-webkit-transform: none;
			 -moz-transform: none;
				-ms-transform: none;
				 -o-transform: none;
						transform: none;
	}




.imagen_presentacion{
  height: 500px;
  width: 500px;
  
  
}
.imagen_presentacion img{
  width: 100%;
  
  
}




.imagen_fondo{
  height: 40vw;
  width: 95vw;
   max-width: 100%;
 max-height: 100%;
 

}
.imagen_fondo img{
  height: 100%;
  width: 100%;
   max-width: 100%;
 max-height: 100%;
 

}



.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  margin-right: 50px;
  margin-left: 50px;
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.container_proj {
  padding-top: 100px;
  padding-bottom: 100px;
}


.mi-proj{
  width: 50%;
  height: 40vh;
  margin: .5vw;
  overflow: hidden;
}

.mi-proj img{
 // position: absolute;
    margin: auto;
    height: 40vh;
  width: 100%;
  object-fit: cover;
}

/*FOOTER*/
footer{
  height: 20vw;
}

footer .info{
  
  width:33.333%
} 


/*COLORS*/
.text-white {color:#fff;}
.bg-dark {background:#35495e8f}
.bg-darkness {background:#000000}

/*BOX RULES*/
.container-box {
  max-width:1200px; /*HAY QUE AJUSTAR*/
  margin:0 auto;
  padding-top:30px;
  padding-bottom:30px;
}
.relative {position:relative;}
.absolute {position: absolute;}
.absolute.full {top:0;right:0;bottom:0; left:0;} 
.align-center {text-align:center;}

.hover-cover {opacity:0}
a:hover .hover-cover {opacity:1}


/* FLEX RULES */
	.flex.row:before, .flex.row:after, .flex.container:before, .flex.container:after {
	  display: none;
	}

	.flex {
	  display: -webkit-box !important;
	  display: -ms-flexbox !important;
	  display: flex !important;
	}
	.visible-phone.flex {
		display:none !important;
	}

	/* y axis */
	.fx-align-center { 
	  -ms-flex-align: center;
	  -webkit-box-align: center;
	  align-items: center;
	}

	.fx-align-end {
	  -ms-flex-align: end;
	  -webkit-box-align: end;
	  align-items: flex-end;
	}
	.fx-align-stretch {
	  -ms-flex-align: stretch;
	  -webkit-box-align: stretch;
	  align-items: stretch;	
	}

	/* x axis */
	.fx-justify-center {
	  -ms-flex-pack: center;
	  -webkit-box-pack: center;
	  justify-content: center;
	}

	.fx-space-between {
	  -ms-flex-pack: justify;
	  -webkit-box-pack: justify;
	  justify-content: space-between;
	}

	.fx-justify-end {
	  -webkit-box-pack: end;
	  -ms-flex-pack: end;
	  justify-content: flex-end;
	}
	.fx-justify-start {
	  -webkit-box-pack: start;
	  -ms-flex-pack: start;
	  justify-content: flex-start;
	}

	/* changing axes */
	.fx-column {
	  -webkit-box-orient: vertical;
	  -webkit-box-direction: normal;
	  -ms-flex-direction: column;
	  flex-direction: column;
	}

	/* break line */
	.fx-wrap {
	  -ms-flex-wrap: wrap;
	  -webkit-box-orient: horizontal;
	  -webkit-box-direction: normal;
	  -ms-flex-flow: row wrap;
	  flex-flow: row wrap;
	  flex-wrap: wrap;
	}

  /*ANIMATION RULE*/
  .ease, .ease * {
    transition: 0.3s all ease-out;
  }  
</style>
