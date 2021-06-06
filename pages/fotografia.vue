<template>
  <div>
   
       
       <div class="menu ">
    <div class="menuitems flex fx-space-between">
      <NuxtLink class="links" to="/">INICIO</NuxtLink>
      <NuxtLink class="links " to="sobremi">SOBRE MÍ</NuxtLink>
      <NuxtLink class="links" to="proyectos">PROYECTOS</NuxtLink>
      <NuxtLink class="links selected" to="fotografia">FOTOGRAFÍA</NuxtLink>
      <NuxtLink class="links" to="contacto">CONTACTO</NuxtLink>
     
      
    </div>
       </div>

    <div class="container">

        <div class="title">
          Fotografía
        </div>
        <br>
         <div id="revelar" class="subtitle">
          Uno de mis rincones favoritos
        </div>
    </div>
     <div class="menu_img">
    <div class="menu_img fx-align-center ">
     <NuxtLink class="links_img selected_img" to="fotografia">CARRETE 1</NuxtLink>
      <NuxtLink class="links_img" to="fotografia_carrete2">CARRETE 2</NuxtLink>
      </div>
       </div>

   <section class="panel bg-darkness">
    <div class="images_1">
	<img src="../img/carrete_b/a.jpg"></div>
</section>
<section class="panel bg-darkness">
  <div class="images_1">
	<img src="../img/carrete_b/b.jpg"></div>
</section>
<section class="panel bg-darkness">
  <div class="images_1">
		<img src="../img/carrete_b/c.jpg"></div>
</section>
 <section class="panel bg-darkness">
    <div class="images_1">
	<img src="../img/carrete_b/d.jpg"></div>
</section>
<section class="panel bg-darkness">
  <div class="images_1">
	<img src="../img/carrete_b/e.jpg"></div>
</section>
<section class="panel bg-darkness">
  <div class="images_1">
		<img src="../img/carrete_b/f.jpg"></div>
</section>
<section class="panel bg-darkness">
  <div class="images_1">
		<img src="../img/carrete_b/g.jpg"></div>
</section>
<section class="panel bg-darkness">
  <div class="images_1">
		<img src="../img/carrete_b/h.jpg"></div>
</section>
  

    
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

	.panel {
    height: 60vw;
	
	}
  .images_1{
    height: 60vw;
   
  }
   .images_1 img{
    height: 100%;
    padding: 4vw;
     display: block;
    margin-left: auto;
    margin-right: auto;
  }

  











.links_img{
  position: relative;
  display: block;
  text-decoration: none;
  font-size: 20px;
  color: #00000052;
  text-transform: uppercase;
  padding: 4px 0;
  transition: 0.5s;
}

.menu_img{
  display: block;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 0vw 2.5vw 0vw 2.5vw;


}
.selected_img{
  color: #000000;
  
  

}
</style>
