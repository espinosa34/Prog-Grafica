<template>
    <div>
        <div>
            <input type="text" placeholder="Ingrese nombre del producto" v-model="valor">
            <button @click="buscar(valor)"> Buscar</button>

            <!-- Sistema de busquedad por nombre -->
            <div v-if="resultado.nombre">
                <p>Resultado de la busquedad  
                   <b> {{ resultado.nombre  }} {{ resultado.precio}} </b>
                </p>                
            </div>
            <!-- Fin del sistema de busquedad por nombre -->

            <!-- Vizualización de Listado de producto -->
            <div>
                <h3>Listado de productos</h3>
                <p v-for="(producto, index) in listado" :key="index"> 
                    {{ producto.nombre  }} {{ producto.precio}}
                </p>
            </div>
            <!-- Fin de vizualización -->
            
        </div>
    </div>
</template>

<script>
export default {
    name: 'producto',
    data() {
        return {
            valor: '',
            listado: [
                { nombre: 'arroz', precio: 10},
                { nombre: 'papa', precio: 1},
                { nombre: 'frutas', precio: 500},
                { nombre: 'cereales', precio: 100},
                { nombre: 'vegetales', precio: 99},
                { nombre: 'carnes', precio: 985},
                { nombre: 'bebidas', precio: 55555},
            ],
            resultado: {}
        }
    },
    methods: {
        buscar: function(ejemplo) {
            console.log('El nombre es: ', ejemplo)
            console.log('El sin enviarlo es: ', this.valor)
            // Se realizada un búsqueda en el arreglo de listado y se retorna la posición del producto si lo encuentra
            let index = this.listado.map( function(i) {
                return i.nombre
            }).indexOf(this.valor)
            
            // si el index es mayor -1 quiere decir que encontró un producto con ese codigo de que estamos buscando
            if(index > -1) {
                // Asignamos el producto al campo de resultado para mostrarlo
                this.resultado = this.listado[index]
            } else {
                // en caso de no encontrar nada simplemente lo asignamos como vacio
                 this.resultado = {}
            }

        }
    }
}
</script>
