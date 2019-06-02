<!--https://codepen.io/AndrewMcDowe/pen/akWBKj-->
<template>
    <div>
        <div></div>
        <ul v-if="players.length">
            <PlayerHealth
                v-for="player in players"
                v-bind:key="player.index"
                v-bind:player="player"
            />
        </ul>
    </div>
</template>

<script>
import PlayerHealth from './PlayerHealth'
export default{
    components: {
        PlayerHealth
    },
    data () { 
        return {
            players:[]
        }
    },
    methods: {
        addPlayer(player) {
            this.players.push(player)
        }
    }
}
</script>