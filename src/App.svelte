<script>
  import * as d3 from "d3"

  import OscaStatue from "./lib/OscaStatue.svelte"
  import CanneStatue from "./lib/CanneStatue.svelte"


  let numbers = [{pelicula:"The Departed (2006)", cantidad:24, otra:23}, 
{pelicula:"A Beautiful Mind (2001)", cantidad:33, otra:35}, 
{pelicula:"Chicago (2002)", cantidad:42, otra: 45}, 
{pelicula:"The Kings Speech (2010)", cantidad:54, otra: 56}, 
{pelicula:"Green Book (2018)", cantidad:63, otra: 50}, 
{pelicula:"Slumdog Millionaire (2008)", cantidad:71, otra: 43}, 
{pelicula:"Gladiator (2000)", cantidad:77, otra: 38}, 
{pelicula:"Forrest Gump (1994)", cantidad:87, otra:32}, 
{pelicula:"LotR: The Return of the King (2003)", cantidad:92, otra: 28}, 
{pelicula:"Titanic (1997)", cantidad:98, otra:25}]

</script>
<div id="titulo"> 
  <h1>¿Ganar un Oscar asegura llenar salas?</h1>
</div>
<main class="container">


  <div >
    <p>Ganar el Oscar a Mejor Película frecuentemente se traduce en una mayor permanencia en cartelera, con las películas disfrutando de un extenso tiempo en salas. Por otro lado, cuando esas mismas películas han sido previamente premiadas en el Festival de Cannes, las semanas en cartelera pueden diferir. Aunque Cannes es un reconocimiento altamente respetado por la crítica y cineastas, el Oscar tiende a atraer una respuesta más amplia del público general, lo que se refleja en una mayor duración en cines tras su victoria.
</p>
  </div>
   <div>

    <h3 >Películas con la mayor cantidad de semanas despues de ganar un Oscar</h3>
   </div>
  </main>
  <OscaStatue numbers={numbers}  />
  <h3 >Cantidad de semanas de las mismas películas despues de ganar en el Festival de Cannes</h3>
  <CanneStatue numbers={numbers}  />
  <main class="container">
  <p> Aunque la visualización anterior muestran las películas que permanecieron más tiempo en cartelera tras ganar el Oscar, ahora analizaremos cómo se comportan esas mismas películas a lo largo del tiempo, organizadas cronológicamente. Al organizarlas por año, es posible observar una tendencia interesante: con el tiempo, la diferencia entre el impacto de Los Oscars y el del Festival de Cannes parece ir reduciéndose. Aunque el Oscar sigue siendo un motor de éxito comercial, cada vez más el público parece estar reconociendo el valor que Cannes ya había señalado antes. Esto podría indicar una mayor sintonía entre la mirada de la crítica y las preferencias del público, o incluso una apertura creciente hacia propuestas cinematográficas más arriesgadas o autorales.</p>
  <h3 >El reconocimiento creciente que se refleja en las salas de cine</h3>
  <div class="flourish-embed flourish-chart" data-src="visualisation/22905140"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/22905140/thumbnail" width="100%" alt="chart visualization" /></noscript></div>
  

    <p>Esto refuerza la idea de que, más allá del impacto inmediato en taquilla, ganar un premio sigue siendo una forma poderosa de reconocimiento. Al observar el promedio de semanas en cartelera, notamos que, aunque las diferencias entre premios se mantienen, la tendencia general es creciente. Esto habla de un público cada vez más dispuesto a descubrir y acompañar películas reconocidas por su calidad. Lo que sugiere que los premios no solo celebran el valor artístico, sino que también ayudan a que esas historias permanezcan vivas por más tiempo en la pantalla grande.</p>
   
    <h3 >Tener un premio es mejor que no tener ninguno.</h3>
   <div class="flourish-embed flourish-chart" data-src="visualisation/22905243"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/22905243/thumbnail" width="100%" alt="chart visualization" /></noscript></div>
 
  </main>
 

<style>
  
  @import url('https://fonts.googleapis.com/css2?family=Alegreya+Sans:ital,wght@0,100;0,300;0,400;0,500;0,700;0,800;0,900;1,100;1,300;1,400;1,500;1,700;1,800;1,900&family=Archivo:ital,wdth,wght@0,98,100..900;1,98,100..900&family=DM+Serif+Display:ital@0;1&family=Libre+Baskerville:ital,wght@0,400;0,700;1,400&family=Open+Sans:ital,wght@0,300..800;1,300..800&family=Source+Sans+3:ital,wght@0,200..900;1,200..900&display=swap');


  .container {

    
    max-width: 1530px;
    margin: 0 auto;
    height: 320px;

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
  padding-left: 110px;

    color: black;

  }


</style>
