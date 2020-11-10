<template>
  <div class="panel panel-default">
                <div class="panel-heading">QUE SUCEDE REALMENTE</div>

                <div class="panel-body">
                    <form action="" v-on:submit.prevent = "newEvento()">
                        <div class="form-group">
                            <label for="evento">¿Planear Evento?</label>
                            <input type="text" class="form-control" name="evento"
                            v-model="descripcion">
                        </div>
                        <button type="submit" class="btn btn-primary">
                            Publicar evento
                        </button>
                    </form>
                </div>
            </div>
</template>

<script>
    export default {
        data(){
            return{
                descripcion : ''
            }
        },
        mounted() {
            console.log('Component mounted.')
        },
        methods: {
            newEvento(){
                let evento = {
                    id : '32',
                    descripcion : this.descripcion,
                    creado : '20/10/1959'
                };
                alert(this.descripcion);
                this.$emit('new',evento);
                this.descripcion = '';
            }

        }
    }
</script>