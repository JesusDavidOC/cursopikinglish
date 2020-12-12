<template>
  <div>
    <div class="row">
      <h3 id="subTitulo">MONTHS OF THE YEAR</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <b-card>
          <p class="parrafoTabla">
            <listaIndex :tabla="$data.tablaP102" />
            <listaIndex :tabla="$data.tablaP102B" />
          </p>
        </b-card>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">FILL IN THE GAPS</p>
      </div>
    </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP103.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div class="col-sm-">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP103.nombre + index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :audio="item.audio"
            :tamano="item.tamano"
          />
        </div>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">CARDINAL NUMBERS</h3>
    </div>

    <div class="row">
      <div class="col-sm-16 row">
        <div class="col-3">
          <b-card>
            <p class="parrafo">
              <strong>From 0 to 9</strong>
            </p>
            <p class="parrafo">Zero: 0</p>
            <p class="parrafo">One: 1</p>
            <p class="parrafo">Two: 2</p>
            <p class="parrafo">Three: 3</p>
            <p class="parrafo">Four: 4</p>
            <p class="parrafo">Five: 5</p>
            <p class="parrafo">Six: 6</p>
            <p class="parrafo">Seven: 7</p>
            <p class="parrafo">Eight: 8</p>
            <p class="parrafo">Nine: 9</p>
          </b-card>
        </div>
        <div class="col-3">
          <b-card>
            <p class="parrafo">
              <strong>From 10 to 12</strong>
            </p>
            <p class="parrafo">Ten: 10</p>
            <p class="parrafo">Eleven: 11</p>
            <p class="parrafo">Twelve: 12</p>
          </b-card>
        </div>
        <div class="col-3">
          <b-card>
            <p class="parrafo">
              <strong>
                From 13 to 19 (
                <span class="colorLetraRojo">teen</span>)
              </strong>
            </p>
            <p class="parrafo">Thirteen: 13</p>
            <p class="parrafo">Fourteen: 14</p>
            <p class="parrafo">Fifteen: 15</p>
            <p class="parrafo">Sixteen: 16</p>
            <p class="parrafo">Seventeen: 17</p>
            <p class="parrafo">Eighteen: 18</p>
            <p class="parrafo">Nineteen: 19</p>
          </b-card>
        </div>
        <div class="col-3">
          <b-card>
            <p class="parrafo">
              <strong>
                From 20 to 90 (
                <span class="colorLetraRojo">ty</span>)
              </strong>
            </p>
            <p class="parrafo">Twenty: 20</p>
            <p class="parrafo">Thirty: 30</p>
            <p class="parrafo">Forty: 40</p>
            <p class="parrafo">Fifty: 50</p>
            <p class="parrafo">Sixty:60</p>
            <p class="parrafo">Seventy: 70</p>
            <p class="parrafo">Eighty: 80</p>
            <p class="parrafo">Ninety: 90</p>
          </b-card>
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          El último numero después de cien, mil o un millón se separa con la
          palabra AND
        </p>
        <ul>
          <h3 class="parrafo">
            <li>
              $109 ( one hundred
              <span class="colorLetraRojo">and</span> nine dollars)
            </li>
            <li>
              $1091 (one thousand
              <span class="colorLetraRojo">and</span> ninety-one dollars)
            </li>
            <li>
              $10,901 (ten thousand nine hundred
              <span class="colorLetraRojo">and</span> one dollars)
            </li>
          </h3>
        </ul>
        <p class="parrafo">
          Los números de dos dígitos se separan con un guión.
        </p>
        <p class="parrafo colorLetraAzul">30 + 3 = thirty-three (33)</p>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">From 100 to 900 (HUNDRED)</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <p class="parrafoTabla">
        <listaIndex :tabla="$data.tablaP94" />
      </p>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo colorLetraAzul">MIL → THOUSAND</p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <p class="parrafoTabla">
        <listaIndex :tabla="$data.tablaP104" />
      </p>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo colorLetraAzul">MILLÓN → MILLION</p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11">
        <p class="parrafo">
          Million nunca se usa en plural:
          <span class="colorLetraRojo">MILLIONS</span>
        </p>
        <p class="parrafo">
          1,000,000 one million - 2,000,000 two million - 3,000,000 three
          million
        </p>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PRACTICE</h3>
    </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP105.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div class="col-sm">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP105.nombre + index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :tamano="item.tamano"
          />
        </div>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">WRITE THE NUMBER|</h3>
    </div>
    <div class="row" v-for="(item, index) in preguntasCompletarP105A.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div class="col-sm-">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP105.nombre + index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :tamano="item.tamano"
          />
        </div>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">COMPLETE THE FOLLOWING SENTENCES</h3>
    </div>
    <div class="row" v-for="(item, index) in preguntasCompletarP105B.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div class="col-sm-">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP105B.nombre + index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :tamano="item.tamano"
          />
        </div>
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
  methods: {
    showModal(text) {
      this.$refs[text].show();
    },
  },
  components: {
    listaIndex,
    inputChecked,
    tablaTC,
    opcionMultiple,
  },
  data() {
    return {
      tablaP94: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "Number" },
          { key: "2", label: "English" },
          { key: "html", label: "Sum" },
        ],
        items: [
          {
            1: "100",
            2: "One hundred",
            html:
              "<p class= 'parrafoTabla colorLetraRojo'><span style='font-style: italic' >+1 = one hundred and one(101)</span></p>",
          },
          {
            1: "200",
            2: "Two hundred",
            html:
              "<p class= 'parrafoTabla colorLetraRojo'><span style='font-style: italic' >+10 = two hundred and ten(210)</span></p>",
          },
          {
            1: "300",
            2: "Three hundred",
            html: "",
          },
          {
            1: "400",
            2: "Four hundred",
            html:
              "<p class= 'parrafoTabla colorLetraRojo'><span style='font-style: italic' >+16 = four hundred and sixteen(416)</span></p>",
          },
          {
            1: "500",
            2: "Five hundred",
            html: "",
          },
          {
            1: "600",
            2: "Six hundred",
            html:
              "<p class= 'parrafoTabla colorLetraRojo'><span style='font-style: italic' >+21 = six hundred and twenty-one(621)</span></p>",
          },
          {
            1: "700",
            2: "Seven hundred",
            html: "",
          },
          {
            1: "800",
            2: "Eight hundred",
            html: "",
          },
          {
            1: "900",
            2: "Nine hundred",
            html:
              "<p class= 'parrafoTabla colorLetraRojo'><span style='font-style: italic'>+99 = nine hundred and ninety-nine(999)</span></p>",
          },
        ],
      },
      tablaP104: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "Number" },
          { key: "2", label: "English" },
        ],
        items: [
          {
            1: "1000",
            2: "One thousand",
          },
          {
            1: "10,000",
            2: "Ten thousand",
          },
          {
            1: "15,000",
            2: "Fifteen thousand",
          },
          {
            1: "20,000",
            2: "Twenty thousand",
          },
          {
            1: "21,000",
            2: "Twenty-one thousand",
          },
          {
            1: "100,000",
            2: "One hundred thousand",
          },
          {
            1: "500,000",
            2: "Five hundred thousand",
          },
          {
            1: "550,000",
            2: "Five hundred fifty thousand",
          },
          {
            1: "555,000",
            2: "Five hundred fifty-five thousand",
          },
          {
            1: "555,555",
            2: "Five hundred fifty-five thousand five hundred and fifty-five",
          },
        ],
      },
      preguntasCompletarP103: {
        nombre: "preguntasCompletarP103",
        items: [
          {
            esperado: ["12"],
            textoA: "1. There are",
            textoD: "months in a year.",
            tamano: 26,
            audio: "aaa",
          },
          {
            esperado: ["december"],
            textoA: "2. Christmas is celebrated in ",
            textoD: ".",
            tamano: 30,
            audio: "",
          },
          {
            esperado: ["january"],
            textoA: "3. The first month of the year is",
            textoD: ".",
            tamano: 30,
            audio: "",
          },
          {
            esperado: ["november"],
            textoA: "4. The month before December is",
            textoD: ".",
            tamano: 33,
            audio: "",
          },
          {
            esperado: ["july"],
            textoA:
              "5. Colombian Declaration of Independence was on the 20 th of",
            textoD: "in 1810.",
            tamano: 50,
            audio: "",
          },
          {
            esperado: ["october"],
            textoA: "6. Halloween is on the 31 st of",
            textoD: ".",
            tamano: 30,
            audio: "",
          },
          {
            esperado: ["february"],
            textoA: "7. The only month with only 28 days is",
            textoD: ".",
            tamano: 35,
            audio: "",
          },
          {
            esperado: ["march"],
            textoA: "8. What month begins with the M and ends with the h?",
            textoD: ".",
            tamano: 43,
            audio: "",
          },
          {
            esperado: ["april"],
            textoA: "9. What is the fourth month of the year?",
            textoD: ".",
            tamano: 33,
            audio: "",
          },
          {
            esperado: ["June"],
            textoA: "10. What is the month after may?",
            textoD: ".",
            tamano: 30,
            audio: "",
          },
        ],
      },
      preguntasCompletarP105A: {
        nombre: "preguntasCompletarP105A",
        items: [
          {
            esperado: ["916"],
            textoA: "1. Nine hundred sixteen",
            textoD: "",
            tamano: 24,
          },
          {
            esperado: ["1001"],
            textoA: "2. one thousand one ",
            textoD: ".",
            tamano: 23,
          },
          {
            esperado: ["21"],
            textoA: "3. twenty-one",
            textoD: ".",
            tamano: 17,
          },
          {
            esperado: ["1101"],
            textoA: "4. One thousand one hundred one",
            textoD: ".",
            tamano: 31,
          },
          {
            esperado: ["66666"],
            textoA: "5. sixty-six thousand six hundred sixty-six",
            textoD: ".",
            tamano: 36,
          },
          {
            esperado: ["999"],
            textoA: "6. Nine hundred ninety-nine",
            textoD: ".",
            tamano: 26,
          },
          {
            esperado: ["1555"],
            textoA: "7. one thousand five hundred fifty-five",
            textoD: ".",
            tamano: 33,
          },
          {
            esperado: ["1100101"],
            textoA: "8. One million one hundred thousand one hundred one",
            textoD: ".",
            tamano: 44,
          },
          {
            esperado: ["33"],
            textoA: "9. thirty-three",
            textoD: ".",
            tamano: 17,
          },
        ],
      },
      preguntasCompletarP105B: {
        nombre: "preguntasCompletarP105A",
        items: [
          {
            esperado: ["one hundred"],
            textoA: "1. One century is",
            textoD: "years",
            tamano: 28,
          },
          {
            esperado: ["ten"],
            textoA: "2. ",
            textoD: "decades is one century.",
            tamano: 24,
          },
          {
            esperado: ["ten"],
            textoA: "3. one decade is",
            textoD: "years.",
            tamano: 23,
          },
          {
            esperado: ["twelve"],
            textoA: "4. one year is",
            textoD: "months.",
            tamano: 24,
          },
          {
            esperado: ["Three hundred sixty four"],
            textoA: "5. one year is",
            textoD: "days.",
            tamano: 33,
          },
          {
            esperado: ["twenty four"],
            textoA: "6. one day is",
            textoD: "hours.",
            tamano: 25,
          },
          {
            esperado: ["one thousand four hundred forty"],
            textoA: "7. one day is",
            textoD: "minutes.",
            tamano: 39,
          },
          {
            esperado: ["sixty"],
            textoA: "8. one hour is",
            textoD: "minutes.",
            tamano: 23,
          },
          {
            esperado: ["three thousand six hundred"],
            textoA: "9. one hour is",
            textoD: "seconds.",
            tamano: 37,
          },
          {
            esperado: ["one thousand six hundred nine"],
            textoA: "10. one mile is",
            textoD: "meters.",
            tamano: 38,
          },
        ],
      },
      preguntasCompletarP105: {
        nombre: "preguntasCompletarP105",
        items: [
          {
            esperado: ["sixteen"],
            textoA: "16",
            textoD: "",
            tamano: 13,
          },
          {
            esperado: ["two"],
            textoA: "2",
            textoD: ".",
            tamano: 11,
          },
          {
            esperado: ["ninety nine"],
            textoA: "99",
            textoD: ".",
            tamano: 16,
          },
          {
            esperado: ["one hundred"],
            textoA: "100",
            textoD: ".",
            tamano: 18,
          },
          {
            esperado: ["one hundred one"],
            textoA: "101",
            textoD: "",
            tamano: 20,
          },
          {
            esperado: ["nine hundred and ninety-nine"],
            textoA: "999",
            textoD: ".",
            tamano: 27,
          },
          {
            esperado: ["one thousand"],
            textoA: "1000",
            textoD: ".",
            tamano: 19,
          },
          {
            esperado: ["ten thousand"],
            textoA: "10,000",
            textoD: ".",
            tamano: 20,
          },
          {
            esperado: ["nine thousand"],
            textoA: "90,000",
            textoD: ".",
            tamano: 20,
          },
          {
            esperado: ["ninety-nine thousand nine hundred ninety-nine"],
            textoA: "99,999",
            textoD: ".",
            tamano: 39,
          },
          {
            esperado: ["hundred thousand"],
            textoA: "100,000",
            textoD: ".",
            tamano: 23,
          },
          {
            esperado: ["twelve"],
            textoA: "12",
            textoD: ".",
            tamano: 13,
          },
          {
            esperado: [
              "one million nine hundred ninety-nine thousand nine hundred seventy-six",
            ],
            textoA: "1,999,976",
            textoD: ".",
            tamano: 55,
          },
        ],
      },
      tablaP102: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "January", thClass: "Blue" },
          { key: "2", label: "February", thClass: "Blue" },
          { key: "3", label: "March", thClass: "Blue" },
          { key: "4", label: "April", thClass: "Blue" },
          { key: "5", label: "May", thClass: "Blue" },
          { key: "6", label: "June", thClass: "Blue" },
        ],
        items: [
          {
            1: "Enero",
            2: "Febrero",
            3: "Marzo",
            4: "Abril",
            5: "Mayo",
            6: "Junio",
          },
        ],
      },
      tablaP102B: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "July", thClass: "Blue" },
          { key: "2", label: "August", thClass: "Blue" },
          { key: "3", label: "September", thClass: "Blue" },
          { key: "4", label: "October", thClass: "Blue" },
          { key: "5", label: "November", thClass: "Blue" },
          { key: "6", label: "December", thClass: "Blue" },
        ],
        items: [
          {
            1: "Julio",
            2: "Agosto",
            3: "Septiembre",
            4: "Octubre",
            5: "Noviembre",
            6: "Diciembre",
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
/deep/.colorLetraAzul {
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
  font-size: 1.5em;
  color: black;
  font-family: "PT Sans";
  font-weight: bold;
  margin-bottom: auto;
}
#numeroMagico2 {
  background: greenyellow;
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
</style>