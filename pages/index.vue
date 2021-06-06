<template>
  <div>
   
       
       <div class="menu ">
    <div class="menuitems flex fx-space-between">
      <NuxtLink class="links selected" to="/">INICIO</NuxtLink>
      <NuxtLink class="links " to="sobremi">SOBRE MÍ</NuxtLink>
      <NuxtLink class="links" to="proyectos">PROYECTOS</NuxtLink>
      <NuxtLink class="links" to="fotografia">FOTOGRAFÍA</NuxtLink>
      <NuxtLink class="links" to="contacto">CONTACTO</NuxtLink>
     
      
    </div>
       </div>

    <div class="container">

        <div class="title">
          Hola
        </div>
        <br>
         <div id="revelar" class="subtitle">
          Bienvenid@ a mi portfolio
        </div>
    </div>
    <div class="container_sobremi">
        <div class="imagen_sobremi">
          <div>
            <img src="../img/antonio_duran.jpeg">
          </div>
          <div class="etiqueta"> Antonio Durán</div>
        </div>
       
    </div>

    <div class="container_ilust">
    <section id="revelar_1" class="flex fx-space-between">
          <div class="mi-ilust relative">
           <a class="full absolute ease">
             <div class="absolute full bg-dark hover-cover flex fx-align-center fx-justify-center">
               <h2 class="text-white">ANTONIO</h2>
             </div>
            <img src="../img/ilustracion1.png">
          </a>

          </div>
          <div class="mi-ilust relative">
           <a  class="full absolute ease">
             <div class="absolute full bg-dark hover-cover flex fx-align-center fx-justify-center">
               <h2 class="text-white">ILUSTRES</h2>
             </div>
            <img src="../img/ilustracion2.png">
          </a>
          </div>
          
          </section>

           <section id="revelar_2" class="flex fx-space-between">
          <div class="mi-ilust relative">
           <a  class="full absolute ease">
             <div class="absolute full bg-dark hover-cover flex fx-align-center fx-justify-center">
               <h2 class="text-white">THE 1975</h2>
             </div>
            <img src="../img/ilustracion3.png">
          </a>

          </div>
          <div class="mi-ilust relative">
           <a  class="full absolute ease">
             <div class="absolute full bg-dark hover-cover flex fx-align-center fx-justify-center">
               <h2 class="text-white">METRO</h2>
             </div>
            <img src="../img/ilustracion4.png">
          </a>
          </div>
           </section>
            <section id="revelar_3" class="flex fx-space-between">
        <div class="mi-ilust relative">
           <a  class="full absolute ease">
             <div class="absolute full bg-dark hover-cover flex fx-align-center fx-justify-center">
               <h2 class="text-white">JON</h2>
             </div>
            <img src="../img/ilustracion5.png">
          </a>

          </div>
          <div class="mi-ilust relative">
           <a  class="full absolute ease">
             <div class="absolute full bg-dark hover-cover flex fx-align-center fx-justify-center">
               <h2 class="text-white">DOMINIO MENTAL</h2>
             </div>
            <img src="../img/ilustracion6.png">
          </a>
          </div>
          
          </section>

           <section id="revelar_4" class="flex fx-space-between">
          <div class="mi-ilust relative">
           <a class="full absolute ease">
             <div class="absolute full bg-dark hover-cover flex fx-align-center fx-justify-center">
               <h2 class="text-white">TACTO</h2>
             </div>
            <img src="../img/ilustracion7.png">
          </a>

          </div>
          <div class="mi-ilust relative">
           <a class="full absolute ease">
             <div class="absolute full bg-dark hover-cover flex fx-align-center fx-justify-center">
               <h2 class="text-white">FUERZA</h2>
             </div>
            <img src="../img/ilustracion8.png">
          </a>
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

    
    var scene2 = new this.$scrollmagic.Scene({ triggerElement: '.container3', duration: 300 })
      // trigger a TweenMax.to tween
      .setPin("#animate2")
      // add indicators (requires plugin)
			//.addIndicators({name: "1 (duration: 300)"})
      //.setTween("#animate2", 0.5, {backgroundColor: "white"})
      //.addTo(controller);


      var sceneC = new this.$scrollmagic.Scene({
						
						
							duration: "200%", // hide 10% before exiting view (80% + 10% from bottom)
							offset: 0 // move trigger to center of element
						})
						.setClassToggle("#revelar", "visibility") // add class to reveal
						// add indicators (requires plugin)
						.addTo(controller);

      var sceneD = new this.$scrollmagic.Scene({
						
						
							duration: "200%", // hide 10% before exiting view (80% + 10% from bottom)
							offset: 550 // move trigger to center of element
						})
						.setClassToggle("#revelar_1", "visibility") // add class to reveal
						// add indicators (requires plugin)
						.addTo(controller);

     var sceneE = new this.$scrollmagic.Scene({
						
						
							duration: "200%", // hide 10% before exiting view (80% + 10% from bottom)
							offset: 1100 // move trigger to center of element
						})
						.setClassToggle("#revelar_2", "visibility") // add class to reveal
						// add indicators (requires plugin)
						.addTo(controller);
      
       var sceneE = new this.$scrollmagic.Scene({
						
						
							duration: "2000%", // hide 10% before exiting view (80% + 10% from bottom)
							offset: 1600 // move trigger to center of element
						})
						.setClassToggle("#revelar_3", "visibility") // add class to reveal
						// add indicators (requires plugin)
						.addTo(controller);

       var sceneF = new this.$scrollmagic.Scene({
						
						
							duration: "2000%", // hide 10% before exiting view (80% + 10% from bottom)
							offset: 2150 // move trigger to center of element
						})
						.setClassToggle("#revelar_4", "visibility") // add class to reveal
						// add indicators (requires plugin)
						.addTo(controller);
  }
}
</script>

<style lang="scss">

#revelar_1 {
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
	#revelar_1.visibility {
   
		opacity: 1;
		-webkit-transform: none;
			 -moz-transform: none;
				-ms-transform: none;
				 -o-transform: none;
						transform: none;
	}

  #revelar_2 {
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
	#revelar_2.visibility {
   
		opacity: 1;
		-webkit-transform: none;
			 -moz-transform: none;
				-ms-transform: none;
				 -o-transform: none;
						transform: none;
	}

#revelar_3 {
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
	#revelar_3.visibility {
   
		opacity: 1;
		-webkit-transform: none;
			 -moz-transform: none;
				-ms-transform: none;
				 -o-transform: none;
						transform: none;
	}

#revelar_4 {
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
	#revelar_4.visibility {
   
		opacity: 1;
		-webkit-transform: none;
			 -moz-transform: none;
				-ms-transform: none;
				 -o-transform: none;
						transform: none;
	}


.mi-ilust{
  width: 50%;
  height: 50vw;
  margin: .5vw;
  overflow: hidden;
}

.mi-ilust img{
 // position: absolute;
   height: 100%;
  width: 100%;
  overflow:hidden;
}

.container_ilust {
  padding-top: 100px;
  padding-bottom: 100px;
}

.container2 {
  background-image: url("../img/fondo_aduran.jpeg");
  
  background-size: cover;
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  
  
}
.imagen_presentacion{
  height: 500px;
  width: 500px;
  
  
}
.imagen_presentacion img{
  width: 100%;
  
  
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


</style>
