<template>
  <div>
     
      
       <div class="menu ">
    <div class="menuitems flex fx-space-between">
      <NuxtLink class="links" to="/">INICIO</NuxtLink>
      <NuxtLink class="links" to="sobremi">SOBRE MÍ</NuxtLink>
      <NuxtLink class="links" to="proyectos">PROYECTOS</NuxtLink>
      <NuxtLink class="links" to="fotografia">FOTOGRAFÍA</NuxtLink>
      <NuxtLink class="links selected" to="contacto">CONTACTO</NuxtLink>
     
      
    </div>
       </div>

    <div class="container">

        <h1 class="title">
          Contacta conmigo
        </h1>
        <br>
         <div id="revelar" class="subtitle">
          Si estás interesado en realizar un proyecto o para conocer cualquier tipo de información relacionada.
        </div>
    </div>


<div id="hidden" class="container_form">
  <form action="/action_page.php">
    <label for="fname">Nombre</label>
    <input type="text" id="fname" name="firstname" >

    <label for="lname">Email</label>
    <input type="text" id="lname" name="lastname" >

    <label for="subject">Comentarios</label>
    <textarea id="subject" name="subject"  style="height:200px"></textarea>

    <input type="submit" value="Enviar">
  </form>
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
						
						
							duration: "400%", // hide 10% before exiting view (80% + 10% from bottom)
							offset: 0 // move trigger to center of element
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
.container_form {
  margin-top: 100px;
  height: 40vw;
   display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  overflow: hidden;
}

input[type=text], select, textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-top: 6px;
  margin-bottom: 16px;
  resize: vertical;
}

input[type=submit] {
  background-color: #000000;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type=submit]:hover {
  background-color: #45a049;
}


</style>
