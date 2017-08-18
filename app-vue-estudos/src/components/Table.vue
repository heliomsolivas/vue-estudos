<template>
    <div>
	    <table class="table table-bordered">
            <thead class="thead-inverse">
                <th>#</th>
                <th>Nome <a href="#"><i class="fa fa-sort-asc" aria-hidden="true"></i></a></th>
                <th>Marca</th>
                <th>Categoria</th>
                <th>Motor</th>
                <th>Câmbio</th>
                <th>Preço</th>
                <th>#</th>
            </thead>
            <tbody>
                <tr v-for="carro in carros">
                    <td>{{carro.nome}}</td>
                    <td>{{carro.marca}}</td>
                    <td>{{carro.categoria}}</td>
                    <td>{{carro.motor}}</td>
                    <td>{{carro.cambio}}</td>
                    <td>{{carro.preco}}</td>
                    <td>Detalhes</td>
                </tr>
            </tbody>
        </table>
	</div>
</template>

<script>
import axios from 'axios';

export default {
data(){
    return{
        carros: [],
    }
    
},
 created() {
            axios.get('http://localhost:8080/src/assets/json/carros.json')
            .then(response => {
                this.carros = response.data
            })
            .catch(e => {
                this.errors.push(e)
            })
        },
}
</script>

<style>

</style>
