<template>
<div class="overflow-auto maxh">
    <b-table id="cuestionario" small :fields="this.cuestionario.fields" :items="this.cuestionario.items" responsive="sm" :bordered="true">
        <template v-slot:cell(complejo1)="row" id="hola921">
            <inputChecked :resuelto="$props.inglesR" :esperado="row.item.complejo1.lista" :conTexto="true" :textoA="row.item.complejo1.textoA" :textoD="row.item.complejo1.textoD" :audio="row.item.complejo1.audio" :tamano="row.item.complejo1.tamano" />
        </template>
        <template v-slot:cell(complejo2)="row" id="hola7471">
            <inputChecked :resuelto="$props.inglesR" :esperado="row.item.complejo2.lista" :conTexto="true" :textoA="row.item.complejo2.textoA" :textoD="row.item.complejo2.textoD" :audio="row.item.complejo2.audio" :tamano="row.item.complejo2.tamano" />
        </template>

        <template v-slot:cell(complejo3)="row" id="hola7417">
            <inputChecked :resuelto="$props.inglesR" :esperado="row.item.complejo3.lista" :conTexto="true" :textoA="row.item.complejo3.textoA" :textoD="row.item.complejo3.textoD" :audio="row.item.complejo3.audio" :tamano="row.item.complejo3.tamano" />
        </template>

        <template v-slot:cell(complejo4)="row" id="hola7427737452">
            <inputChecked :resuelto="$props.inglesR" :esperado="row.item.complejo4.lista" :conTexto="true" :textoA="row.item.complejo4.textoA" :textoD="row.item.complejo4.textoD" :audio="row.item.complejo4.audio" :tamano="row.item.complejo4.tamano" />
        </template>

        <template v-slot:cell(complejo5)="row" id="hola737375375">
            <inputChecked :resuelto="$props.inglesR" :esperado="row.item.complejo5.lista" :conTexto="true" :textoA="row.item.complejo5.textoA" :textoD="row.item.complejo5.textoD" :audio="row.item.complejo5.audio" :tamano="row.item.complejo5.tamano" />
        </template>

        <template v-slot:cell(complejo21)="row" id="hola742742742">
            <inputCE :style="'width:' + row.item.complejo21.tamano + 'em;'" :object="row.item.complejo21" />
        </template>

        <template v-slot:cell(html1)="row" id="hola">
            <a v-html="row.item.html1"> {{ row.item.html1 }} </a>
        </template>
    </b-table>
</div>
</template>

<script>
import inputChecked from "./inputChecked";
import inputCE from "./inputCEnriquecido";

export default {
    components: {
        inputChecked,
        inputCE,
    },
    props: {
        cuestionario: Object,
        espanolR: Boolean,
        inglesR: Boolean,
    },
    mounted() {},
};
</script>

<style scoped>

</style>
