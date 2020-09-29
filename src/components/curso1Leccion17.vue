//<template>
  <div>

      <div class="row">
        <div class="col-sm-12">
          <h3 id="subTitulo">FORMA PARTICIPIO CON VERBOS IRREGULARES</h3>
        </div>
      </div>

  <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice">
          Son aquellos verbos en español terminados en “ido y ado” y en inglés
          se usan después de HAVE,HAS Y HA
        </a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-3"></div>
      <div class="col-sm-4">
        <listaIndex :tabla="$data.tablaP21" />
      </div>
      <div class="col-sm-1"></div>
      <div class="col-ms-4 pt-5">
        <h2>Participio</h2>
      </div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice">Recuerda que HAVE es un verbo (tener) y también un verbo con poder
          (haber, he, has, han,hemos)</a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-9">
        <tablaTC
          :cuestionario="$data.tablaA3"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-2"></div>
    </div>

      <div class="row">
        <div class="col-sm-12">
          <h3 id="subTitulo">FORMA PARTICIPIO CON VERBOS REGULARES</h3>
        </div>
      </div>

<div class="row">
      <div class="col-sm-3"></div>
      <div class="col-sm-7" style="text-align:left;">
        <a id="textPractice">Los verbos regulares en pasado y participio se les agrega ED</a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-3"></div>
      <div class="col-sm-4">
        <listaIndex :tabla="$data.tablaP21" />
      </div>
      <div class="col-sm-1"></div>
      <div class="col-ms-4 pt-5">
        <h2>Participio</h2>
      </div>
    </div>


<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><i class="fa fa-diamond" style="font-size: 1.0em;"></i>Traduce las siguientes oraciones</a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-9">
        <tablaTC
          :cuestionario="$data.tablaA4"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-2"></div>
    </div>

    <div class="row">
          <div class="col-ms-12">
              <h3 id="subTitulo">EL PARTICIPO MAS IMPORTANTE DEL INGLÉS</h3>
          </div>
          <div class="col-sm-2"></div>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <listaIndex :tabla="$data.tablaP51" />
      </div>
      <div class="col-sm-2"></div>
    </div>

    <div class="row">
          <div class="col-ms-12">
              <h3 id="subTitulo">PRACTICE</h3>
          </div>
          <div class="col-sm-2"></div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><i class="fa fa-diamond" style="font-size: 1.0em;"></i>Completa con Have, Has o Had más el verbo en participios</a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-11 row">
        <ul id="textoCompromiso" style="width:100%;">

          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-1"></div>
            <div class="col-sm-11">
              
                <div class="row">
                  <div class="col-sm-11 row" id="inputText">
                    <p>1. ¿Como has estado? How</p>                     
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Have']"
                      style="width: 20%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R1.mp3"
                    />you
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Been']"
                      style="width: 14%; margin-left:10px; margin-right:10px;"
                    />?
                  </div>
                </div> 
            </div>
          </dt>

          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12" id="campoTextoP11">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    2. ¿Dónde has estado? Where
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Have']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R2.mp3"
                    />you
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Been']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />?
                  </div>
                </div>
            </div>
          </dt>

          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    3. ¿Qué has estado haciendo? What
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Have']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R3.mp3"
                    />you
                    <inputChecked
                      :resuelto="false"
                      :esperado="['been']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />doing?
                  </div>
                </div>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    4. Yo no he almorzado aún I
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Have']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R4.mp3"
                    />you
                    <inputChecked
                      :resuelto="false"
                      :esperado="['had']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />lunch  yet
                  </div>
                </div>
            </div>
          </dt>

          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    5. ¿Por qué estas llorando? Why
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Have']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R5.mp3"
                    />you
                    <inputChecked
                      :resuelto="false"
                      :esperado="['been']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />crying?
                  </div>
                </div>
            </div>
          </dt>

          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    6. Ha llovido it
                    <inputChecked
                      :resuelto="false"
                      :esperado="['has']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R6.mp3"
                    />
                    <inputChecked
                      :resuelto="false"
                      :esperado="['rained']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />
                  </div>
                </div>
            </div>
          </dt>

          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    7. Mi vida ha sido maravillosa My life
                    <inputChecked
                      :resuelto="false"
                      :esperado="['has']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R7.mp3"
                    />
                    <inputChecked
                      :resuelto="false"
                      :esperado="['been']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />wonderful
                  </div>
                </div>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    8. He estado pensando en eso  I
                    <inputChecked
                      :resuelto="false"
                      :esperado="['have']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R8.mp3"
                    />
                    <inputChecked
                      :resuelto="false"
                      :esperado="['been']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />thinking about that
                  </div>
                </div>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    9. yo había visto esa pelicula I
                    <inputChecked
                      :resuelto="false"
                      :esperado="['had']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R9.mp3"
                    />
                    <inputChecked
                      :resuelto="false"
                      :esperado="['seen']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />that movie
                  </div>
                </div>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    10. Yo no he tenido tiempo I
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Have']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R10.mp3"
                    />not
                    <inputChecked
                      :resuelto="false"
                      :esperado="['had']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />time
                  </div>
                </div>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    11.¿Qué has hecho últimamente? What
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Have']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R11.mp3"
                    />you
                    <inputChecked
                      :resuelto="false"
                      :esperado="['done']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />lately?
                  </div>
                </div>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    12.¿Quién ha visto mi cartera? Who
                    <inputChecked
                      :resuelto="false"
                      :esperado="['has']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R12.mp3"
                    />
                    <inputChecked
                      :resuelto="false"
                      :esperado="['seen']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />my wallet?
                  </div>
                </div>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    13.Nunca he conocido alguien como tú I
                    <inputChecked
                      :resuelto="false"
                      :esperado="['Have']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R13.mp3"
                    />never 
                    <inputChecked
                      :resuelto="false"
                      :esperado="['met']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />somebody like you
                  </div>
                </div>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    14.Ella ha comprado un nuevo automóvil She
                    <inputChecked
                      :resuelto="false"
                      :esperado="['has']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R14.mp3"
                    />
                    <inputChecked
                      :resuelto="false"
                      :esperado="['bought']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />a new car
                  </div>
                </div>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    15.El profesor no ha enviado el archivo aun The teacher
                    <inputChecked
                      :resuelto="false"
                      :esperado="['has']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R15.mp3"
                    />not
                    <inputChecked
                      :resuelto="false"
                      :esperado="['sent']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />the file yet
                  </div>
                </div>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    16.¿Por Cuando tiempo has estado viviendo aquí? How long
                    <inputChecked
                      :resuelto="false"
                      :esperado="['have']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R16.mp3"
                    />you
                    <inputChecked
                      :resuelto="false"
                      :esperado="['been']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />living here for?
                  </div>
                </div>
            </div>
          </dt>
          <dt>
            <div class="col-sm-12 row"></div>
            <div class="col-sm-12">
                <div class="row">
                  <div id="i" class="col-sm-1">
                  </div>
                  <div class="col-sm-11 row" id="inputText">
                    17.Ellos no habían reportado el accidente They
                    <inputChecked
                      :resuelto="false"
                      :esperado="['had']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                      audio="https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2070/AC1P70R17.mp3"
                    />not
                    <inputChecked
                      :resuelto="false"
                      :esperado="['reported']"
                      style="width: 18%; margin-left:10px; margin-right:10px;"
                    />the accident
                  </div>
                </div>
            </div>
          </dt>
        </ul>
      </div>
    </div>

    <div class="row">
          <div class="col-ms-12">
              <h3 id="subTitulo">PALABRAS IMPORTANTES CON HAVE-HAS-HAD</h3>
          </div>
          <div class="col-sm-2"></div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><strong>Just: </strong>es una fusión con Have-Has y Had y traduce <span class="colorLetraRojo">acabar de.</span></a>
      </div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><strong>Never: </strong>nunca.</a>
      </div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><strong>Ever: </strong>traduce “alguna vez” y se usa en preguntas.</a>
      </div>
    </div>
    
<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><strong>Yet: </strong>traduce “ya” en preguntas, y “aún” en negaciones.</a>

      </div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><strong>Already: </strong>“ya” y se usa en afirmaciones</a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-4">
        <tablaTC :cuestionario="tablaP23" />
      </div>
      <div class="col-sm-8"></div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><i class="fa fa-diamond" style="font-size: 1.0em;"></i>Escribe las oraciones de arriba frente a la traducción correcta</a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-8">
        <tablaTC
          :cuestionario="$data.tabla74"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-2"></div>
    </div>

  </div>
</template>

<script>
import listaIndex from "./listaIndex";
import opcionMultiple from "./opcionMultiple";
import inputChecked from "./inputChecked";
import tablaTC from "./tablaTraduccionCodigos";

export default {
  components: {
    listaIndex,
    tablaTC,
    opcionMultiple,
    inputChecked,
  },
  data() {
    return {

    tabla74: {
        bordered: false,
        fields: [
          { key: "o", label:"Oracioón en español"},
          { key: "complejo1", label: "Oración en  ingles" },

        ],
        items: [
          {
            o: "No he hecho la tarea aún",
            complejo1: { lista: ["I have not done my homework yet"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R11ihavenotdonemyhomeworkyet.mp3"},
          },
          {
            o: "¿Alguna vez has encontrado dinero?",
            complejo1: { lista: ["Have you ever found money?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R12haveyoueverfoundmoney.mp3" },
          },
          {
            o: "Ella acaba de salir para el colegio",
            complejo1: { lista: ["She just left for school"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R13shejustleftforschool.mp3" },
          },
          {
            o: "¿Alguna vez has montado un caballo?",
            complejo1: { lista: ["Have you ever ridden a horse?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R14haveyoueverriddenahorse.mp3" },
          },
          {
            o: "Ya he visto esa película",
            complejo1: { lista: ["I have already seen that movie"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R15ihavealreadyseenthatmovie.mp3" },
          },
          {
            o: "¿Alguna vez ella se ha enamorado?",
            complejo1: { lista: ["Has she ever fallen in love?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R16hassheeverfalleninlove.mp3" },
          },
          {
            o: "Acabo de desayunar",
            complejo1: { lista: ["I just had breakfast"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R17ijusthadbreakfast.mp3" },
          },
        ]
      },

      tablaP23: {
        fields: [
          { key: "complejo1", label: "PHARES", thClass: "Yelow" },
          { key: "Yet", thClass: "Yelow" },
          { key: "Ever", thClass: "Yelow" },
          { key: "Just", thClass: "Yelow" },
          { key: "Already", thClass: "Yelow" },
          { key: "Never", thClass: "Yelow" },
        ],
        items: [
          {
            complejo1: {
              lista: ["ever"],
              audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R1haveyouever..ahorse.mp3",
              textoA: "Have you",
              textoD: "(alguna vez) ridden a horse?",
              tamano: 30,
            },
            Yet: "",
            Ever: "x",
            Just: "",
            Already: "",
            Never: "",
          },
          {
            complejo1: {
              lista: ["never"],
              audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R2ihaveneverhadanarguement.mp3",
              textoA: "I have",
              textoD: "(nunca) had an argument",
              tamano: 27,
            },
            Yet: "",
            Ever: "",
            Just: "",
            Already: "",
            Never: "x",
          },
          {
            complejo1: {
              lista: ["yet"],
              audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R3ihaven'tdonethehomework.mp3",
              textoA: "I haven´t done the homework",
              textoD: "(aún)",
              tamano: 28,
            },
            Yet: "x",
            Ever: "",
            Just: "",
            Already: "",
            Never: "",
          },
          {
            complejo1: {
              lista: ["just"],
              audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R4shejustleftforschool.mp3",
              textoA: "She has",
              textoD: "(acaba) left for the school",
              tamano: 28,
            },
            Yet: "",
            Ever: "",
            Just: "x",
            Already: "",
            Never: "",
          },
          {
            complejo1: {
              lista: ["ever"],
              audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R5hassheeverfalleninlove.mp3",
              textoA: "Has she",
              textoD: "(alguna vez) fallen in love?",
              tamano: 29,
            },
            Yet: "",
            Ever: "x",
            Just: "",
            Already: "",
            Never: "",
          },
          {
            complejo1: {
              lista: ["already"],
              audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R6ihavealreadyseenthatmovie.mp3",
              textoA: "I have",
              textoD: "(ya)seen that movie",
              tamano: 26,
            },
            Yet: "",
            Ever: "",
            Just: "",
            Already: "x",
            Never: "",
          },
          {
            complejo1: {
              lista: ["yet"],
              audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R7haveyoucalledheryet.mp3",
              textoA: "Have you called her",
              textoD: "(ya)?",
              tamano: 23,
            },
            Yet: "x",
            Ever: "",
            Just: "",
            Already: "",
            Never: "",
          },
          {
            complejo1: {
              lista: ["just"],
              audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R8ihavejusteatenlunch.mp3",
              textoA: "I have",
              textoD: "(acaba) eaten lunch",
              tamano: 25,
            },
            Yet: "",
            Ever: "",
            Just: "x",
            Already: "",
            Never: "",
          },
          {
            complejo1: {
              lista: ["never"],
              audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R9wehaveneverfaught.mp3",
              textoA: "We have",
              textoD: "(nunca) fought",
              tamano: 23,
            },
            Yet: "",
            Ever: "",
            Just: "",
            Already: "",
            Never: "x",
          },
          {
            complejo1: {
              lista: ["already"],
              audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2071/AC1P71R10ihavealreadyaskedhertodance.mp3",
              textoA: "I have",
              textoD: "(ya) asked her to dance",
              tamano: 27,
            },
            Yet: "",
            Ever: "",
            Just: "",
            Already: "x",
            Never: "",
          },
        ],
      },

      tablaP21: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "ha", label: "HAVE", thClass: "Yelow" },
          { key: "he", label: "HE, HEMOS, HAN, HAS" },
        ],
        items: [
          {
            ha: "HAS",
            he: "HA",
          },
          {
            ha: "HAD",
            he: "HABÍA",
          },
        ],
      },

      tablaP51: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "pre", label: "PRESENT", thClass: "Yelow" },
          { key: "ps", label: "PAST",thClass: "Red" },
          { key: "par", label: "PARTICIPLE",thClass: "Blue" },
          { key: "pro", label: "PROGRESSIVE",thClass: "Blue2" },
        ],
        items: [
          {
            pre: "BE: Ser-estar",
            ps: "WAS: Era-estaba WERE: eras-estabamos/eramos-estabamos/eran-estaban",
            par: "BEEN: Sido-estado",
            pro: "BEING: Siendo-estando",
          },
        ],
      },

    tablaA3: {
        bordered: false,
        fields: [
          { key: "pr", label:"PRESENT",thClass: "Yelow"},
          { key: "ps", label:"PAST",thClass: "Red"},
          { key: "par", label:"PARTICIPLE",thClass: "Blue"},
          { key: "complejo1", label: "ENGLISH" },
          { key: "s", label:"SPANISH"},

        ],
        items: [
          {
            pr: "See",
            ps: "Saw",
            par: "Seen",
            complejo1: { lista: ["I have seen"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R21ihaveseen.mp3" },
            s: "Yo he visto",
          },
          {
            pr: "Eat",
            ps: "Ate",
            par: "Eaten",
            complejo1: { lista: ["I have eaten"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R22ihaveeaten.mp3" },
            s: "Yo no he comido",
          },
          {
            pr: "Have",
            ps: "Had",
            par: "Had",
            complejo1: { lista: ["I have not had"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R23ihavenothad.mp3" },
            s: "Yo no he tenido",
          },
          {
            pr: "Take",
            ps: "Took",
            par: "Taken",
            complejo1: { lista: ["Have you taken?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R24haveyoutaken.mp3" },
            s: "¿Has llevado/tomado?",
          },
          {
            pr: "Drive",
            ps: "Drove",
            par: "Driven",
            complejo1: { lista: ["He has driven."],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R25hehasdriven.mp3" },
            s: "Él ha conducido",
          },
          {
            pr: "Give",
            ps: "Gave",
            par: "Given",
            complejo1: { lista: ["I have given"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R26ihavegiven.mp3" },
            s: "He dado",
          },
          {
            pr: "Buy",
            ps: "Bought",
            par: "Bought",
            complejo1: { lista: ["Have you bought?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R27haveyoubought.mp3" },
            s: "¿Has comprado?",
          },
          {
            pr: "Steal",
            ps: "Stole",
            par: "Stolen",
            complejo1: { lista: ["I have never stolen anything"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R28ihaveneverstollenanything.mp3" },
            s: "Yo nunca he robado nada",
          },
          {
            pr: "Do",
            ps: "Did",
            par: "Done",
            complejo1: { lista: ["I have done"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R29ihavedone.mp3"},
            s: "He hecho",
          },
          {
            pr: "Make",
            ps: "Made",
            par: "Made",
            complejo1: { lista: ["We have made"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R30wehavemade.mp3" },
            s: "Hemos hecho",
          },
          {
            pr: "Write",
            ps: "Wrote",
            par: "Written",
            complejo1: { lista: ["I have written"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R31ihavewritten.mp3" },
            s: "He escrito",
          },
          {
            pr: "Teach",
            ps: "Taught",
            par: "Taught",
            complejo1: { lista: ["Have you taught?"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R32haveyoutaught.mp3"},
            s: "¿Has enseñado?",
          },
          {
            pr: "Think",
            ps: "Thought",
            par: "Thought",
            complejo1: { lista: ["I have not thought"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R33ihavenotthought.mp3" },
            s: "Yo no he pensado",
          },
          {
            pr: "Catch",
            ps: "Caught",
            par: "Caught",
            complejo1: { lista: ["I have caught"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R34ihavecaught.mp3"},
            s: "He atrapado",
          },
          {
            pr: "Throw",
            ps: "Threw",
            par: "Thrown",
            complejo1: { lista: ["They have not thrown"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R35theyhavenotthrown.mp3" },
            s: "Ellos no han lanzado",
          },
          {
            pr: "Lose",
            ps: "Lost",
            par: "Lost",
            complejo1: { lista: ["I have lost"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R36ihavelost.mp3"},
            s: "He perdido",
          },
          {
            pr: "Win",
            ps: "Won",
            par: "Won",
            complejo1: { lista: ["I have won"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R37ihavewon.mp3"},
            s: "He ganado",
          },
          {
            pr: "Let",
            ps: "Let",
            par: "Let",
            complejo1: { lista: ["I have let"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R38ihavelet.mp3" },
            s: "He permitido",
          },
          {
            pr: "Hear",
            ps: "Hear",
            par: "Heard",
            complejo1: { lista: ["I have not heard"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R39ihavenotheard.mp3"},
            s: "Yo no he escuchado",
          },
          {
            pr: "Leave",
            ps: "Leave",
            par: "Left",
            complejo1: { lista: ["I have left"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2068/AC1P68R40ihaveleft.mp3"},
            s: "He dejado",
          },
        ]
      },

    tablaA4: {
        bordered: false,
        fields: [
          { key: "pr", label:"PRESENT",thClass: "Yelow"},
          { key: "ps", label:"PAST",thClass: "Red"},
          { key: "par", label:"PARTICIPLE",thClass: "Blue"},
          { key: "complejo1", label: "ENGLISH" },
          { key: "s", label:"HAVE-HAS-HAD"},

        ],
        items: [
          {
            pr: "Work",
            ps: "Worked",
            par: "Worked",
            complejo1: { lista: ["I had not worked"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R1ihadnotworked.mp3" },
            s: "Yo no había trabajado",
          },
          {
            pr: "Play",
            ps: "Played",
            par: "Played",
            complejo1: { lista: ["Have you played?"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R2haveyouplayed.mp3" },
            s: "¿Has jugado?",
          },
          {
            pr: "Live",
            ps: "Lived",
            par: "Lived",
            complejo1: { lista: ["She has lived"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R3shehaslived.mp3"},
            s: "Ella ha vivido",
          },
          {
            pr: "Decide",
            ps: "Decided",
            par: "Decided",
            complejo1: { lista: ["We have decided"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R4wehavedecided.mp3"},
            s: "Nosotros hemos decidido",
          },
          {
            pr: "Start",
            ps: "Started",
            par: "Started",
            complejo1: { lista: ["I have not started"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R5ihavenotstrarted.mp3"},
            s: "No he empezado",
          },
          {
            pr: "Kick",
            ps: "Kicked",
            par: "Kicked",
            complejo1: { lista: ["He had kicked"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R6hehadkicked.mp3"},
            s: "Él había pateado",
          },
          {
            pr: "Jump",
            ps: "Jumped",
            par: "Jumped",
            complejo1: { lista: ["No one has jumped"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R7noonehasjumped.mp3"},
            s: "Nadie ha saltado",
          },
          {
            pr: "Watch",
            ps: "Watched",
            par: "Watched",
            complejo1: { lista: ["We have watched"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R8wehavewatched.mp3"},
            s: "Hemos visto",
          },
          {
            pr: "Miss",
            ps: "Missed",
            par: "Missed",
            complejo1: { lista: ["I have missed you"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R9ihavemissedyou.mp3"},
            s: "Te he extrañado",
          },
          {
            pr: "Fix",
            ps: "Fixed",
            par: "Fixed",
            complejo1: { lista: ["I had fixed that"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R10ihadfixedthat.mp3" },
            s: "Yo había arreglado eso",
          },
          {
            pr: "Succeed",
            ps: "Succeeded",
            par: "Succeeded",
            complejo1: { lista: ["I have not succeeded"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R11ihavenotsucceded.mp3" },
            s: "No he tenido éxito",
          },
          {
            pr: "Atack",
            ps: "Attacked",
            par: "Attacked",
            complejo1: { lista: ["He has not attacked"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R12hehasnotattacked.mp3" },
            s: "Él no ha atacado",
          },
          {
            pr: "Sign",
            ps: "Signed",
            par: "Signed",
            complejo1: { lista: ["I have not signed"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R13ihavenotsigned.mp3" },
            s: "Yo no he firmado",
          },
          {
            pr: "Prepare",
            ps: "Prepared",
            par: "Prepared",
            complejo1: { lista: ["I have prepared"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R14ihaveprepared.mp3"},
            s: "He preparado",
          },
          {
            pr: "Need",
            ps: "Needed",
            par: "Needed",
            complejo1: { lista: ["I have not needed"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R15ihavenotneeded.mp3"},
            s: "No he necesitado",
          },
          {
            pr: "Like",
            ps: "Liked",
            par: "Liked",
            complejo1: { lista: ["I have liked it"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R16ihavelikeit.mp3"},
            s: "Me ha gustado",
          },
          {
            pr: "Smile",
            ps: "Smiled",
            par: "Smiled",
            complejo1: { lista: ["Maria has smiled"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R17mariahassmiled.mp3"},
            s: "María ha sonreído",
          },
          {
            pr: "Laugh",
            ps: "Laughed",
            par: "Laughed",
            complejo1: { lista: ["We have laughed"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R18wehavelaughed.mp3"},
            s: "Nos hemos reído",
          },
          {
            pr: "Print",
            ps: "Printed",
            par: "Printed",
            complejo1: { lista: ["I have printed"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R19ihaveprinted.mp3" },
            s: "He impreso",
          },
          {
            pr: "Call",
            ps: "Called",
            par: "Called",
            complejo1: { lista: ["No one has called me"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion17/audios/page%2069/AC1P69R20noonehascalledme.mp3"},
            s: "Nadie me ha llamado",
          },
        ]
      }

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

/deep/ .Blue {
  background-color: cornflowerblue;
}
/deep/ .Blue2 {
  background-color: rgb(154, 189, 253);
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
