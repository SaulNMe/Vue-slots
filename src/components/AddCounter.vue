<template>
    <div class="container">
        <div class="field is-grouped">
            <div class="control">
                <button class="button is-primary" v-on:click="addCounter()">Add</button>
            </div>
        </div>
    </div>
</template>

<script>
import store from "@/store";
import * as types from '@/store/mutationTypes';

export default{
    methods:{
        addCounter() {
            store.dispatch({
                type: types.Increment,
                amount: 100
            });
        }
    }
};
</script>