<template>
  <div>
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8" id="cuadroTexto">
        <p class="parrafo">
          Las tablas lógicas están diseñadas para crear oraciones en ingles de
          forma automática sin margen de error gramatical con solo reemplazar y
          combinar los números. Tal como una tabla de multiplicar estos
          ejercicios contienen resultados exactos según las combinaciones de los
          comandos A, B, C, D, E, F, G, H, I. de símbolos o de colores. Debajo
          del cuadro con las palabras en inglés aparecen unos números que deben
          reemplazarse por palabras según la información de arriba y que
          corresponda a la columna. Debes entonces construir una oración y luego
          traducirla.
        </p>
        <img src="/cursos/curso1/leccion1/imagenes/ejemplo1.PNG" />
      </div>
      <div class="col-sm-2"></div>
    </div>
    <div class="row" id="tablas">
      <div class="col-sm-6 row">
        <div class="col-sm-3" id="tabla">
          <listaIndex :tabla="$data.tablaA" />
        </div>
        <div class="col-sm-3" id="tabla">
          <listaIndex :tabla="$data.tablaB" />
        </div>

        <div class="col-sm-3" id="tabla">
          <listaIndex :tabla="$data.tablaC" />
        </div>

        <div class="col-sm-3" id="tabla">
          <listaIndex :tabla="$data.tablaD" />
        </div>
      </div>
      <div class="col-sm-6 row">
        <div class="col-sm-3" id="tabla">
          <listaIndex :tabla="$data.tablaAEspañol" />
        </div>
        <div class="col-sm-3" id="tabla">
          <listaIndex :tabla="$data.tablaBEspañol" />
        </div>

        <div class="col-sm-3" id="tabla">
          <listaIndex :tabla="$data.tablaCEspañol" />
        </div>

        <div class="col-sm-3" id="tabla">
          <listaIndex :tabla="$data.tablaDEspañol" />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTraduccionCodigos
          id="diiv"
          class="overflow-auto"
          :cuestionario="$data.cuestionario1"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <h3 id="titulo">COMPROMISO PARA ENTENDER EL NÚMERO MÁGICO.</h3>
      <div class="row"></div>
      <ul>
        <dt v-for="item in $data.listadoCompromiso" id="textoCompromiso">
          <i class="fa fa-diamond"></i>
          <a>{{ item }}</a>
        </dt>
      </ul>
    </div>
    <div class="row">
      <h3 id="titulo">PROCESOS PARA ENTENDER EL NÚMERO MÁGICO.</h3>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <iframe
          width="100%"
          height="440"
          src="https://www.youtube.com/embed/OqvyTnU4BpI"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <div class="row">
      <h4 id="subTitulo">IDENTIFICAR EL NÚMERO MÁGICO.</h4>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-1" id="numeroMagico2">2</div>
      <div class="col-sm-1" id="numeroMagico4">4</div>
      <div class="col-sm-1" id="numeroMagico5">5</div>
      <div class="col-sm-1" id="numeroMagico12">12</div>

      <div class="col-sm-1"></div>

      <div class="col-sm-1" id="campoTextoP11">
        <inputChecked :resuelto="false" :esperado="['2']" :tamano="7" />
      </div>
      <div class="col-sm-1" id="campoTextoP11">
        <inputChecked :resuelto="false" :esperado="['4']" :tamano="7" />
      </div>
      <div class="col-sm-1" id="campoTextoP11">
        <inputChecked :resuelto="false" :esperado="['5']" :tamano="7" />
      </div>
      <div class="col-sm-2" id="campoTextoP11">
        <inputChecked :resuelto="false" :esperado="['12']" :tamano="8" />
      </div>
    </div>
    <div class="row">
      <h4 id="subTitulo">DESCIFRAR EL NÚMERO MÁGICO.</h4>
    </div>
    <div class="row">
      <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-1" id="numeroMagico2">2</div>
        <div class="col-sm-3" id="campoTextoP11">
          <h2>Tipos de verbos</h2>
        </div>
        
        <div class="col-sm-1" id="numeroMagico2" >2</div>
        <div class="col-sm-4" id="campoTextoP11">
          <inputChecked :resuelto="false" :esperado="['Tipos de verbos']" />
        </div>
      </div>
      <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-1" id="numeroMagico4">4</div>
        <div class="col-sm-3" id="campoTextoP11">
          <h3>Formas de escribir un verbo</h3>
        </div>
        <div class="col-sm-1" id="numeroMagico4">4</div>
        <div class="col-sm-4" id="campoTextoP11">
          <inputChecked
            :resuelto="false"
            :esperado="[
              'Formas de escribir un verbo',
              'Formas de escribir verbos',
            ]"
          />
        </div>
      </div>
      <div class="row">   
      <div class="col-sm-1"></div>     
        <div class="col-sm-1" id="numeroMagico5">5</div>
        <div class="col-sm-3" id="campoTextoP11">
          <h2>Modificadores del tiempo</h2>
        </div>         
        <div class="col-sm-1" id="numeroMagico5">5</div>
        <div class="col-sm-4" id="campoTextoP11">
          <inputChecked
            :resuelto="false"
            :esperado="['Modificadores del tiempo', 'Modificadores de tiempo']"
          />
        </div>
      </div>
      <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-1" id="numeroMagico12">12</div>
        <div class="col-sm-3" id="campoTextoP11">
          <h2>Verbos con super poder</h2>
        </div>
        <div class="col-sm-1" id="numeroMagico12">12</div>
        <div class="col-sm-4" id="campoTextoP11">
          <inputChecked
            :resuelto="false"
            :esperado="['Verbos con super poder', 'Verbos con super poderes']"
          />
        </div>
      </div>
    </div>
    <div class="row">
      <h4 id="subTitulo">DESGLOSAR EL NÚMERO MÁGICO.</h4>
    </div>
    <div class="row">
      <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-1" id="numeroMagico2">2</div>
        <div class="col-sm-3" id="campoTextoP11">
          <h2>Tipos de verbos:</h2>
        </div>
        <div class="col-sm-6" id="campoTextoP11">
          <h3 id="text">Regulares e Irregulares.</h3>
        </div>
      </div>
      <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-1" id="numeroMagico4">4</div>
        <div class="col-sm-3" id="campoTextoP11">
          <h3>Formas de escribir un verbo:</h3>
        </div>
        <div class="col-sm-6" id="campoTextoP11">
          <h3 id="text">Presente, Pasado, Participio Y Progresivo.</h3>
        </div>
      </div>
      <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-1" id="numeroMagico5">5</div>
        <div class="col-sm-3" id="campoTextoP11">
          <h2>Modificadores de tiempo:</h2>
        </div>
        <div class="col-sm-6" id="campoTextoP11">
          <h3 id="text">Do, Does, Did, Will y Would.</h3>
        </div>
      </div>
      <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-1" id="numeroMagico12">12</div>
        <div class="col-sm-3" id="campoTextoP11">
          <h2>Verbos con súper poder:</h2>
        </div>
        <div class="col-sm-6" id="campoTextoP11">
          <h3 id="text">
            Have-Has-Had /Is-Am-Are-Was-Were/Can-Could-Should-Must
          </h3>
        </div>
      </div>
      <div class="row" style="margin-top: 2em">
        <div class="col-sm-1"></div>
        <div class="col-sm-1" id="numeroMagico2">2</div>
        <div class="col-sm-3" id="campoTextoP11">
          <inputChecked
            :resuelto="false"
            :esperado="['Tipos de verbos']"
            :conTexto="true"
            textoD=":"
          />
        </div>
        <div class="col-sm-6" id="campoTextoP11">
          <inputChecked
            :resuelto="false"
            :esperado="['Irregulares']"
            style="margin-left: 0px"
            :conTexto="true"
            textoA="Regulares e "
            :tamano="23"
          />
        </div>
      </div>
      <div class="row" style="margin-top: 2em">
        <div class="col-sm-1"></div>
        <div class="col-sm-1" id="numeroMagico4">4</div>
        <div class="col-sm-3" id="campoTextoP11">
          <inputChecked
            :resuelto="false"
            :esperado="[
              'Formas de escribir un verbo',
              'Formas de escribir verbos',
            ]"
            :conTexto="true"
            textoD=":"
            :tamano="24"
          />
        </div>

        <div class="col-sm-6" id="campoTextoP11" style="padding-left: 55px">
          <inputCEnriquecido :object="inputCEP11" />
        </div>
      </div>

      <div class="row" style="margin-top: 2em">
        <div class="col-sm-1"></div>
        <div class="col-sm-1" id="numeroMagico5">5</div>
        <div class="col-sm-3" id="campoTextoP11">
          <inputChecked
            :resuelto="false"
            :esperado="['Modificadores del tiempo', 'Modificadores de tiempo']"
            :conTexto="true"
            textoD=":"
            :tamano="23"
          />
        </div>
        <div class="col-sm-6" id="campoTextoP11" style="padding-left:1em;">
          <div class="row">
            <div class="col-sm-8">
              <inputCEnriquecido :object="inputCEP11N2" />
            </div>
            <div class="col-sm-4" style="margin-left: -6em;">
              <inputChecked :resulto="false" :esperado="inputCEP11N3.lista1" :tamano="inputCEP11N3.tamano1" :conTexto="true" textoD="," />
            </div>
          </div>
          <div class="row">
            <div class="col-sm-8" style="margin-top: -30px;">
              <inputChecked :resulto="false" :esperado="['Will']" :tamano="15" :conTexto="true" textoD="y would." />
            </div>
          </div>
        </div>
      </div>
      <div class="row" style="margin-top: -25px">
        <div class="col-sm-1"></div>
        <div class="col-sm-1" id="numeroMagico12">12</div>
        <div class="col-sm-3" id="campoTextoP11">
          <inputChecked
            :resuelto="false"
            :esperado="['Verbos con super poder', 'Verbos con super poderes']"
            :conTexto="true"
            textoD=":"
            :tamano="22"
          />
        </div>
        <div class="col-sm-6" id="campoTextoP11" >
          <div class="row">
            <div class="col-sm-8" >
              <inputCEnriquecido :object="inputCEP11N4" />
            </div>
            <div class="col-sm-4" style="margin-left: -2em;">
              <inputChecked :resulto="false" :esperado="['Am']" :tamano="10" :conTexto="true" textoD="," />
            </div>
          </div>
          <div class="row">
            <div class="col-sm-8" style="margin-top: -30px;">
              <inputCEnriquecido :object="inputCEP11N5" />
            </div>
            <div class="col-sm-4" style="margin-top: -30px; margin-left: -7em;">
              <inputChecked :resulto="false" :esperado="['Were']" :tamano="14" :conTexto="true" textoD="/Can," />
            </div>
          </div>
          <div class="row">
            <div class="col-sm-8" style="margin-top: -30px;">
              <inputCEnriquecido :object="inputCEP11N6" />
            </div>
            <div class="col-sm-4" style="margin-top: -30px; margin-left: -4em;">
              <inputChecked :resulto="false" :esperado="['Must']" :tamano="11" :conTexto="true" textoD="." />
            </div>
          </div>
        </div>
       </div>

      </div>
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico2">2</div>
        <h3 style="margin-top: 0.4em">Types Of Verbs</h3>
        <h4 style="margin-top: 0.4em">Regulars Irregulars</h4>
      </div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico4">4</div>
        <h3 style="margin-top: 0.4em">Spelling Forms</h3>
        <h4 style="margin-top: 0.4em">Present Past Participle Progessive</h4>
      </div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico5">5</div>
        <h3 style="margin-top: 0.4em">Tense Modifiers</h3>
        <h4 style="margin-top: 0.4em">Do Does Did Will Would</h4>
      </div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico12">12</div>
        <h3 style="margin-top: 0.4em">Super Power Verbs</h3>
        <h4 style="margin-top: 0.4em">
          Have Has Had Is Am Are Was Were Can Could Should Must
        </h4>
      </div>
    </div>
    <div class="row">
      <h4 id="subTitulo">DILIGENCIAR LAS PARTES DEL NÚMERO MÁGICO.</h4>
    </div>
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico2">2</div>
        <h3 style="margin-top: 0.4em">Types Of Verbs</h3>
        <listaIndex :tabla="$data.tablasNumeroMagico[0]" />
      </div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico4">4</div>
        <h3 style="margin-top: 0.4em">Spelling Forms</h3>
        <listaIndex :tabla="$data.tablasNumeroMagico[1]" />
      </div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico5">5</div>
        <h3 style="margin-top: 0.4em">Tense Modifiers</h3>
        <listaIndex :tabla="$data.tablasNumeroMagico[2]" />
      </div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico12">12</div>
        <h4 style="margin-top: 0.4em">Super Power Verbs</h4>
        <listaIndex :tabla="$data.tablasNumeroMagico[3]" />
      </div>
    </div>
    <div class="row">
      <h4 id="subTitulo">COMPRENDER TERMINOLOGÍA DEL NÚMERO MÁGICO.</h4>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <iframe
          width="100%"
          height="440"
          src="https://www.youtube.com/embed/NSdcXv2p0j8"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          <strong>Verbos regulares:</strong> Son aquellos que su escritura no
          cambia en pasado ni participio y solo se le agrega “ed”.
        </p>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <b-table :items="tablaContenidoP12[0]" :bordered="true">
          <template v-slot:cell(past)="data">
            <span v-html="data.value"></span>
          </template>

          <template v-slot:cell(participle)="data">
            <span v-html="data.value"></span>
          </template>
        </b-table>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          <strong>Verbos irregulares:</strong> Son aquellos que se escriben
          diferente en pasado y participio y debes aprenderlos.
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <b-table :items="tablaContenidoP12[1]" :bordered="true">
          <template v-slot:cell(past)="data">
            <span v-html="data.value"></span>
          </template>

          <template v-slot:cell(participle)="data">
            <span v-html="data.value"></span>
          </template>
        </b-table>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          <strong>Participio:</strong> Son aquellos verbos que en español
          terminan en “ADO” o “IDO”. Yo he camin<span style="color: red"
            >ado</span
          >, Yo he jug<span style="color: red">ado</span>, Yo he comido, Ella ha
          llev<span style="color: red">ado</span> etc.
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <iframe
          width="100%"
          height="440"
          src="https://www.youtube.com/embed/fdmGdVGuqxc"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          <strong>Progresivo:</strong> Son aquellos verbos que terminan en
          “ANDO” o “ENDO”. Jug<span style="color: red">ando</span>, camin<span
            style="color: red"
            >ando</span
          >, comi<span style="color: red">endo</span> etc. En inglés se debe
          agregar al verbo normal la palabra “ING”. Ejemplo: Work (trabajar)
          Work<span style="color: red">ing</span>
          (trabajando).
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <iframe
          width="100%"
          height="440"
          src="https://www.youtube.com/embed/ng4MrIzJSjc"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          <strong>Modificadores:</strong>Son palabras usadas en una pregunta o
          negación, pero no tienen traducción solo modifican el tiempo del verbo
          y son más conocidos como auxiliares
          <span style="color: red">DO-DOES-DID-WILL-WOULD</span>.
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <iframe
          width="100%"
          height="440"
          src="https://www.youtube.com/embed/i7Zw531Ca20"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          <strong>Verbos con súper poderes:</strong>Son los únicos verbos que
          pueden negarse solos, con solo poner la palabra “not” después de ellos
          y no necesitan modificadores.
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <iframe
          width="100%"
          height="440"
          src="https://www.youtube.com/embed/9h6doGUrlUA"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <iframe
          width="100%"
          height="440"
          src="https://www.youtube.com/embed/EL_AEU5ZsEQ"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-3">
        <h4 style="margin-top: 0.4em">PRIMER GRUPO</h4>
        <listaIndex :tabla="$data.tablaContenidoP13.primerGrupo" />
      </div>
      <div class="col-sm-3">
        <h4 style="margin-top: 0.4em">SEGUNDO GRUPO</h4>
        <listaIndex :tabla="$data.tablaContenidoP13.segundoGrupo" />
      </div>
      <div class="col-sm-3">
        <h4 style="margin-top: 0.4em">TERCER GRUPO</h4>
        <listaIndex :tabla="$data.tablaContenidoP13.tercerGrupo" />
      </div>
    </div>
  </div>
</template>

<script>
import listaIndex from "./listaIndex";
import tablaTraduccionCodigos from "./tablaTraduccionCodigos";
import opcionMultiple from "./opcionMultiple";
import inputChecked from "./inputChecked";
import inputCEnriquecido from "./inputCEnriquecido";
export default {
  components: {
    listaIndex,
    tablaTraduccionCodigos,
    opcionMultiple,
    inputChecked,
    inputCEnriquecido,
  },
  data() {
    return {
      tablaContenidoP13: {
        primerGrupo: {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              thClass: "noHead",
            },
            {
              key: "X",
              thClass: "noHead",
            },
            {
              key: "Y",
              thClass: "noHead",
            },
          ],
          items: [
            {
              Z: "Have",
              X: "Have not",
              Y: "Haven't",
            },
            {
              Z: "Has",
              X: "Has not",
              Y: "Hasn't",
            },
            {
              Z: "Had",
              X: "Had not",
              Y: "Hadn't",
            },
          ],
        },
        segundoGrupo: {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              thClass: "noHead",
            },
            {
              key: "X",
              thClass: "noHead",
            },
            {
              key: "Y",
              thClass: "noHead",
            },
          ],
          items: [
            {
              Z: "Is",
              X: "Is not",
              Y: "Isn't",
            },
            {
              Z: "Am",
              X: "Am not",
              Y: "-----",
            },
            {
              Z: "Are",
              X: "Are not",
              Y: "Aren't",
            },
            {
              Z: "Was",
              X: "Was not",
              Y: "Wasn't",
            },
            {
              Z: "Were",
              X: "Were not",
              Y: "Weren't",
            },
          ],
        },
        tercerGrupo: {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              thClass: "noHead",
            },
            {
              key: "X",
              thClass: "noHead",
            },
            {
              key: "Y",
              thClass: "noHead",
            },
          ],
          items: [
            {
              Z: "Can",
              X: "Can not",
              Y: "Cannot, Can't",
            },
            {
              Z: "Could",
              X: "Could not",
              Y: "Couldn't",
            },
            {
              Z: "Should",
              X: "Should not",
              Y: "Shouldn't",
            },
            {
              Z: "Must",
              X: "Must not",
              Y: "Mustn't",
            },
          ],
        },
      },
      tablaContenidoP12: [
        [
          {
            present: "I work: yo trabajo.",
            past: 'I work<span style="color:red">ed</span>: yo trabajé.',
            participle:
              'I <span style="color:red">have</span> work<span style="color:red">ed</span>: yo he trabajado',
          },
        ],
        [
          {
            present: "I go: yo voy",
            past: 'I <span style="color:red">went</span>: yo fui.',
            participle:
              'I <span style="color:red">have gone</span>: yo he ido.',
          },
        ],
      ],
      tablasNumeroMagico: [
        {
          refs: "tablasNumeroMagicoa",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              thClass: "noHead",
            },
          ],
          items: ["Regulars", "Irregulars"],
        },
        {
          refs: "tablasNumeroMagicob",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              thClass: "noHead",
            },
          ],
          items: ["Present", "Past", "Participle", "Progessive"],
        },
        {
          refs: "tablasNumeroMagicoc",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              thClass: "noHead",
            },
          ],
          items: ["Do", "Does", "Did", "Will", "Would"],
        },
        {
          refs: "tablasNumeroMagicod",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              thClass: "noHead",
            },
          ],
          items: [
            "Have",
            "Has",
            "Had",
            "Is",
            "Am",
            "Are",
            "Was",
            "Were",
            "Can",
            "Could",
            "Should",
            "Must",
          ],
        },
      ],

      inputCEP11: {
        lista1: ["pasado"],
        lista2: ["participio"],
        name: "inputCEP11",
        textoA: "Presente, ",
        textoD: ",",
        textoD2: "y progresivo.",
        tamano1: 18,
        tamano2: 20,
      },

      inputCEP11N2: {
        lista1: ["Do"],
        lista2: ["Does"],
        name: "inputCEP11N2",
        textoA: "",
        textoD: ",",
        textoD2: ",",
        tamano1: 10,
        tamano2: 11,
      },
      inputCEP11N3: {
        lista1: ["Did"],
        lista2: ["Will"],
        name: "inputCEP11N3",
        textoA: "",
        textoD: ",",
        textoD2: "y would",
        tamano1: 10,
        tamano2: 11,
      },

    inputCEP11N4: {
        lista1: ["Has"],
        lista2: ["Had"],
        name: "inputCEP11N4",
        textoA: "Have, ",
        textoD: ",",
        textoD2: "/Is, ",
        tamano1: 14,
        tamano2: 12,
      },
      inputCEP11N5: {
        lista1: ["Are"],
        lista2: ["Was"],
        name: "inputCEP11N5",
        textoA: "",
        textoD: ",",
        textoD2: ",",
        tamano1: 10,
        tamano2: 11,
      },
      inputCEP11N6: {
        lista1: ["Could"],
        lista2: ["Should"],
        name: "inputCEP11N6",
        textoA: "",
        textoD: ",",
        textoD2: ",",
        tamano1: 12,
        tamano2: 12,
      },
      listadoCompromiso: [
        "Ver el video de la lógica dos veces.",
        "Enfocarse en el número mágico y seguir las instrucciones.",
        "Evitar hacer preguntas sobre el verbo TO BE.",
        "Aprobar cada proceso de la lógica.",
        "Exponer a alguien más el credo de la lógica.",
        "Aprenderse el vocabulario del número mágico.",
        "Recuerda siempre que no existe otra manera de aprender la gramática del inglés que no sea a través del número mágico.",
      ],

      cuestionario1: {
        fields: [
          {
            key: "A",
            thClass: "Blue",
          },
          {
            key: "B",
            thClass: "Red",
          },
          {
            key: "C",
            thClass: "Yelow",
          },
          {
            key: "D",
            thClass: "Green",
          },
          {
            key: "complejo1",
            label: "ENGLISH",
          },
          {
            key: "TRADUCCION_ESPAÑOL",
            label: "SPANISH",
          },
        ],
        items: [
          {
            A: 3,
            B: 3,
            C: 3,
            D: 3,
            complejo1: {
              lista: ["we want to work everyday"],
            },
            TRADUCCION_ESPAÑOL: [
              "queremos trabajar todos los días",
              "nosotros queremos trabajar todos los días",
            ],
          },
          {
            A: 2,
            B: 7,
            C: 8,
            D: 1,
            complejo1: {
              lista: ["I have to eat something"],
            },
            TRADUCCION_ESPAÑOL: [
              "tengo que comer algo",
              "yo tengo que comer algo",
            ],
          },
          {
            A: 2,
            B: 7,
            C: 8,
            D: 4,
            complejo1: {
              lista: ["I have to eat very much"],
            },
            TRADUCCION_ESPAÑOL: [
              "tengo que comer mucho",
              "yo tengo que comer mucho",
            ],
          },
        ],
      },
      tablaAEspañol: {
        bordered: true,
        camposInput: false,
        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          {
            key: "A",
            thClass: "Blue",
          },
        ],
        items: [
          {
            A: "el gato",
          },
          {
            A: "yo",
          },
          {
            A: "nosotros",
          },
          {
            A: "mi madre",
          },
          {
            A: "el ratón",
          },
        ],
      },
      tablaBEspañol: {
        bordered: true,
        camposInput: false,
        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          {
            key: "B",
            thClass: "Red",
          },
        ],
        items: [
          {
            B: "comer",
          },
          {
            B: "amar",
          },
          {
            B: "querer",
          },
          {
            B: "tener",
          },
          {
            B: "caminar, pasear",
          },
          {
            B: "beber",
          },
          {
            B: "tener",
          },
          {
            B: "necesitar",
          },
          {
            B: "perseguir",
          },
        ],
      },
      tablaCEspañol: {
        bordered: true,
        camposInput: false,
        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          {
            key: "C",
            thClass: "Yelow",
          },
        ],
        items: [
          {
            C: "mi madre",
          },
          {
            C: "hacer",
          },
          {
            C: "trabajar",
          },
          {
            C: "el perro",
          },
          {
            C: "leche",
          },
          {
            C: "estudiar",
          },
          {
            C: "ratones",
          },
          {
            C: "comer",
          },
          {
            C: "una mascota",
          },
          {
            C: "queso",
          },
        ],
      },
      tablaDEspañol: {
        bordered: true,
        camposInput: false,
        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          {
            key: "D",
            thClass: "Green",
          },
        ],
        items: [
          {
            D: "algo",
          },
          {
            D: "mañana",
          },
          {
            D: "todos los días",
          },
          {
            D: "muchisimo",
          },
          {
            D: "para el examen",
          },
          {
            D: "en la noche",
          },
          {
            D: "llamado 'REX'",
          },
          {
            D: "en la cocina",
          },
        ],
      },
      tablaA: {
        bordered: true,
        camposInput: false,
        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          {
            key: "A",
            thClass: "Blue",
          },
        ],
        items: [
          {
            A: "the cat",
          },
          {
            A: "I",
          },
          {
            A: "we",
          },
          {
            A: "my mother",
          },
          {
            A: "the mouse",
          },
        ],
      },
      tablaB: {
        bordered: true,
        camposInput: false,
        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          {
            key: "B",
            thClass: "Red",
          },
        ],
        items: [
          {
            B: "eats",
          },
          {
            B: "love",
          },
          {
            B: "want",
          },
          {
            B: "has",
          },
          {
            B: "walk",
          },
          {
            B: "drinks",
          },
          {
            B: "have",
          },
          {
            B: "need",
          },
          {
            B: "chases",
          },
        ],
      },
      tablaC: {
        bordered: true,
        camposInput: false,
        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          {
            key: "C",
            thClass: "Yelow",
          },
        ],
        items: [
          {
            C: "my mother",
          },
          {
            C: "to do",
          },
          {
            C: "to work",
          },
          {
            C: "the dog",
          },
          {
            C: "milk",
          },
          {
            C: "to study",
          },
          {
            C: "mice",
          },
          {
            C: "to eat",
          },
          {
            C: "a pet",
          },
          {
            C: "cheese",
          },
        ],
      },
      tablaD: {
        bordered: true,
        camposInput: false,
        fields: [
          // A virtual column that doesn't exist in items
          {
            key: "#",
          },
          ,
          // A column that needs custom formatting
          {
            key: "D",
            thClass: "Green",
          },
        ],
        items: [
          {
            D: "something",
          },
          {
            D: "tomorrow",
          },
          {
            D: "everyday",
          },
          {
            D: "verymuch",
          },
          {
            D: "for the exam",
          },
          {
            D: "at night",
          },
          {
            D: "named 'REX'",
          },
          {
            D: "in the kitchen",
          },
        ],
      },
    };
  },
};
</script>

<style scoped>
/deep/ #tabla {
  padding-right: 0px;
  padding-left: 0px;
}

/deep/ .row {
  width: 100%;
  margin: 0;
  margin-bottom: 1em;
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
  margin-right: auto;
  color: darkcyan;
  margin-top: 1.5em;
}

#textoCompromiso {
  text-align: left;
  margin-bottom: 1em;
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

#campoTextoP11 {
  margin: 0;
  margin-right: 1em;
  margin-top: 1.5em;
  padding: 0;
  text-align: left;
}

#text,
#inputText {
  text-align: left;
}

#diiv {
  max-height: 300px;
  margin-bottom: 2em;
}
</style>
