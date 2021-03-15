<template>
    <div>

        <div v-for="user in users" v-bind:key="user.id">
            <div>{{user.name}}</div>
        </div>

    </div>
</template>


<script>
export default {
    data(){
        return{
            temporaryUser:'',

            users: [
                {id: 1, name: 'Krystian', toShow: false},
                {id: 2, name: 'Tomek', toShow: true},
                {id: 3, name: 'Domka', toShow: true}
            ]
        }
    }

    }

</script>