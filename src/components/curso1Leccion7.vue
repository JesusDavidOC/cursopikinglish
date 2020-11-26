<template>
  <div>

       <div class="row ">
         <div class="col-sm-1"></div>
      <i class="fa fa-diamond " style="font-size: 1.5em"></i>

      <p class="fuenteDiamond">
        
        Escriba la traducción en ingles y completa las oraciones
        
      </p>
    </div>
    <div class="row"  style="padding: 0%;">
      <div class="col-sm-1"></div>
      <div class="col-sm-3"  style="padding: 0%;" v-for="item in $data.tablaUnoPag35">
        <listaIndex :tabla="item" 
         style="padding: 0%;"
        class=""/>
      </div>
    </div>

    <div class="row ">
      <div class="col-sm-1"></div>
      <div class="col-sm-3" style="padding: 0%;">
        <listaIndex :tabla="tablaDosAPag35" 
         style="padding: 0%;"
        class=""/>
        </div>
      <div class="col-sm-3 " style="padding:0%;" v-for="item in $data.tablaDosPag35">
        <tablaTC
          :cuestionario="item"
          class="botTabla"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
    </div>
    <div class="row ">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond " style="font-size: 1.5em"></i>

      <p class="fuenteDiamond">
       
        Aquí hay una lista de los verbos más fáciles del inglés. Reescribe
          las oraciones con “she”
       
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

    <div class="row overflow-auto ">
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

    <div class="row">
      <div class="col-sm-1"></div>
      <h3 class="titulo">LOS VERBOS GEMELOS DE LA LÓGICA DEL INGLÉS</h3>
    </div>
    
    <div class="row ">
      <div class="col-sm-1 "></div>
      <ul>
        <div class="botTabla">
        <li v-for="item in frasesPag37" class="parrafo ">
          {{ item }}
        </li>
        </div>
      </ul >
    </div>

    <div class="row ">
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
      <div class="col-sm-3 " id="tabla">
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

      <div class="col-sm-3 " id="tabla">
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
   
    <div class="row ">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond " style="font-size: 1.5em"></i>
      <p class=" fuenteDiamond">
        
        Practica llenado la tabla de los verbos gemelos.
      </p>
      
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-5">
        <p class="col-sm-12 bg-warning">
          <inputChecked
            style="width: 100%; padding: 0%;"
            :resuelto="false"
            :esperado="['Verbs']"
          />
        </p>
        <div class="row col-sm-12 parrafoBlack" id="tabla">
          <div class="col-sm-4"  style="padding: 0%;">
            <p class="text-center" style="padding: 0%;">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px; padding: 0%;"
                :resuelto="false"
                :esperado="['Present']"
              />
            </p>
            <p class="text-center  "  style="padding: 0%;">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Do-Does']"
              />
            </p>
            <p class="text-center ">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Have-Has']"
              />
            </p>
          </div>
          <div class="col-sm-4"  style="padding: 0%;">
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['past']"
              />
            </p>

            <p class="text-center ">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Did']"
              />
            </p>

            <p class="text-center ">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['Had']"
              />
            </p>
          </div>
          <div class="col-sm-4"  style="padding: 0%;">
            <p class="text-center">
              <inputChecked
                style="width: 100%; margin-left: 10px; margin-right: 10px"
                :resuelto="false"
                :esperado="['participle']"
              />
            </p>
            <p class="text-center ">
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
          <div class="col-sm-6"  style="padding: 0%;">
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
          <div class="col-sm-6"  style="padding: 0%;">
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

      <div class="col-sm-3 parrafoBlack " id="tabla" style="padding: 0%;">
        <p class="col-sm-12 bg-primary">
          <inputChecked
            style="width: 100%; margin-left: 10px; margin-right: 10px"
            :resuelto="false"
            :esperado="['S.P.V']"
          />
        </p>
        <div class="col-sm-12 " >
          <p class="text-center ">
            <inputChecked
              style="width: 100%; margin-left: 10px; margin-right: 10px"
              :resuelto="false"
              :esperado="['Los verbos con poder se pueden negar solos']"
            />
          </p>
        </div>
        <div class="row" style="items-aling: center">
          <div class="col-sm-6" style="padding: 0%;">
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
          <div class="col-sm-6" style="padding: 0%;">
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

    <div class="row  ">
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
              
            />
          </div>
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        
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
               html: '<FONT class=""><strong>ORACIÓN EN PRESENTE  AFIRMATIVO <br> (INGLÉS)</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>I walk everyday</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong> You cry a lot</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>They eat here </strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>I cough every now and then</strong></FONT>',
            },
            {
              html:
                '<FONT class="" ><strong>I watch TV once in a blue moon</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>I go for a run every morning</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>We dance in the rain</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>I brush my teeth twice a day </strong></FONT> ',
            },
            {
              html:
                '<FONT class=""><strong>They speak English very slowly</strong></FONT>',
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
                html: '<FONT class=""><strong>ORACIÓN AFIRMATIVA EN PRESENTE (ESPAÑOL)</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>Yo camino todos los días</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong> Tu lloras muchot</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Ellos comen aquí </strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>Yo toso de vez en cuando</strong></FONT>',
            },
            {
              html:
                '<FONT class="" ><strong>Yo veo televisión muy rara vez</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>Yo voy a correr en la mañana</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>Nosotros bailamos bajo la lluvia</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>Me cepillo mis dientes dos veces al día </strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>Ellos hablan inglés muy despacio</strong></FONT>',
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
              label:"",
              
              thClass: "noHead",
            },
          ],
          items: [
            {
              html :'<FONT ><strong>Si el sujeto es HE, SHE o IT elverbo lleva la s, es o ies</strong></FONT>', 
            },
            {
              html:
                '<FONT class=""><strong>She walk<font class="text-danger">s </font>every day</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong> He cr<font class="text-danger">ies</font> a lot</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>The dog eat<font class="text-danger">s</font> here </strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>My mother cough<font class="text-danger">s</font> </strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>She watch<font class="text-danger">es</font> tv</strong></FONT>',
            },

            {
              html:
                '<FONT class=""><strong>Nobody go<font class="text-danger">es</font> for a run every morning</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>She danc<font class="text-danger">es</font> in the rain</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>He brush<font class="text-danger">es</font> his teeth twice a day</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>My teacher speak<font class="text-danger">s</font> </strong></FONT>',
            },
          ],
        },
      ],
        tablaDosAPag35: 
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "html",
              
              thClass: "noHead fuenteComponentes",
            },
          ],
          items: [
            
             {
               html: '<FONT class=""><strong>I walk everyday </strong></FONT>',
            },
             {
               html: '<FONT class=""><strong>You cry very much </strong></FONT>',
            },
             {
               html: '<FONT class=""><strong>They eat here </strong></FONT>',
            },
            {
               html: '<FONT class=""><strong>You cough every now and then </strong></FONT>',
            },
             {
               html: '<FONT class=""><strong>I watch TV once in a blue moon</strong></FONT>',
            },
             {
               html: '<FONT class=""><strong>We take the kids to the school</strong></FONT>',
            },
             {
               html: '<FONT class=""><strong>We dance in the rain</strong></FONT>',
            },
             {
               html: '<FONT class=""><strong>I brush my teeth twice a day</strong></FONT>',
            },
             {
               html: '<FONT class=""><strong>They speak english very slowly</strong></FONT>',
            },
             {
               html: '<FONT class=""><strong>I walk everyday</strong></FONT>',
            },
             {
               html: '<FONT ><strong>I love you</strong></FONT>',
            },
            
              ],
        },
      

      tablaDosPag35: [
        {
        fields: [
          

          { key: "complejo1", label: "Z", thClass: "noHead" },
         
        ],
        items: [
          {
           
            complejo1: { lista: ["Yo camino todos los días"], tamano: 23 },
          
          },
          {
            complejo1: { lista: ["Tu lloras mucho"], tamano: 23 },
          },
          {
            complejo1: { lista: ["Ellos come aquí"], tamano: 23 },
          },{
            complejo1: { lista: ["Tú toses de vez en cuando"], tamano: 23 },
          },{
            complejo1: { lista: ["Yo veo TV rara vez"], tamano: 23 },
          },{
            complejo1: {
              lista: ["Nosotros llevamos los niños a la escuela"],
              tamano: 23,
            },
            
          },
          {
            complejo1: {
              lista: ["Nosotros bailamos en la lluvia"],
              tamano: 23,
            },
          },{
              complejo1: {
              lista: ["Me cepillo mis dientes dos veces al día"],
              tamano: 23,
            },
          },{
            complejo1: { lista: ["Ellos hablan inglés muy lento"], tamano: 23 },
          },{
            complejo1: { lista: ["Yo camino todos los días"], tamano: 23 },
          },{
            complejo1: { lista: ["Te amo"], tamano: 23 },
          }
        ]

      },{
        fields: [
          

          
          { key: "complejo2", lable: "Z", thClass: "noHead" },
        ],
        items: [
          {
           
            
            complejo2: {
              lista: ["walks"],
              tamano: 17,
              textoA: "He",
              textoD: "everyday",
            },
          },

          {
            
            
            complejo2: {
              lista: ["cries"],
              tamano: 18,
              textoA: "She",
              textoD: "very much",
            },
          },
          
          {
            
            
            complejo2: {
              lista: ["chiken"],
              tamano: 18,
              textoA: "The",
              textoD: "eats here",
            },
          },
         
          {
            
            
            complejo2: {
              lista: ["coughs"],
              tamano: 27,
              textoA: "The baby",
              textoD: "every now and then",
            },
          },
           
          {
            
            
            complejo2: {
              lista: ["watches"],
              tamano: 25,
              textoA: "She",
              textoD: "TV once in a blue moon",
            },
          },
          
          {
            
            
            complejo2: {
              lista: ["takes"],
              tamano: 23,
              textoA: "He",
              textoD: "the kids to the school",
            },
          },
          
          {
           
            
            complejo2: {
              lista: ["dances"],
              tamano: 17,
              textoA: "It",
              textoD: "in the rain",
            },
          },
          
          {
           
          
            complejo2: {
              lista: ["brushes"],
              tamano: 25,
              textoA: "She",
              textoD: "her teeth twice a day",
            },
          },
         
          {
            
            
            complejo2: {
              lista: ["speaks"],
              tamano: 23,
              textoA: "He",
              textoD: "English very slowly",
            },
          },
           
          {
            
            
            complejo2: {
              lista: ["walks"],
              tamano: 19,
              textoA: "The dog",
              textoD: "everyday",
            },
          },
          
          {
            
            
            complejo2: {
              lista: ["loves"],
              tamano: 13,
              textoA: "She",
              textoD: "me",
            },
          },
        ],
        }
      ],
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
          textoD2: "that. Él nunca ha hecho eso",
          tamano1:15,
          tamano2:27,
          
          name: "ice",
        },
        {
          lista1: ["doesn't do"],

          textoA: "She",
          textoD: "anything. Ella no hace nada.",
          tamano:29,
          name: "ic",
        },
        {
          lista1: ["had"],
          lista2: ["done"],
          textoA: "I",
          textoD: "already",
          textoD2: "that. Yo ya había hecho eso.",
          tamano1:15,
          tamano2:27,
          name: "ice",
        },
        {
          lista1: ["didn't do"],

          textoA: "I",

          textoD: "that. Yo no hice eso.",
          tamano:25,
          name: "ic",
        },
        {
          lista1: ["did"],

          textoA: "I",
          tamano:20,
          textoD: "that. Yo hice eso.",
          name: "ic",
        },
        {
          lista1: ["does"],
          tamano:28,
          textoA: "She",

          textoD: "sports. Ella hace deporte.",
          name: "ic",
        },
        {
          lista1: ["didn't"],
          tamano:39,
          textoA: "I",

          textoD: "have to work today. Yo no tuve que trabajar hoy.",
          name: "ic",
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
            complejo1: { lista: ["She eats pizza"], tamano: 20 },
            B: "Irregular",
            C: "Ate – eaten",
          },
          {
            A: "I *Watch* tv",
            complejo1: { lista: ["She watches"], tamano: 20 },
            B: "Irregular",
            C: "Saw - Seen",
          },
          {
            A: "I *Smell* really good",
            complejo1: { lista: ["She smells really good"], tamano: 20 },
            B: "Regular",
            C: "Smelled - smelled",
          },
          {
            A: "I *Spit* on the floor",
            complejo1: { lista: ["She spits on the floor"], tamano: 20 },
            B: "Irregular",
            C: "Spat - spat",
          },
          {
            A: "I *Throw* the ball",
            complejo1: { lista: ["She throws the ball "], tamano: 20 },
            B: "Irregular",
            C: "Threw - thrown",
          },
          {
            A: "I *Push* the door",
            complejo1: { lista: ["She pushes the door"], tamano: 20 },
            B: "Regular",
            C: "Pushed - pushed",
          },
          {
            A: "I *Walk* with a limp",
            complejo1: { lista: ["She walks with a limp"], tamano: 20 },
            B: "Regular",
            C: "Walked - walked",
          },
          {
            A: "I *Think* of you",
            complejo1: { lista: ["She thinks of you"], tamano: 20 },
            B: "Irregular",
            C: "Thought- thought",
          },
          {
            A: "I *Call* the police",
            complejo1: { lista: ["She calls the police"], tamano: 20 },
            B: "Regular",
            C: "Called - called",
          },
          {
            A: "I *Breathe* quickly",
            complejo1: { lista: ["She breathes quicly"], tamano: 20 },
            B: "Regular",
            C: "Breathed- breathed",
          },
          {
            A: "I *Swallow* tablets",
            complejo1: { lista: ["She swallows tablets"], tamano: 20 },
            B: "Irregular",
            C: "Swallowed - swallowed",
          },
          {
            A: "I *Hear* birds",
            complejo1: { lista: ["She hears birds"], tamano: 20 },
            B: "Irregular",
            C: "Heards - heards",
          },
          {
            A: "I *Pry* to God",
            complejo1: { lista: ["She prays God"], tamano: 20 },
            B: "Regular",
            C: "Prayed - prayed",
          },
          {
            A: "I *Swear* to God",
            complejo1: { lista: ["She swears to God"], tamano: 20 },
            B: "Irregular",
            C: "Swore - sworn",
          },
          {
            A: "I *Scream* loudly",
            complejo1: { lista: ["She screams loudly"], tamano: 20 },
            B: "Regular",
            C: "Screamed - screamed",
          },
          {
            A: "I *Cry* a lot",
            complejo1: { lista: ["She cries a lot"], tamano: 20 },
            B: "Regular",
            C: "Cried - cried",
          },
          {
            A: "I *Swim* like a fish",
            complejo1: { lista: ["She swims like a fish"], tamano: 20 },
            B: "Irregular",
            C: "Swam - swum",
          },
          {
            A: "I *Wake up* at 5:45 am",
            complejo1: { lista: ["She wakes up at 5:45 am"], tamano: 20 },
            B: "Irregular",
            C: "Woke - woken",
          },
          {
            A: "I *Get up* at 6:00 am",
            complejo1: { lista: ["She gets up at 6:00 am"], tamano: 20 },
            B: "Irregular",
            C: "Got - gotten",
          },
          {
            A: "I *Dream* about engels",
            complejo1: { lista: ["She dreams about engels"], tamano: 20 },
            B: "Irregular",
            C: "Dreamt - dreamt",
          },
          {
            A: "I *Catch* the ball",
            complejo1: { lista: ["She catches the ball"], tamano: 20 },
            B: "Irregular",
            C: "Caught - caught",
          },
          {
            A: "I *Drive* a car",
            complejo1: { lista: ["She drives a car"], tamano: 20 },
            B: "Irregular",
            C: "Drove - driven",
          },
          {
            A: "I *Ride* a horse",
            complejo1: { lista: ["She rides a horse"], tamano: 20 },
            B: "Irregular",
            C: "Rode - ridden",
          },
          {
            A: "I *Write* a poem",
            complejo1: { lista: ["She writes a poem"], tamano: 20 },
            B: "Irregular",
            C: "Wrote - written",
          },
          {
            A: "I *Taste* the soup",
            complejo1: { lista: ["She tastes the soup"], tamano: 20 },
            B: "Regular",
            C: "Tasted - tasted",
          },
          {
            A: "I *Touch* my nose",
            complejo1: { lista: ["She touches my nose"], tamano: 20 },
            B: "Regular",
            C: "Touched - touched",
          },
          {
            A: "I *Pick up* the pencil",
            complejo1: { lista: ["She picks up the pencil"], tamano: 20 },
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
</style>