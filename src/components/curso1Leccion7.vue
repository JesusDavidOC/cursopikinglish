<template>
  <div>
    <div class="row">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond" style="font-size: 1.5em"></i>

      <p class="fuenteDiamond">
        Escriba la traducción en ingles y completa las oraciones
      </p>
    </div>
    <div class="row" style="padding: 0%">
      <div class="col-sm-1"></div>
      <div
        class="col-sm-3"
        style="padding: 0%"
        v-for="item in $data.tablaUnoPag35"
      >
        <listaIndex :tabla="item" style="padding: 0%"/>
      </div>
    </div>
      <b-row>
   
       <b-col md=1></b-col>
        <i class="fa fa-diamond" style="font-size: 1.5em"></i>
        <p class="fuenteDiamond">
          Completa :
        </p>
         
       
</b-row>
    <div class="row">
      <div class="col-sm-1"></div>
      
      <div class="col-md-9" >
        <tablaTC
          :cuestionario="tablaDosPag35"
          class="botTabla"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond" style="font-size: 1.5em"></i>

      <p class="fuenteDiamond">
        Aquí hay una lista de los verbos más fáciles del inglés. Reescribe las
        oraciones con “she”
      </p>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <font class="parrafo">
        Recuerda que la
        <font class="text-danger">S</font> ,
        <font class="text-danger">ES</font> o
        <font class="text-danger">IES</font> se le agrega a un verbo en presente
        precedida de SHE, HE o IT
      </font>
    </div>

    <div class="row overflow-auto">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC
          :cuestionario="$data.cuestionario1Pag36"
          :inglesR="false"
          :espanolR="true"
          class="botTabla"
        />
      </div>
    </div>
    <div class="row container">
      <div class="col-md-1"></div>
      <b-col md="10" class="titulo" style="margin-bottom:2em;">
        <h3>LOS VERBOS GEMELOS DE LA LÓGICA DEL INGLÉS</h3>
      </b-col>
    </div>

    

    <div class="row">
      <div class="col-sm-1"></div>
      <ul>
        <div class="botTabla">
          <li v-for="item in frasesPag37" class="parrafo">
            {{ item }}
          </li>
        </div>
      </ul>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-5">
        <h3 class="col-sm-12 bg-warning">Verbs</h3>
        <div class="row col-sm-12 parrafoBlack" id="tabla">
          <div class="col-sm-4">
            <h5 class="text-center show-grid">Present</h5>
            <h5 class="text-center BigCelda show-grid">Do-Does</h5>
            <h5 class="text-center BigCelda show-grid botTabla">Have-Has</h5>
          </div>
          <div class="col-sm-4">
            <h5 class="text-center show-grid">past</h5>

            <h5 class="text-center BigCelda show-grid">Did</h5>

            <h5 class="text-center BigCelda show-grid">Had</h5>
          </div>
          <div class="col-sm-4">
            <h5 class="text-center show-grid">participle</h5>
            <h5 class="text-center BigCelda show-grid">Done</h5>
            <h5 class="text-center BigCelda show-grid">Had</h5>
          </div>
        </div>
      </div>
      <div class="col-sm-3" id="tabla">
        <h3 class="col-sm-12 bg-danger">AUXILIARES</h3>
        <div class="row">
          <div class="col-sm-6">
            <h5 class="text-center show-grid">?</h5>
            <h5 class="text-center show-grid">Do</h5>
            <h5 class="text-center show-grid">Does</h5>
            <h5 class="text-center show-grid">Did</h5>
          </div>
          <div class="col-sm-6">
            <h5 class="text-center show-grid">-</h5>
            <h5 class="text-center show-grid">Don't</h5>
            <h5 class="text-center show-grid">Doesn't</h5>
            <h5 class="text-center show-grid">Didn't</h5>
          </div>
          <h5 class="BigCelda text-center show-grid col-sm-12">
            Recuerde que el participio <br />
            se usa con have has y had
          </h5>
        </div>
      </div>

      <div class="col-sm-3" id="tabla">
        <h3 class="col-sm-12 bg-primary">S.P.V</h3>
        <div class="col-sm-12">
          <h5 class="text-center BigCeldaDos show-grid">
            Los verbos con poder se pueden negar solos
          </h5>
        </div>
        <div class="row" style="items-aling: center">
          <div class="col-sm-6">
            <h5 class="text-center show-grid">Do</h5>
            <h5 class="text-center show-grid">Does</h5>
            <h5 class="text-center show-grid">Did</h5>
          </div>
          <div class="col-sm-6">
            <h5 class="text-center show-grid">Don't</h5>
            <h5 class="text-center show-grid">Doesn't</h5>
            <h5 class="text-center show-grid">Didn't</h5>
          </div>
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond" style="font-size: 1.5em"></i>
      <p class="fuenteDiamond">
        Practica llenado la tabla de los verbos gemelos.
      </p>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-5">
        <p class="col-sm-12 bg-warning">
          <inputChecked
            style="width: 100%; padding: 0%"
            :resuelto="false"
            :esperado="['Verbs']"
          />
        </p>
        <div class="row col-sm-12 parrafoBlack" id="tabla">
          <div class="col-sm-4" style="padding: 0%">
            <p class="text-center" style="padding: 0%">
              <inputChecked
                style="
                  width: 100%;
                  margin-left: 10px;
                  margin-right: 10px;
                  padding: 0%;
                "
                :resuelto="false"
                :esperado="['Present']"
              />
            </p>
            <p class="text-center" style="padding: 0%">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Do-Does']"
              />
            </p>
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Have-Has']"
              />
            </p>
          </div>
          <div class="col-sm-4" style="padding: 0%">
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['past']"
              />
            </p>

            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Did']"
              />
            </p>

            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Had']"
              />
            </p>
          </div>
          <div class="col-sm-4" style="padding: 0%">
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['participle']"
              />
            </p>
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Done']"
              />
            </p>
            <p class="text-center BigCelda">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Had']"
              />
            </p>
          </div>
        </div>
      </div>
      <div class="col-sm-3 parrafoBlack" id="tabla">
        <p class="col-sm-12 bg-danger">
          <inputChecked
            style="width: 100%; margin-left: 10px; margin-right: 10px"
            :resuelto="false"
            :esperado="['AUXILIARES']"
          />
        </p>
        <div class="row">
          <div class="col-sm-6" style="padding: 0%">
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['?']"
              />
            </p>
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Do']"
              />
            </p>
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Does']"
              />
            </p>
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Did']"
              />
            </p>
          </div>
          <div class="col-sm-6" style="padding: 0%">
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['-']"
              />
            </p>
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Don´t']"
              />
            </p>
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Does´nt']"
              />
            </p>
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Didn´t']"
              />
            </p>
          </div>
          <p class="BigCelda text-center col-sm-12">
            <inputChecked
              style="width: 100%; margin-left: 10px; margin-right: 10px"
              :resuelto="false"
              :esperado="[
                'Recuerde que el participio se usa con have has y had',
              ]"
            />
          </p>
        </div>
      </div>

      <div class="col-sm-3 parrafoBlack" id="tabla" style="padding: 0%">
        <p class="col-sm-12 bg-primary">
          <inputChecked
            style="width: 100%; margin-left: 10px; margin-right: 10px"
            :resuelto="false"
            :esperado="['S.P.V']"
          />
        </p>
        <div class="col-sm-12">
          <p class="text-center">
            <inputChecked
              style="width: 100%; margin-left: 10px; margin-right: 10px"
              :resuelto="false"
              :esperado="['Los verbos con poder se pueden negar solos']"
            />
          </p>
        </div>
        <div class="row" style="items-aling: center">
          <div class="col-sm-6" style="padding: 0%">
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Do']"
              />
            </p>
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Does']"
              />
            </p>
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Did']"
              />
            </p>
          </div>
          <div class="col-sm-6" style="padding: 0%">
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Don´t']"
              />
            </p>
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Doesn´t']"
              />
            </p>
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Didn´t']"
              />
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond marginn-left" style="font-size: 1.5em"> </i>

      <p class="fuenteDiamond">
        Completa las siguientes oraciones con el verbo, auxiliar o verbo con
        super poder.
      </p>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div
          v-for="(item, index) in frases2Pag37"
          
          style="margin-bottom: 1em;"
        >
          <div v-if="item.name == 'ice'"><inputCE :object="item"  /></div>
          <div v-else-if="item.name == 'ic'">
            <inputChecked
              :resuelto="false"
            
              :esperado="item.lista1"
              :conTexto="true"
              :textoA="item.textoA"
              :textoD="item.textoD"
              :tamano="item.tamano"
              :audio="item.audio"
              
            />
          </div>
        </div>
      </div>
    </div>

    
  </div>
</template>


<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
import inputCE from "./inputCEnriquecido";
import tablaTraduccionCodigos from "./tablaTraduccionCodigos";

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
      tablaUnoPag35: [
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "html",

              thClass: "noHead",
            },
          ],
          items: [
            {
              html:
                '<FONT class="">ORACIÓN EN PRESENTE  AFIRMATIVO <br> (INGLÉS)</FONT>',
            },
            {
              html: '<FONT class="">I walk everyday</FONT>',
            },
            {
              html: '<FONT class=""> You cry a lot</FONT>',
            },
            {
              html: '<FONT class="">They eat here </FONT>',
            },
            {
              html:
                '<FONT class="">I cough every now and then</FONT>',
            },
            {
              html:
                '<FONT class="" >I watch TV once in a blue moon</FONT>',
            },
            {
              html:
                '<FONT class="">I go for a run every morning</FONT>',
            },
            {
              html:
                '<FONT class="">We dance in the rain</FONT>',
            },
            {
              html:
                '<FONT class="">I brush my teeth twice a day </FONT> ',
            },
            {
              html:
                '<FONT class="">They speak English very slowly</FONT>',
            },
          ],
        },
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "html",
              label: "",
              thClass: "noHead",
            },
          ],
          items: [
            {
              html:
                '<FONT class="">ORACIÓN AFIRMATIVA EN PRESENTE (ESPAÑOL)</FONT>',
            },
            {
              html:
                '<FONT class="">Yo camino todos los días</FONT>',
            },
            {
              html: '<FONT class=""> Tu lloras mucho</FONT>',
            },
            {
              html: '<FONT class="">Ellos comen aquí </FONT>',
            },
            {
              html:
                '<FONT class="">Yo toso de vez en cuando</FONT>',
            },
            {
              html:
                '<FONT class="" >Yo veo televisión muy rara vez</FONT>',
            },
            {
              html:
                '<FONT class="">Yo voy a correr en la mañana</FONT>',
            },
            {
              html:
                '<FONT class="">Nosotros bailamos bajo la lluvia</FONT>',
            },
            {
              html:
                '<FONT class="">Me cepillo mis dientes dos veces al día </FONT>',
            },
            {
              html:
                '<FONT class="">Ellos hablan inglés muy despacio</FONT>',
            },
          ],
        },
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "html",
              label: "",

              thClass: "noHead",
            },
          ],
          items: [
            {
              html:
                "<FONT >Si el sujeto es HE, SHE o IT el verbo lleva la s, es o ies</FONT>",
            },
            {
              html:
                '<FONT class="">She walk<font class="text-danger">s </font>every day</FONT>',
            },
            {
              html:
                '<FONT class=""> He cr<font class="text-danger">ies</font> a lot</FONT>',
            },
            {
              html:
                '<FONT class="">The dog eat<font class="text-danger">s</font> here </FONT>',
            },
            {
              html:
                '<FONT class="">My mother cough<font class="text-danger">s</font> </FONT>',
            },
            {
              html:
                '<FONT class="">She watch<font class="text-danger">es</font> tv</FONT>',
            },

            {
              html:
                '<FONT class="">Nobody go<font class="text-danger">es</font> for a run every morning</FONT>',
            },
            {
              html:
                '<FONT class="">She danc<font class="text-danger">es</font> in the rain</FONT>',
            },
            {
              html:
                '<FONT class="">He brush<font class="text-danger">es</font> his teeth twice a day</FONT>',
            },
            {
              html:
                '<FONT class="">My teacher speak<font class="text-danger">s</font> </FONT>',
            },
          ],
        },
      ],
     

      tablaDosPag35: 
        {
          fields: [
                     { key: "html", thClass: "noHead" },
                    { key: "complejo1", label: "Z", thClass: "noHead" },
                    { key: "complejo2", lable: "Z", thClass: "noHead" }
          
          ],
          items: [
            {
              html:"  I walk everyday ",
              complejo1: { lista: ["Yo camino todos los días","camino todos los días"], tamano: 23,
               audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R19.mp3" },
           
              complejo2: {
                lista: ["walks"],
                tamano: 18,
                textoA: "He",
                textoD: "everyday",
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R20.mp3"
              },
            },
            {
              html:"You cry very much  ",
               complejo1: { lista: ["Tu lloras mucho","lloras mucho"], tamano: 23,
               audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R21.mp3" },
           
              complejo2: {
                lista: ["cries"],
                tamano: 19,
                textoA: "She",
                textoD: "very much",
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R22.mp3"
              },
            },
            {
              html:"They eat here ",
              complejo1: { lista: ["Ellos comen aquí"], tamano: 23,
              audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R23.mp3"
              },
           
              
              complejo2: {
                lista: ["chiken"],
                tamano: 19,
                textoA: "The",
                textoD: "eats here",
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R24.mp3"
              },
            
            },
            {
              html:"You cough every now and then ",
              complejo1: { lista: ["Tú toses de vez en cuando","toses de vez en cuando"], tamano: 23,
              audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R25.mp3"
              },
           
             complejo2: {
                lista: ["coughs"],
                tamano: 29,
                textoA: "The baby",
                textoD: "every now and then",
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R26.mp3"
              },
            },
              {
              html:"I watch TV once in a blue moon",
              complejo1: { lista: ["Yo veo TV rara vez","veo TV rara vez"], tamano: 23,
              audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R27.mp3"
              },
           
               complejo2: {
                lista: ["watches"],
                tamano: 29,
                textoA: "She",
                textoD: "TV once in a blue moon",
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R28.mp3"
              },
            },
              {
              html:"We take the kids to the school",
             complejo1: {
                lista: ["Nosotros llevamos los niños a la escuela"],
                tamano: 23,
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R29.mp3"
              },
           
             complejo2: {
                lista: ["takes"],
                tamano: 25,
                textoA: "He",
                textoD: "the kids to the school",
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R30.mp3"
              },
            },
              {
              html:"We dance in the rain",
              complejo1: {
                lista: ["Nosotros bailamos en la lluvia"],
                tamano: 23,
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R31.mp3"
              },
           
               complejo2: {
                lista: ["dances"],
                tamano: 18,
                textoA: "It",
                textoD: "in the rain",
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R32.mp3"
              },
            },
              {
              html:"I brush my teeth twice a day",
               complejo1: {
                lista: ["Me cepillo mis dientes dos veces al día","cepillo mis dientes dos veces al día"],
                tamano: 23,
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R33.mp3"
              },
           
              complejo2: {
                lista: ["brushes"],
                tamano: 25,
                textoA: "She",
                textoD: "her teeth twice a day",
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R34.mp3"
              },
              
            },
            {
              html:"They speak english very slowly",
                complejo1: {
                lista: ["Ellos hablan inglés muy lento"],
                tamano: 23,
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R35.mp3"
              },
           
              complejo2: {
                lista: ["speaks"],
                tamano: 25,
                textoA: "He",
                textoD: "English very slowly",
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R36.mp3"
              },
              
            },
            {
              html:"I walk everyday",
              complejo1: { lista: ["Yo camino todos los días","camino todos los días"], tamano: 23,
              audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R37.mp3"
              },
           
                complejo2: {
                lista: ["walks"],
                tamano: 21,
                textoA: "The dog",
                textoD: "everyday",
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R38.mp3"
              },
            },
            {
              html:"I love you",
              complejo1: { lista: ["Te amo"], tamano: 23,
              audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R39.mp3"
              },
           
              complejo2: {
                lista: ["loves"],
                tamano: 15,
                textoA: "She",
                textoD: "me",
                audio:"/cursos/curso1/leccion7/audios/page35/AC1P35R40.mp3"
              },
              
            },
           
          ],
        },
     
      frasesPag37: [
        " La palabra DO es un verbo que traduce Hacer, pero también es un auxiliar",
        "La tercera persona de DO es DOES, pero DOES también es un auxiliar.",
        "El pasado del verbo DO es DID, pero DID también es un Auxiliar",
        "La palabra HAVE es un verbo que traduce “tener”, pero también es un verbo con súper poder.",
        "La tercera persona de HAVE es HAS, pero Has también es un verbo con súper poder. ",
        "El pasado del verbo HAVE es HAD, pero HAD también es un ",
      ],

      frases2Pag37: [
        {
          lista1: ["has"],
          lista2: ["done"],
          textoA: "He ",
          textoD: "never",
          textoD2: "that.<strong> Él nunca ha hecho eso.</strong>",
          tamano1: 15,
          tamano2: 28,
           
          name: "ice",
          audio:"/cursos/curso1/leccion7/audios/page37/AC1P23R1.mp3",
        },
        {
          lista1: ["doesn't do"],

          textoA: "She",
          textoD: "anything. <strong>Ella no hace nada.</strong>",
          tamano: 33,
          name: "ic",
          audio:"/cursos/curso1/leccion7/audios/page37/AC1P23R2.mp3"
        },
        {
          lista1: ["had"],
          lista2: ["done"],
          textoA: "I",
          textoD: "already",
          textoD2: "that. <strong> Yo ya había hecho eso.</strong>",
          tamano1: 15,
          tamano2: 28,
          name: "ice",
          audio:"/cursos/curso1/leccion7/audios/page37/AC1P23R3.mp3"
        },
        {
          lista1: ["didn't do"],

          textoA: "I",

          textoD: "that. <strong> Yo no hice eso.</strong>",
          tamano: 25,
          name: "ic",
          audio:"/cursos/curso1/leccion7/audios/page37/AC1P23R4.mp3"
        },
        {
          lista1: ["did"],

          textoA: "I",
          tamano: 20,
          textoD: "that. <strong> Yo hice eso.</strong>",
          name: "ic",
          audio:"/cursos/curso1/leccion7/audios/page37/AC1P23R5.mp3"
        },
        {
          lista1: ["does"],
          tamano: 28,
          textoA: "She",

          textoD: "sports. <strong> Ella hace deporte.</strong>",
          name: "ic",
          audio:"/cursos/curso1/leccion7/audios/page37/AC1P23R6.mp3"
        },
        {
          lista1: ["didn't"],
          tamano: 40,
          textoA: "I",

          textoD: "have to work today.  <strong>Yo no tuve que trabajar hoy.</strong>",
          name: "ic",
          audio:"/cursos/curso1/leccion7/audios/page37/AC1P23R7.mp3"
        },
      ],

      cuestionario1Pag36: {
        fields: [
          {
            key: "A",
            thClass: "Yellow parrafoBlack",
            label: "Verbo en presente",
          },
          { key: "complejo1", label: "En tercera persona" },
          { key: "B", label: "Clase" },
          { key: "C", label: "Past and participle" },
        ],
        items: [
          {
            A: "I *Eat* pizza",
            complejo1: { lista: ["She eats pizza"], tamano: 20,
              audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R2.mp3"
            },
            B: "Irregular",
            C: "Ate – eaten",
          },
          {
            A: "I *Watch* tv",
            complejo1: { lista: ["She watches"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R4.mp3"
            },
            B: "Irregular",
            C: "Saw - Seen",
           
          },
          {
            A: "I *Smell* really good",
            complejo1: { lista: ["She smells really good"], tamano: 20,
            audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R6.mp3"
            },
            B: "Regular",
            C: "Smelled - smelled",
            
          },
          {
            A: "I *Spit* on the floor",
            complejo1: { lista: ["She spits on the floor"], tamano: 20,
            audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R8.mp3"
            },
            B: "Irregular",
            C: "Spat - spat",
            
          },
          {
            A: "I *Throw* the ball",
            complejo1: { lista: ["She throws the ball "], tamano: 20, 
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R10.mp3"
            },
            B: "Irregular",
            C: "Threw - thrown",
          },
          {
            A: "I *Push* the door",
            complejo1: { lista: ["She pushes the door"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R12.mp3"
            },
            B: "Regular",
            C: "Pushed - pushed",
          },
          {
            A: "I *Walk* with a limp",
            complejo1: { lista: ["She walks with a limp"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R14.mp3"
            },
            B: "Regular",
            C: "Walked - walked",
          },
          {
            A: "I *Think* of you",
            complejo1: { lista: ["She thinks of you"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R16.mp3"
            },
            B: "Irregular",
            C: "Thought- thought",
          },
          {
            A: "I *Call* the police",
            complejo1: { lista: ["She calls the police"], tamano: 20 ,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R18.mp3"
            },
            B: "Regular",
            C: "Called - called",
          },
          {
            A: "I *Breathe* quickly",
            complejo1: { lista: ["She breathes quicly"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R20.mp3"
            },
            B: "Regular",
            C: "Breathed- breathed",
          },
          {
            A: "I *Swallow* tablets",
            complejo1: { lista: ["She swallows tablets"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R22.mp3"
            },
            B: "Irregular",
            C: "Swallowed - swallowed",
          },
          {
            A: "I *Hear* birds",
            complejo1: { lista: ["She hears birds"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R24.mp3"
            },
            B: "Irregular",
            C: "Heards - heards",
          },
          {
            A: "I *Pry* to God",
            complejo1: { lista: ["She prays God"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R26.mp3"
            },
            B: "Regular",
            C: "Prayed - prayed",
          },
          {
            A: "I *Swear* to God",
            complejo1: { lista: ["She swears to God"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R28.mp3"
            },
            B: "Irregular",
            C: "Swore - sworn",
          },
          {
            A: "I *Scream* loudly",
            complejo1: { lista: ["She screams loudly"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R29.5.mp3"
            },
            B: "Regular",
            C: "Screamed - screamed",
          },
          {
            A: "I *Cry* a lot",
            complejo1: { lista: ["She cries a lot"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R31.mp3"
            },
            B: "Regular",
            C: "Cried - cried",
          },
          {
            A: "I *Swim* like a fish",
            complejo1: { lista: ["She swims like a fish"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R33.mp3"
            },
            B: "Irregular",
            C: "Swam - swum",
          },
          {
            A: "I *Wake up* at 5:45 am",
            complejo1: { lista: ["She wakes up at 5:45 am"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R35.mp3"
            },
            B: "Irregular",
            C: "Woke - woken",
          },
          {
            A: "I *Get up* at 6:00 am",
            complejo1: { lista: ["She gets up at 6:00 am"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R37.mp3"
            },
            B: "Irregular",
            C: "Got - gotten",
          },
          {
            A: "I *Dream* about engels",
            complejo1: { lista: ["She dreams about engels"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R39.mp3"
            },
            B: "Irregular",
            C: "Dreamt - dreamt",
          },
          {
            A: "I *Catch* the ball",
            complejo1: { lista: ["She catches the ball"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R41.mp3"
            },
            B: "Irregular",
            C: "Caught - caught",
          },
          {
            A: "I *Drive* a car",
            complejo1: { lista: ["She drives a car"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R43.mp3"
            },
            B: "Irregular",
            C: "Drove - driven",
          },
          {
            A: "I *Ride* a horse",
            complejo1: { lista: ["She rides a horse"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R45.mp3"
            },
            B: "Irregular",
            C: "Rode - ridden",
          },
          {
            A: "I *Write* a poem",
            complejo1: { lista: ["She writes a poem"], tamano: 20 ,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R47.mp3"
            },
            B: "Irregular",
            C: "Wrote - written",
          },
          {
            A: "I *Taste* the soup",
            complejo1: { lista: ["She tastes the soup"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R49.mp3"
            },
            B: "Regular",
            C: "Tasted - tasted",
          },
          {
            A: "I *Touch* my nose",
            complejo1: { lista: ["She touches my nose"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R51.mp3"
            },
            B: "Regular",
            C: "Touched - touched",
          },
          {
            A: "I *Pick up* the pencil",
            complejo1: { lista: ["She picks up the pencil"], tamano: 20,
             audio:"/cursos/curso1/leccion7/audios/page36/AC1P36R53.mp3"
            },
            B: "Regular",
            C: "Picked - picked",
          },
        ],
      },
    };
  },
};
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

/deep/ .Subrayado {
  text-decoration-line: underline;
}

inputChecked {
  display: inline-flex;
}
.BigCelda {
  height: 90px;
}
.BigCeldaDos {
  height: 120px;
}
/deep/ .row{
  margin-left: 0%;
  margin-right: 0%;
}
</style>