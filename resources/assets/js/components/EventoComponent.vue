<template>
    <div class="panel panel-default">
                <div class="panel-heading">{{evento.creado}}</div>
                    <div class="panel-body">
                        <p> {{evento.descripcion}}</p>
                    </div>

                    <div class="panel-footer">
                        <button class="btn btn-default">
                            Editar
                        </button>

                        <button class="btn btn-danger">
                            Eliminar
                        </button>
                    </div>
             </div>
</template>

<script>
    export default {
        props:['evento'],
        data() {
            return{
            };
        },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
