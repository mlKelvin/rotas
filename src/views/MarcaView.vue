<template>
    <div>
        <h1>Marca</h1>

        <table>
            <tr>
                <th>Id</th>
                <th>Nome</th>
                <th></th>
            </tr>
            <tr v-for="m in marcas" :key="m.Id">
                <th>{{m.Id}}</th>
                <th>{{m.nome}}</th>
                <th> <a href="javascript:void(0)" @click="editar(m)">Editar</a> </th>
            </tr>
        </table>

    </div>

</template>


<script>

export default {
    data() {
        return {
            marcas: [
                {
                    id:1,
                    nome: 'Hyundai'
                },
                {
                    id:2,
                    nome: 'Ford'
                },
            ]
        }
    },
    methods: {
        editar(marca){
            this.$router.push(`/marca-form/${marca.id}`)
        }
    }
}
</script>