//<template>
  <div>

    
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8" id="cuadroTexto"> 
        <img src="https://classroom.pikinglish.com/cursos/curso1/leccion15/imagenes/imagen1.JPG" />
      </div>
      <div class="col-sm-2"></div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7" style="text-align:left;">
        <a id="textPractice"> 
          RECUERDE QUE LOS VERBOS TIENE 4 FORMAS
        </a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <listaIndex :tabla="$data.tablaP21" />
      </div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice">
          <i class="fa fa-diamond" style="font-size: 1.0em;"></i> Niegue las oraciones de la izquierda y escriba el auxiliar didn't mas el verbo en su forma presente.
        </a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC
          :cuestionario="$data.tablaA"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>

      <div class="row">
        <div class="col-sm-12">
          <h3 id="subTitulo">ESCRITURA DE LOS VERBOS REGULARES EN PASADO Y PARTICIPIO</h3>
        </div>
      </div>
        
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8" id="cuadroTexto"> 
        <img src="https://classroom.pikinglish.com/cursos/curso1/leccion15/imagenes/imagen2.JPG" />
      </div>
      <div class="col-sm-2"></div>
    </div>
        
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" id="tabla">
        <listaIndex :tabla="$data.tablaP31" />
      </div>
        <div class="col-sm-1"></div>
    </div>

    <div class="row">
      <div class="col-sm-4"></div>
      <div class="col-sm-4">
        <tablaTC
          :cuestionario="$data.tablaX1"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
     <div class="col-sm-4"></div>
    </div>

    <div class="row">
            <div class="col-ms-12">
                <h3 id="subTitulo">PRACTICE</h3>
            </div>
        </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">

        <div class="col-sm-5" id="tabla">
            <tablaTC
            :cuestionario="$data.tablaA1"
            :inglesR="false"
            :espanolR="false"
            />
        </div>

        <div class="col-sm-2" id="tabla">
        <tablaTC
          :cuestionario="$data.tablaB1"
          :inglesR="false"
          :espanolR="false"
        />
        </div>

        <div class="col-sm-2" id="tabla">
        <tablaTC
          :cuestionario="$data.tablaC1"
          :inglesR="false"
          :espanolR="false"
        />
        </div>

        <div class="col-sm-2" id="tabla">
        <tablaTC
          :cuestionario="$data.tablaD1"
          :inglesR="false"
          :espanolR="false"
        />
        </div>       
      </div>
    </div>

    <div class="row">
      <div class="col-sm-12">
            <h3 id="subTitulo">
                SONIDOS DE LOS VERBOS EN PASADO
            </h3>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <listaIndex :tabla="$data.tablaP71" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-3"></div>
      <div class="col-sm-6">
        <tablaTC
          :cuestionario="$data.tablaW2"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-3"></div>
    </div>

    <div>
        <div class="col-sm-2"></div>
        <div class="mx-auto col-sm-8">
            <a id="textPractice">  
                Nota: En otras palabras, la terminación de los verbos también se explica con la vibración de las cuerdas bucales, es decir
                si al final del verbo el sonido nos hace vibrar las cuerdas bucales entonces en pasado se pronuncia con “d” y si no vibran
                entonces se pronuncia con “t” y los terminados en D y T se pronuncian “id”. La e al final de una palabra es muda.
            </a>
        </div>
        <div class="col-sm-2"></div>
    </div>
    <br>

    <div class="row" id="tablas">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div class="col-sm-6" id="tabla">
            <tablaTC
            :cuestionario="$data.tablaZ1"
            :inglesR="false"
            :espanolR="false"
            />
        </div>
        <div class="col-sm-2" id="tabla">
            <tablaTC
            :cuestionario="$data.tablaV1"
            :inglesR="false"
            :espanolR="false"
            />
        </div>

            <div class="col-sm-2" id="tabla">
            <tablaTC
            :cuestionario="$data.tablaY1"
            :inglesR="false"
            :espanolR="false"
            />
            </div>

            <div class="col-sm-2" id="tabla">
            <tablaTC
            :cuestionario="$data.tablaW1"
            :inglesR="false"
            :espanolR="false"
            />
            </div>
      </div>
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

  methods: {
    showModal(text) {
      this.$refs[text].show();
    },
  },

  data() {
    return { 

    tablaP71: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "es", label: "Ending sounds", thClass: "Yelow" },
          { key: "ver", label: "VERBO", thClass: "Yelow" },
          { key: "ps", label: "PASADO", thClass: "Yelow" },
          { key: "s", label: "SONIDO",thClass: "Yelow"},
          { key: "pr", label: "Pronunciación",thClass: "Yelow"},
        ],
        items: [
          {
            es: "N, L, M, Y, R, U, V, B, G, Z. Some consonants sound differently from Spanish sounds such as: close: z",
            ver: "CLEAN - SMILE - CLAIM - PLAY - POUR - SUE - LIVE - GRAB - CLOG - CLOSE",
            ps: "CLEANED",
            s: "“d”",
            pr: "<Cliind>",
          },
          {
            es: "K, F, SH, S, X, P. Some consonants sound differently from Spanish sounds such as: laugh: f",
            ver: "WORK - FIX - LAUGH - FINISH - MISS - STOP",
            ps: "WORKED",
            s: "“t”",
            pr: "<Workt>",
          },
          {
            es: "T, D. The e sound at the end of a word is silent",
            ver: "WANT - DECIDE",
            ps: "WANTED",
            s: "“id”",
            pr: "<Wantid>",
          },
        ],
      },        

    tablaA: {
        bordered: false,
        fields: [
          { key: "pform", label:"POSITIVE FORM"},
          { key: "complejo1", label: "NEGATIVE FORM" },

        ],
        items: [
          {
            pform: "1.She felt very well",
            complejo1: { lista: ["She didnt feel very well"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P60R1b.mp3" },
          },
          {
            pform: "2.I drove for miles and miles",
            complejo1: { lista: ["I didnt drive for miles and miles"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P60R2b.mp3" },
          },
          {
            pform: "3.We ate at a restaurant near home",
            complejo1: { lista: ["We didnt eat at a restaurant near home"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P60R3b.mp3" },
          },
          {
            pform: "4.I thought that you were working",
            complejo1: { lista: ["I didnt think that you were working"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P60R4b.mp3" },
          },
          {
            pform: "5.I met an interesting person at the bar",
            complejo1: { lista: ["I didnt meet an interesting person at the bar"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P60R5b.mp3" },
          },
          {
            pform: "6.She told me that",
            complejo1: { lista: ["She didnt tell me that"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P60R6b.mp3" },
          },
          {
            pform: "7.They wrote this to you",
            complejo1: { lista: ["They didnt write this to you"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P60R7b.mp3" },
          },
          {
            pform: "8.You lost the game",
            complejo1: { lista: ["You didnt lose the game"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P60R8b.mp3" },
          },
          {
            pform: "9.We had a great moment",
            complejo1: { lista: ["We didnt have a great moment"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P60R9b.mp3" },
          },
          {
            pform: "10.My father taught me",
            complejo1: { lista: ["My father didnt teach me"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R10b.mp3" },
          },
          {
            pform: "11.He bought this car",
            complejo1: { lista: ["He didnt buy this car"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R11b.mp3" },
          },
          {
            pform: "12.I sold my house",
            complejo1: { lista: ["I didnt sell my house"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R12b.mp3" },
          },
          {
            pform: "13.He stole my money",
            complejo1: { lista: ["He didnt steal my money"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R13b.mp3" },
          },
          {
            pform: "14.I went to the bank",
            complejo1: { lista: ["I didnt go to the bank"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R14b.mp3" },
          },
          {
            pform: "15.She took the kids to piano lessons",
            complejo1: { lista: ["She didnt take the kids to"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R15b.mp3" },
          },
          {
            pform: "16.I fell down the stairs last week",
            complejo1: { lista: ["i didnt fall down the stairs"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R16b.mp3" },
          },
          {
            pform: "17.She forgave me",
            complejo1: { lista: ["She didnt forgive me"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R17b.mp3" },
          },
          {
            pform: "18.He broke the glass",
            complejo1: { lista: ["He didnt break the glass"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R18b.mp3" },
          },
          {
            pform: "19.I ran 5 miles this morning",
            complejo1: { lista: ["I didnt run 5 miles this morning"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R19b.mp3" },
          },
          {
            pform: "20.He threw the ball to me",
            complejo1: { lista: ["He didnt throw the ball to me"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R20b.mp3" },
          },
          {
            pform: "21.We rang the bell",
            complejo1: { lista: ["We didnt ring the bell"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R21b.mp3" },
          },
          {
            pform: "22.She sang a beautiful song",
            complejo1: { lista: ["She didnt sing a beautiful song"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R22b.mp3" },
          },
          {
            pform: "23.He became crazy",
            complejo1: { lista: ["He didnt become crazy"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R23b.mp3" },
          },
          {
            pform: "24.I lit a candle",
            complejo1: { lista: ["I didnt light a candle"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R24b.mp3" },
          },
          {
            pform: "25.She shot a bird",
            complejo1: { lista: ["She didnt shoot a bird"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R25b.mp3" },
          },
          {
            pform: "26.I read the book of wisdom",
            complejo1: { lista: ["I didnt read the book of wisdom"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R26b.mp3" },
          },
          {
            pform: "27.She understood very well",
            complejo1: { lista: ["She didnt understand very well"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R27b.mp3" },
          },
          {
            pform: "28.I caught a cold",
            complejo1: { lista: ["I didnt catch a cold"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R28b.mp3" },
          },
          {
            pform: "29.I said that",
            complejo1: { lista: ["I didnt say that"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R29b.mp3" },
          },
          {
            pform: "30.She swam very well",
            complejo1: { lista: ["She didnt swim very well"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R30b.mp3" },
          },
          {
            pform: "31.We kept working",
            complejo1: { lista: ["We didnt keep working"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R31b.mp3" },
          },
          {
            pform: "32.I slept for 2 hours",
            complejo1: { lista: ["I didnt sleep for 2 hours"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2060-61/AC1P61R32b.mp3" },
          },
        ],
      },

      tablaP21: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "present", label: "Present" },
          { key: "past", label: "Past" },
          { key: "participle", label: "Participle" },
          { key: "progressive", label: "Progressive" },
        ],
        items: [
          {
            present: "Go(ir)",
            past: "Went",
            participle: "Gone",
            progressive: "going",
          },
          {
            present: "Work(trabajar)",
            past: "Worked",
            participle: "Worked",
            progressive: "working",
          },
        ],
      },

      tablaX1: {
        fields: [
          { key: "complejo1", label: "Pronunciación" },
        ],
        items: [
          {complejo1: { lista:["study - Studied - Studied", "study, Studied, Studied", "study Studied Studied"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R2%20study%20studied%20studied.mp3"}},
          {complejo1: { lista:["Love - Loved - Loved","Love,Loved, Loved","Love Loved Loved" ],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R1lovelovedloved.mp3" }},
          {complejo1: { lista:["Stop - Stopped - Stopped","Stop, Stopped, Stopped","Stop  Stopped  Stopped"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R3%20stop%20stopped%20stopped.mp3" }},
          {complejo1: { lista:["Work - Worked - Worked","Stop, Stopped, Stopped","Stop  Stopped  Stopped"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R4%20work%20worked%20worked.mp3"}},

        ],
      },

      tablaW2: {
        fields: [
          { key: "complejo1", label: "Pronunciación" },
        ],
        items: [
          {complejo1: { lista:["CLEAN - SMILE - CLAIM - PLAY - POUR - SUE - LIVE - GRAB - CLOG - CLOSE","CLEAN SMILE CLAIM PLAY POUR SUE LIVE GRAB CLOG CLOSE","CLEAN, SMILE, CLAIM, PLAY, POUR, SUE, LIVE, GRAB, CLOG, CLOSE"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2063/AC1P63R1verbs1.mp3"}},
          {complejo1: { lista:["WORK - FIX - LAUGH - FINISH - MISS - STOP","WORK FIX LAUGH FINISH MISS STOP","WORK, FIX, LAUGH, FINISH, MISS, STOP"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2063/AC1P63R2verbs2.mp3" }},
          {complejo1: { lista:["WANT - DECIDE","WANT DECIDE","WANT, DECIDE"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2063/AC1P63R3verbs3.mp3" }},
          
        ],
      },

    tablaP31: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "present", label: "Present"},
          { key: "past", label: "Past" },
          { key: "participle", label: "Past" },
          { key: "a", label: "A un verbo regular se le agrega ED, ID o D solo en pasado y participio" },
          { key: "n", label: "" },
        ],
        items: [
          {
            present: "Study",
            past: "Studied",
            participle: "Studied",
            a: "Los que terminan en Y precedida de consonante se cambia la “Y” por “I” más “Ed”",
            n: "ied",
          },
          {
            present: "Love",
            past: "Loved",
            participle: "Loved",
            a: "Los que terminan en E solo se agrega la D",
            n: "d",
          },
          {
            present: "Stop",
            past: "Stopped",
            participle: "Stopped",
            a: "Con una sola silaba se duplica la última consonante más ED",
            n: "",
          },
          {
            present: "Work",
            past: "Worked",
            participle: "Worked",
            a: "Ninguna de las anteriores",
            n: "ed",
          },
        ],
      },

      tablaA1: {
        fields: [
          { key: "PRESENT", thClass: "Yelow" },
          { key: "TRANSLATION", thClass: "Yelow" },
          { key: "complejo1", label: "PAST “ied”",thClass: "Yelow" },
        ],
        items: [
          {
            PRESENT: "Deny",
            TRANSLATION: "Negar",
            complejo1: { lista: ["denied"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R5denydenied.mp3" },
          },
          {
            PRESENT: "Avoid",
            TRANSLATION: "Evitar",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Claim",
            TRANSLATION: "Reclamar",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Sue",
            TRANSLATION: "Demandar",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Laugh",
            TRANSLATION: "Reir",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Snore",
            TRANSLATION: "Roncar",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Sneeze",
            TRANSLATION: "Estornudar",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Stop",
            TRANSLATION: "Detener",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Plan",
            TRANSLATION: "Planear",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Anwer",
            TRANSLATION: "Responder",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Scratch",
            TRANSLATION: "Rascar",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Last",
            TRANSLATION: "Durar",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Succed",
            TRANSLATION: "Tener éxito",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Afford",
            TRANSLATION: "Darse el lujo",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Smell",
            TRANSLATION: "Oler",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Touch",
            TRANSLATION: "Tocar",
            complejo1: { lista: [] },
          },
          {
            PRESENT: "Fry",
            TRANSLATION: "Freír",
            complejo1: { lista: ["fried"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R21fryfried.mp3" },
          },
        ],
      },

      tablaB1: {
        fields: [
          { key: "complejo1", label: "Double+“ed“",thClass: "Yelow" },
        ],
        items: [
          {complejo1: { lista: [] }},
          {complejo1: { lista: [] }},
          {complejo1: { lista: [] }},
          {complejo1: { lista: [] }},
          {complejo1: { lista: [] }},
          {complejo1: { lista: [] }},
          {complejo1: { lista: []}},   
          {complejo1: { lista: ["stopped"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R12stopstopped.mp3" }},
          {complejo1: { lista: ["planned"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R13planplanned.mp3" }},
          {complejo1: { lista: [] }},
          {complejo1: { lista: [] }},
          {complejo1: { lista: [] }},
          {complejo1: { lista: [] }},
          {complejo1: { lista: [] }},
          {complejo1: { lista: [] }},
          {complejo1: { lista: [] }},
          {complejo1: { lista: [] }},
        ],
      },

      tablaC1: {
        fields: [
          { key: "complejo1", label: "Past “ -ed-  ”",thClass: "Yelow" },
        ],
        items: [
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["avoided"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R6avoidavoided.mp3" }},
          {complejo1: { lista: ["claimed"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R7claimclaimed.mp3" }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["laughed"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R9laughlaughed.mp3" }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"]}},   
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["answered"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R14answeranswered.mp3" }},
          {complejo1: { lista: ["scratched"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R15scratchscratched.mp3" }},
          {complejo1: { lista: ["lasted"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R16lastlasted.mp3" }},
          {complejo1: { lista: ["succeeded"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R17succeedsuceeded.mp3" }},
          {complejo1: { lista: ["afforded"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R18affordafforded.mp3" }},
          {complejo1: { lista: ["smelled"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R19smellsmelled.mp3" }},
          {complejo1: { lista: ["touched"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R20touchtouched.mp3" }},
          {complejo1: { lista: ["Aqui no es"] }},
        ],
      },

      tablaD1: {
        fields: [
          { key: "complejo1", label: "Past “ -d- ”",thClass: "Yelow" },
        ],
        items: [
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["sued"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R8suesued.mp3" }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["snored"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R10snoresnored.mp3" }},
          {complejo1: { lista: ["sneezed"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion15/audios/page%2062/AC1P62R11sneezesneezed.mp3"}},   
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
        ],
      },

      tablaZ1: {
        fields: [
          { key: "PRESENT", thClass: "Yelow" },
          { key: "complejo1", label: " PAST",thClass: "Yelow" },
        ],
        items: [
          {
            PRESENT: "I Want",
            complejo1: { lista: ["I wanted"] },
          },
          {
            PRESENT: "I Paint",
            complejo1: { lista: ["I painted"] },
          },
          {
            PRESENT: "I Smile",
            complejo1: { lista: ["I smiled"] },
          },
          {
            PRESENT: "I Laugh",
            complejo1: { lista: ["I laughed"] },
          },
          {
            PRESENT: "I finish",
            complejo1: { lista: ["I finished"] },
          },
          {
            PRESENT: "I cook",
            complejo1: { lista: ["I cooked"] },
          },
          {
            PRESENT: "I scold",
            complejo1: { lista: ["I scolded"] },
          },
          {
            PRESENT: "I need",
            complejo1: { lista: ["I needed"] },
          },
          {
            PRESENT: "I try",
            complejo1: { lista: ["I tried"] },
          },
          {
            PRESENT: "I play",
            complejo1: { lista: ["i played"] },
          },
          {
            PRESENT: "I admire",
            complejo1: { lista: ["I admired"] },
          },
        ],
      },

      tablaV1: {
        fields: [
          { key: "complejo1", label: "“T Sound“",thClass: "Yelow" },
        ],
        items: [
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["x"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"]}},   
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["x"] }},
          {complejo1: { lista: ["x"] }},
          {complejo1: { lista: ["x"] }},
        ],
      },

      tablaY1: {
        fields: [
          { key: "complejo1", label: "“T Sound“",thClass: "Yelow" },
        ],
        items: [
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["x"] }},
          {complejo1: { lista: ["x"] }},
          {complejo1: { lista: ["x"] }},
          {complejo1: { lista: ["Aqui no es"]}},   
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
        ],
      },

      tablaW1: {
        fields: [
          { key: "complejo1", label: "ID sound”",thClass: "Yelow" },
        ],
        items: [
          {complejo1: { lista: ["x"] }},
          {complejo1: { lista: ["x"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["x"]}},   
          {complejo1: { lista: ["x"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
          {complejo1: { lista: ["Aqui no es"] }},
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
