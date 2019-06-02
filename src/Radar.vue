<template>
    <div>
        <svg class="radar"></svg>
    </div>
</template>

<script>
demofile = require('demofile')
export default {
    props: {
        demofile: {
            type: Object,
            required: true
        }
    }
}
</script>