<template>
	<div>
		<div id="contenedor">
      <div class="clear">
        <div class="bloque1">
          <p>Este es el Bloque 1 dentro del contenedor.</p>
        </div>
        <div class="bloque2">
          <p>Este es el contenido del Bloque 2 dentro del contenedor, este contiene más texto, por eso debe ser más largo.</p>
        </div>
      </div>
    </div>
		<div class="bloque1">
			<p>Este es el Bloque 1 fuera del contenedor.</p>
		</div>

		<div class="bloque2">
			<p>Este es el Bloque 2 fuera del contenedor.</p>
		</div>

		<!-- LISTADO GENERADO POR VUE -->
		<div class="v-container">
			<div 
        v-for="(item, index) in myArray" 
          :key="item.id"
          :class="{ 'gray-bg': index % 2 !== 0 }"
          v-show="index % 2 !== 0">
				<p>Nombre: {{ item.name }}</p>
				<p>Roles: {{ item.roles.join(', ') }}</p>
			</div>
		</div>

		<!-- BOTÓN QUE GENERA EL TOTAL -->
		<div class="btn" @click="mostrarTotal">
			Generar 
		</div>

		<!-- MOSTRAR EL TOTAL -->
		<div class="output">
			{{ output }}
		</div>
	</div>
</template>

<script>
export default {
	name: 'SupportView',
	data() {
		return {
			myArray: [
				{ id: 1, name: 'Carlos', roles: [1, 2] },
				{ id: 2, name: 'María', roles: [3, 4] },
				{ id: 3, name: 'José', roles: [2, 5] },
				{ id: 4, name: 'Ana', roles: [1, 3] },
				{ id: 5, name: 'Pedro', roles: [2, 4] }
			],
			output: ""
		};
	},
	computed: {
		total() {
			return this.myArray.length;
		}
	},
	methods: {
		mostrarTotal() {
			this.output = `El total de listado es: ${this.total}`;
		}
	}
};
</script>

<style scoped>
  * {
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
  }

  body {
    text-align: center;
  }
  body p {
    padding: 10px;
  }

  #contenedor {
    width: 600px;
    margin: 0 0 10px 0;
    padding: 10px;
    border: 1px dotted #808080;
    overflow: hidden;
    min-height: 1px;
  }

  #contenedor .bloque1, #contenedor .bloque2 {
    width: 100px;
    margin: 70px 5px 5px 5px;
    float: left;
  }

  #contenedor .bloque2 {
    margin: 5px;
  }

  #contenedor .bloque1 {
    margin-top: 70px;
    float: left;
  }
  #contenedor .bloque1 p{
    font-style: italic;
  }

  #contenedor .bloque2 {
    float: left;
  }

  #contenedor .clear {
    clear: both;
    overflow: hidden;
  }

  .bloque1{
    background: #ff0000;
    display: block;
  }

  .bloque1 p {
    color: #fff;
  }

  .bloque2{
    background: #ffff00;
    display: block;
  }

  .bloque2 p {
    color: #000;
    font-weight: bold;
  }

  .v-container .gray-bg {
    background-color: #e6e6e6;
    padding: 10px;
    margin-bottom: 5px;
    -webkit-box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
    -moz-box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
  }

  .btn {
    background-color: #007bff;
    color: white;
    padding: 10px;
    text-align: center;
    cursor: pointer;
    margin-top: 10px;
    width: 120px;
    border-radius: 5px;
    -webkit-border-radius: 5px;
    -moz-border-radius: 5px; 
    -ms-border-radius: 5px; 
    -o-border-radius: 5px; 
  }

  .btn:hover {
    background-color: #0056b3;
  }

  .output {
    margin-top: 10px;
    font-weight: bold;
  }
</style>
