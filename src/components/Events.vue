<!-- HTML  -->
<template>
    <v-container>
        <h2>Proximos Eventos</h2> 
        <v-flex xs12 id="card" v-for="e in events">
            <v-card color="blue-grey darken-2" class="white--text">
                <v-card-title primary-title>
                    <div>
                        <div class="headline">Ricardo O'Farrill {{e.name}}</div>
                        <span>Stand Up comedy de un gordo profesional.</span>
                    </div>
                </v-card-title>
                <v-card-actions>
                    <v-btn flat dark>Compra tus boletos</v-btn>
                </v-card-actions>
            </v-card>
        </v-flex>
    </v-container>
</template>


<!-- Script -->
<script>
import axios from 'axios';

export default {
    data(){
        return {
            events: [],
            errors: []
        }
    },

    created: function(){

        axios.get('796d02c6.ngrok.io')
        .then(res => {
            console.log(res)
            this.events = res
        }).catch(err => {
            console.log(err)
        })
    },
    methods: {
        read_api() {
        },
    }
}
</script>

<style>
    #id {
        padding-bottom: 10px;
    }
</style>

