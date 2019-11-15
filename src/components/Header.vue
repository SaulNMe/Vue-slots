<template>
    <div>
        <ul>
            <li v-for="item in datos" v-bind:key="item.id">
            <!-- content -->
            {{item.name}} - {{item.nickName}}
            </li>
        </ul>
        <p ref="foo" class="cosa otra">foo</p>
    </div>
</template>

<script>
export default {
    props: {
        data: Array
    },
    data() {
        return {
            datos: []
        }
    },
    mounted() {
        this.datos = this.data;
        console.log(this.$refs["foo"].classList);
    }
}
</script>