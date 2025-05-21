<!-- Script JS -->
<script>
  /* Importamos d3 para tenerlo disponible */
  import * as d3 from 'd3'
  import Mundo from './Mundo.svelte';

  let planetasA = [
      { nombre: '2015', valor: 24 },
      { nombre: '2016', valor: 33 },
      { nombre: '2017', valor: 42 },
      { nombre: '2018', valor: 54 },
      { nombre: '2019', valor: 63 },
      { nombre: '2020', valor: 71 },
      { nombre: '2021', valor: 77 },
      { nombre: '2022', valor: 87 },
      { nombre: '2023', valor: 92 },
      { nombre: '2024', valor: 98 },
    
    ];

    let planetasB=[
      { nombre: '2015', valor: 23 },
      { nombre: '2016', valor: 35 },
      { nombre: '2017', valor: 45 },
      { nombre: '2018', valor: 56 },
      { nombre: '2019', valor: 50 },
      { nombre: '2020', valor: 43 },
      { nombre: '2021', valor: 38 },
      { nombre: '2022', valor: 32 },
      { nombre: '2023', valor: 28 },
      { nombre: '2024', valor: 25 },
  
    ]; 

  let maxGlobal=Math.max( /*calculo el valor máximo global*/
    ...planetasA.map(p => p.valor), 
    ...planetasB.map(p => p.valor)
  );

  let escalaTamañoCompartida=d3.scaleLinear() /*creo la escala compartida*/
  .domain([0, maxGlobal])
  .range([50, 150]);


</script>

<!-- Estructura contenido HTML -->

<div class="noticia-header">
  <span class="categoria">Tendencias</span>
  <span class="fecha">20 de mayo de 2025</span>
</div>

<main id="container">
    <div class="contenido">
      <h1 class="title"><strong>La evolución tecnológica: cómo la <br> tecnología transformó nuestras vidas</strong></h1>
      <div class="parrafo1">
        <p>La evolución tecnológica ha transformado cómo vivimos, trabajamos y nos comunicamos, <br>permitiendo que un mensaje cruce el mundo en segundos y conecte a millones de personas. </p>
      </div>

      <h2 class="title2"><strong>Conectividad en expansión: cómo creció el acceso a Internet</strong></h2>

      <div class="intro">
        <div class="intro1">
          <p>Entre 2015 y 2024, se incrementó el acceso a Internet y la conectividad global. </p>
        </div>
        <Mundo 
        planetas={planetasA} 
        imagen="./images/small.svg" 
        escalaTamañoPlanetas={escalaTamañoCompartida}
        />
        
        <h2 class="title3"><strong>Brecha creciente: cómo disminuyó el acceso a computadoras</strong></h2>
        <div class= "intro2">
          <p>Desde el 2018, el acceso a computadoras disminuyó, aumentando la desigualdad digital.</p>
        </div>
        <Mundo 
        planetas={planetasB} 
        imagen="./images/Group10.svg" 
        escalaTamañoPlanetas={escalaTamañoCompartida}
        />
      </div>
    </div>


    <div class="contenido">
      <div class="seccion" id="pasado">          
        <div class="tabla">
          <div class="info">
            <h2><strong>Tecnología en casa – Una evolución imparable</strong></h2>
            <p>Desde hace varios años, los hogares han incorporado cada vez más dispositivos tecnológicos. Este gráfico muestra cómo ha evolucionado esa cantidad promedio desde 2016 hasta 2023.</p>
            <div class="grafico1">
              <iframe
              src="https://flo.uri.sh/visualisation/22562788/embed"
              frameborder="0"
              scrolling="no"
              title="Gráfico interactivo de Flourish1"
              class="flourish-iframe"
           
            ></iframe>
      
            </div>
          </div>
          <div class="info2">
            <p> En la última década, el acceso a Internet creció del 24% al 98%, mientras que el acceso a computadoras cayó del 56% en 2018 al 25% en 2024. </p>
            <p> Desde 2019, la brecha entre ambos indicadores se amplió notablemente, reflejando un cambio en los hábitos tecnológicos: los hogares priorizan dispositivos móviles sobre computadoras como vía principal de acceso al mundo digital.</p>
          </div>
        </div>

    </div>
    
    <div class="tabla">
      <div class="info3">
        <h2><strong>De la expansión a la desigualdad: la otra cara del acceso <br>a Internet en Argentina</strong></h2>
          <p> Los gráficos muestran la situación del acceso digital, invitando a reflexionar <br> sobre la democratización tecnológica en Argentina en 2022.</p>
        <div class="grid">
          <!-- Fila de encabezados vacía + etiquetas -->
          <div></div>
          <div class="label">Accesos a Internet</div>
          <div class="label">Accesos a computadoras</div>
        
          <!-- Año 2015 -->
          <div class="grafico2015">
            <div class="year">2015</div>
            <iframe src="https://flo.uri.sh/visualisation/23311793/embed" title="Gráfico1 2015"   class="flourish-iframe"></iframe>
            <iframe src= "https://flo.uri.sh/visualisation/23311857/embed" title="Gráfico2 2015"   class="flourish-iframe"></iframe>
        
          </div>
        
          <!-- Año 2016 -->
          <div class="grafico2016">
            <div class="year">2016</div>
            <iframe src="https://flo.uri.sh/visualisation/23311808/embed"  title="Gráfico1 2016"   class="flourish-iframe"></iframe>
            <iframe src="https://flo.uri.sh/visualisation/23311862/embed" title="Gráfico2 2016"  class="flourish-iframe"></iframe>
          </div>
        
          <!-- Año 2017 -->
          <div class="grafico2017">
            <div class="year">2017</div>
            <iframe src="https://flo.uri.sh/visualisation/23311817/embed"  title="Gráfico1 2017"   class="flourish-iframe"></iframe>
            <iframe src="https://flo.uri.sh/visualisation/23311871/embed"  title="Gráfico2 2017"  class="flourish-iframe"></iframe>
          </div>
        
          <!-- Año 2018 -->
          <div class="grafico2018">
            <div class="year">2018</div>
            <iframe src="https://flo.uri.sh/visualisation/23311822/embed"  title="Gráfico1 2018"  class="flourish-iframe"></iframe>
            <iframe src="https://flo.uri.sh/visualisation/23311898/embed"  title="Gráfico2 2018"  class="flourish-iframe"></iframe>
          </div>
          
          <!-- Año 2019 -->
          <div class="grafico2019">
            <div class="year">2019</div>
            <iframe src="https://flo.uri.sh/visualisation/23311834/embed"  title="Gráfico1 2019"   class="flourish-iframe" ></iframe>
            <iframe src="https://flo.uri.sh/visualisation/23311911/embed"  title="Gráfico2 2019"   class="flourish-iframe"></iframe>
          </div>
        
          <!-- Año 2020 -->
          <div class="grafico2020">
            <div class="year">2020</div>
            <iframe src="https://flo.uri.sh/visualisation/23311838/embed"  title="Gráfico1 2020"  class="flourish-iframe"></iframe>
            <iframe src="https://flo.uri.sh/visualisation/23311921/embed"  title="Gráfico2 2020"  class="flourish-iframe"></iframe>
          </div>
        
          <!-- Año 2021 -->
          <div class="grafico2021">
            <div class="year">2021</div>
            <iframe src="https://flo.uri.sh/visualisation/23311842/embed"  title="Gráfico1 2021"  class="flourish-iframe"></iframe>
            <iframe src="https://flo.uri.sh/visualisation/23311932/embed"  title="Gráfico2 2021"  class="flourish-iframe"></iframe>
          </div>
        
          <!-- Año 2022 -->
          <div class="grafico2022">
            <div class="year">2022</div>
            <iframe src="https://flo.uri.sh/visualisation/22687974/embed"  title="Gráfico1 2022"  class="flourish-iframe"></iframe>
            <iframe src="https://flo.uri.sh/visualisation/22903635/embed"  title="Gráfico2 2022"  class="flourish-iframe"></iframe> 
          </div>
        
          <!-- Año 2023 -->
          <div class="grafico2023">
            <div class="year">2023</div>
            <iframe src="https://flo.uri.sh/visualisation/23311848/embed"  title="Gráfico1 2023"  class="flourish-iframe"></iframe>
            <iframe src="https://flo.uri.sh/visualisation/23311943/embed"  title="Gráfico2 2023"  class="flourish-iframe"></iframe>
          </div>
        
          <!-- Año 2024 -->
          <div class="grafico2024">
            <div class="year">2024</div>
            <iframe src="https://flo.uri.sh/visualisation/23311852/embed"  title="Gráfico1 2024"  class="flourish-iframe"></iframe>
            <iframe src="https://flo.uri.sh/visualisation/23311949/embed"  title="Gráfico2 2024"  class="flourish-iframe"></iframe>
          </div>
        </div>
        
      </div>
      <div class="info4">
        <p>Aunque el acceso a Internet creció de forma sostenida, el acceso a computadoras se mantuvo bajo y desigual. Muchos hogares dependen solo del celular, lo que limita su uso educativo y laboral.   
        </p>
        <p>En 2020, en plena pandemia, la conectividad aumentó sin un salto equivalente en computadoras. En 2022, esta brecha se consolidó. </p>
        <p>Esto evidencia que la inclusión digital debe ir más allá de la conectividad, garantizando también el acceso a tecnología apropiada para una participación plena en la sociedad digital.</p>
    </div>   
  </main>

  <footer class="footer">
    <p>&copy; 2025 Guadalupe Koruk</p>
    <p>Contacto: <a href="mailto:gkoruk@mail.utdt.edu">gkoruk@mail.utdt.edu</a></p>
    <div class="footer-links">
      <a href="https://github.com/guadak21" target="_blank">
      <img src= "images/github.png" alt="GitHub" width="30" height="30">
      </a> |

      <a href="https://www.utdt.edu/" target="_blank">
      <img src= "images/ditella.png" alt="UTDT" width="30" height="30">
      </a>
 
    </div>
  </footer>

<!-- Estilos CSS -->
<style>

.noticia-header {
    display: flex;
    justify-content: space-between;
    font-size: 18px;
    background-color: #f2f2f2;
    padding: 10px;
    color: #555;
    margin-bottom: auto;
    border-bottom: 1px solid #ccc;
    height: 10vh;
    align-items: center;
    box-shadow: 0 2px 6px rgba(0,0,0,0.05);
    font-family: "Avenir", sans-serif;



  }

  #container{
    width: 100%;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    max-width: 1000px;
    margin: 0 auto;
    padding: 0 1 rem;
  }

  main {
    flex-grow: 1; 
    height: 100%;
    font-family: "Avenir", sans-serif;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

  .contenido{
    padding: 30px;
    position: relative;
    border-radius: 8px;


  }
  .contenido h1{
    text-align: center;
    margin: 2rem auto;
    max-width: 70ch;
  }
  
  .parrafo1{
    max-width: 300ch;
    margin-bottom: 100px;
    margin-top: 70px;
    text-align: center;
  }

  .parrafo1 p{
    font-size: 1.4rem;
  }
    
    .seccion{
      background: none;
      position: relative;
      border-radius: 8px;
      margin-top: -30px;
      /*padding: 2rem 1rem;*/
      max-width: 1000px; 
      margin: 0 auto;
      overflow-x: auto;   
      text-align: left; 
      padding: 0 1rem;
      box-sizing: border-box;

    }

    h1{
      color: #3b658e;
      font-size: 3rem;
      }

    h2 {
      color: #A5C5F6; 
      font-size: 1.8rem;
      text-align: center;
      max-width: 70ch;
      margin: 2rem auto 1rem;
    }


    p {
      font-size: 1.2rem;
      color: #444;
      line-height: 1.5;
      max-width: 85ch;
      margin: 1.5rem auto;
      text-align: justify;

    }

    .seccion p{
      margin-top: 25px;
      max-width: 85ch;
      text-align: left !important;
      margin-left: 0 !important;
      margin-right: 0 !important;
    }

    .seccion h2{
      color: #A5C5F6;
      margin-top: 20px;
      text-align: left !important;

    }


    .title2{
      margin-top: 50px;
      color: #a6d71d;
      text-align: center;
      font-size: 1.8rem; ;
    }
    

  .info{
    text-align: left;
    max-width: 1000px;
    width: 100%;
    /*padding: 20px;*/
    margin: 0 auto;
    padding: 0 1rem;
    box-sizing: border-box;
    margin-top: 180px;

  }

  .info h2{
    font-size: 1.8rem;
    color: #5b5b5b;
    text-align: justify;

  }

  .info p{
    text-align: justify;

  }

  .intro1{
    text-align: justify;

  }

  .intro1 p{
    text-align: center;
  }

  .intro2{
    text-align: center;
  }

  .intro2 p{
    text-align: center;
  }
  .info2{
    justify-content: center;
    margin-bottom: 70px;
    text-align: left;
    max-width: 1000px;
    margin-left: auto;
    margin-right: auto;
    /*padding: 20px;*/
    margin-top: -40px;
    margin: 0 auto;
    padding: 0 1rem;
    box-sizing: border-box;

  }

  .info2 p{
    text-align: justify !important;
    margin-left: 0 !important;
    margin-right: 0 !important;
    max-width: 75ch; 

  }
  
  .info3 {
    text-align: left;
    font-size: 1.2rem;
    color: #444;
    font-family: "Avenir", sans-serif;
    justify-content: center;
    flex-direction: column;
    align-items: flex-start;
    max-width: 1000px;
    padding: 0 1rem;
    box-sizing: border-box;
    margin-top: 100px;
    width: 100%;

  }

  .info3 h2{
    font-size: 1.8rem;
    color: #5b5b5b;
    text-align: justify;
    margin-top: 0;
    margin-bottom: 1rem;
    margin-left: 35px;
  }

  .info3 p{
    margin-top: 1rem;
    max-width: 75ch;
    text-align: justify;
    margin-left: 0;
    margin-right: 0; 
  }

  .footer {
    background-color: #f2f2f2;
    padding: 10px;
    text-align: center;
    align-items: center;
    font-size: 0.9rem;
    color: #555;
    margin-top: auto;
    margin-bottom: auto;
    border-top: 1px solid #ccc;
    font-size: 20px;
    font-family: "Avenir", sans-serif;



  }

  .footer p{
    align-items: center;
    text-align: center;

}

.grafico1{
  margin-left: 0px;
  margin-right: 0px;
  align-items: center;
  width: 100%; 
  margin: 0 auto; 
  display: flex;
  justify-content: center;
  max-width: 900px;
  padding: 1rem 0;

}

.grafico1 iframe {
  width: 100%;
  height: 600px;
  max-width: 900px;
  min-width: 300px;
  display: block;
  margin: 0 auto;
  border: none;
}



.title{
  display: flex;
  justify-content: center; 
  align-items: center;     
  text-align: center;
}

.title3{
  color: #91A7FD;
  justify-content: center; 
  text-align: center;
  margin-top: 250px;

}

.tabla{
  margin-top: 100px;
  justify-content: center;
  display: flex;
  gap: 2px;
  flex-wrap: wrap;
  max-width: 2200px;
  margin: 0 auto;
  padding: 0 1rem;
  align-items: center;
  flex-direction: column;
  box-sizing: border-box;
}


.grid {
  display: grid;
  grid-template-columns: auto auto auto;
  gap: 2rem;
  align-items: start;
  width: 100%;
  margin: 0 auto;
  justify-content: center;
  text-align: center;
  max-width: 2200px;  
  padding: 0 1rem;
  box-sizing: border-box;
  margin-top: 70px;
  overflow-x: auto;

}
.grafico2015, .grafico2016, .grafico2017, .grafico2018, .grafico2019,
.grafico2020, .grafico2021, .grafico2022, .grafico2023, .grafico2024 {
  display: contents; 
  max-width: 1800px; 
  margin: 0 auto;
  padding: 0 1rem;
  box-sizing: border-box;
 
}

  .year {
    font-weight: bold;
    text-align: right;
  }

  .label {
    font-weight: bold;
    text-align: center;
    font-size: 1.2rem;
    padding-bottom: 0.5rem;
    white-space: normal;
    word-wrap: break-word;
    max-width: 100%; 
    overflow-wrap: break-word;
  }

  iframe {
    width: 100%;
    height: 120px;
    border: none;

  }

  .flourish-iframe {
    margin: 2rem auto;
    width: 100%;
    height: 400px;
    border: none;

}

.contenido p,
.info2 p,
.info3 p,
.info4 p,
.intro1 p,
.intro2 p {
  margin-left: auto !important;
  margin-right: auto !important;
}

.info3,
.info4,
.info2 {
  margin-left: auto !important;
  margin-right: auto !important;
}

.info4{
  font-size: 1.2rem;
  text-align: justify;
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 1rem;
  box-sizing: border-box;
  line-height: 1.5;
  color: #444;
}

.info4 p{
  text-align: justify;
  max-width: 75ch;
}

.grid,
.grafico2015,
.grafico2016,
.grafico2017,
.grafico2018,
.grafico2019,
.grafico2020,
.grafico2021,
.grafico2022,
.grafico2023,
.grafico2024 {
  overflow: visible;
}

</style>
