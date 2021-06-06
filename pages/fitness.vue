<template>
  <div>
    

       <div class="menu ">
    <div class="menuitems flex fx-space-between">
      <NuxtLink class="links" to="/">INICIO</NuxtLink>
      <NuxtLink class="links " to="sobremi">SOBRE MÍ</NuxtLink>
      <NuxtLink class="links selected" to="proyectos">PROYECTOS</NuxtLink>
      <NuxtLink class="links" to="fotografia">FOTOGRAFÍA</NuxtLink>
      <NuxtLink class="links" to="contacto">CONTACTO</NuxtLink>
     
      
    </div>
       </div>

       
    
    <div class="container">
  
        <div class="title">
          FITNESS HQ
        </div>
        <br>
         <div id="revelar" class="subtitle">
          Un anuncio para un gimnasio americano llamado Fitness HQ
        </div>
    </div>
     <div class="container_bimbo">
        
         <video class="video_bimbo"
          src="../video/bus.mp4"
          controls
          loop
          
        ></video>

    </div>




    <div class="contenido_b">
        <h1 id="hidden" class="title-size">Contexto</h1>
        <p id="hidden" class="txt_container_bimbo"> Se trata de un anuncio para Fitness High Quality, un gimnasio enfocado para empresas.</p>
  

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


  


    const controller = new this.$scrollmagic.Controller({
			globalSceneOptions: {
				triggerHook: 'onLeave',
				duration: "200%" // this works just fine with duration 0 as well
				// However with large numbers (>20) of pinned sections display errors can occur so every section should be unpinned once it's covered by the next section.
				// Normally 100% would work for this, but here 200% is used, as Panel 3 is shown for more than 100% of scrollheight due to the pause.
			}
		});

		// get all slides
		var slides = document.querySelectorAll("section.panel");

		// create scene for every slide
		for (var i=0; i<slides.length; i++) {
			new this.$scrollmagic.Scene({
					triggerElement: slides[i]
				})
				.setPin(slides[i], {pushFollowers: false})
				
				.addTo(controller);
		}




    
    var sceneA = new this.$scrollmagic.Scene({
						
						
							duration: "200%", // hide 10% before exiting view (80% + 10% from bottom)
							offset: 50 // move trigger to center of element
						})
						.setClassToggle("#hidden", "visibility") // add class to reveal
						// add indicators (requires plugin)
						.addTo(controller);
    
    
    var sceneB = new this.$scrollmagic.Scene({
						
						
							duration: "200%", // hide 10% before exiting view (80% + 10% from bottom)
							offset: 50 // move trigger to center of element
						})
						.setClassToggle("#height-out", "visibility") // add class to reveal
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

.contenido_b{
  margin:  auto;
  
  display: flex;
  flex-direction: column;
  padding: 10vw 20vw 5vw 20vw;
  background: rgb(255, 255, 255);
  }


.txt_container_bimbo{
  border-bottom: 1px solid rgba(0, 0, 0, 0.514);
  padding-bottom: 2vw;
  
  line-height: 2.4;

}

#hidden {
  bottom: 0px;
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
	#hidden.visibility {
   bottom: 110px;
		opacity: 1;
		-webkit-transform: none;
			 -moz-transform: none;
				-ms-transform: none;
				 -o-transform: none;
						transform: none;
	}

#zoom-out {
   height: 0%;
   
		opacity: 0;
	
		-webkit-transition: all 1s ease-in-out;
			 -moz-transition: all 1s ease-in-out;
				-ms-transition: all 1s ease-in-out;
				 -o-transition: all 1s ease-in-out;
						transition: all 1s ease-in-out;
	}

  	#zoom-out.visibility {
   height: 500px;
    
		opacity: 1;
		-webkit-transform: none;
			 -moz-transform: none;
				-ms-transform: none;
				 -o-transform: none;
						transform: none;
	}


.bold-w{
  font-weight: 700;
}
.menu{
  display: block;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 2.5vw 2.5vw 0vw 2.5vw;


}

.video_bimbo{
  height: 100%;
}

.container_bimbo {
 // background-image: url("../img/proyecto_bimbo.jpeg");
 //background-attachment: fixed;
 // background-size: cover;
  margin: 0 auto;
  height: 60vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  
  
}
.imagen_bimbo{
  
  height: 500px;
  width: 500px;
  position: relative;
  bottom: -85px;
  box-shadow: 0px 5px 10px 0px rgba(0, 0, 0, 0.521);
  
  
}
.imagen_sobremi > div{
  overflow: hidden;
}

.imagen_sobremi img{
  width: 100%;
  margin-top: 2px;
   
  }

.imagen_sobremi img:hover {
  transform: scale(1.15);
  transition: all .5s ease-in-out;
}

.container_sobremi .etiqueta {
  position:absolute;
  right:-80px;
  background:#000;
  color:#fff;
  font-weight:600;
  bottom: 110px;
  padding: 20px;
}


.txt_container_top{
  width: 30vw;
  line-height: 2.4;
  padding-bottom: 4vw;
}
.txt_container{
  border-top: 1px solid rgba(0, 0, 0, 0.514);
  border-bottom: 1px solid rgba(0, 0, 0, 0.514);
  padding-bottom: 4vw;
  padding-top: 4vw;
  line-height: 2.4;
}


.title-size{
  font-size: 4rem;
  font-weight: 300;
  
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.container3 {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  
  background: aquamarine;
}
.container4 {
  margin: 0 auto;
  height: 50vw;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  
  background: rgb(232, 255, 127);
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
