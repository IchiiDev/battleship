<template>
    <div id="navbar">
        <p v-if="!logged">You need to be logged in to continue</p>
        <div class="content" v-else>
            <p id="room">Room: {{ room }}</p>
            <p id="account">Test: {{ account }}</p>
        </div>
    </div>
</template>

<style scoped>
    #navbar {
        width: 100%;
        height: 4em;
        background-color: #2C2F33;
        color: #99AAB5;
        display: flex;
        justify-content: center;
    }
    .content {
        background-color: white;
        display: flex;
        width: 100%;
    }
    #room {
        justify-self: left;
    }
    #account {
        justify-self: right;
    }
</style>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
@Component
export default class NavBar extends Vue {
  @Prop() public logged = true;
  @Prop() public account!: string;
  @Prop() public room!: string;
}
</script>