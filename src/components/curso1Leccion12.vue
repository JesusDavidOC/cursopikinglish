<template>
    <div>
        <b-row>
   
      <b-col md="10" >
        <p class="parrafo ">Key word:</p>
        <p class="subTitulo marginn-left">
          YESTERDAY (ayer)
        </p>
         
        </b-col>
</b-row>
       
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-8">
        <p
          v-for="item in frases1Pag50"
          v-html="item"
          class="text-left parrafo"
        ></p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-md-auto parrafoBlack">
        <tablaTC
          class="overflow-auto"
          :cuestionario="tabla1P50"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <br /><br /><br />
    </div>
     <b-row>
   
      <b-col md="10" >
        
        <p class="subTitulo marginn-left">
         WORDSEARCH
        </p>
         
        </b-col>
</b-row>
    
    <div class="row">
      <div class="col-sm-1"></div>
      <p class="parrafo">No hay una palabra en la sopa de letras</p>
    </div>
    <img src="/cursos/curso1/leccion12/imagenes/tablaPag51.png" />

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div
          v-for="(item, index) in frases1Pag51"
          
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
              :tamano="item.tamano"
            />
          </div>
        </div>
      </div>
    </div>
    <br /><br /><br />
      <b-row>
   
      <b-col md="10" >
        
        <p class="subTitulo marginn-left">
         PRACTICE
        </p>
         
        </b-col>
</b-row>

        

    <div class="row">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond marginn-left" style="font-size: 1.5em"></i>

      <p class="fuenteDiamond marginn-left">
      Elegir el verbo correcto
      </p>
      
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 ">
        <div
          v-for="(item, index) in frases1Pag52"
          
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
              :tamano="item.tamano"
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

          textoA: "1. <strong>Te vi:</strong> I  ",
          textoD: "you(see/saw)",

          name: "ic",
          tamano:23
        },
        {
          lista1: ["bought"],

          textoA: "2.<strong> Compré un nuevo celular:</strong> I ",
          textoD: "a new phone (Buy/bought)",

          name: "ic",
          tamano:45
        },
        {
          lista1: ["understood"],

          textoA: "3.<strong> Entendí un poco más:</strong> I",
          textoD: "a little bit more (Understand/understood)",

          name: "ic",
          tamano:53
        },
        {
          lista1: ["sat"],

          textoA: "4. <strong>Nos sentamos y hablamos:</strong> We ",
          textoD: "and talked (Sit/sat)",

          name: "ic",
          tamano:40
        },
        {
          lista1: ["brought"],

          textoA: "5.<strong> Te traje algo para comer:</strong> I ",
          textoD: " you something to eat (bring/brought)",

          name: "ic",
          tamano:50
        },
        {
          lista1: ["lit"],

          textoA: "6.<strong> Encendí una vela: </strong>I ",
          textoD: "a candle (light/lit)",

          name: "ic",
          tamano:32
        },
        {
          lista1: ["thought"],

          textoA: "7. <strong>Yo pensé en mi madre:</strong> I ",
          textoD: "of my mother (think/thought)",

          name: "ic",
          tamano:44

        },
        {
          lista1: ["had"],

          textoA: "8. <strong>Tuvimos un buen día:</strong> We",
          textoD: "a good day (have/had)",

          name: "ic",
          tamano:40

        },
        {
          lista1: ["gave"],

          textoA: "9. <strong>Mi mamá me dio esto:</strong> My mother",
          textoD: "me this (give/gave)",

          name: "ic",
          tamano:43
        },
        {
          lista1: ["taught"],

          textoA: "10.<strong>Mi padre me enseñó a conducir:</strong> The teacher  ",
          textoD: "me how to drive (teach/taught)",

          name: "ic",
          tamano:57
        },
        {
          lista1: ["drove"],

          textoA: "11.<strong>El me trajo en carro a la casa:</strong> He  ",
          textoD: "me home (drive/drove)",

          name: "ic",
          tamano:45
        },
        {
          lista1: ["bit"],

          textoA: "12.<strong>El perro mordió a mi amigo:</strong> The dog",
          textoD: " my friend (bite/bit)",

          name: "ic",
          tamano:42
        },
        {
          lista1: ["took"],

          textoA: "13.<strong>Yo tomé una siesta:</strong> I",
          textoD: "a nap (take/took)",

          name: "ic",
          tamano:35
        },
        {
          lista1: ["sold"],

          textoA: "14.<strong>Mi papá vendió su carro:</strong> My dad ",
          textoD: " his car (sell/sold)",

          name: "ic",
          tamano:41
        },
        {
          lista1: ["brought"],

          textoA: "15.<strong>Te traje esto: </strong>I ",
          textoD: "you this (bring/brought)",

          name: "ic",
          tamano:36
        },
        {
          lista1: ["forgot"],

          textoA: "16.<strong>Olvidé cerrar la puerta: </strong>I  ",
          textoD: "to close the door (forget/forgot)",

          name: "ic",
          tamano:45
        },
        {
          lista1: ["spoke"],

          textoA: "17.<strong>Hablé con ella en inglés: </strong>I ",
          textoD: "to her in english (speak/spoke)",

          name: "ic",
          tamano:47
        },

        {
          lista1: ["caught"],

          textoA: "18.<strong>Ella atrapó un pez:</strong> She ",
          textoD: "a fish (catch/caught)",

          name: "ic",
          tamano:38
        },
        {
          lista1: ["woke"],

          textoA: "19.<strong>Me desperté un poco tarde:</strong> I  ",
          textoD: "up a little late (wake/woke)",

          name: "ic",
          tamano:45
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
              lista: ["We understood everything yesterday"],
              textoA: "8 -",
              tamano:30
            },
          },
          {
            A: "2. Desayuné tarde ayer ",
            complejo1: {
              lista: ["I had breakfast late yesterday"],
              textoA: "15-",
              tamano:30
            },
          },
          {
            A: "3. Fui con ella ayer ",
            complejo1: { lista: ["That dog bit me yesterday"], textoA: "5 -" , tamano:30},
          },
          {
            A: "4. Ese perro me mordió ayer ",
            complejo1: { lista: ["That dog bit me yesterday"], textoA: "11 -",tamano:30 },
          },
          {
            A: "5. ese niño me robó mi juguete ayer ",
            complejo1: {
              lista: ["That kid stole my toy yesterday"],
              textoA: "3 -", tamano:30
            },
          },
          {
            A: "6. Vine a despedirme ayer",
            complejo1: {
              lista: ["I came to say good-bye yesterday"],
              textoA: "6 -", tamano:30
            },
          },
          {
            A: "7. Hable con él ayer",
            complejo1: { lista: ["I spoke to him yesterday"], textoA: "7 -" , tamano:30},
          },
          {
            A: "8. Yo te vi ayer ",
            complejo1: { lista: ["I saw you yesterday"], textoA: "1 -",tamano:30 },
          },
          {
            A: "9. Te traje estás flores ayer ",
            complejo1: {
              lista: ["I brought these flowers to you yesterday"],
              textoA: "9 -",tamano:30
            },
          },
          {
            A: "10.Mi padre compró un buen carro ",
            complejo1: {
              lista: ["My father bought a nice car yesterday"],
              textoA: "10 -",tamano:30
            },
          },
          {
            A: "11.Me sentí muy bien ayer",
            complejo1: { lista: ["I felt good yesterday"], textoA: "4 -",tamano:30 },
          },
          {
            A: "12.Me senté al lado tuyo ayer ",
            complejo1: {
              lista: ["I sat next to you yesterday"],
              textoA: "12 -",tamano:30
            },
          },
          {
            A: "13.Pensé que estabas trabajando ",
            complejo1: {
              lista: ["I thought you were working"],
              textoA: "13 -",tamano:30
            },
          },
          {
            A: "14.El niño se cayó de la bicicleta ",
            complejo1: { lista: ["The kid fell off the bike"], textoA: "14 -" ,tamano:30},
          },
          {
            A: "15.Bebí demasiado ayer ",
            complejo1: { lista: ["I drank too much yesterday"], textoA: "2 -" , tamano:30},
          },
        ],
      },
      frases1Pag51: [
        {
          lista1: ["Vi"],

          textoA: "I SAW",
          textoD: "",

          name: "ic",
          tamano:13
        },
        {
          lista1: ["Compré"],

          textoA: "I BOUGHT",
          textoD: "",

          name: "ic",
          tamano:19
        },
        {
          lista1: ["Entendí"],

          textoA: "I UNDERSTOOD",
          textoD: "",

          name: "ic",
          tamano:22
        },
        {
          lista1: ["Me senté"],

          textoA: "I SAT",
          textoD: "",

          name: "ic",
          tamano:16
        },
        {
          lista1: ["Yo compré"],

          textoA: "I BROUGHT",
          textoD: "",

          name: "ic",
          tamano:21
        },
        {
          lista1: ["Encendí"],

          textoA: "I LIT",
          textoD: "",

          name: "ic",
          tamano:15
        },
        {
          lista1: ["Lancé"],

          textoA: "I THREW",
          textoD: "",

          name: "ic",
          tamano:17
        },
        {
          lista1: ["Comí"],

          textoA: "I ATE ",
          textoD: "",

          name: "ic",
          tamano:14
        },
        {
          lista1: ["Me caí"],

          textoA: "I FEL",
          textoD: "",

          name: "ic",
          tamano:15
        },
        {
          lista1: ["Pensé"],

          textoA: "I THOUGHT",
          textoD: "",

          name: "ic",
          tamano:19
        },
        {
          lista1: ["Envié"],

          textoA: "I SENT",
          textoD: "",

          name: "ic",
          tamano:15
        },
        {
          lista1: ["Nadé"],

          textoA: "I SWAM",
          textoD: "",

          name: "ic",
          tamano:16
        },
        {
          lista1: ["Escribí"],

          textoA: "I WROTE",
          textoD: "",

          name: "ic",
          tamano:17
        },
        {
          lista1: ["Encontré"],

          textoA: "I FOUND",
          textoD: "",

          name: "ic",
          tamano:19
        },
        {
          lista1: ["Tuve"],

          textoA: "I HAD",
          textoD: "",

          name: "ic",
          tamano:14
        },
        {
          lista1: ["Hice"],

          textoA: "I DID",
          textoD: "",

          name: "ic",
          tamano:14
        },

        {
          lista1: ["Escondí"],

          textoA: "I HID",
          textoD: "",

          name: "ic",
          tamano:16
        },
        {
          lista1: ["Dí"],

          textoA: "I GAVE",
          textoD: "",

          name: "ic",
          tamano:14
        },
        {
          lista1: ["Perdoné"],

          textoA: "I FORGAVE",
          textoD: "",

          name: "ic",
          tamano:20
        },
        {
          lista1: ["Rompí"],

          textoA: "I BROKE",
          textoD: "",

          name: "ic",
          tamano:17
        },
        {
          lista1: ["Sentí"],

          textoA: "I FELT",
          textoD: "",

          name: "ic",
          tamano:16
        },
        {
          lista1: ["Atrapé"],

          textoA: "I CAUGHT",
          textoD: "",

          name: "ic",
          tamano:18
        },
        {
          lista1: ["Enseñé"],

          textoA: "I TAUGHT",
          textoD: "",

          name: "ic",
          tamano:18
        },
        {
          lista1: ["Hablé"],

          textoA: "I SPOKE",
          textoD: "",

          name: "ic",
          tamano:16
        },
        {
          lista1: ["vine"],

          textoA: "I CAME",
          textoD: "",

          name: "ic",
          tamano:15
        },
        {
          lista1: ["Sostuve"],

          textoA: "I HELD",
          textoD: "",

          name: "ic",
          tamano:17
        },
        {
          lista1: ["Robé"],

          textoA: "I STOLE",
          textoD: "",

          name: "ic",
          tamano:16
        },
        {
          lista1: ["Llevé"],

          textoA: "I TOOK",
          textoD: "",

          name: "ic",
          tamano:15
        },
        {
          lista1: ["Dije"],

          textoA: "I SAID",
          textoD: "",

          name: "ic",
          tamano:14
        },
        {
          lista1: ["Me desperté"],

          textoA: "I WOKE",
          textoD: "",

          name: "ic",
          tamano:20
        },
        {
          lista1: ["Conté"],

          textoA: "I TOLD",
          textoD: "",

          name: "ic",
          tamano:15
        },
        {
          lista1: ["Bebí"],

          textoA: "I DRANK",
          textoD: "",

          name: "ic",
          tamano:16
        },
        {
          lista1: ["Fui"],

          textoA: "I WENT",
          textoD: "",

          name: "ic",
          tamano:15
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