<template>
    <div>
        <h1>Listado de inventario de libros</h1>
        <p v-for="(libro, index) in inventario" :key="index"> {{ libro }} </p>
    </div>
</template>

<script>
export default {
    name: 'visualizar',
    data() {
        return {
            inventario: [
                'El secreto',
                'Romen y Julieta',
                'La sombra del viento',
                'Los juegos del hambre',
                'Harry Potter',
                'Inteligencia',
                'La vaca',
                'El alquimista',
                'La mancha del quijote',
                'Padre rico Padre Pobre',
                'La biblia'
            ]
        }
    }
}
</script>

<style>

</style>
