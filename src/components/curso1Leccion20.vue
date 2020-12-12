<template>
  <div>
    <div class="row">
      <h3 id="subTitulo">LAS 4 CUATRO FORMAS DEL VERBO</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <b-card>
            <p class="parrafoTabla">
              <listaIndex :tabla="tablaP79" />
          </p>
        </b-card>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">EL TIEMPO DE LOS MODIFICADORES</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <b-card>
          <p class="parrafoTabla">
            <listaIndex :tabla="tablaP79P2" />
          </p>
        </b-card>
        <p class="parrafo">
          Has completado la primera parte de la lógica del inglés,
          felicitaciones por atender las clases y realizar todas las
          asignaciones. Lo invitamos a disfrutar de la segunda parte de la
          lógica del inglés y que continúes animado con el nuevo método de
          aprender inglés, esto es solo el comienzo y nos aseguraremos que la
          pasión por el inglés no se acabe.
        </p>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">¿CÓMO DAR ORDENES EN INGLES?</h3>
    </div>

    <div class="row" v-for="(item, index) in tablaPrueba">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row" id="textoCompromiso">
        <div class="col-sm-12">
          <dt>
            <i class="fa fa-diamond fuenteDiamon"></i>
            <a v-html="item.texto">{{ item.texto }}</a>
          </dt>
        </div>
        <div class="row"></div>
        <div class="col-sm-12 row">
          <div
            class="col-sm-3"
            v-for="item2 in item.palabras"
            style="text-align: center; padding: 0"
            v-if="index < 1"
          >
            <p style="parrafo" v-html="item2">{{ item2 }}</p>
          </div>
          <div v-else>
            <p style="parrafo" v-html="item2">{{ item2 }}</p>
          </div>
        </div>
      </div>
      <div class="col-sm-1"></div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PRACTICE</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" id="text">
        <i class="fa fa-diamond fuenteDiamond"></i>
        <a id="textPractice">Escribe la traducción al frente</a>
      </div>
    </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP24.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-">
        <inputChecked
          :esperado="item.esperado"
          :name="preguntasCompletarP24.nombre + index"
          :conTexto="true"
          :textoA="item.textoA"
          :textoD="item.textoD"
          :tamano="item.tamano"
        />
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">COMPLETA LAS SIGUIENTES ORACIONES</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-1" v-for="item in palabrasP81">
        <p class="parrafo">{{ item }}</p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-5">
        <div v-for="(item, index) in preguntasCompletarP81.items">
            <inputChecked
              :esperado="item.esperado"
              :name="preguntasCompletarP81.nombre + index"
              :conTexto="true"
              :textoA="item.textoA"
              :textoD="item.textoD"
              :tamano="item.tamano"
              
            />
          </div>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">TRADUCE</h3>
    </div>

    <div class="row">
      <div class="col-sm-6" v-for="item in palabrasP81P2">
        <h3 calss="parrafo">{{ item }}</h3>
      </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP81P2.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-">
        <inputChecked
          :esperado="item.esperado"
          :name="preguntasCompletarP81P2.nombre + index"
          :conTexto="true"
          :textoA="item.textoA"
          :textoD="item.textoD"
          :tamano="item.tamano"
        />
      </div>
    </div>
  </div>

  <div class="row">
    <p class="parrafo">{{ item }}</p>
  </div>

  <div class="row">
    <div class="col-sm-1"></div>
    <div class="col-sm-10">
      <b-card>
        <tablaTC :cuestionario="tablaP82" />
      </b-card>
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
  components: {
    listaIndex,
    inputChecked,
    tablaTC,
  },
  data() {
    return {
      tablaP82: {
        fields: [
          { key: "AFIRMATIVA", label: "ORDEN AFIRMATIVA", thClass: "Yelow" },
          { key: "TRADUCCIÓN", thClass: "Red" },
          { key: "complejo1", label: "ORDEN NEGATIVA", thClass: "Blue" },
          { key: "complejo2", label: "INVITACIÓN", thClass: "Blue2" },
        ],
        items: [
          {
            AFIRMATIVA: "Do that",
            TRADUCCIÓN: "Haz eso",
            complejo1: {
              lista: ["Don’t do that"],
              textoA: "",
              textoD: "",
              tamano: 15,
            },
            complejo2: {
              lista: ["Let´s do that"],
              textoA: "",
              textoD: "",
              tamano: 15,
            },
          },
          {
            AFIRMATIVA: "Stay there",
            TRADUCCIÓN: "Quédate ahí",
            complejo1: {
              lista: ["Don’t stay there"],
              textoA: "",
              textoD: "",
              tamano: 17,
            },
            complejo2: {
              lista: ["Let’s stay there"],
              textoA: "",
              textoD: "",
              tamano: 17,
            },
          },
          {
            AFIRMATIVA: "Turn right",
            TRADUCCIÓN: "Voltea a la derecha",
            complejo1: {
              lista: ["Don’t turn right"],
              textoA: "",
              textoD: "",
              tamano: 17,
            },
            complejo2: {
              lista: ["Let’s turn right"],
              textoA: "",
              textoD: "",
              tamano: 16,
            },
          },
          {
            AFIRMATIVA: "Turn left",
            TRADUCCIÓN: "Voltea a la izquierda",
            complejo1: {
              lista: ["Don’t turn left"],
              textoA: "",
              textoD: "",
              tamano: 17,
            },
            complejo2: {
              lista: ["Let’s turn left"],
              textoA: "",
              textoD: "",
              tamano: 16,
            },
          },
          {
            AFIRMATIVA: "Go straight",
            TRADUCCIÓN: "Vete derecho",
            complejo1: {
              lista: ["Don’t go straight"],
              textoA: "",
              textoD: "",
              tamano: 17,
            },
            complejo2: {
              lista: ["Let’s go straight"],
              textoA: "",
              textoD: "",
              tamano: 17,
            },
          },
          {
            AFIRMATIVA: "Push the bottom",
            TRADUCCIÓN: "Presiona el botón",
            complejo1: {
              lista: ["Don’t push the button"],
              textoA: "",
              textoD: "",
              tamano: 20,
            },
            complejo2: {
              lista: ["Let’s push the button"],
              textoA: "",
              textoD: "",
              tamano: 20,
            },
          },
          {
            AFIRMATIVA: "Lock the door",
            TRADUCCIÓN: "Asegura la puerta",
            complejo1: {
              lista: ["Don’t lock the door"],
              textoA: "",
              textoD: "",
              tamano: 19,
            },
            complejo2: {
              lista: ["Please lock the door"],
              textoA: "",
              textoD: "",
              tamano: 20,
            },
          },
          {
            AFIRMATIVA: "Insert the coin",
            TRADUCCIÓN: "Inserta la moneda",
            complejo1: {
              lista: ["Don’t insert the coin"],
              textoA: "",
              textoD: "",
              tamano: 19,
            },
            complejo2: {
              lista: ["Please insert the coin"],
              textoA: "",
              textoD: "",
              tamano: 20,
            },
          },
          {
            AFIRMATIVA: "Pay the Bill",
            TRADUCCIÓN: "Paga la cuenta",
            complejo1: {
              lista: ["Don’t pay the bill"],
              textoA: "",
              textoD: "",
              tamano: 17,
            },
            complejo2: {
              lista: ["Please pay the bill"],
              textoA: "",
              textoD: "",
              tamano: 18,
            },
          },
          {
            AFIRMATIVA: "Take out the garbage",
            TRADUCCIÓN: "The garbage Saca la basura",
            complejo1: {
              lista: ["Don’t take out the garbage"],
              textoA: "",
              textoD: "",
              tamano: 23,
            },
            complejo2: {
              lista: ["Let’s take out the garbage"],
              textoA: "",
              textoD: "",
              tamano: 23,
            },
          },
          {
            AFIRMATIVA: "Take off the socks",
            TRADUCCIÓN: "Quítate las medias",
            complejo1: {
              lista: ["Don’t take off the socks"],
              textoA: "",
              textoD: "",
              tamano: 21,
            },
            complejo2: {
              lista: ["Please take off the socks"],
              textoA: "",
              textoD: "",
              tamano: 22,
            },
          },
          {
            AFIRMATIVA: "Put on the glasses",
            TRADUCCIÓN: "Ponte las gafas",
            complejo1: {
              lista: ["Don’t put on the glasses"],
              textoA: "",
              textoD: "",
              tamano: 22,
            },
            complejo2: {
              lista: ["Let’s put on the glasses"],
              textoA: "",
              textoD: "",
              tamano: 22,
            },
          },
          {
            AFIRMATIVA: "Withdraw the money",
            TRADUCCIÓN: "Retira el dinero",
            complejo1: {
              lista: ["Don’t withdraw the money"],
              textoA: "",
              textoD: "",
              tamano: 23,
            },
            complejo2: {
              lista: ["Let’s withdraw the money"],
              textoA: "",
              textoD: "",
              tamano: 22,
            },
          },
          {
            AFIRMATIVA: "Call the police",
            TRADUCCIÓN: "Llama a la policía",
            complejo1: {
              lista: ["Don’t call the police"],
              textoA: "",
              textoD: "",
              tamano: 19,
            },
            complejo2: {
              lista: ["Let’s call the police"],
              textoA: "",
              textoD: "",
              tamano: 19,
            },
          },
          {
            AFIRMATIVA: "Park the car here",
            TRADUCCIÓN: "Parquea el carro aquí",
            complejo1: {
              lista: ["Don’t park the car here"],
              textoA: "",
              textoD: "",
              tamano: 21,
            },
            complejo2: {
              lista: [" Let’s park the car here"],
              textoA: "",
              textoD: "",
              tamano: 21,
            },
          },
          {
            AFIRMATIVA: "Get on the bus",
            TRADUCCIÓN: "Súbete al bus",
            complejo1: {
              lista: ["Don’t get on the bus"],
              textoA: "",
              textoD: "",
              tamano: 19,
            },
            complejo2: {
              lista: ["Let’s get on the bus"],
              textoA: "",
              textoD: "",
              tamano: 19,
            },
          },
          {
            AFIRMATIVA: "Get in the car",
            TRADUCCIÓN: "Entra al carro",
            complejo1: {
              lista: ["Don’t get in the car"],
              textoA: "",
              textoD: "",
              tamano: 19,
            },
            complejo2: {
              lista: ["Let’s get in the car"],
              textoA: "",
              textoD: "",
              tamano: 18,
            },
          },
          {
            AFIRMATIVA: "Fasten your seat belt",
            TRADUCCIÓN: "Abróchate el cinturón",
            complejo1: {
              lista: ["Don’t fasten your seat belt"],
              textoA: "",
              textoD: "",
              tamano: 23,
            },
            complejo2: {
              lista: ["Let’s fasten your seat belt"],
              textoA: "",
              textoD: "",
              tamano: 23,
            },
          },
          {
            AFIRMATIVA: "Hold tight",
            TRADUCCIÓN: "Agárrate fuerte",
            complejo1: {
              lista: ["Don’t hold tight"],
              textoA: "",
              textoD: "",
              tamano: 17,
            },
            complejo2: {
              lista: [" Let’s hold tight"],
              textoA: "",
              textoD: "",
              tamano: 17,
            },
          },
          {
            AFIRMATIVA: "Keep still",
            TRADUCCIÓN: "Quédate quieto",
            complejo1: {
              lista: ["Don’t keep still"],
              textoA: "",
              textoD: "",
              tamano: 16,
            },
            complejo2: {
              lista: ["Let’s keep still"],
              textoA: "",
              textoD: "",
              tamano: 17,
            },
          },
          {
            AFIRMATIVA: "Sleep tight",
            TRADUCCIÓN: "Que sueñes con los angelitos",
            complejo1: {
              lista: ["Don’t sleep tight"],
              textoA: "",
              textoD: "",
              tamano: 17,
            },
            complejo2: {
              lista: ["Let’s sleep tight"],
              textoA: "",
              textoD: "",
              tamano: 17,
            },
          },
          {
            AFIRMATIVA: "Straighten your collar",
            TRADUCCIÓN: "Acomódate el cuello",
            complejo1: {
              lista: ["Don’t straighten your collar"],
              textoA: "",
              textoD: "",
              tamano: 23,
            },
            complejo2: {
              lista: ["Let’s straighten your collar"],
              textoA: "",
              textoD: "",
              tamano: 23,
            },
          },
          {
            AFIRMATIVA: "Make sure to do it",
            TRADUCCIÓN: "Asegúrate de hacerlo",
            complejo1: {
              lista: ["Don’t make sure to do it"],
              textoA: "",
              textoD: "",
              tamano: 22,
            },
            complejo2: {
              lista: ["Let’s make sure to do it"],
              textoA: "",
              textoD: "",
              tamano: 21,
            },
          },
          {
            AFIRMATIVA: "Enjoy it",
            TRADUCCIÓN: "Disfrútalo",
            complejo1: {
              lista: ["Don't Enjoy it"],
              textoA: "",
              textoD: "",
              tamano: 16,
            },
            complejo2: {
              lista: ["Let’s Enjoy it"],
              textoA: "",
              textoD: "",
              tamano: 16,
            },
          },
        ],
      },
      palabrasP81: [
        "STOP",
        "PLAY",
        "EAT",
        "SLEEP",
        "SING",
        "THINK OF",
        "TALK TO",
        "STUDY",
      ],
      palabrasP81P2: [
        "- Don't talk to her",
        "- Go quickly",
        "- Calm down",
        "- Don't smoke in here",
        "- Don't say that",
        "- Let's go",
        "- Don't put off for tomorrow what you can do today",
        "- Call me back tomorrow morning",
        "- Read",
        "- Believe me",
        "- Let's go for a walk",
        "- Don't write",
      ],
      tablaPrueba: [
        {
          texto:
            "Solo es necesario usar el verbo para ordenar una acción a la persona con quien se habla. No se usa subjeto.",
          palabras: [
            "<span class='colorLetraRojo'>Go:</span> <br/>Vete",
            "<span class='colorLetraRojo'>Look at me:</span> <br/>Mírame",
            "<span class='colorLetraRojo'>Listen:</span> <br/>Escucha",
            "<span class='colorLetraRojo'>Sit down:</span> <br/>Siéntate",
          ],
        },
        {
          texto:
            "Si queremos decir no a esas acciones anteriores solo basta con agregar la negación DON´T antes del verbo.",
          palabras: [
            "<span class='colorLetraRojo'>Don’t</span><span class='colorLetraBlue'>go:</span> No vayas |",
            "<span class='colorLetraRojo'>Don’t</span><span class='colorLetraBlue'>look at me:</span> No me mires |",
            "<span class='colorLetraRojo'>Don’t</span><span class='colorLetraBlue'>listen:</span> No escuches |",
          ],
        },
        {
          texto:
            "Si queremos una acción compartida; es decir que la persona con quien hablas haga lo mismo que tú, solo usa LET´S al iniciar la acción seguida del verbo. Esta palabra LET´S hace que un verbo termine en MOS.",
          palabras: [
            "<span class='colorLetraRojo'>Let's</span> <span class='colorLetraBlue'>go:</span> Vamos |",
            "<span class='colorLetraRojo'>Let's</span> <span class='colorLetraBlue'>eat:</span> Comamos|",
            "<span class='colorLetraRojo'>Let's</span> <span class='colorLetraBlue'>sit down:</span> Sentémonos|",
          ],
        },
      ],
      tablaP79: {
        fields: [
          { key: "html", label: "THE MAGIC NUMBER" },
          { key: "present", label: "PRESENT", thClass: "Yelow" },
          { key: "presentsE", label: "PRESENTS-ES-IES", thClass: "Yelow" },
          { key: "past", label: "PAST", thClass: "Red" },
          { key: "participle", label: "PARTICIPLE", thClass: "Blue" },
          { key: "progresive", label: "PROGRESIVE", thClass: "Blue2" },
        ],
        bordered: true,
        items: [
          {
            html:
              "<p class=parrafoTabla>Oraciones en presente</p>",
            present: "Go",
          },
          {
            html:
              "<p class=parrafoTabla>Oraciones en presente afirmativo con <strong>she, he, it</strong></p>",
            presentsE: "Goes",
          },
          {
            html:
              "<p class=parrafoTabla>Oraciones con modificadores <strong> Do-Does-Did-Will-Would </strong> </p>",
            present: "Go",
          },
          {
            html:
              "<p class=parrafoTabla>Oraciones con S.P.V <strong> Can-Could-Should-Must</strong> </p>",
            present: "Go",
          },
          {
            html:
              "<<p class=parrafoTabla>Oraciones en pasado afirmativo</p>",
            past: "Went",
          },
          {
            html:
              "<p class=parrafoTabla>Oraciones con S.P.V <strong> Have-Has-Had </strong></p>",
            participle: "Gone",
          },
          {
            html:
              "<p class=parrafoTabla>Oraciones con S.P.V <strong> Is-Am-Are-Was-Were </strong></p>",
            progresive: "Going",
          },
        ],
      },
      tablaP79P2: {
        fields: [
          { key: "html", label: "MODIFICADORES" },
          { key: "present", label: "PRESENT", thClass: "Yelow" },
          { key: "present2", label: "PRESENT", thClass: "Red" },
          { key: "past", label: "PAST", thClass: "Blue" },
          { key: "futuro", label: "FUTURO", thClass: "Blue2" },
          { key: "ria", label: "'RÍA'", thClass: "White" },
        ],
        bordered: true,
        items: [
          {
            html:
              "<p class = parrafoTabla> Do </strong> you work</p>",
            present: "¿Trabajas?",
          },
          {
            html:
              "<p class = parrafoTabla><strong>Does</strong> she work?</p>",
            present2: "¿Ella trabaja?",
          },
          {
            html:
              "<p class = parrafoTabla><strong> Did </strong> you work? </p>",
            past: "¿Trabajaste?",
          },
          {
            html:
              "<p class = parrafoTabla><strong> Will </strong> you work? </p>",
            futuro: "¿Trabajarás?",
          },
          {
            html:
              "<p class = parrafoTabla> <strong> Would </strong> you work? </p>",
            ria: "¿Trabajarías?",
          },
        ],
      },
      preguntasCompletarP24: {
        nombre: "preguntasCompletarP24",
        items: [
          {
            esperado: ["Go"],
            textoA: "1. ve",
            textoD: "",
            tamano: 12,
          },
          {
            esperado: ["don't go"],
            textoA: "2. no vayas ",
            textoD: "",
            tamano: 20,
          },
          {
            esperado: ["let's go"],
            textoA: "3. vamos",
            textoD: "",
            tamano: 17,
          },
          {
            esperado: ["let's not go"],
            textoA: "4. No vayamos ",
            textoD: "",
            tamano: 23,
          },
          {
            esperado: ["don't do it"],
            textoA: "5. No lo hagas",
            textoD: "",
            tamano: 23,
          },
          {
            esperado: ["do it"],
            textoA: "6. Hazlo",
            textoD: "",
            tamano: 15,
          },
          {
            esperado: ["let's do it"],
            textoA: "7. Hagámoslo",
            textoD: "",
            tamano: 21,
          },
          {
            esperado: ["call me"],
            textoA: "8. Llámame",
            textoD: "",
            tamano: 19,
          },
          {
            esperado: ["don't call me"],
            textoA: "9. No me llames",
            textoD: "",
            tamano: 25,
          },
          {
            esperado: ["let's call her"],
            textoA: "10. Llamémosla",
            textoD: "",
            tamano: 24,
          },
          {
            esperado: ["close the door"],
            textoA: "11. cierra la puerta",
            textoD: "",
            tamano: 27,
          },
          {
            esperado: ["don't close the door"],
            textoA: "12. No cierres la puerta",
            textoD: "",
            tamano: 33,
          },
          {
            esperado: ["listen to music"],
            textoA: "13. Escucha la música",
            textoD: "",
            tamano: 29,
          },
          {
            esperado: ["don't listen to me"],
            textoA: "14 no me escuches",
            textoD: "",
            tamano: 29,
          },
        ],
      },
      preguntasCompletarP81: {
        nombre: "preguntasCompletarP81",
        items: [
          {
            esperado: ["stop"],
            textoA: "1. Hey",
            textoD: ", please! - Hola detente por favor",
            tamano: 33,
          },
          {
            esperado: ["play"],
            textoA: "2. let's",
            textoD: "cards to night! -   Juguemos cartas esta noche",
            tamano: 40,
          },
          {
            esperado: ["eat"],
            textoA: "3. don't",
            textoD: "that, it´s expired! -  No te comas eso, está vencido",
            tamano: 42,
          },
          {
            esperado: ["sleep"],
            textoA: "4. ",
            textoD:"well; tomorrow it will be a long day! - Duerme bien, manana será un largo día",
            tamano: 56,
          },
          {
            esperado: ["study"],
            textoA: "5. let's",
            textoD: "for the test! - Estudiemos para el examen",
            tamano: 38,
          },
          {
            esperado: ["sing"],
            textoA: "6. Please, don't",
            textoD: "out loud - no cantes tan alto",
            tamano: 35,
          },
          {
            esperado: ["think of"],
            textoA: "7. ",
            textoD: "me honey! - Piensa en mi carino",
            tamano: 30,
          },
          {
            esperado: ["talk to"],
            textoA: "8. don't",
            textoD: "her - No hables con ella",
            tamano: 29,
          },
        ],
      },
      preguntasCompletarP81P2: {
        nombre: "preguntasCompletarP81P2",
        items: [
          {
            esperado: ["go quickly"],
            textoA: "1. Ve rápido",
            textoD: "",
            tamano: 21,
          },
          {
            esperado: ["don't say that"],
            textoA: "2. No digas eso",
            textoD: "",
            tamano: 25,
          },
          {
            esperado: ["let's go"],
            textoA: "3. Vamos",
            textoD: "",
            tamano: 17,
          },
          {
            esperado: ["let's go for a walk"],
            textoA: "4. Vamos a dar un paseo",
            textoD: "",
            tamano: 32,
          },
          {
            esperado: ["don't write"],
            textoA: "5. No escribas",
            textoD: "",
            tamano: 22,
          },
          {
            esperado: ["read"],
            textoA: "6. Lee",
            textoD: "",
            tamano: 14,
          },
          {
            esperado: ["don't smoke in here"],
            textoA: "7. No fumes aquí adentro",
            textoD: "",
            tamano: 34,
          },
          {
            esperado: ["call me back tomorrow morning"],
            textoA: "8. Devuélveme la llamada mañana en la mañana",
            textoD: "",
            tamano: 40,
          },
          {
            esperado: ["calm down"],
            textoA: "9. Cálmate",
            textoD: "",
            tamano: 20,
          },
          {
            esperado: ["don’t put off for tomorrow what you can do today"],
            textoA: "10. No dejes para manana lo que puedas hacer hoy",
            textoD: "",
            tamano: 65,
          },
        ],
      },
    };
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

/deep/ .colorText {
  color: white;
}

/deep/ .Blue {
  background-color: #002060;
  color: white;
}
/deep/ .Red {
  background-color: crimson;
  color: white;
}
/deep/ .Yelow {
  background-color: #ffc000;
  color: white;
}
/deep/ .Green {
  background-color: chartreuse;
}
/deep/ .Blue2 {
  background-color: #00b0f0;
  color: white;
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
/deep/.colorLetraBlue {
  color: blue;
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

#textoCompromiso {
  text-align: left;
  margin-bottom: 1em;
  font-size: 1.5em;
}

.textList {
  font-size: 1.5em;
}
</style>
