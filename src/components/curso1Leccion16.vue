//<template>
    <div>
        
    <div class="row" id="tablas">
      <div class="col-sm-10 row mx-auto">
        <div class="col-sm-3" id="tabla">
          <listaIndex :tabla="$data.tablaA" />
        </div>
        <div class="col-sm-3" id="tabla">
          <listaIndex :tabla="$data.tablaB" />
        </div>

        <div class="col-sm-6" id="tabla">
          <listaIndex :tabla="$data.tablaC" />
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC
          :cuestionario="$data.tablaA1"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice">
          <i class="fa fa-diamond" style="font-size: 1.0em;"></i> Reescribe el verbo de la columna F en pasado con el sujeto
        </a>
      </div>
    </div>

    <div class="row" id="tablas">
      <div class="col-sm-10 row mx-auto">

            <div class="col-sm-3" id="tabla">
                <listaIndex :tabla="$data.tablaA2" />
                </div>
                <div class="col-sm-3" id="tabla">
                <listaIndex :tabla="$data.tablaB2" />
            </div>

            <div class="col-sm-6" id="tabla">
                <tablaTC
                :cuestionario="$data.tablaA3"
                :inglesR="false"
                :espanolR="false"
                />
            </div>
        </div>
    </div>

    <div class="row">
            <div class="col-ms-8">
                <h3 id="subTitulo">PRACTICE</h3>
            </div>
            <div class="col-sm-4"></div>
        </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><i class="fa fa-diamond" style="font-size: 1.0em;"></i> Completar la oración con el verbo en su forma correcta</a>
      </div>
    </div>


<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <b-row v-for="(item, index) in preguntasCompletarP24.items">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP24.nombre + index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :audio="item.audio"
            :tamano="item.tamano"
          />
        </b-row>
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
    
    data(){
        return{

      preguntasCompletarP24: {
        nombre: "preguntasCompletarP24",
        items: [
          {
            esperado: ["cooked"],
            textoA: "1. <strong>Ella cocinó algo rápido:</strong> She",
            textoD: "something fast. <span class='colorLetraRojo'>(Cook)</span>",
            tamano: 45,
            audio: "https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R1.mp3"
          },
          {
            esperado: ["started"],
            textoA: "2. <strong>Yo empecé a estudiar:</strong> I",
            textoD: "to study. <span class='colorLetraRojo'>(Start)</span>",
            tamano: 37,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R2.mp3"
          },
          {
            esperado: ["played"],
            textoA: "3. <strong>El niño jugó en el patio:</strong> The boy",
            textoD: "in the backyard. <span class='colorLetraRojo'>(Play)</span>",
            tamano: 46,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R3.mp3"
          },
          {
            esperado: ["wanted"],
            textoA: "4. <strong>Natalie quería ir:</strong> Natalie",
            textoD: "to go. <span class='colorLetraRojo'>(Want)</span>",
            tamano: 36,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R4.mp3"
          },
          {
            esperado: ["finished"],
            textoA: "5. <strong>Yo terminé temprano:</strong> I",
            textoD: "early. <span class='colorLetraRojo'>(Finish)</span>",
            tamano: 36,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R5.mp3"
          },
          {
            esperado: ["pushed"],
            textoA: "6. <strong>Ella empujó la puerta:</strong> She",
            textoD: "the door. <span class='colorLetraRojo'>(Pushes)</span>",
            tamano: 41,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R6.mp3"
          },
          {
            esperado: ["asked"],
            textoA: "7. <strong>Yo le pregunté a Víctor:</strong> I",
            textoD: "Víctor. <span class='colorLetraRojo'>(Ask)</span>",
            tamano: 36,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R7.mp3"
          },
          {
            esperado: ["called"],
            textoA: "8. <strong>Ellos llamarón una ambulancia:</strong> They",
            textoD: "an ambulance. <span class='colorLetraRojo'>(Call)</span>",
            tamano: 48,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R8.mp3"
          },
          {
            esperado: ["worked"],
            textoA: "9. <strong>Mi mamá trabajó hoy:</strong> My mother",
            textoD: "today.<span class='colorLetraRojo'>(Work)</span>",
            tamano: 42,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R9.mp3"
          },
          {
            esperado: ["suggested"],
            textoA: "10. <strong>El profesor sugirió algo:</strong> The teacher",
            textoD: "something. <span class='colorLetraRojo'>(Suggest)</span>",
            tamano: 51,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R10.mp3"
          },
          {
            esperado: ["lived"],
            textoA: "11. <strong>Él vivió acá hace un par de años:</strong> He",
            textoD: "here a couple years ago. <span class='colorLetraRojo'>(Live)</span>",
            tamano: 54,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R11.mp3"
          },
          {
            esperado: ["barked"],
            textoA: "12. <strong>El perro ladró toda la noche:</strong> The dog",
            textoD: "all night long. <span class='colorLetraRojo'>(Bark)</span>",
            tamano: 49,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R12.mp3"
          },
          {
            esperado: ["rained"],
            textoA: "13. <strong>Llovió mucho hace dos días:</strong> It ",
            textoD: "very much two days ago. <span class='colorLetraRojo'>(Rain)</span>",
            tamano: 51,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R13.mp3"
          },
          {
            esperado: ["kicked"],
            textoA: "14. <strong>El jugador pateó el balón:</strong> The player ",
            textoD: "the ball. <span class='colorLetraRojo'>(Kick)</span>",
            tamano: 45,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R14.mp3"
          },
          {
            esperado: ["cried"],
            textoA: "15. <strong>Yo lloré un poco:</strong> I ",
            textoD: "a little. <span class='colorLetraRojo'>(Cry)</span>",
            tamano: 32,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R15.mp3"
          },
          {
            esperado: ["arrested"],
            textoA: "16. <strong>El policía arrestó al criminal:</strong> The police ",
            textoD: "the criminal. <span class='colorLetraRojo'>(Arrest)</span>",
            tamano: 51,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R16.mp3"
          },
          {
            esperado: ["needed"],
            textoA: "17. <strong>Yo te necesitaba:</strong> I ",
            textoD: "you. <span class='colorLetraRojo'>(Need)</span>",
            tamano: 33,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R17.mp3"
          },
          {
            esperado: ["liked"],
            textoA: "18. <strong>Me gustó:</strong> I ",
            textoD: "it. <span class='colorLetraRojo'>(Like)</span>",
            tamano: 25,
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2067/AC1P67R18.mp3"
          },
        ],
      },

    tablaA3: {
        bordered: false,
        fields: [
          { key: "n", label:"D",thClass: "Yelow"},
          { key: "complejo1", label: "F",thClass: "Red" },
          { key: "s", label:"SPANISH"},

        ],
        items: [
          {
            n: "1",
            complejo1: { lista: ["I played"] },
             s: "Yo Jugué",
          },
          {
            n: "2",
            complejo1: { lista: ["I worked"] },
             s: "Yo Trabajé",
          },
          {
            n: "3",
            complejo1: { lista: ["I finished"] },
             s: "Yo Terminé",
          },
          {
            n: "4",
            complejo1: { lista: ["I tried"] },
             s: "Yo Intenté",
          },
          {
            n: "5",
            complejo1: { lista: ["I cried"] },
             s: "Yo Lloré",
          },
          {
            n: "6",
            complejo1: { lista: ["I cooked"] },
             s: "Yo Cociné",
          },
          {
            n: "7",
            complejo1: { lista: ["I walked"] },
             s: "Yo Caminé",
          },
          {
            n: "8",
            complejo1: { lista: ["I decided"] },
             s: "Yo Decidí",
          },
          {
            n: "9",
            complejo1: { lista: ["I wanted"] },
             s: "Yo Quería",
          },
          {
            n: "10",
            complejo1: { lista: ["I started"] },
             s: "Yo Inicie",
          },
          {
            n: "11",
            complejo1: { lista: ["I washed"] },
             s: "Yo Lavé",
          },
          {
            n: "12",
            complejo1: { lista: ["I laughed"] },
             s: "Yo Reí",
          },
          {
            n: "13",
            complejo1: { lista: ["I smiled"] },
             s: "Yo Sonreí",
          },
          {
            n: "14",
            complejo1: { lista: ["I realized"] },
             s: "Yo Me Di Cuenta",
          },
          {
            n: "15",
            complejo1: { lista: ["I kicked"] },
             s: "Yo Pateé",
          },
          {
            n: "16",
            complejo1: { lista: ["I needed"] },
             s: "Yo Necesité",
          },
          {
            n: "17",
            complejo1: { lista: ["I achieved"] },
             s: "Yo Logré",
          },
          {
            n: "18",
            complejo1: { lista: ["I avoided"] },
             s: "Yo Evite",
          },
          {
            n: "19",
            complejo1: { lista: ["I denied"] },
             s: "Yo Negué",
          },
          {
            n: "20",
            complejo1: { lista: ["I liked"] },
             s: "A Mí Me Gusto",
          },
          {
            n: "21",
            complejo1: { lista: ["I loved"] },
             s: "Me Encantó",
          },
          {
            n: "22",
            complejo1: { lista: ["I pushed"] },
             s: "Yo Empujé",
          },
          {
            n: "23",
            complejo1: { lista: ["I opened"] },
             s: "Yo Abrí",
          },
          {
            n: "24",
            complejo1: { lista: ["I closed"] },
             s: "Yo Cerré",
          },
          {
            n: "25",
            complejo1: { lista: ["I practiced"] },
             s: "Yo Practiqué",
          },
          {
            n: "26",
            complejo1: { lista: ["I examined"] },
             s: "Yo Examiné",
          },
          {
            n: "27",
            complejo1: { lista: ["I claimed"] },
             s: "Yo Reclamé",
          },
          {
            n: "28",
            complejo1: { lista: ["I yelled"] },
             s: "Yo Grité",
          },
          {
            n: "29",
            complejo1: { lista: ["I scolded"] },
             s: "Yo Regañé",
          },
          {
            n: "30",
            complejo1: { lista: ["I admitted"] },
             s: "Yo Admití",
          },
          {
            n: "31",
            complejo1: { lista: ["I developed"] },
             s: "Yo Desarrollé",
          },
          {
            n: "32",
            complejo1: { lista: ["I painted"] },
             s: "Yo Pinté",
          },
          {
            n: "33",
            complejo1: { lista: ["I fixed"] },
             s: "Yo Arreglé",
          },
          {
            n: "34",
            complejo1: { lista: ["I cleaned"] },
             s: "Yo Limpié",
          },
          {
            n: "35",
            complejo1: { lista: ["I identified"] },
             s: "Yo Identifiqué",
          },
        ],
      },

      tablaA2: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "D", thClass: "Yelow" },
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

      tablaB2: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "F", thClass: "Red" },
        ],
        items: [
          { F: "1. Play" },
          { F: "2. Work" },
          { F: "3. Finish" },
          { F: "4. Try" },
          { F: "5. Cry" },
          { F: "6. Cook" },
          { F: "7. Walk" },
          { F: "8. Decide" },
          { F: "9. Want" },
          { F: "10. Start" },
          { F: "11. Wash" },
          { F: "12. Laugh" },
          { F: "13. Smile" },
          { F: "14. Realize" },
          { F: "15. Kick" },
          { F: "16. Need" },
          { F: "17. Achieve" },
          { F: "18. Avoid" },
          { F: "19. Deny" },
          { F: "20. Like" },
          { F: "21. Love" },
          { F: "22. Push" },
          { F: "23. Open" },
          { F: "24. Close" },
          { F: "25. Practice" },
          { F: "26. Examine" },
          { F: "27. Claim" },
          { F: "28. Yell" },
          { F: "29. Scold" },
          { F: "30. Admit" },
          { F: "31. Develop" },
          { F: "32. Paint" },
          { F: "33. Fix" },
          { F: "34. Clean" },
          { F: "35. Identify" },  
        ],
      },

    tablaA1: {
        bordered: false,
        fields: [
          { key: "d", label:"D", thClass: "Yelow"},
          { key: "f", label:"F", thClass: "Red"},
          { key: "i", label:"I", thClass: "Blue"},
          { key: "complejo1", label: "ENGLISH" },
          { key: "s", label:"SPANISH"},

        ],
        items: [
          {
            d: "1",
            f: "1",
            i: "1",
            complejo1: { lista: ["I played soccer with Victor"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R1iplayed...mp3" },
            s: "Yo jugué fútbol con Víctor"
          },
          {
            d: "3",
            f: "3",
            i: "3",
            complejo1: { lista: ["She finished late"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R2shefinnishedlate.mp3" },
            s: "Ella terminó tarde"
          },
          {
            d: "2",
            f: "2",
            i: "2",
            complejo1: { lista: ["You worked here one year ago"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R3youworkedhere....mp3" },
            s: "Tú trabajaste aquí hace un año"
          },
          {
            d: "4",
            f: "4",
            i: "4",
            complejo1: { lista: ["He tried it"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R4hetriedit.mp3" },
            s: "Él lo intentó"
          },
          {
            d: "6",
            f: "6",
            i: "6",
            complejo1: { lista: ["We cooked a delicious chicken soup"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R5wecookedadeliciouschickensoup.mp3" },
            s: "Cocinamos una deliciosa sopa de pollo"
          },
          {
            d: "1",
            f: "12",
            i: "5",
            complejo1: { lista: ["I laughed very much"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R6ilaughedverymuch.mp3" },
            s: "Yo me reí mucho"
          },
          {
            d: "3",
            f: "8",
            i: "8",
            complejo1: { lista: ["She decided to go to the party"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R7shedecidedtogotothep....mp3" },
            s: "Ella decidió ir a la fiesta"
          },
          {
            d: "1",
            f: "9",
            i: "10",
            complejo1: { lista: ["I wanted a lot of things"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R8iwantedalotofthings.mp3" },
            s: "Yo quería muchas cosas"
          },
          {
            d: "7",
            f: "14",
            i: "14",
            complejo1: { lista: ["They realized you didnt love me"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R9theyrealized....mp3" },
            s: "Ellos se dieron cuenta que tu no me amas"
          },
          {
            d: "1",
            f: "17",
            i: "19",
            complejo1: { lista: ["I achieved something"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R10iachievedsomething.mp3" },
            s: "Yo logré algo"
          },
          {
            d: "1",
            f: "20",
            i: "4",
            complejo1: { lista: ["I liked it"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R11ilikedit.mp3" },
            s: "Me gustó"
          },
          {
            d: "3",
            f: "28",
            i: "35",
            complejo1: { lista: ["She yelled at me"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R12sheyelledatme.mp3" },
            s: "Ella me gritó"
          },
          {
            d: "1",
            f: "9",
            i: "27",
            complejo1: { lista: ["I wanted to tell you"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R13iwantedto....mp3" },
            s: "Yo quería contarte"
          },
          {
            d: "6",
            f: "32",
            i: "26",
            complejo1: { lista: ["We painted the house of my dreams"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R14wepaintedthehouseof...mp3" },
            s: "Pintamos la casa de mis sueños"
          },
          {
            d: "1",
            f: "24",
            i: "17",
            complejo1: { lista: ["I closed the door"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R15iclosedthedoor.mp3" },
            s: "Yo cerré la casa"
          },
          {
            d: "4",
            f: "36",
            i: "32",
            complejo1: { lista: ["He adjusted my shirt"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R16headjustedmyshirt.mp3" },
            s: "El ajustó mi camiseta"
          },
          {
            d: "4",
            f: "40",
            i: "36",
            complejo1: { lista: ["He baked the cake"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R17hebakedthecake.mp3" },
            s: "Él horneó una torta"
          },
          {
            d: "1",
            f: "33",
            i: "11",
            complejo1: { lista: ["I fixed my car"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R18ifixedmycar.mp3" },
            s: "Yo arreglé mi carro"
          },
          {
            d: "2",
            f: "2",
            i: "7",
            complejo1: { lista: ["You worked all day long"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R19youworkedalldaylong.mp3"},
            s: "Trabajaste todo el día"
          },
          {
            d: "6",
            f: "11",
            i: "11",
            complejo1: { lista: ["He washed my car"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R20hewashedmycar.mp3"},
            s: "Él lavó mi carro"
          },
          {
            d: "7",
            f: "4",
            i: "4",
            complejo1: { lista: ["They tried it"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R21theytriedit.mp3" },
            s: "Ellos lo intentaron"
          },
          {
            d: "4",
            f: "29",
            i: "38",
            complejo1: { lista: ["He scolded the man"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R22hescoldedtheman.mp3" },
            s: "Él regañó el hombre"
          },
          {
            d: "1",
            f: "15",
            i: "21",
            complejo1: { lista: ["I kicked the ball"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R23ikickedtheball.mp3" },
            s: "Yo pateé el balón"
          },
          {
            d: "1",
            f: "3",
            i: "10",
            complejo1: { lista: ["I finished a lot of things"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R24ifinishedalotofthings.mp3" },
            s: "Yo terminé muchas cosas"
          },
          {
            d: "2",
            f: "8",
            i: "8",
            complejo1: { lista: ["You decided to go to the party"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R25youdecidedtogoto....mp3" },
            s: "Tú decidiste ir a la fiesta"
          },
          {
            d: "4",
            f: "17",
            i: "5",
            complejo1: { lista: ["He achieved very much"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R26heachieved%20verymuch.mp3"},
            s: "Él logró mucho"
          },
          {
            d: "7",
            f: "32",
            i: "11",
            complejo1: { lista: ["They painted my car"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R27theypaintedmycar.mp3" },
            s: "Yo jugué fútbol con Víctor"
          },
          {
            d: "5",
            f: "10",
            i: "3",
            complejo1: { lista: ["It started late"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R28itstartedlate.mp3" },
            s: "Empezó tarde"
          },
          {
            d: "3",
            f: "8",
            i: "8",
            complejo1: { lista: ["She decided to go to the party"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R29shedecidedtogo....mp3" },
            s: "Ella decidió ir a la fiesta"
          },
          {
            d: "1",
            f: "1",
            i: "12",
            complejo1: { lista: ["I played until i got tired"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R30iplayeduntiligottired.mp3"},
            s: "Jugué hasta que me cansé"
          },
          {
            d: "7",
            f: "27",
            i: "14",
            complejo1: { lista: ["They claimed you didnt love me"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R31theyclaimedyoudidn'tloveme.mp3" },
            s: "Ellos reclamaron que tú no me amabas"
          },
          {
            d: "3",
            f: "35",
            i: "31",
            complejo1: { lista: ["She identified the keys under the bed"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R32sheidentifiedthekeys....mp3" },
            s: "Ella identificó las llaves debajo de la cama"
          },
          {
            d: "6",
            f: "31",
            i: "4",
            complejo1: { lista: ["We developed it"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R33wedevelopedit.mp3" },
            s: "Nosotros lo desarrollamosa"
          },
          {
            d: "5",
            f: "40",
            i: "36",
            complejo1: { lista: ["It baked a cake"] ,audio:"https://classroom.pikinglish.com/cursos/curso1/leccion16/audios/page%2065/AC1P65R34itbakedacake.mp3"},
            s: "Horneó una torta"
          },
        ],
      },

      tablaA: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "D", thClass: "Yelow" },
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

      tablaB: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "F", thClass: "Red" },
        ],
        items: [
          { F: "1. Played" },
          { F: "2. Worked" },
          { F: "3. Finished" },
          { F: "4. Tried" },
          { F: "5. Cried" },
          { F: "6. Cooked" },
          { F: "7. Walked" },
          { F: "8. Decided" },
          { F: "9. Wanted" },
          { F: "10. Started" },
          { F: "11. Washed" },
          { F: "12. Laughed" },
          { F: "13. Smiled" },
          { F: "14. Realized" },
          { F: "15. Kicked" },
          { F: "16. Needed" },
          { F: "17. Achieved" },
          { F: "18. Avoided" },
          { F: "19. Denied" },
          { F: "20. Likeed" },
          { F: "21. Loved" },
          { F: "22. Pushed" },
          { F: "23. Opened" },
          { F: "24. Closed" },
          { F: "25. Practiced" },
          { F: "26. Examined" },
          { F: "27. Claimed" },
          { F: "28. Yelled" },
          { F: "29. Scolded" },
          { F: "30. Admitted" },
          { F: "31. Developed" },
          { F: "32. Painted" },
          { F: "33. Fixed" },
          { F: "34. Cleaned" },
          { F: "35. Identified" },
          { F: "36. Adjusted" },
          { F: "37. Scratched" },
          { F: "38. Dried" },
          { F: "39. Admired" },
          { F: "40. Baked" },
          { F: "41. Studied" },
          { F: "42. Checked" },
        ],
      },
      tablaC: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "I", thClass: "Blue" },
        ],
        items: [
          { I: "1. Soccer with Victor" },
          { I: "2. Here one year ago" },
          { I: "3. Late" },
          { I: "4. It" },
          { I: "5. Very much" },
          { I: "6. A delicious chicken soup" },
          { I: "7. All day long" },
          { I: "8. To go to the party" },
          { I: "9. It was late" },
          { I: "10. A lot of things" },
          { I: "11. My car" },
          { I: "12. Until I got tired" },
          { I: "13. Good" },
          { I: "14. You didn´t love me" },
          { I: "15. It well" },
          { I: "16. My son to be educated" },
          { I: "17. That house" },
          { I: "18. The accident" },
          { I: "19. Something" },
          { I: "20. Everything" },
          { I: "21. The ball" },
          { I: "22. On the floor" },
          { I: "23. My arm" },
          { I: "24. Early this morning" },
          { I: "25. My Facebook" },
          { I: "26. The house of my dreams" },
          { I: "27. To tell you" },
          { I: "28. This to you" },
          { I: "29. A pair of old shoes" },
          { I: "30. A big hole" },
          { I: "31. The keys under the bed" },
          { I: "32. My shirt" },
          { I: "33. My father" },
          { I: "34. Angry with her" },
          { I: "35. At me" },
          { I: "36. A cake" },
          { I: "37. Doing that" },
          { I: "38. The man" },
          { I: "39. The mistake" },
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
