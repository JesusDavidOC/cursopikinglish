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
          <h3 style="margin-top:0.4em;">Types Of Verbs</h3>
          <listaIndex :tabla="$data.tablasNumeroMagicoP14[0]" />
        </div>
        <div class="col-sm-2">
          <div class="col-sm-7" id="numeroMagico4">4</div>
          <h3 style="margin-top:0.4em;">Spelling Forms</h3>
          <listaIndex :tabla="$data.tablasNumeroMagicoP14[1]" />
        </div>
        <div class="col-sm-2">
          <div class="col-sm-7" id="numeroMagico5">5</div>
          <h3 style="margin-top:0.4em;">Tense Modifiers</h3>
          <listaIndex :tabla="$data.tablasNumeroMagicoP14[2]" />
        </div>
        <div class="col-sm-2">
          <div class="col-sm-7" id="numeroMagico12">12</div>
          <h4 style="margin-top:0.4em;">Super Power Verbs</h4>
          <div class="overflow-auto" style="max-height: 350px;">
            <listaIndex :tabla="$data.tablasNumeroMagicoP14[3]" />
          </div>
        </div>
      </div>
    </div>

    <div class="row">
        <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <iframe width="100%" height="440" src="https://www.youtube.com/embed/YvkfIwFzXVU" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
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
        <i class="fa fa-diamond" style="font-size: 1.5em;"></i>
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
      <b-modal ref="my-modal1" hide-footer title="RESULTADO">{{ mensajeRespuestasP13 }}</b-modal>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modal1')">VERIFICAR PREGUNTAS</b-button>
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
            <div class="row" v-if="index== 3">
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
        <div class="col-sm-3" v-for="item in $data.tablasTiempoP15" style="margin:0; padding:0;">
          <listaIndex :tabla="item" />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-8" id="subTitulo">
        <h3>PRACTICE</h3>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-11 row">
        <ul id="textoCompromiso" style="width:100%;">
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
              <a>
                <div class="row">
                  <div id="i" class="col-sm-1">
                    <i class="fa fa-diamond"></i>
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    Hay dos tipos de verbos
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Regulares']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />e
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Irregulares']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />, ambos tienen cuatro formas
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Presente']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />,
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Pasado']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />,
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Participio']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />y
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Progresivo']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />.
                  </div>
                </div>
              </a>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12" id="campoTextoP11">
              <a>
                <div class="row">
                  <div id="i" class="col-sm-1">
                    <i class="fa fa-diamond"></i>
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    Los verbos en Presente se usan después de los verbos con poder
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Can']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />,
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Could']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />,
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Should']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />o
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Must']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />.
                  </div>
                </div>
              </a>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
              <a>
                <div class="row">
                  <div id="i" class="col-sm-1">
                    <i class="fa fa-diamond"></i>
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    Los verbos en presente también se usan con los auxiliares
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Do']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Does']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />,
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Did']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />,
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Will']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />o
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Would']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />.
                  </div>
                </div>
              </a>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
              <a>
                <div class="row">
                  <div id="i" class="col-sm-1">
                    <i class="fa fa-diamond"></i>
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    Los verbos en presente también se usan con los auxiliares
                    <ul>
                      <dt>
                        <div class="col-sm-12 row"></div>
                        <div class="col-sm-12" id="campoTextoP11">
                          <a>
                            <div class="row">
                              <div id="i" class="col-sm-1">
                                <i class="fa fa-check"></i>
                              </div>
                              <div class="col-sm-11 row" id="inputText">
                                El
                                <span
                                  class="colorLetraRojo"
                                  style="margin-left:4px; margin-right:4px;"
                                >Do</span> es para preguntar en
                                <inputChecked
                                  :resuelto="false"
                                  :esperado="['Presente']"
                                  style="width: 20%; margin-left:10px; margin-right:10px;"
                                />, y su negación es
                                <span
                                  class="colorLetraRojo"
                                  style="margin-left:4px; margin-right:4px;"
                                >don't.</span>
                              </div>
                            </div>
                          </a>
                        </div>
                      </dt>
                      <dt>
                        <div class="col-sm-12 row"></div>
                        <div class="col-sm-12" id="campoTextoP11">
                          <a>
                            <div class="row">
                              <div id="i" class="col-sm-1">
                                <i class="fa fa-check"></i>
                              </div>
                              <div class="col-sm-11 row" id="inputText">
                                El
                                <inputChecked
                                  :resuelto="false"
                                  :esperado="['Does']"
                                  style="width: 20%; margin-left:10px; margin-right:10px;"
                                />para preguntar en presente, pero con she, he, it,
                                <a
                                  style="width:100%; margin:0px;"
                                >
                                  y su negación es
                                  <span
                                    class="colorLetraRojo"
                                    style="margin-left:4px; margin-right:4px;"
                                  >doesn't.</span>
                                </a>
                              </div>
                            </div>
                          </a>
                        </div>
                      </dt>
                      <dt>
                        <div class="col-sm-12 row"></div>
                        <div class="col-sm-12" id="campoTextoP11">
                          <a>
                            <div class="row">
                              <div id="i" class="col-sm-1">
                                <i class="fa fa-check"></i>
                              </div>
                              <div class="col-sm-11 row" id="inputText">
                                El
                                <span
                                  class="colorLetraRojo"
                                  style="margin-left:4px; margin-right:4px;"
                                >Did</span> es para preguntar en
                                <inputChecked
                                  :resuelto="false"
                                  :esperado="['pasado']"
                                  style="width: 16%; margin-left:10px; margin-right:10px;"
                                />y su negación es
                                <inputChecked
                                  :resuelto="false"
                                  :esperado="['didn´t']"
                                  style="width: 16%; margin-left:10px; margin-right:10px;"
                                />.
                              </div>
                            </div>
                          </a>
                        </div>
                      </dt>
                      <dt>
                        <div class="col-sm-12 row"></div>
                        <div class="col-sm-12" id="campoTextoP11">
                          <a>
                            <div class="row">
                              <div id="i" class="col-sm-1">
                                <i class="fa fa-check"></i>
                              </div>
                              <div class="col-sm-11 row" id="inputText">
                                El
                                <inputChecked
                                  :resuelto="false"
                                  :esperado="['Will']"
                                  style="width: 16%; margin-left:10px; margin-right:10px;"
                                />para preguntar en futuro y el
                                <inputChecked
                                  :resuelto="false"
                                  :esperado="['Won´t']"
                                  style="width: 15%; margin-left:10px; margin-right:10px;"
                                />para negar.
                              </div>
                            </div>
                          </a>
                        </div>
                      </dt>
                      <dt>
                        <div class="col-sm-12 row"></div>
                        <div class="col-sm-12" id="campoTextoP11">
                          <a>
                            <div class="row">
                              <div id="i" class="col-sm-1">
                                <i class="fa fa-check"></i>
                              </div>
                              <div class="col-sm-11 row" id="inputText">
                                El
                                <span
                                  class="colorLetraRojo"
                                  style="margin-left:4px; margin-right:4px;"
                                >Would</span> se usa para preguntarcon un verbo que termina en “
                                <inputChecked
                                  :resuelto="false"
                                  :esperado="['ría']"
                                  style="width: 16%; margin-left:10px; margin-right:10px;"
                                />”
                                <span>Ejemplo: comería, haría, dormiría, jugaría etc y su negación es</span>
                                <inputChecked
                                  :resuelto="false"
                                  :esperado="['wouldn´t']"
                                  style="width: 16%; margin-left:10px; margin-right:10px;"
                                />.
                              </div>
                            </div>
                          </a>
                        </div>
                      </dt>
                    </ul>
                  </div>
                </div>
              </a>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
              <a>
                <div class="row">
                  <div id="i" class="col-sm-1">
                    <i class="fa fa-diamond"></i>
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    Un verbo se usa en forma
                    <span
                      class="colorLetraRojo"
                      style="margin-left:4px; margin-right:4px;"
                    >Pasado</span> solo en una
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Afirmación']"
                      style="width: 15%; margin-left:10px; margin-right:10px;"
                    />; si es regular se agrega
                    “
                    <inputChecked
                      :resuelto="false"
                      :esperado="['ed']"
                      style="width: 15%; margin-left:10px; margin-right:10px;"
                    />” y si es
                    irregular se aprende.
                  </div>
                </div>
              </a>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
              <a>
                <div class="row">
                  <div id="i" class="col-sm-1">
                    <i class="fa fa-diamond"></i>
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    Un verbo se usa en su forma participio únicamente después de los verbos con poder
                    '
                    <inputChecked
                      :resuelto="false"
                      :esperado="['have']"
                      style="width: 15%; margin-left:10px; margin-right:10px;"
                    />,
                    <span class="colorLetraRojo">has</span>,
                    <inputChecked
                      :resuelto="false"
                      :esperado="['had']"
                      style="width: 15%; margin-left:10px; margin-right:10px;"
                    />'
                    Si es regular se le agrega 'ed' y si es irregular se aprende.
                  </div>
                </div>
              </a>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
              <a>
                <div class="row">
                  <div id="i" class="col-sm-1">
                    <i class="fa fa-diamond"></i>
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    Los verbos con poder no necesitan
                    <inputChecked
                      :resuelto="false"
                      :esperado="['auxiliares']"
                      style="width: 15%; margin-left:10px; margin-right:10px;"
                    />
                    <span>en una pregunta, afirmación ni negación y</span> son los únicos que se niegan al poner la palabra “NOT” delante de ellos y existen doce.
                  </div>
                </div>
              </a>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
              <a>
                <div class="row">
                  <div id="i" class="col-sm-1">
                    <i class="fa fa-diamond"></i>
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    "Un verbo se usa en su forma progresiva después de los verbos con poder
                    <span
                      class="colorLetraRojo"
                    >IS,</span>
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Am']"
                      style="width: 15%; margin-left:10px; margin-right:10px;"
                    />,
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Are']"
                      style="width: 15%; margin-left:10px; margin-right:10px;"
                    />,
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Was']"
                      style="width: 15%; margin-left:10px; margin-right:10px;"
                    />o
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Were']"
                      style="width: 15%; margin-left:10px; margin-right:10px;"
                    />y al verbo se le agrega “
                    <inputChecked
                      :resuelto="false"
                      :esperado="['ING']"
                      style="width: 14%; margin-left:10px; margin-right:10px;"
                    />”
                    <span>al final.</span>
                  </div>
                </div>
              </a>
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
          v-for="item in $data.tablasTiempoPreguntaP15"
          style="margin:0; padding:0;"
        >
          <listaIndex :tabla="item" />
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
        <i class="fa fa-diamond" style="font-size: 1.5em;"></i>
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
      <b-modal ref="my-modal1" hide-footer title="RESULTADO">{{mensajeRespuestasP17 }}</b-modal>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modal1')">VERIFICAR PREGUNTAS</b-button>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" style="text-align:left;">
        <legend
          id="5__BV_label_"
          tabindex="-1"
          class="bv-no-focus-ring col-form-label pt-0 col-form-label-lg labelPregunta"
        >7. Escriba los verbos con súper poder</legend>
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
      <div class="col-sm-6" style="text-align:left;">
        <legend
          id="5__BV_label_"
          tabindex="-1"
          class="bv-no-focus-ring col-form-label pt-0 col-form-label-lg labelPregunta"
        >8. Escriba las cuatro formas del verbo</legend>
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
      <div class="col-sm-6" style="text-align:left;">
        <legend
          id="5__BV_label_"
          tabindex="-1"
          class="bv-no-focus-ring col-form-label pt-0 col-form-label-lg labelPregunta"
        >9. Escribe los 5 auxiliares del inglés para preguntar y negar</legend>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <div
          class="col-sm-2"
          style="margin:0; padding:0;"
          v-for="(item, index) in tablaPregunta8P17"
        >
          <listaIndex :tabla="item" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import listaIndex from "./listaIndex";
import tablaTraduccionCodigos from "./tablaTraduccionCodigos";
import opcionMultiple from "./opcionMultiple";
import inputChecked from "./inputChecked";
export default {
  components: {
    listaIndex,
    tablaTraduccionCodigos,
    opcionMultiple,
    inputChecked,
  },
  data() {
    return {
      
      tablaPregunta8P17: [
        {
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "En presente" },
          ],
          items: ["Do"],
        },
        {
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "En presente con she, he e it" },
          ],
          items: ["Does"],
        },
        {
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "En pasado" },
          ],
          items: ["Did"],
        },
        {
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "En futuro" },
          ],
          items: ["will"],
        },
        {
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "Un verbo termina en ría." },
          ],
          items: ["Would"],
        },
      ],
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