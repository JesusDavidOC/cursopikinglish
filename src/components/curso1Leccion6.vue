<template>
  <div>
    <div class="row container">
      <div class="col-md-1"></div>
      <b-col md="10" class="titulo">
        <h3>FORMA PRESENTE DEL VERBO</h3>
      </b-col>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7">
        <img src="https://classroom.pikinglish.com/cursos/curso1/leccion6/imagenes/tablaPag32.png" />
      </div>
    </div>

    <div class="row botTabla">
      <div class="col-sm-1"></div>
      <div class="col-sm-2" v-for="item in $data.tablaUnoPag32">
        <listaIndex :tabla="item" />
      </div>
      <div class="col-sm-1"></div>
      <div class="col-sm-3" style="margin-top: auto; margin-bottom: auto">
        <p class="parrafo">
          Si el sujeto es HE, SHE O IT el verbo lleva la letra “s” al final o
          algunas veces lleva la “es” o la “ies”.
        </p>
      </div>
    </div>
<b-row>
   
      <b-col md="10" >
        <p class="subTitulo marginn-left">
          REGLAS DEL LOS VERBOS EN PRESENTE AFIRMATIVO
        </p>
         
        </b-col>
</b-row>
    

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-2" v-for="item in $data.tablaDosPag32">
        <listaIndex :tabla="item" class="botTabla" />
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond marginn-left" style="font-size: 1.5em"></i>

      <p class="fuenteDiamond">
        Escribe la forma presente para terceras personas.
      </p>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-4">
        <tablaTC
          class="overflow-auto botTabla"
          :cuestionario="tablaTresPag32"
          
        />
      </div>
      
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond" style="font-size: 1.5em"></i>

      <p class="fuenteDiamond">
        Reemplaza los números por letras y utiliza el verbo en su forma
        correcta.
      </p>
    </div>

    <div class="row botTabla">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div class="col-sm-2">
          <listaIndex :tabla="$data.tablaAPag33" class="botTabla" />
        </div>
        <div class="col-sm-2">
          <listaIndex :tabla="$data.tablaBPag33" class="botTabla" />
        </div>

        <div class="col-sm-2">
          <listaIndex :tabla="$data.tablaCPag33" class="botTabla" />
        </div>

        <div class="col-sm-3">
          <listaIndex :tabla="$data.tablaDPag33" class="botTabla" />
        </div>
      </div>
    </div>

    <div class="row botTabla">
      <div class="col-sm-1"></div>
      <div class="col-md-auto">
        <tablaTC
          :cuestionario="$data.cuestionario1Pag33"
          :inglesR="false"
          :espanolR="true"
          style="padding: 0%"
          class=""
        />
      </div>
    </div>
    <br />
    <br />
    <br />
    <div class="row">
      <div class="col-sm-1"></div>
      <i class="fa fa-diamond marginn-left" style="font-size: 1.5em"></i>

      <p class="fuenteDiamond">
        Add the S, ES or IES to the verb if necessary.
      </p>
    </div>
  <b-row>
   
      <b-col md="10" >
        <p class="subTitulo marginn-left">
          DICTIONARY
        </p>
         
        </b-col>
</b-row>
    
    

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-0.9" v-for="item in $data.tablaUnoPag34">
        <listaIndex :tabla="item" class="botTabla" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <FONT class="">
        <div class="col-sm-11" id>
          <inputChecked
            :resuelto="false"
            :esperado="['works']"
            :tamano="48"
            :conTexto="true"
            textoA="1. Ella trabaja muy duro todos los días: She"
            textoD="very hard every day."
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :resuelto="false"
            :esperado="['live']"
            :tamano="39"
            :conTexto="true"
            textoA="2. Yo vivo con mi Madre acá: I"
            textoD="with my mother here."
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :resuelto="false"
            :conTexto="true"
            :tamano="55"
            :esperado="['has']"
            textoA="3. Él tiene que trabajar mañana en la mañana: He"
            textoD="to work tomorrow morning."
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :conTexto="true"
            :resuelto="false"
            :tamano="47"
            :esperado="['does']"
            textoA="4. Natalie hace deporte todos los días: Natalie"
            textoD="sports every day."
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :conTexto="true"
            :resuelto="false"
            :tamano="34"
            textoA=" 5. Yo voy a trabajar en bus: I"
            textoD="to work by bus."
            :esperado="['go']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :conTexto="true"
            :tamano="38"
            textoA="6. Ella va al colegio a pie: She"
            textoD="to school on foot."
            :resuelto="false"
            :esperado="['goes']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :conTexto="true"
            :tamano="39"
            textoA="7. Llueve mucho en New York: It"
            textoD="a lot in New York."
            :resuelto="false"
            :esperado="['rains']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :conTexto="true"
            :tamano="32"
            textoA="8. Amar tiene sentido: Loving"
            textoD="sense."
            :resuelto="false"
            :esperado="['makes']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :tamano="41"
            :conTexto="true"
            :resuelto="false"
            textoA="9. Él tiene que trabajar mañana: He"
            textoD="to work tomorrow."
            :esperado="['has']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            textoA="10. Mi novia mira televisión los sábados: My girlfriend"
            textoD="tv on Saturdays."
            :tamano="53"
            :resuelto="false"
            :conTexto="true"
            :esperado="['watches']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :conTexto="true"
            :resuelto="false"
            :tamano="29"
            textoA="11. Ella tiene un carro: She"
            :esperado="['has']"
            textoD="a car."
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :conTexto="true"
            :resuelto="false"
            :tamano="36"
            textoA="12. Ella no tiene un carro: She doesn’t"
            textoD="a car."
            :esperado="['have']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :resuelto="false"
            :conTexto="true"
            :tamano="37"
            textoA="13. Víctor llora todos los días: Victor"
            textoD="everyday."
            :esperado="['cries']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :conTexto="true"
            textoA="14. El gato tiene cuatro patas: The cat"
            :resuelto="false"
            textoD="four paws."
            :esperado="['has']"
            :tamano="38"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :resuelto="false"
            :conTexto="true"
            textoA="15. Mi mamá me ama: My mother"
            textoD="me."
            :tamano="32"
            :esperado="['loves']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :resuelto="false"
            :conTexto="true"
            textoA="16. El profesor enseña muy bien: The teacher"
            textoD="very well."
            :tamano="44"
            :esperado="['teaches']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :resuelto="false"
            :conTexto="true"
            textoA="17. Eso huele mal: That"
            textoD="bad."
            :tamano="28"
            :esperado="['smells']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :resuelto="false"
            :conTexto="true"
            textoA="18. Ese niño estudia inglés: That boy"
            textoD="English."
            :tamano="38"
            :esperado="['studies']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :resuelto="false"
            :conTexto="true"
            textoA=" 19. Él ama el número mágico: He"
            textoD="the magic number."
            :tamano="41"
            :esperado="['loves']"
          />
          <br />
          <br />
        </div>
        <div class="col-sm-11">
          <inputChecked
            :resuelto="false"
            :conTexto="true"
            textoA=" 20. Él tiene que madrugar: He"
            textoD="to wake up early."
            :tamano="37"
            :esperado="['has']"
          />
          <br />
          <br />
        </div>
      </FONT>
    </div>
    <br />
    <br />
    <br />
  </div>
</template>
<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
import inputCE from "./inputCEnriquecido";

import tablaTC from "./tablaTraduccionCodigos";
export default {
  components: {
    listaIndex,
    inputChecked,
    inputCE,
    tablaTC,

    posiblesRespuestasTabla,
    tablaTC,
  },
  data() {
    return {
      tablaUnoPag32: [
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html: '<FONT class=" ">I</FONT>',
            },
            {
              html: '<FONT class="">YOU</FONT>',
            },
            {
              html: '<FONT class=" ">WE  </FONT>',
            },
            {
              html: '<FONT class=" ">THEY</FONT>',
            },
            {
              html: '<FONT class=" " ><strong>SHE</strong></FONT>',
            },
            {
              html: '<FONT class=" "><strong>IT</strong></FONT>',
            },
            {
              html: '<FONT class=" "><strong>HE</strong></FONT>',
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
              html: '<FONT class=" ">SEE</FONT>',
            },
            {
              html: '<FONT class="">SEE</FONT>',
            },
            {
              html: '<FONT class=" ">SEE</FONT>',
            },
            {
              html: '<FONT class=" ">SEE</FONT>',
            },
            {
              html: '<FONT class=" "><strong>SEES</strong></FONT>',
            },
            {
              html: '<FONT class=" "><strong>SEES</strong></FONT>',
            },
            {
              html: '<FONT class=" "><strong>SEES</strong></FONT>',
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
              html: '<FONT class=" ">Yo veo</FONT>',
            },
            {
              html: '<FONT class=" ">Tu ves</FONT>',
            },
            {
              html: '<FONT class="">Nosotros vemos</FONT>',
            },
            {
              html: '<FONT class=" ">Ellos ven</FONT>',
            },
            {
              html: '<FONT class=" "><strong>Ella ve</strong></FONT>',
            },
            {
              html: '<FONT class=" "><strong>Ve</strong></FONT>',
            },
            {
              html: '<FONT class=" "><strong>El ve</strong></FONT>',
            },
          ],
        },
      ],
      tablaDosPag32: [
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html: '<FONT class=" "><strong>SHE______</strong></FONT>',
            },
            {
              html: '<FONT class=" "><strong>HE______</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>IT______</strong></FONT>',
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
                '<FONT ><strong>Verbos terminados en<br><FONT class=" text-danger"> o, x, s, sh, ch, z </FONT>se<br>le agrega</strong></FONT><br><br>',
            },

            {
              html:
                '<FONT  class="text-danger  p-2   bg-warning"><strong> ES </strong></FONT>',
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
                '<FONT class=" "><strong>Verbos terminados en <FONT class="text-danger">Y</FONT><br>precedida de consonante<br>se cambia la y por <FONT class="text-danger">i</FONT> más<br><FONT class="text-danger ">es</FONT><br></strong></FONT>',
            },

            {
              html:
                '<FONT class="text-danger  p-2   bg-warning"><strong> IES </strong></FONT>',
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
                '<FONT class=""><strong>Los demás<br>verbos se les<br>agrega la <br><FONT class="text-danger ">s</FONT><br></strong></FONT>',
            },

            {
              html:
                '<FONT  class=" text-danger  p-2   bg-warning"><strong> S </strong></FONT>',
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
                '<FONT class=" "><strong>Y “have” se<br>convierte en<br>“has”<br><br></strong></FONT>',
            },

            {
              html:
                '<FONT  class="text-danger  p-2   bg-warning"><strong> HAS </strong></FONT>',
            },
          ],
        },
      ],

      tablaTresPag32: {
        fields: [
          { key: "A", label: "A", thClass: "noHead" },
          { key: "complejo1", label: "A", thClass: "noHead" },
        ],
        items: [
          {
            A: "I go",
            complejo1: {
              textoA: "She",
              lista: ["goes"],
              tamano: 13,
            },
          },

          {
            A: "We have",
            complejo1: {
              textoA: "Victor",
              lista: ["has"],
              tamano: 13,
            },
          },

          {
            A: "They cry",

            complejo1: {
              textoA: "She",
              lista: ["cries"],
              tamano: 13,
            },
          },
          {
            A: "You play",
            complejo1: {
              textoA: "He",
              lista: ["plays"],
              tamano: 13,
            },
          },
          {
            A: "I watch",
            complejo1: {
              textoA: "She",
              lista: ["watches"],
              tamano: 15,
            },
          },
          {
            A: "We study",
            complejo1: {
              textoA: "The boy",
              lista: ["studies"],
              tamano: 17,
            },
          },
          {
            A: "I do",
            complejo1: {
              textoA: "My sister",
              lista: ["does"],
              tamano: 14,
            },
          },
        ],
      },

      tablaAPag33: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "A", thClass: "Blue  " },
        ],

        items: [
          { A: " I" },
          { A: " YOU " },
          { A: " SHE" },
          { A: " HE" },
          { A: " IT" },
          { A: " WE" },
          { A: " THEY" },
        ],
      },

      tablaBPag33: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "B", thClass: "Red " },
        ],
        items: [
          { B: " go/goes" },
          { B: " have / has" },
          { B: " cry/ cries" },
          { B: " watch / watches" },
          { B: " buy / buys" },
          { B: " do / does" },
          { B: " work / works" },
          { B: " eat / eats" },
          { B: " stay / stays" },
        ],
      },
      tablaCPag33: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "C", thClass: "Yelow " },
        ],

        items: [
          { C: " there" },
          { C: " to admit" },
          { C: " movies" },
          { C: " a lot" },
          { C: " what" },
          { C: " here" },
          { C: " healthy" },
          { C: " sport" },
        ],
      },
      tablaDPag33: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "D", thClass: "Green " },
        ],

        items: [
          { D: " on Sundays" },
          { D: " it" },
          { D: " that" },
          { D: " everyday" },
          { D: " from time to time" },
          { D: " at night" },
          { D: " I want" },
          { D: " from Monday to Friday" },
          { D: " in the morning" },
        ],
      },
      cuestionario1Pag33: {
        fields: [
          { key: "A", thClass: "Blue parrafo" },
          { key: "B", thClass: "Red parrafo" },
          { key: "C", thClass: "Yelow parrafo" },
          { key: "D", thClass: "Green parrafo" },
          { key: "complejo1", label: "ENGLISH", thClass: "" },
          { key: "E", label: "SPANISH" },
        ],
        items: [
          {
            A: 1,
            B: 1,
            C: 1,
            D: 1,
            complejo1: { lista: ["I go there on sundays"], tamano: 25 },
            E: "Voy allá los domingos",
          },
          {
            A: 3,
            B: 2,
            C: 2,
            D: 2,
            complejo1: { lista: ["She has to admit it"], tamano: 25 },
            E: "Ella tiene que admitirlo",
          },
          {
            A: 6,
            B: 7,
            C: 6,
            D: 4,
            complejo1: { lista: ["We work here everyday"], tamano: 25 },
            E: "Nosotros trabajamos aquí todos los días",
          },
          {
            A: 1,
            B: 6,
            C: 8,
            D: 9,
            complejo1: { lista: ["I do sport in the morning"], tamano: 25 },
            E: "Yo hago deporte en la mañana",
          },
          {
            A: 4,
            B: 4,
            C: 3,
            D: 6,
            complejo1: { lista: ["He watches movies at night "], tamano: 25 },
            E: "Él ve películas en la noche",
          },
          {
            A: 2,
            B: 9,
            C: 1,
            D: 8,
            complejo1: {
              lista: ["You stay there from Monday to Friday"],
              tamano: 25,
            },
            E: "Tú te quedas allá de lunes a viernes",
          },
          {
            A: 1,
            B: 8,
            C: 4,
            D: 4,
            complejo1: { lista: ["I eat a lot everyday "], tamano: 25 },
            E: "Yo como mucho todos los días",
          },
          {
            A: 3,
            B: 6,
            C: 5,
            D: 7,
            complejo1: { lista: ["She does what I want"], tamano: 25 },
            E: "Ella hace lo que yo quiera",
          },
          {
            A: 7,
            B: 8,
            C: 7,
            D: 9,
            complejo1: {
              lista: ["They eat healthy in the morning"],
              tamano: 25,
            },
            E: "Ellos comen saludable en la mañana",
          },
          {
            A: 3,
            B: 5,
            C: 6,
            D: 5,
            complejo1: {
              lista: ["She buys here from time to time"],
              tamano: 25,
            },
            E: "Ella compra aquí de vez en cuando",
          },
          {
            A: 4,
            B: 4,
            C: 3,
            D: 1,
            complejo1: { lista: ["He watches movies on Sundays"], tamano: 25 },
            E: "Él ve películas los domingos",
          },
          {
            A: 7,
            B: 7,
            C: 4,
            D: 4,
            complejo1: { lista: ["They work a lot everyday"], tamano: 25 },
            E: "Ellos trabajan mucho todos los días",
          },
          {
            A: 1,
            B: 2,
            C: 2,
            D: 3,
            complejo1: { lista: ["I have to admit that"], tamano: 25 },
            E: "Yo tengo que admitir eso",
          },
          {
            A: 1,
            B: 8,
            C: 5,
            D: 7,
            complejo1: { lista: ["I eat what I want"], tamano: 25 },
            E: "Yo como lo que yo quiero",
          },
          {
            A: 3,
            B: 3,
            C: 4,
            D: 6,
            complejo1: { lista: ["She cries a lot at night"], tamano: 25 },
            E: "Ella llora mucho en la noche",
          },
        ],
      },
      tablaUnoPag34: [
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
                '<FONT  class="  p-2 bg-warning"><strong>Work</strong></FONT>',
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
                '<FONT  class="p-2 bg-warning"><strong>Have</strong></FONT>',
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
              html:
                '<FONT  class="  p-2 bg-warning"><strong>Do</strong></FONT>',
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
              html: '<FONT  class="p-2 bg-warning "><strong>Go</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Ir</strong></FONT>',
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
                '<FONT class="p-2 bg-warning "><strong>Rain</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Llover</strong></FONT>',
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
                '<FONT class="p-2 bg-warning "><strong>Watch</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Mirar</strong></FONT>',
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
                '<FONT class="p-2 bg-warning "><strong>Love</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Amar</strong></FONT>',
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
                '<FONT class="p-2 bg-warning"><strong>Teach</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Enseñar</strong></FONT>',
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
                '<FONT  class="p-2 bg-warning "><strong>Smell</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Oler</strong></FONT>',
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
                '<FONT  class="p-2 bg-warning"><strong>Study</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>Estudiar</strong></FONT>',
            },
          ],
        },
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
#centrar {
  padding-right: 50%;
  padding-left: 50%;
}

#inputText {
  text-align: left;
}

/deep/ .Blue {
  background-color: cornflowerblue;
}
/deep/ .Red {
  background-color: crimson;
}
/deep/ .Yelow {
  background-color: yellow;
}
/deep/ .ancho {
  width: 400px;
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