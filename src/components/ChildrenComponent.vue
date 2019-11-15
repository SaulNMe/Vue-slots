<template>
    <div>
    <slot>
        <p>Hello from the child!</p>{{hello}}
    </slot>

    </div>
</template>

<script>
export default {
    props: {
        hello: String
    }
}
</script>