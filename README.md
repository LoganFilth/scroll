<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>scrollLeft demo</title>
    <style>
      div.demo
      {
        background:#CCCCCC none repeat scroll 0 0;
        border:3px solid #666666;
        margin:5px;
        padding:5px;
        position:relative;
        width:800px;
        height:400px;
        overflow:auto;
      }
      p { margin:10px;padding:5px;border:2px solid #666;width:1000px;height:1000px; }
    </style>
    <script src="http://code.jquery.com/jquery-1.9.1.js"></script>
  </head>
  <body>
    <center>
      <div class="demo">
        <h1>Ajusta la posición horizontal actual de la barra de desplazamiento para cada uno del conjunto de elementos emparejados.</h1>
        <p>
          La posición de desplazamiento horizontal es el mismo que el número de píxeles que están ocultas a la vista por encima de la zona desplazable. Ajuste de el scrollLeft posiciona el desplazamiento horizontal de cada elemento coincidente.
        </p>
      </div>
      <input type="button" value="boton" id="bot">
      <div id="div1"></div>
      <br>
      <input type="button" value="Click" id="cli">
    </center>
  </body>
</html>
<script>
  var divv = $("div.demo");
  $("div.demo").scrollLeft(300); //Un entero que indica la nueva posición para ajustar la barra de desplazamiento.
  
  $("#bot").click(function()
  {
    $("#div1").text( "scrollLeft:" + divv.scrollLeft());
  });
  
  $("#cli").click(function()
  { 
    $("#div1").text( "Diste un click");
  });
  
  $("#cli").dblclick(function()
  {
    $("#div1").text( "Diste DOBLE click");
  });
  
   $("div.demo").click(function()
  { 
    $("div.demo").css( "background", "white");
  });

  $("div.demo").dblclick(function()
  { 
    $("div.demo").css( "background", "#CCCCCC");
  });
</script>
