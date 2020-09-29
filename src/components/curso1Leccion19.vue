//<template>
    <div>

      <div class="row">
        <div class="col-sm-12">
          <h3 id="subTitulo">PRACTICE</h3>
        </div>
      </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice">Completa con el verbo con poder correspondiente a la traducción.</a>
      </div>
    </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP24.items" :key="index">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">

        <div :class="'col-sm-'+item.tamaño">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP24.nombre+index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :audio="item.audio"
          />
        </div>
      </div>
    </div>
    
      <div class="row">
        <div class="col-sm-12">
          <h3 id="subTitulo">Completa la oración con la forma correcta del verbo.</h3>
        </div>
      </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC :cuestionario="tablaP63" />
      </div>
      <div class="col-sm-1"></div>
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
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <tablaTC
          :cuestionario="$data.tablaA4"
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

    
    data(){
        return{

    tablaA4: {
        bordered: false,
        fields: [
          { key: "a", label:"A",thClass: "Yelow"},
          { key: "b", label:"B",thClass: "Red"},
          { key: "c", label:"C",thClass: "Blue"},
          { key: "d", label:"D", thClass: "Blue2"},
          { key: "e", label:"E"},
          { key: "f", label:"F"},
          { key: "g", label:"G"},
          { key: "h", label:"H"},
          { key: "complejo1", label: "ENGLISH PHRASE" },

        ],
        items: [
          {
            a: "1",
            b: "1",
            c: "",
            d: "2",
            e: "13",
            f: "",
            g: "",
            h: "",
            complejo1: { lista: ["What do you feel?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R1whatdoyoufeel.mp3" },
          },
          {
            a: "3",
            b: "",
            c: "2",
            d: "3",
            e: "",
            f: "",
            g: "",
            h: "12",
            complejo1: { lista: ["Why is she swimming?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R2whyissheswimming.mp3" },
          },
          {
            a: "5",
            b: "3",
            c: "",
            d: "2",
            e: "1",
            f: "",
            g: "",
            h: "",
            complejo1: { lista: ["When did you go?"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R3whendidyougo.mp3"},
          },
          {
            a: "8",
            b: "",
            c: "10",
            d: "1",
            e: "41",
            f: "",
            g: "",
            h: "",
            complejo1: { lista: ["What time could I come?"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R4wahttimecouldicome.mp3"},
          },
          {
            a: "2",
            b: "2",
            c: "",
            d: "3",
            e: "17",
            f: "",
            g: "",
            h: "",
            complejo1: { lista: ["Where does she teach?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R5wheredoessheteach.mp3" },
          },
          {
            a: "1",
            b: "",
            c: "6",
            d: "2",
            e: "",
            f: "",
            g: "",
            h: "16",
            complejo1: { lista: ["What were you doing?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R6whatwereyoudoing.mp3" },
          },
          {
            a: "6",
            b: "3",
            c: "",
            d: "2",
            e: "18",
            f: "",
            g: "",
            h: "",
            complejo1: { lista: ["Who did you forgive?"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R7whodidyouforgive.mp3"},
          },
          {
            a: "1",
            b: "",
            c: "1",
            d: "1",
            e: "16",
            f: "",
            g: "",
            h: "",
            complejo1: { lista: ["What can I do?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R8whatcanido.mp3" },
          },
          {
            a: "4",
            b: "3",
            c: "",
            d: "2",
            e: "23",
            f: "",
            g: "",
            h: "",
            complejo1: { lista: ["How did you sleep?"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R9howdidyousleep.mp3"},
          },
          {
            a: "2",
            b: "5",
            c: "",
            d: "2",
            e: "35",
            f: "",
            g: "",
            h: "",
            complejo1: { lista: ["Where would you hide?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R10wherewouldyouhide.mp3" },
          },
          {
            a: "10",
            b: "",
            c: "12",
            d: "1",
            e: "7",
            f: "",
            g: "",
            h: "",
            complejo1: { lista: ["How much must I eat?"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R11howmuchmustieat.mp3"},
          },
          {
            a: "5",
            b: "",
            c: "8",
            d: "2",
            e: "",
            f: "",
            g: "",
            h: "41",
            complejo1: { lista: ["When are you coming?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R12whenareyoucoming.mp3" },
          },
          {
            a: "1",
            b: "",
            c: "5",
            d: "4",
            e: "",
            f: "",
            g: "",
            h: "11",
            complejo1: { lista: ["What was he selling.?"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R13whatwasheselling.mp3"},
          },
          {
            a: "9",
            b: "",
            c: "3",
            d: "2",
            e: "",
            f: "",
            g: "3",
            h: "",
            complejo1: { lista: ["How many have you had?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R14howmanyhaveyouhad.mp3" },
          },
          {
            a: "2",
            b: "",
            c: "4",
            d: "3",
            e: "",
            f: "",
            g: "1",
            h: "",
            complejo1: { lista: ["Where has she gone?"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R15wherehasshegone.mp3"},
          },
          {
            a: "",
            b: "",
            c: "4",
            d: "3",
            e: "",
            f: "",
            g: "14",
            h: "",
            complejo1: { lista: ["Has she fallen?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R16hasshefallen.mp3" },
          },
          {
            a: "",
            b: "",
            c: "",
            d: "1",
            e: "",
            f: "17",
            g: "",
            h: "",
            complejo1: { lista: ["I taught"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R17itaught.mp3" },
          },
          {
            a: "1",
            b: "",
            c: "11",
            d: "3",
            e: "",
            f: "",
            g: "4",
            h: "",
            complejo1: { lista: ["What had she said?"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R18whathadshesaid.mp3"},
          },
          {
            a: "1",
            b: "",
            c: "7",
            d: "1",
            e: "",
            f: "",
            g: "",
            h: "16",
            complejo1: { lista: ["What am I doing?"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R19whatamidoing.mp3"},
          },
          {
            a: "1",
            b: "3",
            c: "",
            d: "2",
            e: "13",
            f: "",
            g: "",
            h: "",
            complejo1: { lista: ["What did you feel?"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R20whatdidyoufeel.mp3" },
          },
          {
            a: "5",
            b: "4",
            c: "",
            d: "2",
            e: "41",
            f: "",
            g: "",
            h: "",
            complejo1: { lista: ["When will you come?"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R21whenwillyoucome.mp3"},
          },
          {
            a: "",
            b: "",
            c: "5",
            d: "1",
            e: "",
            f: "",
            g: "18",
            h: "",
            complejo1: { lista: ["Was I forgiven?"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2078/AC1P78R22wasiforgiven.mp3"},
          },
        ]
      },

      tablaAEspañol: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "A",label:"Present" },
        ],
        items: [
          { A: "1. Go" },
          { A: "2. See" },
          { A: "3. Have" },
          { A: "4. Say" },
          { A: "5. Tell" },
          { A: "6. Take" },
          { A: "7. Eat" },
          { A: "8. Steal" },
          { A: "9. Give" },
          { A: "10. Buy" },
          { A: "11. Sell" },
          { A: "12. Swim" },
          { A: "13. Fee" },
          { A: "14. Fall" },
          { A: "15. Think" },
          { A: "16. Do" },
          { A: "17. Teach" },
          { A: "18. Forgive" },
          { A: "19. Drink" },
          { A: "20. Understand" },
          { A: "21. Find" },
          { A: "22. Catch" },
          { A: "23. Sleep" },
          { A: "24. Bite" },
          { A: "25. Wake" },
          { A: "26. Get" },
          { A: "27. Break" },
          { A: "28. Begin" },
          { A: "29. Build" },
          { A: "30. Forget" },
          { A: "31. Write" },
          { A: "32. Throw" },
          { A: "33. Wear" },
          { A: "36. Dig" },
          { A: "35. Hide" },
          { A: "36. Tear" },
          { A: "37. Swear" },
          { A: "38. Send" },
          { A: "39. Lend" },
          { A: "40. Become" },
          { A: "41. Come" },
          { A: "42. Shoot" },
        ],
      },
      tablaBEspañol: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "B", label:"Past"},
        ],
        items: [
          { B: "1. went" },
          { B: "2. saw" },
          { B: "3. had" },
          { B: "4. said" },
          { B: "5. told" },
          { B: "6. took" },
          { B: "7. ate" },
          { B: "8. stole" },
          { B: "9. gave" },
          { B: "10. bought" },
          { B: "11. sold" },
          { B: "12. swam" },
          { B: "13. felt" },
          { B: "14. fell" },
          { B: "15. thought" },
          { B: "16. did" },
          { B: "17. taught" },
          { B: "18. forgave" },
          { B: "19. drank" },
          { B: "20. understood" },
          { B: "21. found" },
          { B: "22. caught" },
          { B: "23. slept" },
          { B: "24. bit" },
          { B: "25. woke" },
          { B: "26. got" },
          { B: "27. broke" },
          { B: "28. began" },
          { B: "29. built" },
          { B: "30. forgot" },
          { B: "31. wrote" },
          { B: "32. threw" },
          { B: "33. wore" },
          { B: "34. dug" },
          { B: "35. hid" },
          { B: "36. tore" },
          { B: "37. swore" },
          { B: "38. sent" },
          { B: "39. lent" },
          { B: "40. became" },
          { B: "41. came" },
          { B: "42. shot" },
        ],
      },
      tablaCEspañol: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "C",label:"Participle"},
        ],
        items: [
          { C: "1. gone " },
          { C: "2. seen" },
          { C: "3. had" },
          { C: "4. said" },
          { C: "5. told" },
          { C: "6. taken" },
          { C: "7. eaten" },
          { C: "8. stolen" },
          { C: "9. given" },
          { C: "10. bought" },
          { C: "11. sold" },
          { C: "12. swum" },
          { C: "13. felt" },
          { C: "14. fallen" },
          { C: "15. thought" },
          { C: "16. done" },
          { C: "17. taught" },
          { C: "18. forgiven" },
          { C: "19. drunk" },
          { C: "20. understood" },
          { C: "21. found" },
          { C: "22. caught" },
          { C: "23. slept" },
          { C: "24. bitten" },
          { C: "25. woken" },
          { C: "26. gotten" },
          { C: "27. broken" },
          { C: "28. begun" },
          { C: "29. built" },
          { C: "30. forgotten" },
          { C: "31. written" },
          { C: "32. thrown" },
          { C: "33. worn" },
          { C: "34. dug" },
          { C: "35. hidden" },
          { C: "36. torn" },
          { C: "37. sworn" },
          { C: "38. sent" },
          { C: "39. lent" },
          { C: "40. become" },
          { C: "41. come" },
          { C: "42. shot" },
        ],
      },
      tablaDEspañol: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "D",label:"Progressive" },
        ],
        items: [
          { D: "1. going" },
          { D: "2. seeing" },
          { D: "3. having" },
          { D: "4. saying" },
          { D: "5. telling" },
          { D: "6. taking" },
          { D: "7. eating" },
          { D: "8. stealing" },
          { D: "9. giving" },
          { D: "10. buying" },
          { D: "11. selling" },
          { D: "12. swimming" },
          { D: "13. feeling" },
          { D: "14. falling" },
          { D: "15. thinking" },
          { D: "16. doing" },
          { D: "17. teaching" },
          { D: "18. forgiving" },
          { D: "19. drinking" },
          { D: "20. understanding" },
          { D: "21. finding" },
          { D: "22. catching" },
          { D: "23. sleeping" },
          { D: "24. biting" },
          { D: "25. waking" },
          { D: "26. getting" },
          { D: "27. breaking" },
          { D: "28. beginning" },
          { D: "29. building" },
          { D: "30. forgetting" },
          { D: "31. writing" },
          { D: "32. throwing" },
          { D: "33. wearing" },
          { D: "34. digging" },
          { D: "35. hiding" },
          { D: "36. tearing" },
          { D: "37. swearing" },
          { D: "38. sending" },
          { D: "39. lending" },
          { D: "40. becoming" },
          { D: "41. coming" },
          { D: "42. shooting" },
        ],
      },
      tablaA: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "A", thClass: "Yelow" },
        ],
        items: [
          { A: "1. What" },
          { A: "2. Where" },
          { A: "3. Why" },
          { A: "4. How" },
          { A: "5. When" },        
          { A: "6. Who" },        
          { A: "7. How long" },        
          { A: "8. What time" },        
          { A: "9. How many" },        
          { A: "10. How much" },        
        ],
      },

      tablaB: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "B", thClass: "Red" },
        ],
        items: [
          { B: "1. Do" },
          { B: "2. Does" },
          { B: "3. Did" },
          { B: "4. Will" },
          { B: "5. Would" },
        ],
      },
      tablaC: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "C", thClass: "Blue" },
        ],
        items: [
          { C: "1. Can" },
          { C: "2. Is" },
          { C: "3. Have" },
          { C: "4. Has" },
          { C: "5. Was" },
          { C: "6. Were" },
          { C: "7. Am" },
          { C: "8. Are" },
          { C: "9. Should" },
          { C: "10. Could" },
          { C: "11. Had" },
          { C: "12. Must" },
        ],
      },
      tablaD: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "D", thClass: "Blue2" },
        ],
        items: [
          { D: "1. I" },
          { D: "2. You" },
          { D: "3. She" },
          { D: "4. He" },
          { D: "5. It" },
          { D: "6. We" },
          { D: "7. They" },
        ],
      },

        tablaP63: {
            fields: [
            { key: "complejo1", label: "PHARES", thClass: "Yelow" },
            { key: "PRESENT", thClass: "Yelow" },
            { key: "PAST", thClass: "Yelow" },
            { key: "PARTICIPLE", thClass: "Yelow" },
            { key: "PROGRESSIVE", thClass: "Yelow" },
            ],
            items: [
            {
                complejo1: {
                lista: ["working"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R13iamworking...mp3",
                textoA: "I am",
                textoD: "until 5pm",
                tamano: 18,
                },
                PRESENT: "Work",
                PAST: "Worked",
                PARTICIPLE: "Worked",
                PROGRESSIVE: "Working",
            },
            {
                complejo1: {
                lista: ["seen"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R14ihaveseenhim....mp3",
                textoA: "I have",
                textoD: "him twice today",
                tamano: 22,
                },
                PRESENT: "See",
                PAST: "Saw",
                PARTICIPLE: "Seen",
                PROGRESSIVE: "Seeing",
            },
            {
                complejo1: {
                lista: ["go"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R15wecangoanywhere...mp3",
                textoA: "We can",
                textoD: "anywhere on Sundays",
                tamano: 25,
                },
                PRESENT: "go",
                PAST: "Went",
                PARTICIPLE: "gone",
                PROGRESSIVE: "going",
            },
            {
                complejo1: {
                lista: ["going"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R16whereareyougoingthis...mp3",
                textoA: "Where are you",
                textoD: "this weeekend?",
                tamano: 27,
                },
                PRESENT: "go",
                PAST: "Went",
                PARTICIPLE: "gone",
                PROGRESSIVE: "going",
            },
            {
                complejo1: {
                lista: ["raining"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R17isitraininglightly...mp3",
                textoA: "It is",
                textoD: "lightly",
                tamano: 16,
                },
                PRESENT: "rain",
                PAST: "rained",
                PARTICIPLE: "rained",
                PROGRESSIVE: "raining",
            },
            {
                complejo1: {
                lista: ["doing"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R18whatareyoudoinglatertoday.mp3",
                textoA: "What are you",
                textoD: "later today?",
                tamano: 23,
                },
                PRESENT: "do",
                PAST: "did",
                PARTICIPLE: "done",
                PROGRESSIVE: "doing",
            },
            {
                complejo1: {
                lista: ["eat"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R19ithinkweshouldeat...mp3",
                textoA: "I think we should",
                textoD: "pizza",
                tamano: 21,
                },
                PRESENT: "eat",
                PAST: "ate",
                PARTICIPLE: "eaten",
                PROGRESSIVE: "eating",
            },
            {
                complejo1: {
                lista: ["been"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R20ithasbeenraining.mp3",
                textoA: "It has",
                textoD: "raining all day",
                tamano: 20,
                },
                PRESENT: "Be",
                PAST: "Was - were",
                PARTICIPLE: "been",
                PROGRESSIVE: "being",
            },
            {
                complejo1: {
                lista: ["Meet"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R21canwemeettomorrow.mp3",
                textoA: "Can we",
                textoD: "tomorrow at the park?",
                tamano: 26,
                },
                PRESENT: "Meet",
                PAST: "Met",
                PARTICIPLE: "Met",
                PROGRESSIVE: "Meeting",
            },
            {
                complejo1: {
                lista: ["found"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R22wefoundakittenina.mp3",
                textoA: "We",
                textoD: "a kitten in a box",
                tamano: 20,
                },
                PRESENT: "find",
                PAST: "found",
                PARTICIPLE: "found",
                PROGRESSIVE: "finding",
            },
            {
                complejo1: {
                lista: ["run"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R23ihavn'traninyears.mp3",
                textoA: "I haven’t",
                textoD: "in years",
                tamano: 19,
                },
                PRESENT: "run",
                PAST: "ran",
                PARTICIPLE: "run",
                PROGRESSIVE: "running",
            },
            ],
          },

      preguntasCompletarP24: {
        nombre: "preguntasCompletarP24",
        items: [
          {
            esperado: ["can"],
            textoA: "1. I ",
            textoD: "do that (yo puedo hacer eso)",
            tamaño: 6,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R1.mp3"
          },
          {
            esperado: ["is"],
            textoA: "2. This",
            textoD: "funny (esto es divertido)",
            tamaño: 5,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R2.mp3"
          },
          {
            esperado: ["are"],
            textoA: "3. We",
            textoD: "fed up with her (estamos hartos de ella)",
            tamaño: 7,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R3.mp3"
          },
          {
            esperado: ["am"],
            textoA: "4. I",
            textoD: "fed up with this (estoy harto de esto)",
            tamaño: 6,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R4.mp3"
          },
          {
            esperado: ["was"],
            textoA: "5. I",
            textoD: "busy working (yo estaba ocupado trabajando)",
            tamaño: 7,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R5.mp3"
          },
          {
            esperado: ["were"],
            textoA: "6. They",
            textoD: "crazy (ellos estaban locos)",
            tamaño: 6,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R6.mp3"
          },
          {
            esperado: ["could"],
            textoA: "7. I",
            textoD: "help you (yo podría ayudarte)",
            tamaño: 6,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R7.mp3"
          },
          {
            esperado: ["should"],
            textoA: "8. We",
            textoD: "do something quickly (deberíamos hacer algo rápido)",
            tamaño: 9,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R8.mp3"
          },
          {
            esperado: ["have"],
            textoA: "9. I",
            textoD: "had a problem (he tenido un problema)",
            tamaño: 7,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R9.mp3"
          },
          {
            esperado: ["has"],
            textoA: "10. It",
            textoD: "been raining (ha estado lloviendo)",
            tamaño: 6,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R10.mp3"
          },
          {
            esperado: ["had"],
            textoA: "11. I",
            textoD: "done it (yo lo había hecho)",
            tamaño: 5,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R11.mp3"
          },
          {
            esperado: ["must"],
            textoA: "12. You",
            textoD: "go home now (debes irte a casa ahora)",
            tamaño:7,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion19/audios/page%2076/AC1P76R12.mp3"
          },
        ],
      },

        }
    }
}
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