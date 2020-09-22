<template>
  <div>
    <div class="row">
      <div class="col-sm-1"></div>
      <h3 class="titulo">FORMA PRESENTE DEL VERBO</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7">
        <img src="/cursos/curso1/leccion6/imagenes/img1.PNG" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-2" v-for="item in $data.tablaUnoPag32">
        <listaIndex :tabla="item" />
      </div>
      <div class="col-sm-1"></div>
      <div class="col-sm-3" style="margin-top:auto; margin-bottom:auto;">
        <p class="parrafoBlack">
          Si el sujeto es HE, SHE O IT el verbo lleva la letra “s” al final o algunas
          veces lleva la “es” o la “ies”.
        </p>
      </div>
    </div>
      
    <div class="row">
      <p class="parrafoBlack marginn-left">
        <i>
          <b>REGLAS DEL LOS VERBOS EN PRESENTE AFIRMATIVO</b>
        </i>
      </p>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-2" v-for="item in $data.tablaDosPag32">
        <listaIndex :tabla="item" />

        <br />
        <br />
        <br />
      </div>
    </div>
    <div class="row">
      <i class="fa fa-diamond marginn-left"></i>

      <p class="parrafoBlack marginn-left">
        &nbsp;
        <b>Escribe la forma presente para terceras personas.</b>
        <br />
      </p>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC
          class="overflow-auto"
          :cuestionario="tablaTresPag32"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <i class="fa fa-diamond marginn-left"></i>

      <p class="parrafoBlack marginn-left">
        &nbsp;
        <b>Reemplaza los números por letras y utiliza el verbo en su forma correcta.</b>
        <br />
      </p>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-8 row">
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaAPag33" />
        </div>
        <div class="col-sm-4 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaBPag33" />
        </div>

        <div class="col-sm-3 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaCPag33" />
        </div>

        <div class="col-sm-3 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaDPag33" />
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTraduccionCodigosDos
          :cuestionario="$data.cuestionario1Pag33"
          :inglesR="false"
          :espanolR="true"
        />
      </div>
    </div>
    <br />
    <br />
    <br />
    <div class="row">
      <i class="fa fa-diamond marginn-left"></i>

      <p class="parrafoBlack marginn-left">
        &nbsp;
        <b>Add the S, ES or IES to the verb if necessary.</b>
        <br />
      </p>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>

      <p class="parrafoBlack">
        <b>DICTIONARY</b>
        <br />
      </p>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-0.9" v-for="item in $data.tablaUnoPag34">
        <listaIndex :tabla="item" />

        <br />
        <br />
        <br />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <FONT class="text-left parrafoBlack">
        <div class="col-sm-11 row" id>
          1. Ella trabaja muy duro todos los días: She
          <inputChecked
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :resuelto="false"
            :esperado="['works']"
          />very hard every day.
          <br />
        </div>
        <div class="col-sm-11 row">
          2. Yo vivo con mi Madre acá: I
          <inputChecked
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :resuelto="false"
            :esperado="['live']"
          />with my mother here.
          <br />
        </div>
        <div class="col-sm-11 row">
          3. Él tiene que trabajar mañana en la mañana: He
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['has']"
          />to work tomorrow morning.
          <br />
        </div>
        <div class="col-sm-11 row">
          4. Natalie hace deporte todos los días: Natalie
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['does']"
          />sports every day.
          <br />
        </div>
        <div class="col-sm-11 row">
          5. Yo voy a trabajar en bus: I
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['go']"
          />to work by bus.
          <br />
        </div>
        <div class="col-sm-11 row">
          6. Ella va al colegio a pie: She
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['goes']"
          />to school on foot.
          <br />
        </div>
        <div class="col-sm-11 row">
          7. Llueve mucho en New York: It
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['rains']"
          />a lot in New York.
          <br />
        </div>
        <div class="col-sm-11 row">
          8. Amar tiene sentido: Loving
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['makes']"
          />sense.
        </div>
        <div class="col-sm-11 row">
          9. Él tiene que trabajar mañana: He
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['has']"
          />to work tomorrow.
          <br />
        </div>
        <div class="col-sm-11 row">
          10. Mi novia mira televisión los sábados: My girlfriend
          <inputChecked
            :resuelto="false"
            style="width: 25%; margin-left:10px; margin-right:10px;"
            :esperado="['watches']"
          />tv on Saturdays.
          <br />
        </div>
        <div class="col-sm-11 row">
          11. Ella tiene un carro: She
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['has']"
          />a car.
          <br />
        </div>
        <div class="col-sm-11 row">
          12. Ella no tiene un carro: She doesn’t
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['have']"
          />a car.
          <br />
        </div>
        <div class="col-sm-11 row">
          13. Víctor llora todos los días: Victor
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['cries']"
          />everyday.
          <br />
        </div>
        <div class="col-sm-11 row">
          14. El gato tiene cuatro patas: The cat
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['has']"
          />four paws.
          <br />
        </div>
        <div class="col-sm-11 row">
          15. Mi mamá me ama: My mother
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['loves']"
          />me.
          <br />
        </div>
        <div class="col-sm-11 row">
          16. El profesor enseña muy bien: The teacher
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['teaches']"
          />very well.
          <br />
        </div>
        <div class="col-sm-11 row">
          17. Eso huele mal: That
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['smells']"
          />bad.
          <br />
        </div>
        <div class="col-sm-11 row">
          18. Ese niño estudia inglés: That boy
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['studies']"
          />English.
          <br />
        </div>
        <div class="col-sm-11 row">
          19. Él ama el número mágico: He
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['loves']"
          />the magic number.
          <br />
        </div>
        <div class="col-sm-11 row">
          20. Él tiene que madrugar: He
          <inputChecked
            :resuelto="false"
            style="width: 20%; margin-left:10px; margin-right:10px;"
            :esperado="['has']"
          />to wake up early.
        </div>
      </FONT>
    </div>
    <br />
    <br />
    <br />
    <div class="row">
      <i class="fa fa-diamond marginn-left"></i>

      <p class="parrafoBlack marginn-left">
        &nbsp;
        <b>ESCRIBA LA TRADUCCIÓN EN INGLES Y COMPLETA LAS ORACIONES.</b>
        <br />
      </p>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3 show-grid" v-for="item in $data.tablaUnoPag35">
        <listaIndex :tabla="item" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC :cuestionario="$data.tablaDosPag35" />
      </div>
    </div>
    <div class="row">
      <i class="fa fa-diamond marginn-left"></i>

      <p class="parrafoBlack marginn-left">
        &nbsp;
        <b>Aquí hay una lista de los verbos más fáciles del inglés. Reescribe las oraciones con “she”</b>
        <br />
      </p>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <font class="parrafoBlack">
        Recuerda que la
        <font class="text-danger">S</font> ,
        <font class="text-danger">ES</font> o
        <font class="text-danger">IES</font> se le agrega a un verbo en presente precedida de SHE, HE o IT
      </font>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTraduccionCodigosDos
          :cuestionario="$data.cuestionario1Pag36"
          :inglesR="false"
          :espanolR="true"
        />
      </div>
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
import tablaTraduccionCodigos from "./tablaTraduccionCodigos";
import tablaTraduccionCodigosDos from "./tablaTraduccionCodigosDos";
import tablaTC from "./tablaTraduccionCodigos";
export default {
  components: {
    listaIndex,
    inputChecked,
    tablaTraduccionCodigos,
    tablaTraduccionCodigosDos,
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
              tamano: 15,
            },
          },
          {
            A: "We have",
            complejo1: {
              textoA: "Victor",
              lista: ["has"],
              tamano: 15,
            },
          },
          {
            A: "They cry",

            complejo1: {
              textoA: "She",
              lista: ["cries"],
              tamano: 15,
            },
          },
          {
            A: "You play",
            complejo1: {
              textoA: "He",
              lista: ["plays"],
              tamano: 15,
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
              tamano: 15,
            },
          },
          {
            A: "I do",
            complejo1: {
              textoA: "My sister",
              lista: ["does"],
              tamano: 15,
            },
          },
        ],
      },

      tablaAPag33: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "A", thClass: "Blue  " },
        ],

        items: [
          { A: "1. I" },
          { A: "2. YOU " },
          { A: "3. SHE" },
          { A: "4. HE" },
          { A: "5. IT" },
          { A: "6. WE" },
          { A: "7. THEY" },
        ],
      },

      tablaBPag33: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "B", thClass: "Red " },
        ],
        items: [
          { B: "1. go/goes" },
          { B: "2. have / has" },
          { B: "3. cry/ cries" },
          { B: "4. watch / watches" },
          { B: "5. buy / buys" },
          { B: "6. do / does" },
          { B: "7. work / works" },
          { B: "8. eat / eats" },
          { B: "9. stay / stays" },
        ],
      },
      tablaCPag33: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "C", thClass: "Yelow " },
        ],

        items: [
          { C: "1. there" },
          { C: "2. to admit" },
          { C: "3. movies" },
          { C: "4. a lot" },
          { C: "5. what" },
          { C: "6. here" },
          { C: "7. healthy" },
          { C: "8. sport" },
        ],
      },
      tablaDPag33: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "D", thClass: "Green " },
        ],

        items: [
          { D: "1. on Sundays" },
          { D: "2. it" },
          { D: "3. that" },
          { D: "4. everyday" },
          { D: "5. from time to time" },
          { D: "6. at night" },
          { D: "7. I want" },
          { D: "8. from Monday to Friday" },
          { D: "9. in the morning" },
        ],
      },
      cuestionario1Pag33: {
        fields: [
          { key: "A", thClass: "Blue parrafoBlack" },
          { key: "B", thClass: "Red parrafoBlack" },
          { key: "C", thClass: "Yelow parrafoBlack" },
          { key: "D", thClass: "Green parrafoBlack" },
          { key: "ENGLISH_PHRASE", label: "ENGLISH" },
          { key: "TRADUCCION_ESPAÑOL", label: "SPANISH" },
        ],
        items: [
          {
            A: 1,
            B: 1,
            C: 1,
            D: 1,
            ENGLISH_PHRASE: ["I go there on sundays"],
            TRADUCCION_ESPAÑOL: ["Voy allá los domingos"],
          },
          {
            A: 3,
            B: 2,
            C: 2,
            D: 2,
            ENGLISH_PHRASE: ["She has to admit it"],
            TRADUCCION_ESPAÑOL: ["Ella tiene que admitirlo"],
          },
          {
            A: 6,
            B: 7,
            C: 6,
            D: 4,
            ENGLISH_PHRASE: ["We work here everyday"],
            TRADUCCION_ESPAÑOL: ["Nosotros trabajamos aquí todos los días"],
          },
          {
            A: 1,
            B: 6,
            C: 8,
            D: 9,
            ENGLISH_PHRASE: ["I do sport in the morning"],
            TRADUCCION_ESPAÑOL: ["Yo hago deporte en la mañana"],
          },
          {
            A: 4,
            B: 4,
            C: 3,
            D: 6,
            ENGLISH_PHRASE: ["He watches movies at night "],
            TRADUCCION_ESPAÑOL: ["Él ve películas en la noche"],
          },
          {
            A: 2,
            B: 9,
            C: 1,
            D: 8,
            ENGLISH_PHRASE: ["You stay there from Monday to Friday"],
            TRADUCCION_ESPAÑOL: ["Tú te quedas allá de lunes a viernes"],
          },
          {
            A: 1,
            B: 8,
            C: 4,
            D: 4,
            ENGLISH_PHRASE: ["I eat a lot everyday "],
            TRADUCCION_ESPAÑOL: ["Yo como mucho todos los días"],
          },
          {
            A: 3,
            B: 6,
            C: 5,
            D: 7,
            ENGLISH_PHRASE: ["She does what I want"],
            TRADUCCION_ESPAÑOL: [" Ella hace lo que yo quiera"],
          },
          {
            A: 7,
            B: 8,
            C: 7,
            D: 9,
            ENGLISH_PHRASE: ["They eat healthy in the morning"],
            TRADUCCION_ESPAÑOL: ["Ellos comen saludable en la mañana"],
          },
          {
            A: 3,
            B: 5,
            C: 6,
            D: 5,
            ENGLISH_PHRASE: ["She buys here from time to time"],
            TRADUCCION_ESPAÑOL: ["Ella compra aquí de vez en cuando"],
          },
          {
            A: 4,
            B: 4,
            C: 3,
            D: 1,
            ENGLISH_PHRASE: ["He watches movies on Sundays"],
            TRADUCCION_ESPAÑOL: ["Él ve películas los domingos"],
          },
          {
            A: 7,
            B: 7,
            C: 4,
            D: 4,
            ENGLISH_PHRASE: ["They work a lot everyday"],
            TRADUCCION_ESPAÑOL: ["Ellos trabajan mucho todos los días"],
          },
          {
            A: 1,
            B: 2,
            C: 2,
            D: 3,
            ENGLISH_PHRASE: ["I have to admit that"],
            TRADUCCION_ESPAÑOL: ["Yo tengo que admitir eso"],
          },
          {
            A: 1,
            B: 8,
            C: 5,
            D: 7,
            ENGLISH_PHRASE: ["I eat what I want"],
            TRADUCCION_ESPAÑOL: ["Yo como lo que yo quiero"],
          },
          {
            A: 3,
            B: 3,
            C: 4,
            D: 6,
            ENGLISH_PHRASE: ["She cries a lot at night"],
            TRADUCCION_ESPAÑOL: ["Ella llora mucho en la noche"],
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
      tablaUnoPag35: [
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "html",
              label: "ORACIÓN EN PRESENTE  AFIRMATIVO (INGLÉS)",
              thClass: "",
            },
          ],
          items: [
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
                '<FONT class=""><strong>I brush my teeth twice a day </strong></FONT> <br><br>',
            },
            {
              html:
                '<FONT class=""><strong>They speak English very slowly</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>I walk everyday </strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>You cry very much</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>They eat here</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>You cough every now and then</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>I watch TV once in a blue moon</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>We take the kids to the school</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>We dance in the rain</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>I brush my teeth twice a day</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>They speak english very slowly</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>I walk everyday</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>I love you</strong></FONT>',
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
              label: "ORACIÓN AFIRMATIVA EN PRESENTE (ESPAÑOL)",
              thClass: "",
            },
          ],
          items: [
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
            {
              html: '<inputChecked :esperado="["adsd"]" :resuelto="false"/>',
            },
            {
              html: '<FONT class=""><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>&nbsp;</strong></FONT>',
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
              label:
                "Si el sujeto es HE, SHE o IT elverbo lleva la s, es o ies",
              thClass: "",
            },
          ],
          items: [
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
                '<FONT class=""><strong>Nobody go <font class="text-danger">es</font> for a run every morning</strong></FONT>',
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
            {
              html: '<FONT class=""><strong>He______ everyday</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>She _______ vey much</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>The chicken ________ here;</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>The baby _________ every now and then</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>She ___________ tv once in a blue moon</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>He __________ the kids to the school</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>It ________ in the rain</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>She _________ her teeth twice a day</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>He _________ English very slowly</strong></FONT>',
            },
            {
              html:
                '<FONT class=""><strong>The dog ________ everyday</strong></FONT>',
            },
            {
              html: '<FONT class=""><strong>She_______ me</strong></FONT>',
            },
          ],
        },
      ],
      tablaDosPag35: [
        {
          fields: [
            { key: "complejo1", label: "AUXILIARIES" },
            { key: "A", label: "4.1" },
            { key: "B", label: "4.2" },
            { key: "C", label: "4.3" },
            { key: "D", label: "4.4" },
          ],
          items: [
            {
              complejo1: {
                lista: ["Go"],
                textoA: "Do you",
                textoD: "to school?",
                tamano: 20,
              },
              A: "",
              B: "Went",
              C: "Gone",
              D: "Going",
            },
          ],
        },
      ],

      cuestionario1Pag36: {
        fields: [
          {
            key: "A",
            thClass: "Yellow parrafoBlack",
            label: "Verbo en presente",
          },
          { key: "ENGLISH_PHRASE", label: "En tercera persona" },
          { key: "B", label: "Clase" },
          { key: "C", label: "Past and participle" },
        ],
        items: [
          {
            A: "I *Eat* pizza",
            B: "Irregular",
            C: "Ate – eaten",

            ENGLISH_PHRASE: ["She eats pizza"],
          },
          {
            A: "I *Watch* tv",
            B: "Irregular",
            C: "Saw - Seen",

            ENGLISH_PHRASE: ["She watches"],
          },
          {
            A: "I *Smell* really good",
            B: "Regular",
            C: "Smelled - smelled",

            ENGLISH_PHRASE: ["She smells really good"],
          },
          {
            A: "I *Spit* on the floor",
            B: "Irregular",
            C: "Spat - spat",

            ENGLISH_PHRASE: ["She spits on the floor"],
          },
          {
            A: "I *Throw* the ball",
            B: "Irregular",
            C: "Threw - thrown",
            ENGLISH_PHRASE: ["She throws the ball "],
          },
          {
            A: "I *Push* the door",
            B: "Regular",
            C: "Pushed - pushed",
            ENGLISH_PHRASE: ["She pushes the door"],
          },
          {
            A: "I *Walk* with a limp",
            B: "Regular",
            C: "Walked - walked",
            ENGLISH_PHRASE: ["She walks with a limp"],
          },
          {
            A: "I *Think* of you",
            B: "Irregular",
            C: "Thought- thought",
            ENGLISH_PHRASE: ["She thinks of you"],
          },
          {
            A: "I *Call* the police",
            B: "Regular",
            C: "Called - called",

            ENGLISH_PHRASE: ["She calls the police"],
          },
          {
            A: "I *Breathe* quickly",
            B: "Regular",
            C: "Breathed- breathed",
            ENGLISH_PHRASE: ["She breathes quicly"],
          },
          {
            A: "I *Swallow* tablets",
            B: "Irregular",
            C: "Swallowed - swallowed",
            ENGLISH_PHRASE: ["She swallows tablets"],
          },
          {
            A: "I *Hear* birds",
            B: "Irregular",
            C: "Heards - heards",
            ENGLISH_PHRASE: ["She hears birds"],
            TRADUCCION_ESPAÑOL: ["Ellos trabajan mucho todos los días"],
          },
          {
            A: "I *Pry* to God",
            B: "Regular",
            C: "Prayed - prayed",

            ENGLISH_PHRASE: ["She prays God"],
          },
          {
            A: "I *Swear* to God",
            B: "Irregular",
            C: "Swore - sworn",
            ENGLISH_PHRASE: ["She swears to God"],
          },
          {
            A: "I *Scream* loudly",
            B: "Regular",
            C: "Screamed - screamed",
            ENGLISH_PHRASE: ["She screams loudly"],
          },
          {
            A: "I *Cry* a lot",
            B: "Regular",
            C: "Cried - cried",
            ENGLISH_PHRASE: ["She cries a lot"],
          },
          {
            A: "I *Swim* like a fish",
            B: "Irregular",
            C: "Swam - swum",
            ENGLISH_PHRASE: ["She swims like a fish"],
          },
          {
            A: "I *Wake up* at 5:45 am",
            B: "Irregular",
            C: "Woke - woken",
            ENGLISH_PHRASE: ["She wakes up at 5:45 am"],
          },
          {
            A: "I *Get up* at 6:00 am",
            B: "Irregular",
            C: "Got - gotten",
            ENGLISH_PHRASE: ["She gets up at 6:00 am"],
          },
          {
            A: "I *Dream* about engels",
            B: "Irregular",
            C: "Dreamt - dreamt",
            ENGLISH_PHRASE: ["She dreams about engels"],
          },
          {
            A: "I *Catch* the ball",
            B: "Irregular",
            C: "Caught - caught",
            ENGLISH_PHRASE: ["She catches the ball"],
          },
          {
            A: "I *Drive* a car",
            B: "Irregular",
            C: "Drove - driven",
            ENGLISH_PHRASE: ["She drives a car"],
          },
          {
            A: "I *Ride* a horse",
            B: "Irregular",
            C: "Rode - ridden",
            ENGLISH_PHRASE: ["She rides a horse"],
          },
          {
            A: "I *Write* a poem",
            B: "Irregular",
            C: "Wrote - written",
            ENGLISH_PHRASE: ["She writes a poem"],
          },
          {
            A: "I *Taste* the soup",
            B: "Regular",
            C: "Tasted - tasted",
            ENGLISH_PHRASE: ["She tastes the soup"],
          },
          {
            A: "I *Touch* my nose",
            B: "Regular",
            C: "Touched - touched",
            ENGLISH_PHRASE: ["She touches my nose"],
          },
          {
            A: "I *Pick up* the pencil",
            B: "Regular",
            C: "Picked - picked",
            ENGLISH_PHRASE: ["She picks up the pencil"],
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