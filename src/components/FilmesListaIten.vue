<template>
    <div>
        <input type="text" :value="titulo" :placeholder="$attrs.placeholder">
    </div>
    <!-- <li class="list-group-item">
        <span>{{ filmeTituloConcatenado }} | {{ ano }}</span>
        <button class="btn btn-secondary float-right">Selecionar</button>
    </li> -->
</template>

<script>
export default {
    inheritAttrs: false,
    props: {
        titulo: {
            type: String,
            required: true
        },
        ano: {
            type: Number,
            required: true
        }
    },
    computed: {
        filmeTituloConcatenado() {
            return `Título: ${this.titulo}`
        }
    },
    created() {
        console.log('Attrs: ', this.$attrs)
    }
}
</script>

