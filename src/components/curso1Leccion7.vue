<template>
    <div>

         <div class="col-sm-1"></div>
        <h3 class="titulo" > LOS VERBOS GEMELOS DE LA LÓGICA DEL INGLÉS</h3>
        <div class="row">
                <div class="col-sm-1"></div>
                <ul>
            <li v-for="item in frasesPag37 " class="text-left">{{item}}</li>
        </ul>
        
        </div>

         <div class="row" >
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <div class="col-sm-4 parrafoBlack" id="tabla">

          <listaIndex :tabla="$data.tablaAPag33" />

        </div>
        <div class="col-sm-4 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaBPag33" />
        </div>

        <div class="col-sm-3 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaCPag33" />
        </div>

        
      </div>
      </div>

      <div class="row">
     
      <i class="fa fa-diamond marginn-left" >   </i>
      
        <p class="parrafoBlack marginn-left">  &nbsp;<b>Completa las siguientes oraciones con el verbo, auxiliar o verbo con super poder. </b> </p><br>
    </div>
     <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-8 row">
        
          <div v-for="(item, index) in frases2PAg37" :class=" ' row col-sm-'+item.tamano" style="margin-bottom:0.5em;">
            <inputChecked
              :esperado="item.esperado"
              :resuelto="false"
              :name="'P21-'+index"
              :textoA="item.textoA"
              :textoD="item.textoD"
              :conTexto="true"
              
            /> 
          </div>
          </div>
          </div>

  
   
    </div>
</template>


<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
import tablaTraduccionCodigos from "./tablaTraduccionCodigos";
import tablaTraduccionCodigosDos from "./tablaTraduccionCodigosDos";
import tablaTC from "./tablaTraduccionCodigos";
export default {
    components:{
        listaIndex,
        inputChecked,
        tablaTraduccionCodigos, 
        tablaTraduccionCodigosDos, 
        posiblesRespuestasTabla,
    tablaTC,
    },
    data(){
        return{
                frasesPag37 : [" La palabra DO es un verbo que traduce Hacer, pero también es un auxiliar","La tercera persona de DO es DOES, pero DOES también es un auxiliar.",
                 "El pasado del verbo DO es DID, pero DID también es un Auxiliar",
"La palabra HAVE es un verbo que traduce “tener”, pero también es un verbo con súper poder.",
 "La tercera persona de HAVE es HAS, pero Has también es un verbo con súper poder. ",
  "El pasado del verbo HAVE es HAD, pero HAD también es un "],

    tablaAPag33: {
        bordered: true,
        
        fields: [
          // A virtual column that doesn't exist in items
          
          // A column that needs custom formatting
          { key: "A", thClass: "Blue  ", label:"Verbs" },
        ],
        
        items: [
          {A: "Present Past Participle"},
          { A: "Does.....|.....Did......|.....Done"},
          { A: "3. SHE" },
          { A: "4. HE" },
          { A: "5. IT" },
          { A: "6. WE" },
          { A: "7. THEY"}
        ],
      },
      
       tablaBPag33: {
        bordered: true,
        
        fields: [
          // A virtual column that doesn't exist in items
          
          // A column that needs custom formatting
          { key: "B", thClass: "Red " },
        ],
        items: [
          { B: "1. Arreglar" },
          { B: "2. have / has" },
          { B: "3. cry/ cries" },
          { B: "4. watch / watches" },
          { B: "5. buy / buys" },
          { B: "6. do / does" },
          { B: "7. work / works" },
          { B: "8. eat / eats" },
          { B: "9. stay / stays" },
        ],
      },
      tablaCPag33: {
        bordered: true,
       
        fields: [
          // A virtual column that doesn't exist in items
          
          // A column that needs custom formatting
          { key: "C", thClass: "Yelow " },
        ],
        

        items: [
          { C: "1. Arreglar" },
          { C: "2. to admit" },
          { C: "3. movies" },
          { C: "4. a lot" },
          { C: "5. what" },
          { C: "6. here" },
          { C: "7. healthy" },
          { C: "8. sport" },
          
        ],
      },
        frases2PAg37: [
        { esperado: ["has"], textoA: "He ", tamano: 3, textoD:"" },
        { esperado: ["done"], textoA: "never",tamano: 3, textoD:"that. Él nunca ha hecho eso. "},
        
        { esperado: ["doesn't do"], textoA: "She", tamano: 4, textoD:"anything. Ella no hace nada."},
        { esperado: ["had"], textoA: "I", tamano: 2, textoD:""},
        { esperado: ["done"], textoA: "already", tamano: 3, textoD:" that. Yo ya había hecho eso." },
        { esperado: ["could"], textoA: "Pude-podría", tamano: 4 },
        { esperado: ["has"], textoA: "Ha", tamano: 3 },
        { esperado: ["is"], textoA: "Es-está", tamano: 3 },
        { esperado: ["had"], textoA: "Había", tamano: 3 },
        { esperado: ["are"], textoA: "Eres-estás-somos-estamos-son-están", tamano: 8 },
        { esperado: ["were"], textoA: "Eras-estabas-éramos-estábamos-eran-estaban", tamano: 9 },   

      ],
      




        }
    }
}
</script>
<style scoped>
.show-grid {
  border:1px solid ;
  color: black;
 

}




#text,
#inputText {
  text-align: left;
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



inputChecked{
  display: inline-flex;
}
</style>