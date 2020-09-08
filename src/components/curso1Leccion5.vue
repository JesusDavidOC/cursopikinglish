<template>
  <div>
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8" id="cuadroTexto">
        <h3>
          Recuerde que un verbo se usa su
          <span
            class="colorLetraRojo"
          >forma presente lógicamente en presente</span> o después de un auxiliar y siempre tenga en cuenta que los auxiliares sirven para negar o preguntar.
        </h3>
      </div>
      <div class="col-sm-2"></div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7 row">
        <div class="col-sm-3" v-for="item in tablasContenido1P27">
          <listaIndex :tabla="item" />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-9">
        <tablaTC
          class="overflow-auto"
          :cuestionario="$data.cuestionario1P27"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7 row">
        <div class="col-sm-3" v-for="item in tablasContenido2P27">
          <listaIndex :tabla="item" />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7">
        <tablaTC
          class="overflow-auto"
          :cuestionario="cuestionario2P27"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8" id="cuadroTexto">
        <h3>
          Hay dos tipos de verbos
          <span class="colorLetraRojo">Regulares</span>
          e
          <span class="colorLetraRojo">Irregulares</span>, y ambos tienen 4 formas; -
          <span
            class="colorLetraRojo"
          >presente, pasado, participio y progresivo.</span>
          existen
          <span class="colorLetraRojo">cinco auxiliares.</span>
        </h3>
      </div>
      <div class="col-sm-2"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC
          class="overflow-auto"
          :cuestionario="$data.cuestionario2P28"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" id="text">
        <i class="fa fa-diamond" style="font-size: 1.5em;"></i>
        <a id="textPractice">Escribe la forma del verbo debajo del grupo de verbos con poder.</a>
      </div>
    </div>
    <div class="row" style="margin:0em;">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div
          class="col-sm-1"
          v-for="(item, index) in palabrasListaP28.fields"
          style="margin:0; padding:0;"
        >
          <listaIndex :tabla="{bordered:true, fields: [item]}" />
        </div>
      </div>
    </div>
    <div class="row" style="margin-top:-1.5em;">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div class="col-sm-3" style="padding:0;">
          <inputChecked :esperado="['participio']" :resuelto="false" />
        </div>
        <div class="col-sm-5" style="padding:0;">
          <inputChecked :esperado="['progresivo']" :resuelto="false" />
        </div>
        <div class="col-sm-4" style="padding:0;">
          <inputChecked :esperado="['presente']" :resuelto="false" />
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" id="text">
        <i class="fa fa-diamond" style="font-size: 1.5em;"></i>
        <a id="textPractice">Escribe la traducción en frente de cada frase en inglés.</a>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-9">
        <tablaTC
          class="overflow-auto"
          :cuestionario="tabla1P29"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" id="text">
        <i class="fa fa-diamond" style="font-size: 1.5em;"></i>
        <a id="textPractice">Ahora niegue cada oración.</a>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-9">
        <tablaTC
          class="overflow-auto"
          :cuestionario="tabla2P29"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>

    <div class="row">
      <h3 id="subTitulo">EXAMEN DE APROBACIÓN DE LA LÓGICA DEL INGLÉS</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" id="text">
        <opcionMultiple
          :options="$data.cuestionarioP30"
          :rEsperadas="$data.respuestasCuestionarioP30"
          @respuestas="$data.mensajeRespuestasP30 = $event"
        />
      </div>
      <b-modal ref="my-modalP30" hide-footer title="RESULTADO">{{mensajeRespuestasP30}}</b-modal>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modalP30')">VERIFICAR PREGUNTAS</b-button>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" style="text-align:left;">
        <legend
          id="5__BV_label_"
          tabindex="-1"
          class="bv-no-focus-ring col-form-label pt-0 col-form-label-lg labelPregunta"
        >7. Ubique la forma del verbo “ir” en inglés en las siguientes oraciones:</legend>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-9">
        <tablaTC
          class="overflow-auto"
          :cuestionario="tabla3P29"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>
    <div class="row" v-for="(item, index) in preguntasCompletarP30.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div :class="'col-sm-'+item.tamaño">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP30.nombre+index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
          />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" style="text-align:left;">
        <legend
          id="5__BV_label_"
          tabindex="-1"
          class="bv-no-focus-ring col-form-label pt-0 col-form-label-lg labelPregunta"
        >8. Ubique al frente de la traducción en español el verbo con poder en inglés.</legend>
      </div>
    </div>
  </div>
</template>

<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import opcionMultiple from "./opcionMultiple";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
import tablaTC from "./tablaTraduccionCodigos";

export default {
  data() {
    return {
      preguntasCompletarP30: {
        nombre: "preguntasCompletarP24",
        items: [
          {
            esperado: ["go"],
            textoA: "a.    Where did you",
            textoD: "? - " + "<strong> ¿Donde fuiste? </strong> ",
            tamaño: 7,
          },
          {
            esperado: ["went"],
            textoA: "b.    Nobody",
            textoD:
              "to the party last night.- <strong> Nadie fue a la fiesta anoche.</strong> ",
            tamaño: 9,
          },
          {
            esperado: ["go"],
            textoA: "c.    I always",
            textoD:
              "to school on foot. - <strong> Yo siempre voy hasta el colegio a pie.</strong> ",
            tamaño: 10,
          },
          {
            esperado: ["gone"],
            textoA: "d.    have you ",
            textoD:
              "to the gym recently?. - <strong> ¿Has ido al gymnasio recientemente?.</strong> ",
            tamaño: 10,
          },
          {
            esperado: ["go"],
            textoA: "e.    She didn’t",
            textoD: "to work . - <strong> Ella no fue a trabajar.</strong> ",
            tamaño: 7,
          },
          {
            esperado: ["went"],
            textoA: "f.     He",
            textoD:
              "to visit his friend. - <strong> Él fue a visitar a su amigo.</strong> ",
            tamaño: 8,
          },
          {
            esperado: ["gone"],
            textoA: " g.    He has",
            textoD:
              "to school three times this morning. - <strong> Él ha ido al colegio tres veces esta mañana.</strong> ",
            tamaño: 12,
          },
          {
            esperado: ["going"],
            textoA: " h.    Where are you",
            textoD: "? . - <strong> ¿Donde estás yendo?.</strong> ",
            tamaño: 8,
          },
        ],
      },
      mensajeRespuestasP30: "",
      respuestasCuestionarioP30: ["B", "B", "A", "A", "C", "C"],
      cuestionarioP30: [
        {
          respuesta: "",
          pregunta: "1.    ¿Por qué se les llama Super Power Verbs?",
          options: [
            {
              text: "A) Necesitan auxiliares.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) No necesitan auxiliares.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "2.        ¿Cuántas clases de verbos hay en inglés y cuáles son?",
          options: [
            {
              text: "A) Una clase, verbos en presente.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Dos clases, regulares e irregulares.",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Tres clases, presente, pasado y participio.",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "3.        ¿Cuáles son las formas de un verbo? ",
          options: [
            {
              text: "A) Presente, Pasado, Participio Y Progresivo.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Do, Does, Did, Will Y Would.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "4.    ¿Cuándo se usa un verbo en su forma presente?",
          options: [
            {
              text: "A) En oraciones en presente y después de un auxiliar.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) En oraciones en presente afirmativo o en pasado.",
              value: "B",
              disabled: false,
            },
            {
              text: "C) En oraciones negativas o afirmativas.",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "5.   ¿Cuántos auxiliares hay en inglés?",
          options: [
            {
              text: "A) Tres.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Dos.",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Cinco.",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "6.   ¿Cuándo se usa el participio de un verbo?",
          options: [
            {
              text: "A) Después de un auxiliar.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) En presente.",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Después de Have, Has Y Had.",
              value: "C",
              disabled: false,
            },
          ],
        },
      ],
      tabla3P29: {
        fields: [
          { key: "present", label: "Present", thClass: "Yelow" },
          { key: "past", label: "Past", thClass: "Red" },
          { key: "participle", label: "Participle", thClass: "Blue" },
          { key: "progressive", label: "Progressive", thClass: "Green" },
        ],
        items: [
          {
            present: "3,1",
            past: "3,2",
            participle: "3,3",
            progressive: "3,4",
          },
          {
            present: "Go",
            past: "Went",
            participle: "Gone",
            progressive: "Going",
          },
        ],
      },
      tabla2P29: {
        fields: [
          { key: "A", label: "A", thClass: "noHead" },
          { key: "complejo1", label: "A", thClass: "noHead" },
          { key: "B", label: "A", thClass: "noHead" },
          { key: "complejo2", label: "A", thClass: "noHead" },
        ],
        items: [
          {
            A: "I eat",
            complejo1: { lista: ["I don't eat", "I do not eat"], tamano: 18 },
            B: "She eats",
            complejo2: {
              lista: ["She doesn't eat", "She does not eat"],
              tamano: 18,
            },
          },
          {
            A: "I ate",
            complejo1: { lista: ["I didn´t eat", "I did not eat"], tamano: 18 },
            B: "I will eat",
            complejo2: { lista: ["I won´t eat", "I will not eat"], tamano: 18 },
          },
          {
            A: "I would eat",
            complejo1: {
              lista: ["I wouldn´t eat", "I would not eat"],
              tamano: 18,
            },
            B: "I could eat",
            complejo2: {
              lista: ["I couldn´t eat", "I could not eat"],
              tamano: 18,
            },
          },
          {
            A: "I can eat",
            complejo1: { lista: ["I can´t eat", "I can not eat"], tamano: 18 },
            B: "I should eat",
            complejo2: {
              lista: ["I shouldn´t eat", "I should not eat"],
              tamano: 18,
            },
          },
          {
            A: "I must eat",
            complejo1: {
              lista: ["I mustn´t eat", "I must not eat"],
              tamano: 18,
            },
            B: "I have eaten",
            complejo2: {
              lista: ["I haven´t eaten", "I have not eaten"],
              tamano: 18,
            },
          },
          {
            A: "She has eaten",
            complejo1: {
              lista: ["She hasn´t eaten", "She has not eaten"],
              tamano: 18,
            },
            B: "I had eaten",
            complejo2: {
              lista: ["I hadn´t eaten", "I had not eaten"],
              tamano: 18,
            },
          },
          {
            A: "I am eating",
            complejo1: { lista: ["I am not eating"], tamano: 18 },
            B: "She is eating",
            complejo2: {
              lista: ["She isn´t eating", "She is not eating"],
              tamano: 18,
            },
          },
          {
            A: "You are eating",
            complejo1: {
              lista: ["You aren´t eating", "You are not eating"],
              tamano: 18,
            },
            B: "I was eating",
            complejo2: {
              lista: ["I wasn´t eating", "I wasn´t eating"],
              tamano: 18,
            },
          },
          {
            A: "We were eating",
            complejo1: {
              lista: ["Yo estoy comiendo", "estoy comiendo"],
              tamano: 18,
            },
            B: "",
            complejo2: { lista: [""], tamano: 18 },
          },
        ],
      },
      tabla1P29: {
        fields: [
          { key: "A", label: "A", thClass: "noHead" },
          { key: "complejo1", label: "A", thClass: "noHead" },
          { key: "B", label: "A", thClass: "noHead" },
          { key: "complejo2", label: "A", thClass: "noHead" },
        ],
        items: [
          {
            A: "I eat",
            complejo1: { lista: ["Yo como", "como"], tamano: 18 },
            B: "She eats",
            complejo2: { lista: ["Ella come", "come"], tamano: 20 },
          },
          {
            A: "Do you eat?",
            complejo1: {
              lista: [
                "¿tú comes?",
                "¿comes?",
                "¿comes",
                "comes?",
                "¿tú comes",
                "tú comes?",
              ],
              tamano: 18,
            },
            B: "Does she eat?",
            complejo2: {
              lista: [
                "¿ella come?",
                "¿come?",
                "¿come",
                "come?",
                "¿ella come",
                "ella come?",
              ],
              tamano: 20,
            },
          },
          {
            A: "Did you eat?",
            complejo1: {
              lista: [
                "¿tú comiste?",
                "¿comiste?",
                "¿comiste",
                "comiste?",
                "¿tú comiste",
                "tú comiste?",
              ],
              tamano: 18,
            },
            B: "Will you eat?",
            complejo2: {
              lista: [
                "¿tú comerás?",
                "¿comerás?",
                "¿comerás",
                "comerás?",
                "¿tú comerás",
                "tú comerás?",
              ],
              tamano: 20,
            },
          },
          {
            A: "Would you eat?",
            complejo1: {
              lista: [
                "¿tú comerías?",
                "¿comerías?",
                "¿comerías",
                "comerías?",
                "¿tú comerías",
                "tú comerías?",
              ],
              tamano: 18,
            },
            B: "I can eat",
            complejo2: { lista: ["Yo puedo comer", "puedo comer"], tamano: 20 },
          },
          {
            A: "I should eat",
            complejo1: {
              lista: ["Yo debería comer", "debería comer"],
              tamano: 18,
            },
            B: "I must eat",
            complejo2: { lista: ["Yo debo comer", "debo comer"], tamano: 20 },
          },
          {
            A: "I could eat",
            complejo1: { lista: ["Yo pude comer", " pude comer"], tamano: 18 },
            B: "She is eating",
            complejo2: {
              lista: ["Ella está comiendo", "está comiendo"],
              tamano: 20,
            },
          },
          {
            A: "I ate",
            complejo1: { lista: ["Yo comí", "comí"], tamano: 18 },
            B: "I have eaten",
            complejo2: { lista: ["Yo he comido", "he comido"], tamano: 20 },
          },
          {
            A: "She has eaten",
            complejo1: { lista: ["Ella ha comido", "ha comido"], tamano: 18 },
            B: "I had eaten",
            complejo2: {
              lista: ["Yo había comido", "había comido"],
              tamano: 20,
            },
          },
          {
            A: "I am eating",
            complejo1: {
              lista: ["Yo estoy comiendo", "estoy comiendo"],
              tamano: 18,
            },
            B: "You are eating",
            complejo2: {
              lista: ["Tú estás comiendo", "estás comiendo"],
              tamano: 20,
            },
          },
          {
            A: "I was eating",
            complejo1: {
              lista: ["Yo estaba comiendo", "estaba comiendo"],
              tamano: 18,
            },
            B: "We were eating",
            complejo2: {
              lista: ["Nosotros estábamos comiendo", "estábamos comiendo"],
              tamano: 22,
            },
          },
        ],
      },
      palabrasListaP28: {
        fields: [
          "Have",
          "Has",
          "Had",
          "Is",
          "Are",
          "Am",
          "Was",
          "Were",
          "Can",
          "Could",
          "Should",
          "Must",
        ],
      },
      cuestionario2P28: {
        fields: [
          { key: "complejo1", label: "EN PRESENTE" },
          { key: "complejo2", label: "EN PRESENTE CON HE-SHE-IT" },
          { key: "complejo3", label: "EN PASADO" },
          { key: "complejo4", label: "EN FUTURO" },
          { key: "complejo5", label: "UN VERBO TERMINA EN RÍA" },
        ],
        items: [
          {
            complejo1: { lista: ["Do"], tamano: 11 },
            complejo2: { lista: ["Does"], tamano: 15 },
            complejo3: { lista: ["Did"], tamano: 10 },
            complejo4: { lista: ["Will"], tamano: 11 },
            complejo5: { lista: ["Would"], tamano: 15 },
          },
        ],
      },
      cuestionario2P27: {
        fields: [
          { key: "A", thClass: "Blue" },
          { key: "B", thClass: "Red" },
          { key: "C", thClass: "Yelow" },
          { key: "complejo1", label: "ENGLISH" },
          { key: "ESPANOL", label: "SPANISH" },
        ],
        items: [
          {
            A: 1,
            B: 1,
            C: 1,
            complejo1: { lista: ["Do you go?"] },
            ESPANOL: "¿Tú vas?",
          },
          {
            A: 2,
            B: 2,
            C: 1,
            complejo1: { lista: ["Does she go?"] },
            ESPANOL: "¿Ella va?",
          },
          {
            A: 3,
            B: 2,
            C: 1,
            complejo1: { lista: ["Did she go?"] },
            ESPANOL: "¿Ella fue?",
          },
          {
            A: 4,
            B: 1,
            C: 1,
            complejo1: { lista: ["Will you go?"] },
            ESPANOL: "¿Tú irás?",
          },
          {
            A: 5,
            B: 2,
            C: 1,
            complejo1: { lista: ["Would she go?"] },
            ESPANOL: "¿Ella iría?",
          },
        ],
      },
      tablasContenido2P27: [
        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            "#",
            // A column that needs custom formatting
            { key: "A", thClass: "Blue" },
          ],
          items: [
            { A: "Do" },
            { A: "Does" },
            { A: "Did" },
            { A: "Will" },
            { A: "Would" },
          ],
        },

        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            "#",
            // A column that needs custom formatting
            { key: "B", thClass: "Red" },
          ],
          items: [{ B: "You" }, { B: "She" }],
        },
        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            "#",
            // A column that needs custom formatting
            { key: "C", thClass: "Yelow" },
          ],
          items: [{ C: "go ...?" }],
        },
      ],
      cuestionario1P27: {
        fields: [
          { key: "A", thClass: "Blue" },
          { key: "B", thClass: "Red" },
          { key: "C", thClass: "Yelow" },
          { key: "D", thClass: "Green" },
          { key: "complejo1", label: "ENGLISH" },
          { key: "ESPANOL", label: "SPANISH" },
        ],
        items: [
          {
            A: 1,
            B: 1,
            C: 1,
            D: 2,
            complejo1: { lista: ["I don´t have a friend"] },
            ESPANOL: "Yo no tengo un amigo",
          },
          {
            A: 2,
            B: 2,
            C: 1,
            D: 1,
            complejo1: { lista: ["She doesn´t have that"] },
            ESPANOL: "Ella no tiene eso",
          },
          {
            A: 1,
            B: 3,
            C: 2,
            D: 1,
            complejo1: { lista: ["I didn´t do that"] },
            ESPANOL: "Yo no hice eso",
          },
          {
            A: 2,
            B: 4,
            C: 2,
            D: 1,
            complejo1: { lista: ["She won´t do that"] },
            ESPANOL: "Ella no hará eso",
          },
          {
            A: 1,
            B: 5,
            C: 2,
            D: 1,
            complejo1: { lista: ["I wouldn´t do that"] },
            ESPANOL: "Yo no haría eso",
          },
        ],
      },
      tablasContenido1P27: [
        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            "#",
            // A column that needs custom formatting
            { key: "A", thClass: "Blue" },
          ],
          items: [{ A: "I" }, { A: "SHE" }],
        },

        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            "#",
            // A column that needs custom formatting
            { key: "B", thClass: "Red" },
          ],
          items: [
            { B: "Don´t" },
            { B: "Doesn´t" },
            { B: "Didn´t" },
            { B: "Won´t" },
            { B: "Wouldn´t" },
          ],
        },
        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            "#",
            // A column that needs custom formatting
            { key: "C", thClass: "Yelow" },
          ],
          items: [{ C: "Have" }, { C: "Do" }],
        },
        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            { key: "#" },
            ,
            // A column that needs custom formatting
            { key: "D", thClass: "Green" },
          ],
          items: [{ D: "That" }, { D: "A friend" }],
        },
      ],
    };
  },
  methods: {
    showModal(text) {
      this.$refs[text].show();
    },
  },
  components: {
    opcionMultiple,
    listaIndex,
    inputChecked,
    posiblesRespuestasTabla,
    tablaTC,
  },
};
</script>

<style scoped>
#textPractice {
  text-align: left;
  margin-bottom: 1em;
  font-size: 1.5em;
}
/deep/.labelPregunta {
  font-weight: bold;
}

/deep/ #tabla {
  padding-right: 0px;
  padding-left: 0px;
}
/deep/ .row {
  width: 100%;
  margin: 0;
  margin-bottom: 1em;
  padding: 0;
}

/deep/ #EnglishInput,
#SpanishInput {
  width: 100%;
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

/deep/.colorLetraRojo {
  color: red;
  margin-left: 8px;
  margin-right: 8px;
}

#cuadroTexto {
  margin-bottom: 1em;
}

img {
  width: 100%;
}

/deep/ #textRequired {
  width: 200px;
}

/deep/ #inputText {
  margin: 0;
  display: inline-flex;
}

#titulo {
  color: red;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 1.5em;
}

#subTitulo {
  padding: 0;
  margin-right: auto;
  color: darkcyan;
  margin-top: 1.5em;
  text-align: left;
}
.textList {
  font-size: 1.5em;
}

#numeroMagico2,
#numeroMagico4,
#numeroMagico5,
#numeroMagico12 {
  background-color: salmon;
  margin-right: auto;
  margin-left: auto;
  padding-top: 0.5em;
  padding-bottom: 0.5em;
  border-style: solid;
  border-radius: 1em;
  border-color: black;
  font-size: 2em;
  color: black;
  font-family: "PT Sans";
  font-weight: bold;
  margin-bottom: auto;
}
#numeroMagico2 {
  background: yellow;
}

#numeroMagico4 {
  background: red;
}
#numeroMagico5 {
  background: royalblue;
}
#numeroMagico12 {
  background: cadetblue;
}

#text,
#inputText {
  text-align: left;
  margin-left: 1em;
}

#textoCompromiso {
  text-align: left;
  margin-bottom: 1em;
  font-size: 1.5em;
}
#i {
  padding-right: 0;
  text-align: end;
}
</style>