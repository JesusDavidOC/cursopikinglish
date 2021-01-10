<template>
  <div>
    <div class="row container">
      <div class="col-md-1"></div>
      <b-col md="10" class="titulo" style="margin-bottom:2em;">
        <h3>FORMA PRESENTE CON AUXILIARES NEGATIVOS</h3>
      </b-col>
    </div>
   
    

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaAPag38" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaBPag38" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaCPag38" />
        </div>
        <div class="col-sm-2 botTabla" id="tabla">
          <listaIndex :tabla="$data.tablaDPag38" />
        </div>
      </div>
    </div>

    <br />

    <div class="row">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond " style="font-size: 1.5em"></i>

      <p class=" fuenteDiamond">
        
        Un verbo también se usa en su forma presente después de un
          auxiliar.
      </p>
      <br />
    </div>
    <div class="row">
      <div class="col-sm-2"></div>
       <img src="/cursos/curso1/leccion8/imagenes/tablaPag38.png" />

    </div>
   
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="fuenteDiamond">
        Existen cinco maneras de preguntar y negar en inglés
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-9">
        <tablaTC
          class="overflow-auto botTabla"
          :cuestionario="tabla1P38"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond marginn-left" style="font-size: 1.5em"></i>

      <p class="fuenteDiamond">
       
        Ubique el auxiliar negativo en las siguientes oraciones.
      </p>
     
    </div>

    <div class="row ">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 ">
        <div
          v-for="(item, index) in frases1Pag38"
          
          style="margin-bottom: 0.5em"
        >
          <inputChecked
            :esperado="item.esperado"
            :resuelto="false"
            :name="'P21-' + index"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :conTexto="true"
            :tamano="item.tamano"
            :audio="item.audio"
          />
        </div>
      </div>
    </div>
      <br><br><br>

       <div class="row container">
      <div class="col-md-1"></div>
      <b-col md="10" class="titulo" style="margin-bottom:2em;">
        <h3>AUXILIARES NEGATIVOS</h3>
      </b-col>
    </div>
   
    <div class="row">
      <div class="col-sm-1"></div>
      <p class="parrafo">
        Recuerde que un verbo se usa en su forma presente por lógica en presente
        o después de un auxiliar.
      </p>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <div class="col-sm-2 " id="tabla">
          <listaIndex :tabla="$data.tablaAPag39" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaBPag39" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaCPag39" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaDPag39" />
        </div>
        <div class="col-sm-2" id="tabla">
          <listaIndex :tabla="$data.tablaEPag39" />
        </div>
      </div>
    </div>

    <br />
    <div class="row">
      <div class="col-sm-1 row"></div>
      <div class="col-sm-8">
        <ul>
          <li
            v-for="item in frasesPag39"
            v-html="item"
            class="text-left parrafo"
          ></li>
        </ul>
      </div>
    </div>
    <br /><br /><br />

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <div class="col-sm-1 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tabla2APag39" />
        </div>
        <div class="col-sm-1 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tabla2BPag39" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tabla2CPag39" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tabla2DPag39" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tabla2EPag39" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tabla2FPag39" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tabla2GPag39" />
        </div>
      </div>
    </div>
    <br />
    <br />
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10"> <p class="parrafo ">
        Los auxiliares se usan para preguntar y negar, así que lo más importante
        es usar el correcto y recuerde que Does se usa para preguntar con she,
        he, it en presente y doesn´t para negar.
      </p></div>
     
    </div>
    <br /><br /><br />
    <div class="row">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond marginn-left" style="font-size: 1.5em"></i>

      <p class="fuenteDiamond">
       
        Escribe el auxiliar negativo
      </p>
      <br />
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-8 ">
        <div
          v-for="(item, index) in frases2Pag39"
          
          style="margin-bottom: 0.5em"
        >
          <inputChecked
            :esperado="item.esperado"
            :resuelto="false"
            :name="'P39-' + index"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :conTexto="true"
            :tamano="item.tamano"
            :audio="item.audio"
          />
        </div>
      </div>
    </div>
    <br /><br /><br />
<b-row>
   
      <b-col md="10" >
        <p class="subTitulo marginn-left">
          DICTIONARY
        </p>
         
        </b-col>
</b-row>
    

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-0.9" v-for="item in $data.tablaUnoPag40">
        <listaIndex :tabla="item" />

        <br />
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <p class="parrafo ">
        Write the corresponding letter in front of the Spanish phrase.
      </p>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-md-auto">
        <div
          v-for="(item, index) in frases1Pag40"
          
          style="margin-bottom: 0.5em"
        >
          <inputChecked
            :esperado="item.esperado"
            :resuelto="false"
            :name="'P40-' + index"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :conTexto="true"
            :tamano="item.tamano"
            :audio="item.audio"
          />
        </div>
      </div>
      <div class="col-md-auto">
        <p
          v-for="item in frases2Pag40"
          v-html="item"
          class="text-left parrafo ' '"
        ></p>
      </div>
    </div>
    <img src="/cursos/curso1/leccion8/imagenes/tablaPag40.png" />
    <br><br><br>
   
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
        tablaAPag38: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "A", thClass: "Yellow Subrayado", label: "PRESENT" },
        ],

        items: [],
      },

      tablaBPag38: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "PAST", thClass: "Subrayado" },
        ],
        items: [],
      },

      tablaCPag38: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "PARTICIPE", thClass: " Subrayado" },
        ],
        items: [],
      },

      tablaDPag38: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "PROGRESSIVE", thClass: " Subrayado" },
        ],
        items: [],
      },

      tabla1P38: {
        fields: [
          { key: "Z", label: "1.", thClass: "noHead" },
          { key: "A", label: "A", thClass: "noHead" },
          { key: "complejo1", label: "A", thClass: "noHead" },
          { key: "B", label: "A", thClass: "noHead" },
          { key: "complejo2", label: "A", thClass: "noHead" },
        ],
        items: [
          {
            Z: "1.",
            A: "Do you eat?",
            complejo1: { lista: ["¿Tú comes?","¿comes?"], tamano: 18,
            audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R1.mp3",
            },
            B: "I don't eat",
            complejo2: { lista: ["Yo no como","no como"], tamano: 18,
             audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R2.mp3",
            },
          },
          {
            Z: "2.",
            A: "Did you eat?",
            complejo1: { lista: ["¿Tú comiste?","¿comiste?"], tamano: 18,
             audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R3.mp3",
            },
            B: "I didn´t eat",
            complejo2: { lista: ["Yo no comí","no comí"], tamano: 18,
             audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R4.mp3",
            },
          },
          {
            Z: "3.",
            A: "Will you eat?",
            complejo1: { lista: ["¿Tú comerás?","¿comerás?"], tamano: 18,
             audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R5.mp3",
            },
            B: "I won't eat",
            complejo2: { lista: ["Yo no comeré","no comeré"], tamano: 18,
             audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R6.mp3",
            },
          },
          {
            Z: "4.",
            A: "Would you eat?",
            complejo1: { lista: ["¿Tú comerías?","¿comerías?"], tamano: 18,
             audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R7.mp3",
            },
            B: "I wouldn't eat",
            complejo2: { lista: ["Yon no comería","no comería"], tamano: 18,
             audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R8.mp3",
            },
          },
          {
            Z: "5",
            A: "Does she it?",
            complejo1: { lista: ["¿Ella come?"], tamano: 18,
             audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R9.mp3",
            },
            B: "She doesn't eat",
            complejo2: { lista: ["Ella no come"], tamano: 18 ,
             audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R10.mp3",
            },
          },
        ],
      },

      frases1Pag38: [
        {
          esperado: ["didn't"],
          textoA: "1. I ",
          tamano: 29,
          textoD: "understand. <strong>(Yo no entendí) </strong>",
           audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R11.mp3",
        },

        {
          esperado: ["doesn't "],
          textoA: "2. She",
          tamano: 33,
          textoD: "live here. <strong>(Ella no vive aquí)</strong>",
           audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R12.mp3",
        },
        {
          esperado: ["won't"],
          textoA: "3. You",
          tamano: 34,
          textoD: "understand. <strong>(Tú no entenderías)</strong>",
           audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R13.mp3",
        },
        {
          esperado: ["don't"],
          textoA: "4. I",
          tamano: 26,
          textoD: " care. <strong>(No me importa)</strong>",
           audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R14.mp3",
        },
        {
          esperado: ["won't"],
          textoA: "5. They",
          tamano: 36,
          textoD: "say anything.<strong> (Ellos no dirán nada)</strong>",
           audio:"/cursos/curso1/leccion8/audios/page38/AC1P38R15.mp3",
        },
      ],
      tablaAPag39: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "A", thClass: "text-primary", label: "Don´t" },
        ],

        items: [],
      },

      tablaBPag39: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "Doesn´t", thClass: "text-primary" },
        ],
        items: [],
      },

      tablaCPag39: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "Didn´t", thClass: "text-primary" },
        ],
        items: [],
      },

      tablaDPag39: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "Won´t", thClass: " text-primary" },
        ],
        items: [],
      },

      tablaEPag39: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "Wouldn´t", thClass: " text-primary" },
        ],
        items: [],
      },
      frasesPag39: [
        "El <FONT class='text-danger'> don’t </FONT>es el no para un verbo en presente",
        "El <FONT class='text-danger'>doesn´t </FONT>es el no para un verbo en presente y solo se usa con she, he, it",
        "El <FONT class='text-danger'>didn´t </FONT>es el no para un verbo en pasado",
        "El <FONT class='text-danger'>won´t </FONT>es el no para un verbo en futuro",
        " El <FONT class='text-danger'>wouldn´t </FONT>es el no para un verbo que termine en “ría”",
      ],
      tabla2APag39: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "A", thClass: "Yellow", label: "PRESENT" },
        ],

        items: [],
      },

      tabla2BPag39: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "B", thClass: "", label: "I GO" },
        ],
        items: [],
      },

      tabla2CPag39: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "C", thClass: "", label: "I don't go" },
        ],
        items: [{ C: "Yo no voy" }],
      },

      tabla2DPag39: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "D", thClass: " ", label: "She doesn’t go" },
        ],
        items: [{ D: "Ella no va" }],
      },

      tabla2EPag39: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "E", thClass: " ", label: "I didn´t go" },
        ],
        items: [{ E: "Yo no fui " }],
      },
      tabla2FPag39: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "F", label: "I won´t go" },
        ],
        items: [{ F: "Yo no iré" }],
      },
      tabla2GPag39: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "G", thClass: " ", label: "I wouldn´t go" },
        ],
        items: [{ G: "Yo no iría" }],
      },
      frases2Pag39: [
        {
          esperado: ["didn't"],
          textoA: "1. I ",
          tamano: 29,
          textoD: "understand. <strong>(Yo no entendí)</strong>",
          audio:"/cursos/curso1/leccion8/audios/page39/AC1P39R1.mp3"
        },

        {
          esperado: ["doesn't "],
          textoA: "2. She",
          tamano: 32,
          textoD: "live here. <strong>(Ella no vive aquí)</strong>",
          audio:"/cursos/curso1/leccion8/audios/page39/AC1P39R2.mp3"
        },
        {
          esperado: ["wouldn't"],
          textoA: "3. You",
          tamano: 35,
          textoD: "understand. <strong>(Tú no entenderías)</strong>",
          audio:"/cursos/curso1/leccion8/audios/page39/AC1P39R3.mp3"
        },
        {
          esperado: ["don't"],
          textoA: "4. I",
          tamano: 26,
          textoD: " care. <strong>(No me importa)</strong>",
          audio:"/cursos/curso1/leccion8/audios/page39/AC1P39R4.mp3"
        },
        {
          esperado: ["won't"],
          textoA: "5. They",
          tamano: 36,
          textoD: "say anything. <strong>(Ellos no dirán nada)</strong>",
          audio:"/cursos/curso1/leccion8/audios/page39/AC1P39R5.mp3"
        },
        {
          esperado: ["don't"],
          textoA: "6. I",
          tamano: 38,
          textoD: "have any time. <strong>(No tengo nada de tiempo)</strong>",
          audio:"/cursos/curso1/leccion8/audios/page39/AC1P39R6.mp3"
        },
        {
          esperado: ["wouldn't"],
          textoA: "7. He",
          tamano: 31,
          textoD: "do that. <strong>(El no haría eso)</strong>",
          audio:"/cursos/curso1/leccion8/audios/page39/AC1P39R7.mp3"
        },
        {
          esperado: ["won't"],
          textoA: "8. We",
          tamano: 40,
          textoD: "say anything. <strong>(Nosotros no diremos nada)</strong>",
          audio:"/cursos/curso1/leccion8/audios/page39/AC1P39R8.mp3"
        },
        {
          esperado: ["doesn't"],
          textoA: "9. my father",
          tamano: 44,
          textoD: "speak english. <strong>(Mi padre no habla inglés)</strong>",
          audio:"/cursos/curso1/leccion8/audios/page39/AC1P39R9.mp3"
        },
        {
          esperado: ["didn't"],
          textoA: "10. I",
          tamano: 47,
          textoD: "understand what he said.<strong> (Yo no entendí lo que él dijo)</strong>",
          audio:"/cursos/curso1/leccion8/audios/page39/AC1P39R10.mp3"
        },
      ],

      tablaUnoPag40: [
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html:
                '<FONT  class="  p-2 bg-warning"><strong>Understand</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Entender</strong></FONT>',
            },
          ],
        },
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html:
                '<FONT  class="  p-2 bg-warning"><strong>Know</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Saber</strong></FONT>',
            },
          ],
        },
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html: '<FONT  class="p-2 bg-warning"><strong>Say</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Decir</strong></FONT>',
            },
          ],
        },
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html:
                '<FONT  class="  p-2 bg-warning"><strong>Live</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Vivir</strong></FONT>',
            },
          ],
        },
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html:
                '<FONT  class="p-2 bg-warning "><strong>Have</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Tener</strong></FONT>',
            },
          ],
        },
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html: '<FONT class="p-2 bg-warning "><strong>Do</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Hacer</strong></FONT>',
            },
          ],
        },
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html:
                '<FONT class="p-2 bg-warning "><strong>Make Sense</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Tener Sentido</strong></FONT>',
            },
          ],
        },
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html:
                '<FONT class="p-2 bg-warning "><strong>Work</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Trabajar</strong></FONT>',
            },
          ],
        },
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html:
                '<FONT  class="p-2 bg-warning "><strong>Cry</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Llorar</strong></FONT>',
            },
          ],
        },
      ],

      frases1Pag40: [
        {
          esperado: ["c"],
          textoA: "1. yo no entiendo nada ",
          tamano: 22,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R3.mp3"
          
        },

        {
          esperado: ["d"],
          textoA: "2. Ella no entendio nada",
          tamano: 23,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R4.mp3"
        },
        {
          esperado: ["b"],
          textoA: "3. Yo no entendí nada",
          tamano: 22,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R2.mp3"
        },
        {
          esperado: ["e"],
          textoA: "4. Yo no entendería nada",
          tamano: 23,
          textoD: " ",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R5.mp3"
        },
        {
          esperado: ["a"],
          textoA: "5. Yo no entenderé nada",
          tamano:23,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R1.mp3"
        },
        {
          esperado: ["g"],
          textoA: "6. No tiene sentido",
          tamano: 20,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R7.mp3"
        },
        {
          esperado: ["n"],
          textoA: "7. Él no trabajó hoy",
          tamano: 20,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R14.mp3"
        },
        {
          esperado: ["o"],
          textoA: "8. El niño no lloró",
          tamano: 19,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R15.mp3"
        },
        {
          esperado: ["m"],
          textoA: "9. yo no lo haré",
          tamano: 18,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R13.mp3"
        },
        {
          esperado: ["j"],
          textoA: "10. Nosotros no tendríamos ningún problema",
          tamano: 34,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R10.mp3"
        },
        {
          esperado: ["h"],
          textoA: "11. Yo no dije nada",
          tamano: 20,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R8.mp3"

        },
        {
          esperado: ["k"],
          textoA: "12. Él no fue a ninguna parte",
          tamano: 25,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R11.mp3"
        },
        {
          esperado: ["l"],
          textoA: "13. Yo no haría nada",
          tamano: 20,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R12.mp3"
        },
        {
          esperado: ["i"],
          textoA: "14. Ella no vive acá",
          tamano: 20,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R9.mp3"
        },
        {
          esperado: ["f"],
          textoA: "15. Yo no sé nada",
          tamano: 19,
          textoD: "",
          audio:"/cursos/curso1/leccion8/audios/page40/AC1P40R6.mp3"
        },
      ],
      frases2Pag40: [
        "a. I <FONT class='bg-warning '> won´t</FONT> understand anything",
        "b. I <FONT class='bg-warning'>didn´t</FONT> understand anything",
        "c. I <FONT class='bg-warning'>don’t</FONT> understand anything",
        "d. She <FONT class='bg-warning'>doesn’t</FONT> understand anything",
        "e. I <FONT class='bg-warning'>wouldn’t</FONT> understand anything",
        "f. I <FONT class='bg-warning'>don’t</FONT> know anything",
        "g. It <FONT class='bg-warning'>doesn’t</FONT> make sense",
        "h. I <FONT class='bg-warning'>didn’t</FONT> say anything",
        "i. She <FONT class='bg-warning'>doesn’t</FONT> live here",
        "j. We <FONT class='bg-warning'>wouldn’t</FONT> have any problem",
        "k. He <FONT class='bg-warning'>didn’t</FONT> go anywhere",
        "l. I <FONT class='bg-warning'>wouldn’t</FONT> do anything",
        "m. I <FONT class='bg-warning'>won´t</FONT> do it",
        "n. He <FONT class='bg-warning'>didn’t</FONT> work today",
        "o. The boy <FONT class='bg-warning'>didn’t</FONT> cry",
      ],
      
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
/deep/ .row{
  margin-left: 0%;
  margin-right: 0%;
}
</style>