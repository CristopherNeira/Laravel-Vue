<template>
    <div class="row">
            <div class="col-md-8 col-md-offset-2">
            
                <form-evento-component @new = "addEvento"></form-evento-component>
                <evento-component
                    v-for="evento in eventos"
                    :key="evento.id"
                    :evento="evento">
                </evento-component>
                    
            </div>
    </div>
</template>

<script>
    export default {
        props:['evento'],
        data() {
            return{
                eventos:[{
                    'id': 1,
                    'descripcion': 'adbdasda',
                    'creado': '20/20/2020'

                }]
            }
        },
        mounted() {
            console.log('Component mounted.')
        }, 
        methods : {
            addEvento(evento){
                this.eventos.push(evento);
            }
        }
    }
</script>
