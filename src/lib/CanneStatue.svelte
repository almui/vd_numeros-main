<script>
  import * as d3 from "d3"

  export let numbers = ""

  let width = 100;
  let height = 50;


let alturaCannes = d3.scaleLinear()
    .domain([0, 100])
    .range([0, 95])
 
  let color =  d3.scaleLinear()
    .domain([0, d3.max(numbers, n => n.cantidad)]) 
    .range(["	rgb(220, 139, 40)","#Bd4b1a"])
 


  
</script>


<div class="oscar-container">



  {#each numbers as n}
  <div>

    <div class="item-wrapper">
      <p class="number" style= "color: {color(n.otra)}">{n.otra}</p>
      <div class="column-wrapper-cannes">
        <div class="dorado-c" style="background-color: #E7B548"></div>
        <div class="column-oscar-c" style="height: { alturaCannes(n.otra)}%; background-color: {color(n.otra)}"></div>
        <img class="cannes" src="./images/cannes2.svg" alt="">
      </div>
      <p class="pelicula">{n.pelicula}</p>
    </div>
  </div>

  {/each}

</div>


<style>


  .oscar-container {
    display: flex;
    flex-wrap: wrap;
    gap: 2px;
    padding-left: 110px;
    padding-right: 0px;
    width: 1130px;
    height: 425px;
   
  

    
  }
  .item-wrapper {
    display: flex;
    flex-direction: column;
  width: 100px;
  
 
    align-items: center;
    gap: 10px;
  }
 
  .column-wrapper-cannes {
    position: relative;
    width: 100px;
    height: 218px;
 
  }


  .dorado-c{
    position: absolute;
    /*background-color: #E7B548;*/
    left: 2%;
    right: 20%;
    bottom: -5px;
    height: 95%;
    width: 95%;
 
    /*opacity: 0.8;*/
  }

  .column-oscar-c {
    position: absolute;
    /*background-color: #E7B548;*/
    left: 2%;
    right: 20%;
    bottom: -5px;
    height: 95%;
    width: 95%;

    background-color: red;
  }
  

  .cannes {
    position: absolute;
    bottom: -10px;
    width: 100%;
    height:100%;
  }

  
  .number {
    display: flex;
    text-align: center;
    font-weight: bold;
    font-size: 25px;
    font-family: Arial;
    padding-top: 3px;
    padding-bottom: 0px;
    margin-bottom: 0px;
  }
  .pelicula{
    display: flex;
    text-align: center;
    font-size: 20px;
    font-family: Arial;
    color: grey;
    padding-top: 0px;
    padding-bottom: 0px;
    margin: 1px 0;

  }


</style>
