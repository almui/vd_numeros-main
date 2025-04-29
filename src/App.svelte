<script>
  import * as d3 from "d3"

  import OscaStatue from "./lib/OscaStatue.svelte"


  let numbers = [{pelicula:"The Departed (2006)", cantidad:24, otra:100}, 
{pelicula:"A Beautiful Mind (2001)", cantidad:33, otra:35}, 
{pelicula:"Chicago (2002)", cantidad:42, otra: 45}, 
{pelicula:"The Kings Speech (2010)", cantidad:54, otra: 56}, 
{pelicula:"Green Book (2018)", cantidad:63, otra: 50}, 
{pelicula:"Slumdog Millionaire (2008)", cantidad:71, otra: 43}, 
{pelicula:"Gladiator (2000)", cantidad:77, otra: 38}, 
{pelicula:"Forrest Gump (1994)", cantidad:87, otra:32}, 
{pelicula:"LotR: The Return of the King (2003)", cantidad:92, otra: 28}, 
{pelicula:"Titanic (1997)", cantidad:100, otra:25}]

</script>
<div id="titulo"> 
  <h1>¿Ganar un Oscar asegura llenar salas?</h1>
</div>
<main class="container">


  <div >
    <p>Ganar el Oscar a Mejor Película es un gran reconocimiento, pero no garantiza automáticamente un éxito duradero en taquilla. Sin embargo, hay casos en los que el prestigio del premio se transforma en un fenómeno de público. A lo largo de los años, algunas ganadoras se convirtieron en verdaderos fenómenos de taquilla, permaneciendo en cartelera durante meses, incluso más de un año. Otras, en cambio, lograron su mayor impacto en la temporada de premios, pero no mantuvieron el mismo nivel de asistencia en los cines después.
</p>
  </div>
   <div>
    <h3 >Semanas en cartelera tras ganar el Oscar a Mejor Película.</h3>
   </div>
  </main>
  <OscaStatue numbers={numbers}  />
  <main class="container">
  <p> Un ejemplo destacable es Titanic, ya que se ha reestrenado varias veces desde su estreno original en 1997, y cada vez fue un éxito en taquilla. Otra notable ganadora es Forrest Gump, una película profundamente dramática que ha perdurado en la memoria colectiva gracias a sus frases icónicas y su emotiva historia.

    De hecho, al analizar las películas que ganaron el Oscar a Mejor Película entre 1994 y 2020, se observa que la mayoría pertenecen al género drama. Esta tendencia resalta cómo el drama ha sido históricamente un vehículo eficaz para conectar con el público y los votantes de los premios de la industria cinematográfica.</p>
  <h3 >El aumento es notable</h3>
  <div class="flourish-embed flourish-chart" data-src="visualisation/22905140"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/22905140/thumbnail" width="100%" alt="chart visualization" /></noscript></div>
  

    <p>En los últimos años, parece cada vez más evidente que las nominaciones y premios en los Oscar tienen un impacto directo en el comportamiento del público. A diferencia de décadas anteriores, cuando el efecto de los premios se limitaba principalmente al prestigio, ahora parece que ser nominado o ganar un Oscar podría influir en la duración de una película en cartelera. Es interesante notar que muchas películas experimentan un “segundo aire” comercial tras las nominaciones, atrayendo a nuevos espectadores que inicialmente no las habían considerado. Este fenómeno podría estar sugiriendo que, además de ser un reconocimiento artístico, los Oscar también se han convertido en una poderosa herramienta para aumentar la visibilidad y el éxito comercial de una película.</p>
   
    <h3 >Tener un premio es mejor que no tener ninguno.</h3>
   <div class="flourish-embed flourish-chart" data-src="visualisation/22905243"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/22905243/thumbnail" width="100%" alt="chart visualization" /></noscript></div>
 
  </main>
 

<style>
  
  @import url('https://fonts.googleapis.com/css2?family=Alegreya+Sans:ital,wght@0,100;0,300;0,400;0,500;0,700;0,800;0,900;1,100;1,300;1,400;1,500;1,700;1,800;1,900&family=Archivo:ital,wdth,wght@0,98,100..900;1,98,100..900&family=DM+Serif+Display:ital@0;1&family=Libre+Baskerville:ital,wght@0,400;0,700;1,400&family=Open+Sans:ital,wght@0,300..800;1,300..800&family=Source+Sans+3:ital,wght@0,200..900;1,200..900&display=swap');


  .container {

    
    max-width: 1530px;
    margin: 0 auto;
    height: 300px;

    background-color: white;
  }
  #titulo{
    background-color: #D6BB6E;
    z-index:1;
    /*
    max-width: 1580px;
margin: 0px;
    padding-right: 0px;
    padding-left: 0px;
    */
  }
 p {

  font-family: "Open Sans", sans-serif;

  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
  font-variation-settings:
    "wdth" 100;
    color: rgb(43, 43, 43);
    font-size: 22px;
 
    display: flex;
    justify-content: space-around;
    text-align: justify;
    position: relative;
    z-index:3;
    margin-top: 0px;
      padding-left: 188px;
  padding-right: 180px;
  }
 
  h1 {
    font-family: "Libre Baskerville", serif;
  font-weight: 800;
  font-style: normal;
    color: white;
    text-align: center;
    line-height: 54px;
    padding-top: 50px;
    padding-bottom: 50px;
    align-items: center;
    justify-content: center;
    margin: 19px;
   
  }

  h3 {
    font-family: "Libre Baskerville", serif;
  font-weight: 400;
  font-style: normal;
  text-align: left;

    color: black;

  }


</style>
