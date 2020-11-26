<template>
    <div>
       <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <div class="col-sm-1 " id="tabla">
          <listaIndex :tabla="$data.tablaAPag53" />
        </div>
        <div class="col-sm-2 " id="tabla">
          <listaIndex :tabla="$data.tablaBPag53" />
        </div>

        <div class="col-sm-2 " id="tabla">
          <listaIndex :tabla="$data.tablaCPag53" />
        </div>

        <div class="col-sm-3 " id="tabla">
          <listaIndex :tabla="$data.tablaDPag53" />
        </div>
       
      </div>
    </div>

         

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7">
        <tablaTC
          :cuestionario="$data.cuestionario1Pag54"
          :inglesR="false"
          :espanolR="true"
        />
      </div>
    </div>
    <br />
    <br />
    <br />

    <p class="subTitulo marginn-left Subrayado">
      <i>
        <b>WHAT DID YOU DO YESTERDAY?</b><br />
        <b>DIALOGUE 1</b>
      </i>
    </p>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-8">
        <p
          v-for="item in dialogoPag55"
          v-html="item"
          class=" parrafoBlack"
        ></p>
      </div>
    </div>

    </div>
</template>
<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
import tablaTraduccionCodigos from "./tablaTraduccionCodigos";
import inputCE from "./inputCEnriquecido";
import tablaTC from "./tablaTraduccionCodigos";

export default {
  components: {
    listaIndex,
    inputChecked,
    tablaTraduccionCodigos,
   
    posiblesRespuestasTabla,
    tablaTC,
    inputCE,
  },
  data() {
    return {
        tablaAPag53: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "A", thClass: "Yellow ", label:"D"},
        ],

        items: [
          { A: " I" },
          { A: " You " },
          { A: " She" },
          { A: " He" },
          { A: " It" },
          { A: " They" },
          { A: "We " },
          
        ],
      },

      tablaBPag53: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "B", thClass: "Red ", label:"Present" },
        ],
        items: [
          { B: " GO" },
          { B: " See" },
          { B: " Have" },
          { B: "  Say" },
          { B: "Tell" },
          { B: "Take" },
          { B: "Eat" },
          { B: "Steal" },
          { B: "Give" },
          { B: "Buy" },
          { B: "Sell" },
          { B: "Swim" },
          { B: "Feel" },
          { B: "Fall" },
          { B: "Think" },
          { B: "Do" },
          { B: "Teach" },
          { B: "Forgive" },
          { B: "Drink" },
          { B: "Understand" },
          { B: "Find" },

          { B: "Catch" },
          { B: "Sleep" },
          { B: "Bite" },
          { B: "Wake" },
          
          { B: "Get" },
          { B: "Break" },
          { B: "Begin" },
          { B: "Build" },
          { B: "Forget" },
          { B: "Write" },
          { B: "Throw" },
          { B: "Wear" },
          { B: "Dig" },
          { B: "Hide" },
          { B: "Tear" },
          { B: "Swear" },
          { B: "Send" },
          { B: "Lend" },
          { B: "Become" },
          { B: "Come" },
          { B: "Shoot" },
          { B: "Know" },


        
        ],
      },
      tablaCPag53: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "C", thClass: "Blue ", label:"F (Past)" },
        ],

        items: [
          { C: "Went" },
          { C: "Saw" },
          { C: "Had" },
          { C: " Said" },
          { C: "Told" },
          { C: " Took" },
          { C: " Ate" },
          { C: "Stole " },
          { C: "Gave " },
          { C: " Bought" },
          { C: " Sold" },
          { C: " Swam" },

          { C: "Felt " },
          { C: "Fell " },
          { C: " Thought" },
          { C: " Did" },
          { C: "Taught " },
          { C: " Forgave" },
          { C: " Drank" },
          { C: "Understood " },
          { C: " Found" },
          { C: " Caught" },
          { C: " Slept" },
          { C: " Bit" },
          { C: " Woke" },
          { C: " Got" },
          { C: " Broke" },
          { C: "Began " },
          { C: "Built " },
          { C: "Forgot " },
          { C: "wrote " },
          { C: "Threw " },
          { C: "Wore " },
          { C: " Dug" },
          { C: " Hid" },
          { C: " Tore" },
          { C: "Swore " },
          { C: "Sent " },
          { C: " Lent" },
          { C: "Became " },
          { C: "Came" },
          { C: "Shot" },
          { C: " Knew" },

        ],
      },
        tablaDPag53: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "A", thClass: "Green  ", label:"C" },
        ],

        items: [
        
          {A:"To work"},
          {A:"You"},
          {A:" A good day"},
          {A:"That"},
          {A:"A taxi"},
          {A:"Breakfast late"},
          {A:" Lunch today"},
          {A:"Dinner at midnight"},
          {A:"Her a gift"},
          {A:"A lot of things"},
          {A:"My car"},
          {A:"Until I got tired"},
          {A:" Good"},
          {A:"You didn’t love me"},
          {A:"It well"},
          {A:" My son good manners"},
          {A:"Me"},
          {A:"Into the river"},
          {A:"Something"},
          {A:"Everything"},

          {A:" The ball"},
          {A:"On the floor"},
          {A:" My arm"},
          {A:" Up early this morning"},
          {A:" It"},
          {A:" The house of my dream"},
          {A:"To tell you"},
          {A:"This to you"},
          {A:" A pair of old shoes"},
          {A:"A big house"},
          {A:"The keys under the bed"},
          {A:"My shirt"},
          {A:"To God"},
          {A:"Angry with her"},


        ],
      },

      cuestionario1Pag54: {
        fields: [
          { key: "D", thClass: "Red parrafoBlack" },
          { key: "F", thClass: "Yellow parrafoBlack" },
          { key: "C", thClass: "Green parrafoBlack" },
          { key: "complejo1", label: "ENGLISH" },
          { key: "E", label: "SPANISH" },
        ],
        items: [
          {
            D: 1,
            F: 5,
            C: 2,

            complejo1: { lista: ["I told you  "], tamano: 25 },
            E: " Te lo dije",
          },
          {
            D: 3,
            F: 7,
            C: 6,

            complejo1: { lista: ["She ate breakfast late  "], tamano: 25 },
            E: "Ella desayunó tarde ",
          },
          {
            D: 6,
            F: 2,
            C: 2,

            complejo1: { lista: [" We saw you N"], tamano: 25 },
            E: " osotros te vimos",
          },
          {
            D: 1,
            F: 25,
            C: 24,

            complejo1: {
              lista: [" I woke up early this morning "],
              tamano: 25,
            },
            E: " Me desperté temprano esta mañana",
          },
          {
            D: 4,
            F: 11,
            C: 20,

            complejo1: { lista: [" He sold everything "], tamano: 25 },
            E: "Él vendió todo ",
          },
          {
            D: 1,
            F: 20,
            C: 4,

            complejo1: { lista: [" I understood that "], tamano: 25 },
            E: "Yo entendí eso ",
          },
          {
            D: 7,
            F: 13,
            C: 13,

            complejo1: { lista: [" They felt good "], tamano: 25 },
            E: "Ellos se sintieron bien ",
          },
          {
            D: 1,
            F: 15,
            C: 14,

            complejo1: { lista: [" I thought you didn´t love me"], tamano: 25 },
            E: "  Pensé que no me amabas",
          },
          {
            D: 3,
            F: 22,
            C: 21,

            complejo1: { lista: ["She caught the ball "], tamano: 25 },
            E: " Ella atrapó el balón ",
          },
          {
            D: 2,
            F: 16,
            C: 15,

            complejo1: { lista: ["You did it well  "], tamano: 25 },
            E: "Lo hiciste bien ",
          },
          {
            D: 1,
            F: 40,
            C: 34,

            complejo1: { lista: [" I became angry with her "], tamano: 25 },
            E: "Me enojé con ella ",
          },
          {
            D: 6,
            F: 30,
            C: 27,

            complejo1: { lista: ["They forgot to tell you"], tamano: 25 },
            E: " Ellos olvidaron decirte  ",
          },
          {
            D: 1,
            F: 44,
            C: 25,

            complejo1: { lista: [" I knew it "], tamano: 25 },
            E: "Yo lo sabía ",
          },
          {
            D: 1,
            F: 21,
            C: 29,

            complejo1: { lista: [" I found a pair of old shoes "], tamano: 25 },
            E: " Encontré un par de zapatos viejos",
          },
          {
            D: 3,
            F: 27,
            C: 25,

            complejo1: { lista: [" She broke it"], tamano: 25 },
            E: "  Ella lo rompió",
          },
          {
            D: 1,
            F: 23,
            C: 22,

            complejo1: { lista: [" I slept on the floor "], tamano: 25 },
            E: " Yo dormí en el suelo",
          },
          {
            D: 1,
            F: 17,
            C: 16,

            complejo1: {
              lista: [" I taught my son good manners "],
              tamano: 25,
            },
            E: " Le enseñé a mi hijo buenos modales",
          },
          {
            D: 4,
            F: 19,
            C: 25,

            complejo1: { lista: ["He drank it "], tamano: 25 },
            E: "Él se lo tomó  ",
          },
          {
            D: 1,
            F: 14,
            C: 18,

            complejo1: { lista: ["I fell into the river"], tamano: 25 },
            E: "  Me caí al rio ",
          },
          {
            D: 1,
            F: 10,
            C: 10,

            complejo1: { lista: [" I bought a lot of things "], tamano: 25 },
            E: " Yo compré muchas cosas",
          },
          {
            D: 6,
            F: 10,
            C: 10,

            complejo1: { lista: ["We bought a lot of things "], tamano: 25 },
            E: "Compramos muchas cosas ",
          },
          {
            D: 1,
            F: 2,
            C: 10,

            complejo1: { lista: ["I saw a lot of things  "], tamano: 25 },
            E: " Yo vi muchas cosas",
          },
          {
            D: 2,
            F: 8,
            C: 12,

            complejo1: { lista: ["You stole my car"], tamano: 25 },
            E: "  Tú te robaste mi carro ",
          },
          {
            D: 1,
            F: 4,
            C: 4,

            complejo1: { lista: [" I said that "], tamano: 25 },
            E: " Yo dije eso",
          },
          {
            D: 3,
            F: 18,
            C: 17,

            complejo1: { lista: ["She forgave me  "], tamano: 25 },
            E: "Ella me perdonó ",
          },
          {
            D: 6,
            F: 9,
            C: 9,

            complejo1: { lista: [" We gave her a gift "], tamano: 25 },
            E: " Nosotros le dimos a ella un regalo",
          },
          {
            D: 1,
            F: 1,
            C: 1,

            complejo1: { lista: ["I went to work  "], tamano: 25 },
            E: " Yo fui a trabajar",
          },
          {
            D: 2,
            F: 2,
            C: 10,

            complejo1: { lista: [" You saw a lot of things "], tamano: 25 },
            E: " Tú vistes muchas cosas",
          },
          {
            D: 3,
            F: 7,
            C: 7,

            complejo1: { lista: ["She had lunch today  "], tamano: 25 },
            E: " Ella almorzó hoy",
          },
          {
            D: 4,
            F: 6,
            C: 5,

            complejo1: { lista: ["He took a taxi  "], tamano: 25 },
            E: " Él tomó un taxi",
          },
          {
            D: 4,
            F: 8,
            C: 5,

            complejo1: { lista: [" He stole a taxi"], tamano: 25 },
            E: " Él robó un taxi ",
          },
          {
            D: 1,
            F: 12,
            C: 12,

            complejo1: { lista: [" I swam until I got tired "], tamano: 25 },
            E: "Nadé hasta que me cansé ",
          },
          {
            D: 3,
            F: 24,
            C: 23,

            complejo1: { lista: [" She bit my arm "], tamano: 25 },
            E: "Ella me mordió mi brazo ",
          },
        ],
      },
      dialogoPag55: [
        "Ariel: Hi, how are you?",
        "<strong>David:</strong> Hi, I am very well, thank you! how about you?",
        "<strong>Ariel:</strong> So far, so good!",
        "<strong>David:</strong> Wow! I´m glad to hear that, and what did you do yesterday?",
        "<strong>Ariel:</strong> Yesterday? Well, I <FONT class='text-danger Subrayado'>had</FONT> a very busy day",
        "<strong>David:</strong> Oh really?",
        "<strong>Ariel:</strong> Oh yeah! I <FONT class='text-danger Subrayado'>had</FONT> a very long day. I <FONT class='text-danger Subrayado'>woke up</FONT> really early because my father <FONT class='text-danger Subrayado'>made</FONT> too much noise. I <FONT class='text-danger Subrayado'>had to</FONT> take a cold shower because my mom <FONT class='text-danger Subrayado'>forgot</FONT> to pay the electricity bill, however, I <FONT class='text-danger Subrayado'>felt</FONT> very good. At 7:00 am everyone including me <FONT class='text-danger Subrayado'>sat</FONT> at the table to have breakfast. I <FONT class='text-danger Subrayado'>ate</FONT> faster than my sister so she <FONT class='text-danger Subrayado'>had</FONT> to do the dishes because I <FONT class='text-danger Subrayado'>won</FONT>. I <FONT class='text-danger Subrayado'>left</FONT> home at twenty to eight (7:40) and I <FONT class='text-danger Subrayado'>got</FONT> to school at eight o´clock (8:00). It <FONT class='text-danger Subrayado'>took</FONT> me about twenty (20) minutes to get to school from my house.",
        "<strong>ARIEL:</strong> And what did you do, David?",
        "<strong>David:</strong> Well, I <FONT class='text-danger Subrayado'>had</FONT> a very busy day yesterday, too. I <FONT class='text-danger Subrayado'>woke up</FONT> late and <FONT class='text-danger Subrayado'>got up</FONT> right away, I <FONT class='text-danger Subrayado'>went</FONT> to the bathroom, took a shower quickly, then I <FONT class='text-danger Subrayado'>put</FONT> my clothes <FONT class='text-danger Subrayado'>on</FONT>, <FONT class='text-danger Subrayado'>made</FONT> my bed, so I <FONT class='text-danger Subrayado'>went</FONT> downstairs quickly and <FONT class='text-danger Subrayado'>told</FONT> my mother “I love you”. I <FONT class='text-danger Subrayado'>sat</FONT> at the table and <FONT class='text-danger Subrayado'>ate</FONT> a tasty sandwich for breakfast. I <FONT class='text-danger Subrayado'>did</FONT> the dishes as fast as I <FONT class='text-danger Subrayado'>could</FONT> and before going to school, I <FONT class='text-danger Subrayado'>gave</FONT> my mother a hug and a kiss. I <FONT class='text-danger Subrayado'>left</FONT> home quickly so I <FONT class='text-danger Subrayado'>could</FONT> catch the bus on time because as you know the school is a little far from home. On the way to school I <FONT class='text-danger Subrayado'>saw</FONT> an accident at one side of the road. A car <FONT class='text-danger Subrayado'>hit</FONT> another car in the back but nothing <FONT class='text-danger Subrayado'>happened</FONT> to the passengers. The funny thing is that as I <FONT class='text-danger Subrayado'>got off</FONT> the bus a man on a bike <FONT class='text-danger Subrayado'>ran</FONT> me <FONT class='text-danger Subrayado'>over</FONT> and <FONT class='text-danger Subrayado'>caused</FONT> me some injuries, but fortunately it <FONT class='text-danger Subrayado'>was</FONT> a mild injury. As soon as I <FONT class='text-danger Subrayado'>got</FONT> to school, I <FONT class='text-danger Subrayado'>spoke</FONT> to my teacher about the incident so I wouldn’t be marked late. At break time I <FONT class='text-danger Subrayado'>played</FONT> basketball with Victor and we <FONT class='text-danger Subrayado'>had</FONT> fun. At lunch time I <FONT class='text-danger Subrayado'>bought</FONT> a hamburger and a portion of French fries. I didn’t do too much in the afternoon at school. At night I just <FONT class='text-danger Subrayado'>drank</FONT> a glass of orange juice before going to bed at 9:00.",
      ],

    }
    }
    }
    </script>
    <style scoped>
.show-grid {
  border: 1px solid;
  color: black;
}

#text,
#inputText {
  text-align: left;
}
/deep/ .Subrayado {
  text-decoration-line: underline;
}
/deep/ .Blue {
  background-color: cornflowerblue;
}
/deep/ .Red {
  background-color: crimson;
}
/deep/ .Yellow {
  background-color: yellow;
}
/deep/ .Green {
  background-color: chartreuse;
}

/deep/ .noHead {
  border-width: 0;
  font-size: 0;
}

inputChecked {
  display: inline-flex;
}
</style>