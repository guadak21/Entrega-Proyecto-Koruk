<script>
    import * as d3 from "d3"
    import { scaleLinear } from 'd3-scale';
    export let imagen = "";
    export let title = ""
    export let numbers = []
    export let planetas = [];

    let numbersDivided5 = numbers.map(n => Math.floor(n / 5))
    const escalaTamañoPlanetas = d3.scaleLinear()
    .domain([0, Math.max(...planetas.map(p => p.valor))])
    .range([50, 150]);

    const escalaXPlanetas = d3.scaleLinear()
    .domain([0, planetas.length - 1])
    .range([0, 1100]);

  </script>
  
  <h3 class="headline">{title}</h3>
  <div class="mundo-container">
  <!-- Gráfico único de planetas -->
<div class="contenedor">
  <div class="sistema">
    {#each planetas as planeta, i}
      <div
        class="planeta"
        style="
          left: {escalaXPlanetas(i)}px;
          width: {escalaTamañoPlanetas(planeta.valor)}px;
          height: {escalaTamañoPlanetas(planeta.valor)}px;
        "
      >
        <div class="valor">{planeta.valor}</div>
        <img src={imagen} alt={planeta.nombre} style="width: 100%; height: 100%;" />
        <div class="anio">{planeta.nombre}
      </div>
      
      </div>
    {/each}
  </div>
</div>
</div>
  
  <style>
    .mundo-container {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
      width: 90%;
      margin: 20px auto;
      /*padding: 60px;*/
      border-radius: 8px;
      gap: 20px;
      max-width: 800px;    
      margin-top: 20px;  
      margin-bottom: 20px;
    }

    .headline {
      text-align: center;
      font-size: 2.5rem;
      color: #3b658e;
      margin-bottom: 20px; 
      font-weight: bold;
      margin-top: 10px; 
    }

    .contenedor {
      display: flex;
      justify-content: center;
      padding: 50px;
      min-width: 400px;
      overflow-x: auto;

    }

    .sistema {
      position: absolute;
      width: 1100px;
      height: 150px;
      border-radius: 1rem;
      align-items: flex;
      margin-left: -110px; 
      justify-content: center;
      flex-wrap: wrap;
      
    }

    .planeta {
      position: absolute;
      bottom: 30px;
      text-align: center;
      
    }

    .planeta img {
      display: block;
      margin: 0 auto;
      object-fit: contain;
    }

    .anio{
    white-space: nowrap;
    margin-left: -1px;
  }
  

</style>
  