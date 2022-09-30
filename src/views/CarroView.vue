<template>
    <div>
        <h1>Carro</h1>

        <table>
            <tr>
                <th>Id</th>
                <th>Nome</th>
                <th></th>
            </tr>
            <tr v-for="c in carros" :key="c.Id">
                <th>{{c.Id}}</th>
                <th>{{c.nome}}</th>
                <th> <a href="javascript:void(0)" @click="editar(c)">Editar</a> </th>
            </tr>
        </table>
    </div>

</template>


<script>

export default {
    data() {
        return {
            carros: [
                {
                    id:1,
                    nome: 'Gol'
                },
                {
                    id:2,
                    nome: 'Tiguan'
                },
            ]
        }
    },
    methods: {
        editar(carro){
            this.$router.push(`/carro-form/${carro.id}`)
        }
    }
}
</script>