<template>
<div>
    <div class="row" style="margin-top:-5em;">
        <h3 id="subTitulo">MEZCLAS CON LAS FORMAS DEL VERBO</h3>
    </div>
    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-10 row">
            <div class="col-sm-3" v-for="item in tablasTiempoP23" style="margin:0; padding:0;">
                <listaIndex :tabla="item" />
            </div>
        </div>
    </div>

    <div class="row">
        <h3 id="subTitulo">PRACTICE</h3>
    </div>
    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-10" id="text">
            <i class="fa fa-diamond" style="font-size: 1.5em;"></i>
            <a id="textPractice">Completar con la forma del verbo correcta</a>
        </div>
    </div>

    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-10 row">
            <tablaTC :cuestionario="tablaP23" />
        </div>
    </div>

    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-10" id="text">
            <i class="fa fa-diamond" style="font-size: 1.5em;"></i>
            <a id="textPractice">
                Escribe el modificador correspondiente
                <a class="colorLetraRojo">DO-DOES-DID-WILL-WOULD</a>
            </a>
        </div>
    </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP24.items">
        <div class="col-sm-1"></div>
        <div class="col-sm-10">
            <div :class="'col-sm-'+item.tamaño">
                <inputChecked :esperado="item.esperado" :name="preguntasCompletarP24.nombre+index" :conTexto="true" :textoA="item.textoA" :textoD="item.textoD" />
            </div>
        </div>
    </div>

    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-10" id="text">
            <i class="fa fa-diamond" style="font-size: 1.5em;"></i>
            <a id="textPractice">Marca la negacion correcta</a>
        </div>
    </div>

    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-6">
            <opcionMultiple id="text" :options="$data.cuestionarioP24" :rEsperadas="$data.respuestasCuestionarioP24" @respuestas="$data.mensajeRespuestasP24 = $event" />
        </div>
        <b-modal ref="my-modalP18" hide-footer title="RESULTADO">{{mensajeRespuestasP24 }}</b-modal>
        <div class="col-sm-1"></div>
    </div>
    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-3">
            <b-button variant="primary" @click="showModal('my-modalP18')">VERIFICAR PREGUNTAS</b-button>
        </div>
    </div>

    <div class="row">
        <h3 id="subTitulo">CONCLUIR USO DE LA LÓGICA A TRAVÉS DEL “2 4 5 12”</h3>
    </div>

    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-10">
            <ul>
                <dt v-for="item in listaConclusionP25" id="textoCompromiso">
                    <i class="fa fa-diamond"></i>
                    <a>{{ item }}</a>
                </dt>
            </ul>
        </div>
    </div>

    <div class="row">
        <h3 id="subTitulo">PRACTICE</h3>
    </div>
    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-10" id="text">
            <i class="fa fa-diamond" style="font-size: 1.5em;"></i>
            <a id="textPractice">Ubica la forma correspondiente del verbo en las siguientes oraciones.</a>
        </div>
    </div>

    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-10 row">
            <div class="col-sm-12" v-for="(item, index) in tablasP25" style="margin-bottom:2em;">
                <tablaTC :cuestionario="item" />
            </div>
        </div>
    </div>

    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-10" id="text">
            <i class="fa fa-diamond" style="font-size: 1.5em;"></i>
            <a id="textPractice">Completa las siguientes oraciones con la forma correcta del verbo.</a>
        </div>
    </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP26.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div :class="'col-sm-'+item.tamaño">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP26.nombre+index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
          />
        </div>
    </div>
</div>
</template>

<script>
     },  fields: [
            { key: "complejo1", label: "IS-AM-ARE-WAS-WERE" },
            { key: "A", label: "4.1" },
            { key: "B", label: "4.2" },
            { key 
          ],
          items: [
            {
              complejo1: {
                lista: ["Thinking"],
                textoA: "What are you",
                textoD: "about?",
                tamano: 22,
              },
              A: "Think",
              B: "Thought",
              C: "Thought",
              D: "Thinking",
            },
            {
              complejo1: {
                lista: ["Going"],
                textoA: "Where were you",
                textoD: "?",
                tamano: 24,
                audio: "/cursos/curso1/leccion4/page25/AC1P24R13.mp3"
                audio: "/cursos/curso1/leccion4/page25/AC1P24R14.mp3"
              },
              A: "Make",
              B: "Made",
              C:  
            },   
            {
              complejo1: {
                lista: ["Paying"],
                textoA: "Sorry! I was not",
                textoD: "attention",
                tamano: 25,
              },
              A: "Pay",
              B: "Paid",
              C: "Paid",
              D: "Paying",
            },         
          ],
        }
      ],
      listaConclusionP25: [
        "Siempre recuerda para que sirven los modificadores (auxiliares). para preguntar o negar.",
        "Recuerda que un verbo se usa en pasado solo en afirmación.",
        "Los verbos con poderes se niegan solos, ellos no necesitan auxiliares.",
         PRESENT: "Drive",
            PAST: "Drove",
            PARTICIPLE: "Driven",
            PROGRESSIVE: "Driving",
            complejo1: {
              lista: ["Driven"],
              textoA: "She has never",
              textoD: "a car",
              tamano: 23,
            },
          },
          {
            SPANISH: "Aprender",
            PRESENT: "Learn",
            PAST: "Learned",
            PARTICIPLE: "Learned",
            PROGRESSIVE: "Learning",
            complejo1: {
              lista: ["Learn"],
              textoA: "You need to",
              textoD: "the numbers in English",
              tamano: 30,
              audio: '/cursos/curso1/leccion4/audios/page23/AC1P22R16.mp3'
