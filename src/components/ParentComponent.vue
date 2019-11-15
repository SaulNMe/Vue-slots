<template>
    <div>
        <slot v-bind:data="data"></slot>
        <!-- <ChildrenComponent>
        <p>Hello from the parent!</p>
        </ChildrenComponent>
        <ChildrenComponent></ChildrenComponent> -->
    </div>
</template>

<script>
export default {
    data() {
        return {
            data: [
                {
                    id: 1,
                    name: 'Luas',
                    nickName: 'Loquillo'
                }, {
                    id: 2,
                    name: 'Saul',
                    nickName: 'Ls'
                }, {
                    id: 3,
                    name: 'Loquillo',
                    nickName: 'M'
                }
            ],
            hello: 'Hello to my children component!'
        }
    }
}
</script>