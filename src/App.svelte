<script>
  import * as d3 from "d3"

// Función para generar los arcos
  function arcGenerator({startAngle, endAngle, innerRadius, outerRadius}) {
    return d3.arc()({
      startAngle,
      endAngle,
      innerRadius,
      outerRadius,
    })
  }
</script>

<main>
  <h1 class="titulo container">Representación de magnitudes en formato torta</h1>
  <div>
  <h3 class="headline container">Torta entera</h3>
  <svg width="200" height="200" viewBox="-100 -100 200 200" class="arco">
    <path
      d={arcGenerator({
        startAngle: 0,
        endAngle: 0,
        innerRadius: 0,
        outerRadius: 100,
      })}
      fill="white"
      stroke="white"
      stroke-width="0"
    />
  </svg>
</div>
<div>
  <h3 class="headline container">Quedan 3/4 de torta</h3>
  <svg width="200" height="200" viewBox="-100 -100 200 200" class="arco">
    <path
      d={arcGenerator({
        startAngle: 0,
        endAngle: 6.28319 / 4,
        innerRadius: 0,
        outerRadius: 100,
      })}
      fill="white"
      stroke="white"
      stroke-width="5"
    />
  </svg>
</div>
<div>
  <h3 class="headline container">Queda 1/2 torta</h3>
  <svg width="200" height="200" viewBox="-100 -100 200 200" class="arco">
    <path
      d={arcGenerator({
        startAngle: 0,
        endAngle: 6.28319 / 2,
        innerRadius: 0,
        outerRadius: 100,
      })}
      fill="white"
      stroke="white"
      stroke-width="5"
    />
  </svg>
</div>
<div>
  <h3 class="headline container">Quedan 1/4 de torta</h3>
  <svg width="200" height="200" viewBox="-100 -100 200 200" class="arco">
    <path 
      d={arcGenerator({
        startAngle: 0,
        endAngle: 6.28319 / 1.333333333,
        innerRadius: 0,
        outerRadius: 100,
      })}
      fill="white"
      stroke="white"
      stroke-width="5"
      
    />
  </svg>
</div>
<div>
  <h3 class="headline container">Se acabó la torta</h3>
  <svg width="200" height="200" viewBox="-100 -100 200 200" class="arco">
    <path
      d={arcGenerator({
        startAngle: 0,
        endAngle: 6.28319,
        innerRadius: 0,
        outerRadius: 100,
      })}
      fill="white"
      stroke="white"
      stroke-width="5"
    />
  </svg>
</div>
</main>

<style>
  .arco {
    background-image: url('../images/graf.svg');
    background-size: cover;
    background-position: center;
    background-color: white;
  }
  .titulo {
    font-size: 25px;
    color:firebrick;
    
  }
  .headline {
    text-align: center;
    margin-top: 50px;
    color:lightpink;
    z-index: 2;
  }
  .container {
    display: flex;
    flex-wrap: nowrap;
    flex-flow: row nowrap;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: baseline;
  }

</style>
