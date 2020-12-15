<template>
  <div>
    <div class="row">
      <h4 id="subTitulo">FAMILIARIZARSE CON EL NÚMERO MÁGICO.</h4>
    </div>

    <div class="row">
      <div class="row">
        <div class="col-sm-2"></div>
        <div class="col-sm-2">
          <div class="col-sm-7" id="numeroMagico2">2</div>
          <h3 style="margin-top: 0.4em">Types Of Verbs</h3>
          <listaIndex :tabla="$data.tablasNumeroMagicoP14[0]" />
        </div>
        <div class="col-sm-2">
          <div class="col-sm-7" id="numeroMagico4">4</div>
          <h3 style="margin-top: 0.4em">Spelling Forms</h3>
          <listaIndex :tabla="$data.tablasNumeroMagicoP14[1]" />
        </div>
        <div class="col-sm-2">
          <div class="col-sm-7" id="numeroMagico5">5</div>
          <h3 style="margin-top: 0.4em">Tense Modifiers</h3>
          <listaIndex :tabla="$data.tablasNumeroMagicoP14[2]" />
        </div>
        <div class="col-sm-2">
          <div class="col-sm-7" id="numeroMagico12">12</div>
          <h4 style="margin-top: 0.4em">Super Power Verbs</h4>
          <div class="overflow-auto" style="max-height: 350px">
            <listaIndex :tabla="$data.tablasNumeroMagicoP14[3]" />
          </div>
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <iframe
          width="100%"
          height="440"
          src="https://www.youtube.com/embed/YvkfIwFzXVU"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-2" id="subTitulo">
        <h3>PRACTICE</h3>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-4" id="text">
        <i class="fa fa-diamond" style="font-size: 1.5em"></i>
        <a id="textPractice">Elige la respuesta correcta</a>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" id="text">
        <opcionMultiple
          :options="$data.cuestionarioP13"
          :rEsperadas="$data.respuestasCuestionarioP13"
          @respuestas="mensajeRespuestasP13 = $event"
        />
      </div>
      <b-modal ref="my-modal1" hide-footer title="RESULTADO">{{
        mensajeRespuestasP13
      }}</b-modal>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modal1')"
          >VERIFICAR PREGUNTAS</b-button
        >
      </div>
    </div>

    <div class="row">
      <div class="col-sm-8" id="subTitulo">
        <h3>ANALIZAR Y COMPRENDER EL NÚMERO MÁGICO.</h3>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <ul>
          <dt v-for="(item, index) in $data.listadoP14" id="textoCompromiso">
            <i class="fa fa-diamond"></i>
            <a v-html="item">{{ item }}</a>
            <div class="row" v-if="index == 3">
              <div class="col-sm-1"></div>
              <div class="col-sm-10">
                <ul>
                  <dt v-for="item in $data.subListadoP14">
                    <i class="fa fa-check"></i>
                    <a v-html="item">{{ item }}</a>
                  </dt>
                </ul>
              </div>
            </div>
          </dt>
        </ul>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div
          class="col-sm-3"
          v-for="item in $data.tablasTiempoP15"
          style="margin: 0; padding: 0"
        >
          <listaIndex :tabla="item" />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-8" id="subTitulo">
        <h3>PRACTICE</h3>
      </div>
    </div>

    <b-row>
      <b-col md="1"> </b-col>

      <b-col md="11">
        <div class="row">
          <b-row style="margin: 0">
            <b-col md="auto" style="padding: 0">
              <i class="fa fa-diamond" style="padding-top: 0.8em"></i>
            </b-col>
            <b-col md="auto">
              <inputCEnriquecido :object="inputCEP15N1" />
            </b-col>
          </b-row>

          <div class="row">
            <div style="margin-top: -20px">
              <inputChecked
                :resuelto="false"
                :esperado="['Presente']"
                :conTexto="true"
                textoD=","
                :tamano="14"
              />
            </div>
            <b-col md="auto" style="padding: 0px; margin-top: -20px">
              <inputCEnriquecido :object="inputCEP15N2" />
            </b-col>
            <b-col md="auto" style="padding: 0px; margin-top: -20px">
              <inputChecked
                :resuelto="false"
                :esperado="['Progresivo']"
                :conTexto="true"
                textoD="."
                :tamano="14"
              />
            </b-col>
          </div>
        </div>

        <div class="row">
          <b-row style="margin: 0">
            <b-col md="auto" style="padding: 0">
              <i class="fa fa-diamond" style="padding-top: 0.8em"></i>
            </b-col>
            <b-col md="auto">
              <inputCEnriquecido :object="inputCEP15N3" />
            </b-col>
          </b-row>

          <div class="row">
            <div style="margin-top: -20px">
              <inputCEnriquecido :object="inputCEP15N4" />
            </div>
            <b-col md="auto" style="padding: 0px; margin-top: -20px">
              <inputChecked
                :resuelto="false"
                :esperado="['Must']"
                :conTexto="true"
                textoD="."
                :tamano="11"
              />
            </b-col>
          </div>
        </div>

        <div class="row">
          <b-row style="margin: 0">
            <b-col md="auto" style="padding: 0">
              <i class="fa fa-diamond" style="padding-top: 0.8em"></i>
            </b-col>
            <b-col md="auto">
              <inputCEnriquecido :object="inputCEP15N5" />
            </b-col>
          </b-row>

          <div class="row">
            <div style="margin-top: -20px">
              <inputCEnriquecido :object="inputCEP15N6" />
            </div>
            <b-col md="auto" style="padding: 0px; margin-top: -20px">
              <inputChecked
                :resuelto="false"
                :esperado="['Would']"
                :conTexto="true"
                textoD="."
                :tamano="13"
              />
            </b-col>
          </div>
        </div>

        <div class="row">
          <b-row style="margin: 0">
            <b-col md="auto" style="padding: 0">
              <i class="fa fa-diamond" style="padding-top: 0.4em"></i>
            </b-col>
            <b-col md="auto">
              <p class="parrafoIC">
                Los
                <span
                  class="colorLetraRojo"
                  style="margin-left: 4px; margin-right: 4px"
                  >auxiliares</span
                >se usan para preguntar y negar.
              </p>
            </b-col>
          </b-row>

          <b-row>
            <b-col md="1"> </b-col>
            <b-col md="11">
              <b-row>
                <b-col md="auto">
                  <i class="fa fa-diamond" style="padding-top: 2em"></i>
                </b-col>
                <b-col md="auto" style="padding-top: 1.5em">
                  <inputChecked
                    :resuelto="false"
                    :esperado="['Presente']"
                    :conTexto="true"
                    textoA="El <span class='colorLetraRojo'>Do</span>es para preguntar en"
                    textoD="y su negación es <span class='colorLetraRojo'>don´t</span>."
                    :tamano="44"
                  />
                </b-col>
              </b-row>
              <b-row>
                <b-col md="auto">
                  <i class="fa fa-diamond" style="padding-top: 0.4em"></i>
                </b-col>
                <b-col md="auto">
                  <inputChecked
                    :resuelto="false"
                    :esperado="['Does']"
                    :conTexto="true"
                    textoA="El"
                    textoD="para preguntar en presente, pero con she, he, it, y su negación es <span class='colorLetraRojo'>doesn´t</span> . "
                    :tamano="56"
                  />
                </b-col>
              </b-row>

              <b-row>
                <b-col md="auto">
                  <i class="fa fa-diamond" style="padding-top: 0.4em"></i>
                </b-col>
                <b-col md="auto">
                  <inputCEnriquecido :object="inputCEP15N7" />
                </b-col>
              </b-row>

              <b-row>
                <b-col md="auto">
                  <i class="fa fa-diamond" style="padding-top: 0.4em"></i>
                </b-col>
                <b-col md="auto">
                  <inputCEnriquecido :object="inputCEP15N8" />
                </b-col>
              </b-row>

              <b-row>
                <b-col md="auto">
                  <i class="fa fa-diamond" style="padding-top: 0.4em"></i>
                </b-col>
                <b-col md="auto">
                  <inputChecked
                    :resuelto="false"
                    :esperado="['Ría']"
                    :conTexto="true"
                    textoA="El <span class='colorLetraRojo'>Would</span>se usa para preguntar con un verbo que termina en “"
                    textoD="” – ejemplo: comería,"
                    :tamano="59"
                  />
                </b-col>
              </b-row>

              <b-row>
                <b-col md="auto" style="margin-top: -30px">
                  <inputChecked
                    :resuelto="false"
                    :esperado="['Wouldn´t']"
                    :conTexto="true"
                    textoA="haría, dormiría, jugaría etc y su negación es"
                    textoD="."
                    :tamano="39"
                  />
                </b-col>
              </b-row>
            </b-col>
          </b-row>
        </div>

        <div class="row">
          <b-row style="margin: 0">
            <b-col md="auto" style="padding: 0">
              <i class="fa fa-diamond" style="padding-top: 0.8em"></i>
            </b-col>
            <b-col md="auto">
              <inputCEnriquecido :object="inputCEP15N9" />
            </b-col>
          </b-row>

          <div class="row">
            <div class="parrafoIC" style="margin-top: -30px">
              y si es irregular se aprende.
            </div>
          </div>
        </div>

        <div class="row">
          <b-row style="margin: 0">
            <b-col md="auto" style="padding: 0">
              <i class="fa fa-diamond" style="padding-top: 0.8em"></i>
            </b-col>
            <b-col md="auto">
              <inputChecked
                :resuelto="false"
                :esperado="['Has']"
                :conTexto="true"
                textoA="Un verbo se usa en su forma participio únicamente después de los verbos con poder <span class='colorLetraRojo'>“have</span>,"
                textoD="<span class='colorLetraRojo'>o</span>"
                :tamano="66"
              />
            </b-col>
          </b-row>

          <div class="row" style="margin-top: -20px">
            <div>
              <inputChecked
                :resuelto="false"
                :esperado="['Had']"
                :conTexto="true"
                textoD="<span class='colorLetraRojo'>.”</span>Si es regular se le agrega “ed” y si es irregular se aprende."
                :tamano="46"
              />
            </div>
          </div>
        </div>

        <div class="row" style="margin-top: -8px">
          <b-row style="margin: 0">
            <b-col md="auto" style="padding: 0">
              <i class="fa fa-diamond" style="padding-top: 0.8em"></i>
            </b-col>
            <b-col md="auto">
              <inputChecked
                :resuelto="false"
                :esperado="['Auxiliares']"
                :conTexto="true"
                textoA="Los verbos con poder no necesitan"
                textoD="en una pregunta, afirmación ni negación y son los únicos"
                :tamano="66"
              />
            </b-col>
          </b-row>
        </div>
        <div class="row" style="margin-top: -20px">
          <div class="parrafoIC">
            que se niegan al poner la palabra “NOT” delante de ellos y existen
            doce.
          </div>
        </div>

        <div class="row" style="margin-top: 45px">
          <b-row style="margin: 0">
            <b-col md="auto" style="padding: 0">
              <i class="fa fa-diamond" style="padding-top: 0.8em"></i>
            </b-col>
            <b-col md="auto">
              <inputCEnriquecido :object="inputCEP15N10" />
            </b-col>
          </b-row>
        </div>
        <div class="row" style="margin-top: -40px">
          <div>
            <inputCEnriquecido :object="inputCEP15N11" />
          </div>
          <div style="margin-left: 1em">
            <inputChecked
              :resuelto="false"
              :esperado="['ING']"
              :conTexto="true"
              textoA="“"
              textoD="” al final."
              :tamano="15"
            />
          </div>
        </div>
      </b-col>
    </b-row>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div
          class="col-sm-3"
          v-for="item in $data.tablasTiempoPreguntaP15"
          style="margin: 0; padding: 0"
        >
          <listaIndex :tabla="item" class="fuenteComponentes" />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-12" id="subTitulo">
        <h3>CUESTIONARIO SOBRE EL NÚMERO MÁGICO.</h3>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-4" id="text">
        <i class="fa fa-diamond" style="font-size: 1.5em"></i>
        <a id="textPractice">Elige la respuesta correcta</a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" id="text">
        <opcionMultiple
          :options="$data.cuestionarioP17"
          :rEsperadas="$data.respuestasCuestionarioP17"
          @respuestas="$data.mensajeRespuestasP17 = $event"
        />
      </div>
      <div class="col-sm-1"></div>
      <b-modal ref="my-modal1" hide-footer title="RESULTADO">{{
        mensajeRespuestasP17
      }}</b-modal>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modal1')"
          >VERIFICAR PREGUNTAS</b-button
        >
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" style="text-align: left">
        <legend
          id="5__BV_label_"
          tabindex="-1"
          class="bv-no-focus-ring col-form-label pt-0 col-form-label-lg labelPregunta"
        >
          7. Escriba los verbos con súper poder
        </legend>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <listaIndex :tabla="$data.tablaEsperadosP17" />
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" style="text-align: left">
        <legend
          id="5__BV_label_"
          tabindex="-1"
          class="bv-no-focus-ring col-form-label pt-0 col-form-label-lg labelPregunta"
        >
          8. Escriba las cuatro formas del verbo.
        </legend>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <listaIndex :tabla="$data.tablaEsperadosP17a" />
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" style="text-align: left">
        <legend
          id="5__BV_label_"
          tabindex="-1"
          class="bv-no-focus-ring col-form-label pt-0 col-form-label-lg labelPregunta"
        >
          9. Escribe los 5 auxiliares del inglés para preguntar y negar.
        </legend>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11">
        <tablaTC :cuestionario ="tablaPregunta8P17"/>
      </div>
    </div>
  </div>
</template>

<script>
import listaIndex from "./listaIndex";
import tablaTC from "./tablaTraduccionCodigos";
import opcionMultiple from "./opcionMultiple";
import inputChecked from "./inputChecked";
import inputCEnriquecido from "./inputCEnriquecido";
import InputCEnriquecido from "./inputCEnriquecido.vue";
export default {
  components: {
    listaIndex,
    tablaTC,
    opcionMultiple,
    inputChecked,
    inputCEnriquecido,
  },
  data() {
    return {
      tablaPregunta8P17: {
        fields: [

          {
            key: "complejo1",
            label: "En presente."
          },
          { 
             key: "complejo2",
             label: "En presente con she, he e it."
          },
          { 
             key: "complejo3",
             label: "En pasado."
          },
          { 
             key: "complejo4",
             label: "En futuro."
          },
           { 
             key: "complejo5",
             label: "Un verbo termina en ría."
          },
          
        ],
        items:[
          {
            complejo1:{
              
              lista: [
                "Do"
              ],
              tamano:10
            },
             complejo2:{
              
              lista: [
                "Does"
              ],
              tamano:12
            },
             complejo3:{
              
              lista: [
                "Did"
              ],
              tamano:10
            },
             complejo4:{
              
              lista: [
                "Will"
              ],
              tamano:10
            },
             complejo5:{
              
              lista: [
                "Would"
              ],
              tamano:12
            },
            
          }
        ]
      },

      tablaEsperadosP17a: {
        items: ["presente", "pasado", "participio", "progresivo"],
        refs: "tablaEsperadosP17a",
        camposInput: true,
        fields: [
          // A virtual column that doesn't exist in items
          // A column that needs custom formatting
          { key: "Z", label: "T", thClass: "noHead" },
        ],
      },
      tablaEsperadosP17: {
        items: [
          "have",
          "has",
          "had",
          "is",
          "am",
          "are",
          "were",
          "was",
          "can",
          "could",
          "must",
          "should",
        ],
        refs: "tablaEsperadosP17",
        camposInput: true,
        fields: [
          // A virtual column that doesn't exist in items
          // A column that needs custom formatting
          { key: "Z", label: "T", thClass: "noHead" },
        ],
      },

      tablasTiempoPreguntaP15: [
        {
          refs: "tablasTiempoPreguntaP15a",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "PRESENT", thClass: "colorLetraRojo" },
          ],
          items: [
            "Do",
            "Does",
            "Did",
            "Will",
            "Would",
            "Can",
            "Could",
            "Should",
            "Must",
          ],
        },
        {
          bordered: false,
          camposInput: true,
          refs: "tablasTiempoPreguntaP15b",
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "PAST", thClass: "colorLetraRojo" },
          ],
          items: ["Oraciones Afirmativas"],
        },
        {
          refs: "tablasTiempoPreguntaP15c",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "PARTICIPLE " + "'ado-ido'",
              thClass: "colorLetraRojo",
            },
          ],
          items: ["Have", "Has", "Had"],
        },
        {
          refs: "tablasTiempoPreguntaP15d",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "PROGRESSIVE \n 'ando-endo'",
              thClass: "colorLetraRojo",
            },
          ],
          items: ["Is", "Am", "Are", "Was", "Were"],
        },
      ],

      inputCEP15N1: {
        lista1: ["Regulares"],
        lista2: ["Irregulares"],
        name: "inputCEP15N1",
        textoA: "Hay dos tipos de verbos ",
        textoD: "e",
        textoD2: "y ambos tienen 4 formas:",
        tamano1: 30,
        tamano2: 30,
      },

      inputCEP15N2: {
        lista1: ["Pasado"],
        lista2: ["Participio"],
        name: "inputCEP15N2",
        textoA: "",
        textoD: ",",
        textoD2: "y",
        tamano1: 13,
        tamano2: 14,
      },

      inputCEP15N3: {
        lista1: ["Presente"],
        lista2: ["Can"],
        name: "inputCEP15N3",
        textoA: "Los verbos en",
        textoD: "se usan después de los verbos con poder",
        textoD2: ",",
        tamano1: 46,
        tamano2: 11,
      },

      inputCEP15N4: {
        lista1: ["Could"],
        lista2: ["Should"],
        name: "inputCEP15N4",
        textoA: "",
        textoD: ",",
        textoD2: "o",
        tamano1: 12,
        tamano2: 13,
      },

      inputCEP15N5: {
        lista1: ["Do"],
        lista2: ["Does"],
        name: "inputCEP15N5",
        textoA: "Los verbos en presente también se usan con los auxiliares",
        textoD: ",",
        textoD2: ",",
        tamano1: 44,
        tamano2: 12,
      },

      inputCEP15N6: {
        lista1: ["Did"],
        lista2: ["Will"],
        name: "inputCEP15N6",
        textoA: "",
        textoD: ",",
        textoD2: "o",
        tamano1: 10,
        tamano2: 11,
      },

      inputCEP15N7: {
        lista1: ["Pasado"],
        lista2: ["Didn´t"],
        name: "inputCEP15N7",
        textoA:
          "El <span class='colorLetraRojo'>Did</span> es para preguntar en",
        textoD: "y su negación es",
        textoD2: ".",
        tamano1: 39,
        tamano2: 11,
      },

      inputCEP15N8: {
        lista1: ["Will"],
        lista2: ["Won´t"],
        name: "inputCEP15N8",
        textoA: "El",
        textoD: "para preguntar en un futuro y el",
        textoD2: "para negar.",
        tamano1: 29,
        tamano2: 18,
      },

      inputCEP15N9: {
        lista1: ["Afirmación"],
        lista2: ["Ed"],
        name: "inputCEP15N9",
        textoA:
          "Un verbo se usa en forma <span class='colorLetraRojo'>Pasado</span> solo en una",
        textoD: "; si es regular se agrega “",
        textoD2: "”",
        tamano1: 56,
        tamano2: 10,
      },

      inputCEP15N10: {
        lista1: ["Am"],
        lista2: ["Are"],
        name: "inputCEP15N10",
        textoA:
          "Un verbo se usa en su forma progresiva después de los verbos con poder <span class='colorLetraRojo'>IS,</span>",
        textoD: ",",
        textoD2: ",",
        tamano1: 56,
        tamano2: 10,
      },

      inputCEP15N11: {
        lista1: ["Was"],
        lista2: ["Were"],
        name: "inputCEP15N11",
        textoD: " y",
        textoD2: "y al verbo se le agrega",
        tamano1: 11,
        tamano2: 24,
      },

      tablasTiempoP15: [
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "PRESENT", thClass: "colorLetraRojo" },
          ],
          items: [
            { Z: "Do" },
            { Z: "Does" },
            { Z: "Did" },
            { Z: "Will" },
            { Z: "Would" },
            { Z: "Can" },
            { Z: "Could" },
            { Z: "Should" },
            { Z: "Must" },
          ],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "PAST", thClass: "colorLetraRojo" },
          ],
          items: [{ Z: "Oraciones Afirmativas" }],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "PARTICIPLE " + "'ado-ido'",
              thClass: "colorLetraRojo",
            },
          ],
          items: [{ Z: "Have" }, { Z: "Has" }, { Z: "Had" }],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "PROGRESSIVE \n 'ando-endo'",
              thClass: "colorLetraRojo",
            },
          ],
          items: [
            { Z: "Is" },
            { Z: "Am" },
            { Z: "Are" },
            { Z: "Was" },
            { Z: "Were" },
          ],
        },
      ],
      listadoP14: [
        "Hay dos tipos de verbos <span class='colorLetraRojo'>Regulares</span> e  <span class='colorLetraRojo'>Irregulares</span>, y ambos tienen cuatro formas <span class='colorLetraRojo'>Presente</span>, <span class='colorLetraRojo'>Pasado</span>, <span class='colorLetraRojo'>Participio</span> y <span class='colorLetraRojo'>Progresivo</span>.",
        "Los verbos en <span class='colorLetraRojo'>Presente</span> se usan después de los verbos con poder <span class='colorLetraRojo'>Can</span>, <span class='colorLetraRojo'>Could</span>, <span class='colorLetraRojo'>Should</span> o <span class='colorLetraRojo'>Must</span>.",
        "Los verbos en presente también se usan con los auxiliares <span class='colorLetraRojo'>Do</span>, <span class='colorLetraRojo'>Does</span>, <span class='colorLetraRojo'>Did</span>, <span class='colorLetraRojo'>Will</span> o <span class='colorLetraRojo'>Would</span>.",
        "Los <span class='colorLetraRojo'>auxiliares</span> se usan para preguntar y negar.",
        "Un verbo se usa en forma <span class='colorLetraRojo'>Pasado</span> solo en una <span class='colorLetraRojo'>afirmacion</span>; si es regular se agrega “ed” y si es irregular se aprende.",
        "Un verbo se usa en su forma participio únicamente después de los verbos con poder  <span class='colorLetraRojo'>'have, has, had'</span> " +
          "Si es regular se le agrega 'ed' y si es irregular se aprende.",
        "Los verbos con poder no necesitan auxiliares en una pregunta, afirmación ni negación y son los únicos que se niegan al poner la palabra “NOT” delante de ellos y existen doce.",
        "Un verbo se usa en su forma progresiva después de los verbos con poder <span class='colorLetraRojo'>IS, AM, ARE, WAS Y WERE</span> y al verbo se le agrega “ING” al final.",
      ],
      subListadoP14: [
        "El <span class='colorLetraRojo'>Do</span> es para preguntar en presente y su negación es <span class='colorLetraRojo'>don't</span>",
        "El <span class='colorLetraRojo'>Does</span> es para preguntar en presente, pero con she, he, it, y su negación es <span class='colorLetraRojo'>desn't</span> .",
        "El <span class='colorLetraRojo'>Did</span> para preguntar en pasado y su negación es <span class='colorLetraRojo'>didn't</span>.",
        "El <span class='colorLetraRojo'>Will</span> para preguntar en futuro y el <span class='colorLetraRojo'>Won't</span> para negar.",
        "El <span class='colorLetraRojo'>Would</span> se usa para preguntar con un verbo que termina en “ría” – ejemplo: comería, haría, dormiría, jugaría etc  y su negación es <span class='colorLetraRojo'>wouldn't</span>.",
      ],
      listadoP15: [
        "Haty dos tipos de verbos <inputChecked :resuelto=false :esperado=" +
          ["Regulares"] +
          " /> e  <span class='colorLetraRojo'>Irregulares</span>, y ambos tienen cuatro formas <span class='colorLetraRojo'>Presente</span>, <span class='colorLetraRojo'>Pasado</span>, <span class='colorLetraRojo'>Participio</span> y <span class='colorLetraRojo'>Progresivo</span>.",
        "Los verbos en <span class='colorLetraRojo'>Presente</span> se usan después de los verbos con poder <span class='colorLetraRojo'>Can</span>, <span class='colorLetraRojo'>Could</span>, <span class='colorLetraRojo'>Should</span> o <span class='colorLetraRojo'>Must</span>.",
        "Los verbos en presente también se usan con los auxiliares <span class='colorLetraRojo'>Do</span>, <span class='colorLetraRojo'>Does</span>, <span class='colorLetraRojo'>Did</span>, <span class='colorLetraRojo'>Will</span> o <span class='colorLetraRojo'>Would</span>.",
        "Los <span class='colorLetraRojo'>auxiliares</span> se usan para preguntar y negar.",
        "Un verbo se usa en forma <span class='colorLetraRojo'>Pasado</span> solo en una <span class='colorLetraRojo'>afirmacion</span>; si es regular se agrega “ed” y si es irregular se aprende.",
        "Un verbo se usa en su forma participio únicamente después de los verbos con poder  <span class='colorLetraRojo'>'have, has, had'</span> " +
          "Si es regular se le agrega 'ed' y si es irregular se aprende.",
        "Los verbos con poder no necesitan auxiliares en una pregunta, afirmación ni negación y son los únicos que se niegan al poner la palabra “NOT” delante de ellos y existen doce.",
        "Un verbo se usa en su forma progresiva después de los verbos con poder <span class='colorLetraRojo'>IS, AM, ARE, WAS Y WERE</span> y al verbo se le agrega “ING” al final.",
      ],
      subListadoP15: [
        "El <span class='colorLetraRojo'>Do</span> es para preguntar en presente y su negación es <span class='colorLetraRojo'>don't</span>",
        "El <span class='colorLetraRojo'>Does</span> es para preguntar en presente, pero con she, he, it, y su negación es <span class='colorLetraRojo'>doesn't</span> .",
        "El <span class='colorLetraRojo'>Did</span> para preguntar en pasado y su negación es <span class='colorLetraRojo'>didn't</span>.",
        "El <span class='colorLetraRojo'>Will</span> para preguntar en futuro y el <span class='colorLetraRojo'>Won't</span> para negar.",
        "El <span class='colorLetraRojo'>Would</span> se usa para preguntar con un verbo que termina en “ría” – ejemplo: comería, haría, dormiría, jugaría etc  y su negación es <span class='colorLetraRojo'>wouldn't</span>.",
      ],
      cuestionarioP13: [
        {
          respuesta: "",
          pregunta: "1. ¿Qué es un verbo regular?",
          options: [
            {
              text: "A) En pasado y participio se escribe diferente.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) En pasado y participio se escribe igual más “ed”.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "2. ¿Qué son modificadores?",
          options: [
            {
              text: "A) Verbos que terminan en ado e ido en español.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Palabras usadas para determinar el tiempo del verbo.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "3. ¿Qué es un verbo en su forma participio?",
          options: [
            {
              text: "A) Los que terminan en ado o ido.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Los que terminan en ando o endo.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "4. ¿Por qué se llaman verbos con super poderes?",
          options: [
            {
              text: "A) Estos verbos pueden negarse solos.",
              value: "A",
              disabled: false,
            },
            {
              text:
                "B) Necesitan de un modificador en las negaciones o preguntas.",
              value: "B",
              disabled: false,
            },
          ],
        },
      ],
      mensajeRespuestasP13: "",
      respuestasCuestionarioP13: ["B", "B", "A", "A"],
      tablaContenidoP12: [
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "Present" },
          ],
          items: [
            {
              html: "I go: yo voy.",
            },
          ],
        },
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "Past" },
          ],
          items: [
            {
              html: 'I <span style="color:red">went</span>: yo fui.',
            },
          ],
        },
        {
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "Participle" },
          ],
          items: [
            {
              html: 'I <span style="color:red">went</span>: yo fui.',
            },
          ],
        },
      ],
      cuestionarioP17: [
        {
          respuesta: "",
          pregunta: "1. ¿Cuántos modificadores hay en inglés?",
          options: [
            {
              text: "A) 5.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 2.",
              value: "B",
              disabled: false,
            },
            {
              text: "C) 3.",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "2. ¿Cuántas formas tiene un verbo?",
          options: [
            {
              text: "A) 12.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 4.",
              value: "B",
              disabled: false,
            },
            {
              text: "C) 5.",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "3. ¿Para qué sirven los auxiliares?",
          options: [
            {
              text: "A) Para negar y afirmar.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Para preguntar y negar.",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Para solo afirmar.",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "4. ¿Cuántos verbos con súper poderes hay?",
          options: [
            {
              text: "A) 2.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 12.",
              value: "B",
              disabled: false,
            },
            {
              text: "C) 15.",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "5. ¿Cuáles son los tipos de verbos según la lógica?",
          options: [
            {
              text: "A) Presente, pasado y participio.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Auxiliares y verbos con poder.",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Regulares e irregulares.",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "6. ¿Cuándo se usa la forma progresiva de un verbo?",
          options: [
            {
              text: "A) Después de un auxiliar.",
              value: "A",
              disabled: false,
            },
            {
              text:
                "B) Después de los verbos con poder CAN, COULD, SHOULD Y MUST.",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Después de IS, AM, ARE, WAS Y WERE.",
              value: "C",
              disabled: false,
            },
          ],
        },
      ],
      respuestasCuestionarioP17: ["A", "B", "B", "B", "C", "C"],
      mensajeRespuestasP17: "",
      tablasNumeroMagicoP14: [
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "#", thClass: "noHead" },
            { key: "Z", thClass: "noHead" },
          ],
          items: [{ Z: "Regulars" }, { Z: "Irregulars" }],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "#", thClass: "noHead" },
            { key: "Z", thClass: "noHead" },
          ],
          items: [
            { Z: "Present" },
            { Z: "Past" },
            { Z: "Participle" },
            { Z: "Progessive" },
          ],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "#", thClass: "noHead" },
            { key: "Z", thClass: "noHead" },
          ],
          items: [
            { Z: "Do" },
            { Z: "Does" },
            { Z: "Did" },
            { Z: "Will" },
            { Z: "Would" },
          ],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "#", thClass: "noHead" },
            { key: "Z", thClass: "noHead" },
          ],
          items: [
            { Z: "Have" },
            { Z: "Has" },
            { Z: "Had" },
            { Z: "Is" },
            { Z: "Am" },
            { Z: "Are" },
            { Z: "Was" },
            { Z: "Were" },
            { Z: "Can" },
            { Z: "Could" },
            { Z: "Should" },
            { Z: "Must" },
          ],
        },
      ],
    };
  },
  methods: {
    showModal(text) {
      this.$refs[text].show();
    },
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
  text-align: center;
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