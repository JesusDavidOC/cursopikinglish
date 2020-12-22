<template>
  <div>
    <div class="row">
      <h3 id="subTitulo">MONTHS OF THE YEAR</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <listaIndex :tabla="$data.tablaP102" />
        <listaIndex :tabla="$data.tablaP102B" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3>FILL IN THE GAPS</h3>
      </div>
    </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP103.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div :class="'col-sm-'+item.tamaño">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP103.nombre+index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :audio="item.audio"
          />
        </div>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">CARDINAL NUMBERS</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <h4 style="text-align: left">
        <strong>Zero: 0</strong>
      </h4>
      <div class="col-sm-10 row">
        <div class="col-3" style="text-align: left">
          <h4>
            <strong>From 1 to 9</strong>
          </h4>
          <h5>One: 1</h5>
          <h5>Two: 2</h5>
          <h5>Three: 3</h5>
          <h5>Four: 4</h5>
          <h5>Five: 5</h5>
          <h5>Six: 6</h5>
          <h5>Seven: 7</h5>
          <h5>Eight: 8</h5>
          <h5>Nine: 9</h5>
        </div>
        <div class="col-3">
          <h4>
            <strong>From 10 to 12</strong>
          </h4>
          <h5>Ten: 10</h5>
          <h5>Eleven: 11</h5>
          <h5>Twelve: 12</h5>
        </div>
        <div class="col-3">
          <h4>
            <strong>
              From 13 to 19 (
              <span class="colorLetraRojo">teen</span>)
            </strong>
          </h4>
          <h5>Thirteen: 13</h5>
          <h5>Fourteen: 14</h5>
          <h5>Fifteen: 15</h5>
          <h5>Sixteen: 16</h5>
          <h5>Seventeen: 17</h5>
          <h5>Eighteen: 18</h5>
          <h5>Nineteen: 19</h5>
        </div>
        <div class="col-3">
          <h4>
            <strong>
              From 20 to 90 (
              <span class="colorLetraRojo">ty</span>)
            </strong>
          </h4>
          <h5>Twenty: 20</h5>
          <h5>Thirty: 30</h5>
          <h5>Forty: 40</h5>
          <h5>Fifty: 50</h5>
          <h5>Sixty:60</h5>
          <h5>Seventy: 70</h5>
          <h5>Eighty: 80</h5>
          <h5>Ninety: 90</h5>
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3>El último numero después de cien, mil o un millón se separa con la palabra AND</h3>
        <ul>
          <h3 style="text-align: left">
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
        <h3>Los números de dos dígitos se separan con un guión.</h3>
        <h1 class="colorLetraAzul">30 + 3 = thirty-three (33)</h1>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">From 100 to 900 (HUNDRED)</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <listaIndex :tabla="$data.tablaP94" />
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3 class="colorLetraAzul">MIL → THOUSAND</h3>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <listaIndex :tabla="$data.tablaP104" />
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3 class="colorLetraAzul">MILLÓN → MILLION</h3>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11">
        <h5>Million nunca se usa en plural: <span class="colorLetraRojo">MILLIONS</span></h5>
        <h5>1,000,000 one million - 2,000,000 two million - 3,000,000 three million</h5> 
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">
        PRACTICE
      </h3>
    </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP105.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div :class="'col-sm-'+item.tamaño">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP105.nombre+index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
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
        <div :class="'col-sm-'+item.tamaño">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP105.nombre+index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
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
        <div :class="'col-sm-'+item.tamaño">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP105B.nombre+index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
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
              "<h3 class='colorLetraRojo'><span style='font-style: italic' >+1 = one hundred and one(101)</span></h3>",
          },
          {
            1: "200",
            2: "Two hundred",
            html:
              "<h3 class='colorLetraRojo'><span style='font-style: italic' >+10 = two hundred and ten(210)</span></h3>",
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
              "<h3 class='colorLetraRojo'><span style='font-style: italic' >+16 = four hundred and sixteen(416)</span></h3>",
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
              "<h3 class='colorLetraRojo' ><span style='font-style: italic' >+21 = six hundred and twenty-one(621)</span></h3>",
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
              "<h3 class='colorLetraRojo'><span style='font-style: italic'>+99 = nine hundred and ninety-nine(999)</span></h3>",
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
            tamaño: 5,
            audio: ''
          },
          {
            esperado: ["december"],
            textoA: "2. Christmas is celebrated in ",
            textoD: ".",
            tamaño: 6,
            audio: ''
          },
          {
            esperado: ["january"],
            textoA: "3. The first month of the year is",
            textoD: ".",
            tamaño: 6,
            audio: ''
          },
          {
            esperado: ["november"],
            textoA: "4. The month before December is",
            textoD: ".",
            tamaño: 6,
            audio: ''
          },
          {
            esperado: ["july"],
            textoA:
              "5. Colombian Declaration of Independence was on the 20 th of",
            textoD: "in 1810.",
            tamaño: 9,
            audio: ''
          },
          {
            esperado: ["october"],
            textoA: "6. Halloween is on the 31 st of",
            textoD: ".",
            tamaño: 6,
            audio: ''
          },
          {
            esperado: ["february"],
            textoA: "7. The only month with only 28 days is",
            textoD: ".",
            tamaño: 7,
            audio: ''
          },
          {
            esperado: ["march"],
            textoA: "8. What month begins with the M and ends with the h?",
            textoD: ".",
            tamaño: 8,
            audio: ''
          },
          {
            esperado: ["april"],
            textoA: "9. What is the fourth month of the year?",
            textoD: ".",
            tamaño: 6,
            audio: ''
          },
          {
            esperado: ["June"],
            textoA: "10. What is the month after may?",
            textoD: ".",
            tamaño: 6,
            audio: ''
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
            tamaño: 5,
          },
          {
            esperado: ["1001"],
            textoA: "2. one thousand one ",
            textoD: ".",
            tamaño: 5,
          },
          {
            esperado: ["21"],
            textoA: "3. twenty-one",
            textoD: ".",
            tamaño: 4,
          },
          {
            esperado: ["1101"],
            textoA: "4. One thousand one hundred one",
            textoD: ".",
            tamaño: 6,
          },
          {
            esperado: ["66666"],
            textoA:
              "5. sixty-six thousand six hundred sixty-six",
            textoD: ".",
            tamaño: 7,
          },
          {
            esperado: ["999"],
            textoA: "6. Nine hundred ninety-nine",
            textoD: ".",
            tamaño: 5,
          },
          {
            esperado: ["1555"],
            textoA: "7. one thousand five hundred fifty-five",
            textoD: ".",
            tamaño: 6,
          },
          {
            esperado: ["1100101"],
            textoA: "8. One million one hundred thousand one hundred one",
            textoD: ".",
            tamaño: 8,
          },
          {
            esperado: ["33"],
            textoA: "9. thirty-three",
            textoD: ".",
            tamaño: 4,
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
            tamaño: 5,
          },
          {
            esperado: ["ten"],
            textoA: "2. ",
            textoD: "decades is one century.",
            tamaño: 5,
          },
          {
            esperado: ["ten"],
            textoA: "3. one decade is",
            textoD: "years.",
            tamaño: 5,
          },
          {
            esperado: ["twelve"],
            textoA: "4. one year is",
            textoD: "months.",
            tamaño: 5,
          },
          {
            esperado: ["Three hundred sixty four"],
            textoA:
              "5. one year is",
            textoD: "days.",
            tamaño: 4,
          },
          {
            esperado: ["twenty four"],
            textoA: "6. one day is",
            textoD: "hours.",
            tamaño: 5,
          },
          {
            esperado: ["one thousand four hundred forty"],
            textoA: "7. one day is",
            textoD: "minutes.",
            tamaño: 6,
          },
          {
            esperado: ["sixty"],
            textoA: "8. one hour is",
            textoD: "minutes.",
            tamaño: 6,
          },
          {
            esperado: ["three thousand six hundred"],
            textoA: "9. one hour is",
            textoD: "seconds.",
            tamaño: 6,
          },
          {
            esperado: ["one thousand six hundred nine"],
            textoA: "10. one mile is",
            textoD: "meters.",
            tamaño: 7,
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
            tamaño: 3,
          },
          {
            esperado: ["two"],
            textoA: "2",
            textoD: ".",
            tamaño: 3,
          },
          {
            esperado: ["ninety nine"],
            textoA: "99",
            textoD: ".",
            tamaño: 3,
          },
          {
            esperado: ["one hundred"],
            textoA: "100",
            textoD: ".",
            tamaño: 4,
          },
          {
            esperado: ["one hundred one"],
            textoA:
              "101",
            textoD: "",
            tamaño: 4,
          },
          {
            esperado: ["nine hundred and ninety-nine"],
            textoA: "999",
            textoD: ".",
            tamaño: 4,
          },
          {
            esperado: ["one thousand"],
            textoA: "1000",
            textoD: ".",
            tamaño: 4,
          },
          {
            esperado: ["ten thousand"],
            textoA: "10,000",
            textoD: ".",
            tamaño: 4,
          },
          {
            esperado: ["nine thousand"],
            textoA: "90,000",
            textoD: ".",
            tamaño: 4,
          },
          {
            esperado: ["ninety-nine thousand nine hundred ninety-nine"],
            textoA: "99,999",
            textoD: ".",
            tamaño: 7,
          },
          {
            esperado: ["hundred thousand"],
            textoA: "100,000",
            textoD: ".",
            tamaño: 4,
          },
          {
            esperado: ["twelve"],
            textoA: "12",
            textoD: ".",
            tamaño: 3,
          },
          {
            esperado: ["one million nine hundred ninety-nine thousand nine hundred seventy-six"],
            textoA: "1,999,976",
            textoD: ".",
            tamaño: 9,
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