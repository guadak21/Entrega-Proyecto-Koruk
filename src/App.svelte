<!-- Script JS -->
<script>
  /* Importamos d3 para tenerlo disponible */
  import * as d3 from 'd3'
  import Mundo from './Mundo.svelte';

  let numbers1 =[24,33,42,54,63,71,77,87,92,98];//serie A
  let numbers2 =[23,35,45,56,50,43,38,32,28,25]; //Serie B

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
    

</script>

<!-- Estructura contenido HTML -->

<div class="noticia-header">
  <span class="categoria">Tendencias</span>
  <span class="fecha">20 de mayo de 2025</span>
</div>

<main id="container">
    <div class="contenido">
      <h1 class="title"><strong>La evolución tecnológica: cómo la tecnología transformó nuestras vidas</strong></h1>
      <div class="parrafo1">
        <p>La evolución tecnológica ha transformado cómo vivimos, trabajamos y nos comunicamos, permitiendo que un mensaje cruce el mundo en segundos y conecte a millones de personas. </p>
      </div>

      <h2 class="title2"><strong>Conectividad en expansión: cómo creció el acceso a Internet</strong></h2>

      <div class="intro">
        <div class="intro1">
          <p>Entre 2015 y 2024, se incrementó el acceso a Internet y la conectividad global. </p>
        </div>
        <Mundo planetas={planetasA} imagen="./images/small.svg" />
        
        <h2 class="title3"><strong>Brecha creciente: cómo disminuyó el acceso a computadoras</strong></h2>
        <div class= "intro2">
          <p>Desde 2018, el acceso a computadoras disminuyó, aumentando la desigualdad digital.</p>
        </div>
        <Mundo planetas={planetasB} imagen="./images/Group10.svg" />
      
    
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
        <h2><strong>De la expansión a la desigualdad: la otra cara del acceso a internet en Argentina</strong></h2>
        <p> Los gráficos muestran la situación del acceso digital, invitando a reflexionar sobre la democratización tecnológica en Argentina en 2022.</p>
        <div class="grafico2">
          <iframe
          src="https://flo.uri.sh/visualisation/22687974/embed"
          frameborder="0"
          scrolling="no"
          title="Gráfico interactivo de Flourish2"
          class="flourish-iframe"
       
        ></iframe>
        <iframe
          src="https://flo.uri.sh/visualisation/22903635/embed"
          frameborder="0"
          scrolling="no"
          title="Gráfico interactivo de Flourish3"
          class="flourish-iframe"
          ></iframe>
        </div>
      </div>
      <div class="info4">
        <p>Aunque el 87% de los hogares tiene acceso a Internet, solo el 32% posee computadoras, lo que revela una brecha significativa en el acceso a dispositivos adecuados.  
        </p>
        <p> Muchos dependen de teléfonos móviles, limitando el uso efectivo de herramientas educativas y laborales. 
        </p>
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
    margin-bottom: 20px;
    margin-left: 250px;
    margin-right: 250px;
  }
    
  .contenido p{
    margin-left: 300px ;
    margin-right: 300px ;
  }
  
  .parrafo1{
    max-width: 300ch;
    margin-bottom: 100px;
    margin-top: 70px;
    text-align: center;
  }
    
    .seccion{

      background: #fff;
      position: relative;
      border-radius: 8px;
      margin-left: -15px;
      margin-right: -15px;
      margin-top: -30px;
    }
    h1{
      color: #3b658e;
      font-size: 3rem;
      }

    h2 {
      color: #A5C5F6; 
      font-size: 1.8rem;
    }


    p {
      font-size: 1.2rem;
      color: #444;
      line-height: 1.5;
      max-width: 85ch;
      
    }

    .seccion p{
      margin-top: 25px;
      max-width: 85ch;
    }

    .seccion h2{
      color: #A5C5F6;
      margin-top: 20px;
    }


    .title2{
      margin-top: 50px;
      color: #b6d462;
      text-align: center;
      font-size: 1.6rem; ;
    }
    

  .info{
    text-align: justify;
    margin-top: 90px;
    margin-left: 100px;
    margin-right: 90px;
  }

  .info h2{
    font-size: 1.8rem;
    color: #5b5b5b;
    margin-left: -90px;

  }

  .info p{
    margin-left: 0px;
    margin-right: 0px;
    max-width: 85ch;
    margin-left: -50px;
  }

  .intro1{
    text-align: justify;
  /*margin-top: 200px;*/

  }

  .intro1 p{
    /*margin-left: 150px;
    margin-right: 150px;*/
    text-align: center;
  }

  /*.intro p{
    margin-left: 170px;
    margin-right: 170px;
  }*/

  .intro2{
    text-align: center;
  }

  .info2{
    justify-content: center;
    margin-bottom: 70 px;
    margin: 20px auto 70px auto; /* margen vertical y centrado horizontal */

  }
  .info2 p{
    text-align: justify;
    font-size: 1.2rem;
    margin-top: 20px;
    color: #444;
    font-family: "Avenir", sans-serif;
    justify-content: center;
    line-height: 1.5;
    margin-left: 70px;
    margin-right: 100px;

  }
  .info3 {
    text-align: center;
    font-size: 1.2rem;
    margin-top: -80px;
    color: #444;
    font-family: "Avenir", sans-serif;
    justify-content: center;
    margin-left: 110px;
    margin-right: 100px;
  }

  .info3 h2{
    font-size: 1.8rem;
    color: #5b5b5b;
    text-align: justify;
    margin-top: -10px;
  }

  .info3 p{
    text-align: justify;
    margin-top: 40px;
    margin-left: 70px;
    margin-right: 100px;
    justify-content: center;
    line-height: 1.5;
    margin-bottom: 80px;
  }

  .info4{
    justify-content: center;
    margin-bottom: 100px;

  }

  .info4 p{
    text-align: justify;
    font-size: 1.2rem;
    margin-top: 20px;
    color: #444;
    font-family: "Avenir", sans-serif;
    justify-content: center;
    margin-left: 200px;
    margin-right: 200px;
    line-height: 1.5;

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
    margin-left: 300px;
    margin-right: 300px;
  }

  .grafico2{
    width: 100%;
    margin-top: 20px;
    margin-bottom: 20px;
    border-radius: 8px;
    overflow: hidden;
    position: relative;
    display: flex;             
    gap: 20px;                 
    justify-content: center;   
    flex-wrap: wrap;          
  }

.grafico2 iframe {
  width: 48%;
  height: 450px;
  border: none;
  border-radius: 8px;

}

.grafico1{
  margin-left: 0px;
  margin-right: 0px;
  align-items: center;
  width: 110%; /* usa todo el ancho del contenedor */
  margin: 0 auto; /* centra horizontalmente */
  display: flex;
  justify-content: center;
}

.grafico1 iframe {
  width: 100%;
  height: 600px;
  border: none;
  margin-left: -100px;

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
  /*margin-left: 150px;*/
  text-align: center;
  margin-top: 200px;

}

.tabla{
  margin-top: 100px;
  /*margin-left: 60px;
  margin-right: 60px;
  justify-content: center;*/
  margin-left: auto;
  margin-right: auto;
  justify-content: center;
  display: flex;
  gap: 30px;
  flex-wrap: wrap;
  align-items: flex-start;
}

</style>
