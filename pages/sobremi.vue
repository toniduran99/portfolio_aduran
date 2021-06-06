<template>
  <div>
    

       <div class="menu ">
    <div class="menuitems flex fx-space-between">
      <NuxtLink class="links" to="/">INICIO</NuxtLink>
      <NuxtLink class="links selected" to="sobremi">SOBRE MÍ</NuxtLink>
      <NuxtLink class="links" to="proyectos">PROYECTOS</NuxtLink>
      <NuxtLink class="links" to="fotografia">FOTOGRAFÍA</NuxtLink>
      <NuxtLink class="links" to="contacto">CONTACTO</NuxtLink>
     
      
    </div>
       </div>

       
    
    <div class="container">

        <div class="title">
          Sobre mí
        </div>
        <br>
         <div id="revelar"  class="subtitle">
          Mi nombre es Antonio Durán, un apasionado por la animación 2D y 3D.
        </div>
    </div>
     <div class="container_sobremi">
        <div  class="imagen_sobremi">
          <div >
            <img src="../img/antonio_duran.jpeg">
          </div>
          <div id="hidden" class="etiqueta"> Antonio Durán</div>
        </div>
       
    </div>




    <div class="contenido_sobremi">
        <h1 id="hidden" class="title-size">Mi experiencia</h1>
        <p id="hidden" class="txt_container_top"> Soy estudiante  de 3º de carrera ee la <a class="bold-w"> Escuela Superior de Diseño de Madrid</a> y siempre he tenido interés por la animación visual, la comunicación y el arte.</p>
  

        <p id="hidden" class="txt_container"> Hola! soy Toni, encantado de saludarte! Cuento un poco sobre mi para que vayas conociéndome 

Soy diseñador gráfico de la ESD especialista en animación e ilustración . He tenido la oportunidad de trabajar para diferentes tipos de agencias de publicidad y grupos musicales.

Actualmente me dedico a la animación audiovisual para una agencia llamada Temper Tatrum, empresa de baile ubicada en Los Ángeles la cual se encarga de mandarme proyectos mensuales.
Si te quedas con ganas de saber algo más en mi currículum tendrás toda la información profesional. Aquí estoy para ayudarte!</p>
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

#revelar {
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
	#revelar.visibility {
   
		opacity: 1;
		-webkit-transform: none;
			 -moz-transform: none;
				-ms-transform: none;
				 -o-transform: none;
						transform: none;
	}



#hidden {
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


.container {
  margin: 2.5vw 2.5vw 2.5vw 2.5vw;
  
   display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.container_sobremi {
  
  background-image: url("../img/esdmadrid-escuela00.jpeg");
 background-attachment: fixed;
  background-size: cover;
  margin: 0 auto;
  height: 60vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  
  
}
.imagen_sobremi{
  min-height: 300px ;
  min-width: 300px ;
  max-height: 500px ;
  max-width: 500px;
  height: 35vw;
  width: 35vw;
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

.contenido_sobremi{
  margin:  auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  padding: 10vw 20vw 5vw 20vw;
  background: rgb(255, 255, 255);
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
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}



.links{
  position: relative;
  display: block;
  text-decoration: none;
  font-size: 20px;
  color: #00000052;
  text-transform: uppercase;
  padding: 4px 0;
  transition: 0.5s;
}
.links:after {
  position: absolute;
  content: "";
  width: 100%;
  height: 3px;
  top: 100%;
  left: 0;
  background: #000000;
  transition: transform 0.5s;
  transform: scaleX(0);
  transform-origin: right;
}
.links:hover {
  color: #000000;
}
.links:hover::after {
  transform: scaleX(1);
  transform-origin: left;
}

.selected{
  color: #000000;
  border-bottom: 3px solid black;
  

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
