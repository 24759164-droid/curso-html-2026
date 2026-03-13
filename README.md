<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>pagina</title>
</head>
<body>
 <link rel="stylesheet" href="/css/stile.css">  
  <script src="/js/Scrip.js"></script>

   




<h1>holaaa</h1>
<p>sherk</p>







<img src="imm.pg.webp"  width="300" style="border-radius: 15px;">


<p>Saludos</p>

<!DOCTYPE html>
<html lang="es">
<body>

    <h1>tabla1</h1>
    <h1>cafeteria</h1>
    <p>los mejores de la ciudad</p>
    <img src="img.px.jpeg"  width="150" style="border-radius: 15px;">  
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cafeeeee</title>
    <link rel="stylesheet" href="Style.css">
</head>

<body>
    
<table id="table1" name="tabla1" border="1"
    <thead>
        <tr>
            <th></th><th></th><th></th>
        </tr>
    </thead>

    <tbody>

        <tr> <td>Cantidad</td>    <td><input type="number" id="cantidad" value="1" min="1">  </td><td></td></tr>

        <tr> <td>Matricula</td>   <td><input type="text" id="matri">   </td><td></td></tr>
        <tr> <td>Nombre</td>      <td><input type="text" id="nom">       </td><td></td></tr>

        <tr> <td>Grande $35</td>  <td><input name="tn" type="radio" value="35">  </td><td></td></tr>
        <tr> <td>Mediano $28</td> <td><input name="tn" type="radio" value="28">  </td><td></td></tr>

        <tr> <td>Chico $20</td><td><input name="tn" type="radio" value="20"></td><td></td></tr>
        <tr> <td>cafe $10</td> <td><input type="checkbox" class="extra" value="10" data-nombre="cafe">        </td><td></td></tr>

        <tr> <td>Chocolate $10</td> <td><input type="checkbox" class="extra" value="10" data-nombre="Chocolate">  </td><td></td></tr>
        <tr> <td>Crema $10</td> <td><input type="checkbox" class="extra" value="10" data-nombre="Crema"></td>       <td></td></tr>
        <tr> <td>ExtraAzucar $10</td> <td><input type="checkbox" class="extra" value="10" data-nombre="ExtraAzucar"></td>     <td></td></tr>

</tbody>
</table>

<br>
<button id="botonalgo" onclick="saludar()">Ordenar</button>

<button id="botonDos">Boton Dos</button>

<h2 id="resultado"></h2>

<script>

function calcularTotalConCantidad(precioBase) {
    let cantidad = document.getElementById("cantidad").value;
    return precioBase * Number(cantidad);
}

function saludar() {

    let mat = document.getElementById("matri").value;
    let nom = document.getElementById("nom").value;

    let tamaño = document.querySelector('input[name="tn"]:checked');
    const extras = document.querySelectorAll(".extra:checked");

    let total = 0;


    if (tamaño) {
        total += Number(tamaño.value);
    }

    
    extras.forEach(extra => {
        total += Number(extra.value);
    });

    
    total = calcularTotalConCantidad(total);

    let listaExtras = "";
    extras.forEach(extra => {
        listaExtras += extra.dataset.nombre + " ";
    });

    let mensaje =
        "Matricula: " + mat +
        "\nNombre: " + nom +
        "\nTotal a pagar: $" + total +
        "\nExtras: " + listaExtras;

    alert(mensaje);

    document.getElementById("resultado").textContent =
        "Total a pagar: $" + total;
}


</script>

