<template>
    <div class="container">
        <div class="field is-grouped">
            <div class="control">
                <button class="button is-primary" v-on:click="removeCounter()">Remove</button>
            </div>
        </div>
    </div>
</template>

<script>
import store from "@/store/index";
import * as types from '@/store/mutationTypes';

export default{
    methods:{
        removeCounter() {
            store.dispatch({
                type: types.Decrement, 
                amount: 100
            });
        }
    }
};
</script>
<style lang="scss">
$color: #42b983;
$hoverColor: #2f815c;
$textColor: #fff;
    .button {
        border-radius: 5px;
        outline: none;
        border: 1px solid $color;
        background-color: $color;
        color: $textColor;
        margin: 10px;
        &:hover {
            background-color: $hoverColor;
            border-color: $hoverColor;
        }
    }
</style>