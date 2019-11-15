<template>
    <div>
        <slot v-bind:user="user"></slot>
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
            data: {
                name: 'Luas',
                nickName: 'Loquillo'
            },
            user: {
                name: 'me',
                lastname: 'N',
                surname: 'Me'
            },
            hello: 'Hello to my children component!'
        }
    }
}
</script>