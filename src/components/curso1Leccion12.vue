<template>
    <div>

             <div class="">
      <p class="parrafoBlack">Key word:</p>
      <h4 class="subTitulo">YESTERDAY (ayer)</h4>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-8">
        <p
          v-for="item in frases1Pag50"
          v-html="item"
          class="text-left parrafoBlack"
        ></p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 parrafoBlack">
        <tablaTC
          class="overflow-auto"
          :cuestionario="tabla1P50"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <br /><br /><br />
    </div>

    <div class="row">
      <p class="subTitulo marginn-left">
        <i>
          <b>WORDSEARCH</b>
        </i>
      </p>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <p class="parrafoBlack">No hay una palabra en la sopa de letras</p>
    </div>
    <img src="/cursos/curso1/leccion12/imagenes/tablaPag51.png" />

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div
          v-for="(item, index) in frases1Pag51"
          :class="'  col-sm-4'"
          style="margin-bottom: 0.5em"
        >
          <div v-if="item.name == 'ice'"><inputCE :object="item" /></div>
          <div v-else-if="item.name == 'ic'">
            <inputChecked
              :resuelto="false"
              style="margin-right: 10px; display: inline-flex"
              :esperado="item.lista1"
              :conTexto="true"
              :textoA="item.textoA"
              :textoD="item.textoD"
            />
          </div>
        </div>
      </div>
    </div>
    <br /><br /><br />


            <p class="subTitulo marginn-left">
      <i>
        <b>PRACTICE</b>
      </i>
    </p>

    <div class="row">
      <i class="fa fa-diamond marginn-left" style="font-size: 1.5em"></i>

      <p class="parrafoBlack marginn-left">
        &nbsp;
        <b>Elegir el verbo correcto</b>
      </p>
      <br />
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div
          v-for="(item, index) in frases1Pag52"
          :class="' row col-sm-10'"
          style="margin-bottom: 0.5em"
        >
          <div v-if="item.name == 'ice'"><inputCE :object="item" /></div>
          <div v-else-if="item.name == 'ic'">
            <inputChecked
              :resuelto="false"
              style="margin-right: 10px; display: inline-flex"
              :esperado="item.lista1"
              :conTexto="true"
              :textoA="item.textoA"
              :textoD="item.textoD"
            />
          </div>
        </div>
      </div>
    </div>
    
    <br /><br /><br />



    </div>
</template>
<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
import tablaTraduccionCodigos from "./tablaTraduccionCodigos";
import inputCE from "./inputCEnriquecido";
import tablaTC from "./tablaTraduccionCodigos";

export default {
  components: {
    listaIndex,
    inputChecked,
    tablaTraduccionCodigos,
   
    posiblesRespuestasTabla,
    tablaTC,
    inputCE,
  },
  data() {
    return {

                frases1Pag52: [
        {
          lista1: ["saw"],

          textoA: "1. Te vi: I  ",
          textoD: "you(see/saw)",

          name: "ic",
        },
        {
          lista1: ["bought"],

          textoA: "2. Compré un nuevo celular: I ",
          textoD: "a new phone (Buy/bought)",

          name: "ic",
        },
        {
          lista1: ["understood"],

          textoA: "3. Entendí un poco más: I",
          textoD: "a little bit more (Understand/understood)",

          name: "ic",
        },
        {
          lista1: ["sat"],

          textoA: "4. Nos sentamos y hablamos: We ",
          textoD: "and talked (Sit/sat)",

          name: "ic",
        },
        {
          lista1: ["brought"],

          textoA: "5. Te traje algo para comer: I ",
          textoD: " you something to eat (bring/brought)",

          name: "ic",
        },
        {
          lista1: ["lit"],

          textoA: "6. Encendí una vela: I ",
          textoD: "a candle (light/lit)",

          name: "ic",
        },
        {
          lista1: ["thought"],

          textoA: "7. Yo pensé en mi madre: I ",
          textoD: "of my mother (think/thought)",

          name: "ic",
        },
        {
          lista1: ["had"],

          textoA: "8. Tuvimos un buen día: We",
          textoD: "a good day (have/had)",

          name: "ic",
        },
        {
          lista1: ["gave"],

          textoA: "9. Mi mamá me dio esto: My mother",
          textoD: "me this (give/gave)",

          name: "ic",
        },
        {
          lista1: ["taught"],

          textoA: "10.Mi padre me enseñó a conducir: The teacher  ",
          textoD: "me how to drive (teach/taught)",

          name: "ic",
        },
        {
          lista1: ["drove"],

          textoA: "11.El me trajo en carro a la casa: He  ",
          textoD: "me home (drive/drove)",

          name: "ic",
        },
        {
          lista1: ["bit"],

          textoA: "12.El perro mordió a mi amigo: The dog",
          textoD: " my friend (bite/bit)",

          name: "ic",
        },
        {
          lista1: ["took"],

          textoA: "13.Yo tomé una siesta: I",
          textoD: "a nap (take/took)",

          name: "ic",
        },
        {
          lista1: ["sold"],

          textoA: "14.Mi papá vendió su carro: My dad ",
          textoD: " his car (sell/sold)",

          name: "ic",
        },
        {
          lista1: ["brought"],

          textoA: "15.Te traje esto: I ",
          textoD: "you this (bring/brought)",

          name: "ic",
        },
        {
          lista1: ["forgot"],

          textoA: "16.Olvidé cerrar la puerta: I  ",
          textoD: "to close the door (forget/forgot)",

          name: "ic",
        },
        {
          lista1: ["spoke"],

          textoA: "17.Hablé con ella en inglés: I ",
          textoD: "to her in english (speak/spoke)",

          name: "ic",
        },

        {
          lista1: ["caught"],

          textoA: "18.Ella atrapó un pez: She ",
          textoD: "a fish (catch/caught)",

          name: "ic",
        },
        {
          lista1: ["woke"],

          textoA: "19.Me desperté un poco tarde: I  ",
          textoD: "up a little late (wake/woke)",

          name: "ic",
        },
      ],
       frases1Pag50: [
        "1. I <FONT class='text-danger'>saw</FONT> you yesterday",
        "2. I <FONT class='text-danger'>drank</FONT> too much yesterday",
        "3. That <FONT class='text-danger'>kid</FONT> stole my toy yesterday",
        "4. I <FONT class='text-danger'>felt</FONT> very well yesterday",
        "5. I <FONT class='text-danger'>went</FONT> with her yesterday",
        "6. I <FONT class='text-danger'>came</FONT> to say good bye yesterday",
        "7. I <FONT class='text-danger'>spoke</FONT> to him yesterday",
        "8. We <FONT class='text-danger'>understood</FONT> everything yesterday",
        "9. I <FONT class='text-danger'>brought</FONT> these flowers to you yesterday",
        "10.My father <FONT class='text-danger'>bough</FONT> a nice car yesterday",
        "11.That dog <FONT class='text-danger'>bit</FONT> me yesterday",
        "12.I <FONT class='text-danger'>sat</FONT> next to you yesterday",
        "13.I <FONT class='text-danger'>thought</FONT> you were working yesterday",
        "14.The kid <FONT class='text-danger'>fell</FONT> off the bike yesterday",
        "15.I <FONT class='text-danger'>had</FONT> breakfast late yesterday",
      ],

      tabla1P50: {
        fields: [
          { key: "A", label: "", thClass: "noHead " },
          { key: "complejo1", label: "", thClass: "" },
        ],
        items: [
          {
            A: "1. Entendimos todo ayer ",
            complejo1: {
              lista: [" We understood everything yesterday"],
              textoA: "8 -",
            },
          },
          {
            A: "2. Desayuné tarde ayer ",
            complejo1: {
              lista: ["I had breakfast late yesterday"],
              textoA: "15-",
            },
          },
          {
            A: "3. Fui con ella ayer ",
            complejo1: { lista: [" That dog bit me yesterday"], textoA: "5 -" },
          },
          {
            A: "4. Ese perro me mordió ayer ",
            complejo1: { lista: ["That dog bit me yesterday"], textoA: "11 -" },
          },
          {
            A: "5. ese niño me robó mi juguete ayer ",
            complejo1: {
              lista: ["That kid stole my toy yesterday"],
              textoA: "3 -",
            },
          },
          {
            A: "6. Vine a despedirme ayer",
            complejo1: {
              lista: ["I came to say good-bye yesterday"],
              textoA: "6 -",
            },
          },
          {
            A: "7. Hable con él ayer",
            complejo1: { lista: [" I spoke to him yesterday"], textoA: "7 -" },
          },
          {
            A: "8. Yo te vi ayer ",
            complejo1: { lista: ["I saw you yesterday"], textoA: "1 -" },
          },
          {
            A: "9. Te traje estás flores ayer ",
            complejo1: {
              lista: ["I brought these flowers to you yesterday"],
              textoA: "9 -",
            },
          },
          {
            A: "10.Mi padre compró un buen carro ",
            complejo1: {
              lista: ["My father bought a nice car yesterday"],
              textoA: "10 -",
            },
          },
          {
            A: "11.Me sentí muy bien ayer",
            complejo1: { lista: ["I felt good yesterday"], textoA: "4 -" },
          },
          {
            A: "12.Me senté al lado tuyo ayer ",
            complejo1: {
              lista: ["I sat next to you yesterday"],
              textoA: "12 -",
            },
          },
          {
            A: "13.Pensé que estabas trabajando ",
            complejo1: {
              lista: ["I thought you were working"],
              textoA: "13 -",
            },
          },
          {
            A: "14.El niño se cayó de la bicicleta ",
            complejo1: { lista: ["The kid fell off the bike"], textoA: "14 -" },
          },
          {
            A: "15.Bebí demasiado ayer ",
            complejo1: { lista: ["I drank too much yesterday"], textoA: "2 -" },
          },
        ],
      },
      frases1Pag51: [
        {
          lista1: ["Vi"],

          textoA: "I SAW",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Compré"],

          textoA: "I BOUGHT",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Entendí"],

          textoA: "I UNDERSTOOD",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Me senté"],

          textoA: "I SAT",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Yo compré"],

          textoA: "I BROUGHT",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Encendí"],

          textoA: "I LIT",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Lancé"],

          textoA: "I THREW",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Comí"],

          textoA: "I ATE ",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Me caí"],

          textoA: "I FEL",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Pensé"],

          textoA: "I THOUGHT",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Envié"],

          textoA: "I SENT",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Nadé"],

          textoA: "I SWAM",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Escribí"],

          textoA: "I WROTE",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Encontré"],

          textoA: "I FOUND",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Tuve"],

          textoA: "I HAD",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Hice"],

          textoA: "I DID",
          textoD: "",

          name: "ic",
        },

        {
          lista1: ["Escondí"],

          textoA: "I HID",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Dí"],

          textoA: "I GAVE",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Perdoné"],

          textoA: "I FORGAVE",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Rompí"],

          textoA: "I BROKE",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Sentí"],

          textoA: "I FELT",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Atrapé"],

          textoA: "I CAUGHT",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Enseñé"],

          textoA: "I TAUGHT",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Hablé"],

          textoA: "I SPOKE",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["vine"],

          textoA: "I CAME",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Sostuve"],

          textoA: "I HELD",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Robé"],

          textoA: "I STOLE",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Llevé"],

          textoA: "I TOOK",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Dije"],

          textoA: "I SAID",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Me desperté"],

          textoA: "I WOKE",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Conté"],

          textoA: "I TOLD",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Bebí"],

          textoA: "I DRANK",
          textoD: "",

          name: "ic",
        },
        {
          lista1: ["Fui"],

          textoA: "I WENT",
          textoD: "",

          name: "ic",
        },
      ],

    }
    }
    }
    </script>
    <style scoped>
.show-grid {
  border: 1px solid;
  color: black;
}

#text,
#inputText {
  text-align: left;
}
/deep/ .Subrayado {
  text-decoration-line: underline;
}
/deep/ .Blue {
  background-color: cornflowerblue;
}
/deep/ .Red {
  background-color: crimson;
}
/deep/ .Yellow {
  background-color: yellow;
}
/deep/ .Green {
  background-color: chartreuse;
}

/deep/ .noHead {
  border-width: 0;
  font-size: 0;
}

inputChecked {
  display: inline-flex;
}
</style>