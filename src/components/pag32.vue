<template>
<div>
    <div class="row">
         <div class="col-sm-1"></div>
        <h3 class="titulo" >FORMA PRESENTE DEL VERBO</h3>

    </div>
    <div class="row">
        
        <h4 class="parrafoBlack marginn-left "> <b>Los verbos en presente en oraciones afirmativas se escriben de dos formas.</b> </h4>
    </div>
    <hr>
       <div class="row">
           <div class="col-sm-1"></div>
        <div class="col-md-1"><FONT  class=" parrafoWhite p-2   bg-blueBackground rounded-circle p-1">PRESENT</FONT></div>
        <div class="col-md-1"><FONT   class="parrafoWhite p-2   bg-blueBackground rounded-circle">PRESENT</FONT></div>
        
              
    </div> <hr>
    
   
    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-md-1 parrafoWhite bg-blueBackground show-grid " ><FONT >SE<FONT class="text-danger">E</FONT> </FONT></div>
        <div class="col-md-1 parrafoWhite bg-blueBackground show-grid" ><FONT id="parrafoWhite" >SEE<FONT class="text-danger">S</FONT> </FONT></div>
        <div class="col-md-1 show-grid parrafoBlack"><FONT >Saw</FONT></div>
        <div class="col-md-1 show-grid parrafoBlack"><FONT>Seen</FONT></div>
        <div class="col-md-1 show-grid parrafoBlack"><FONT>Seeing</FONT></div>
  
     </div>
     <br>
     <br>
         <div class="row">
             <div class="col-sm-1"></div>
            <div class="col-sm-1" v-for="item in $data.tablaUnoPag32">

        <listaIndex :tabla="item"/>
      </div>
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
          <br><br><br><br><br><br><br><br>
          <p class="parrafoBlack">Si el sujeto es HE, SHE O IT el verbo lleva la letra “s” al final o algunas
                            veces lleva la “es” o la “ies”.
          </p>
      </div>
                      
    </div>
    <br><br><br>
    <div class="row"> 
        
        <p class="parrafoBlack marginn-left"><i> <b> REGLAS DEL LOS VERBOS EN PRESENTE AFIRMATIVO</b></i> </p>
    </div>

      <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-2 " v-for="item in $data.tablaDosPag32">

        <listaIndex :tabla="item"/>
    
        <br><br><br>
      </div>
    </div>
    <div class="row">
     
      <i class="fa fa-diamond marginn-left" >   </i>
      
        <p class="parrafoBlack marginn-left">  &nbsp;<b>Escribe la forma presente para terceras personas. </b> </p><br>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-2" v-for="item in $data.tablaTresPag32">

        <listaIndex :tabla="item"/>
        <br><br><br>
        
      </div>
    </div>
       <div class="row">
     
      <i class="fa fa-diamond marginn-left" >   </i>
      
        <p class="parrafoBlack marginn-left">&nbsp;<b>Reemplaza los números por letras y utiliza el verbo en su forma correcta. </b> <br></p>
    </div>
    
    <div class="row" >
      <div class="col-sm-1"></div>
      <div class="col-sm-8 row">
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaAPag33" />
        </div>
        <div class="col-sm-4 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaBPag33" />
        </div>

        <div class="col-sm-3 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaCPag33" />
        </div>

        <div class="col-sm-3  parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaDPag33" />
        </div>
      </div>
      </div>
  
         <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTraduccionCodigos
          :cuestionario="$data.cuestionario1Pag33"
          :inglesR="false"
          :espanolR="true"
        />
      </div>
      </div>
       <br><br><br>
       <div class="row">
      
      <i class="fa fa-diamond marginn-left" >   </i>
      
        <p class="parrafoBlack marginn-left">&nbsp;<b>Add the S, ES or IES to the verb if necessary. </b> </p><br>
    </div>

     <div class="row">
      <div class="col-sm-1"></div>
 
        <p class="parrafoBlack"><b>DICTIONARY</b> </p><br>
    </div>
    
      <div class="row">

      <div class="col-sm-1"></div>
      <div class="col-sm-0.9 " v-for="item in $data.tablaUnoPag34">

        <listaIndex :tabla="item"/>
    
        <br><br><br>
      </div>
    </div>
    

    <div class = "row">
      <div class="col-sm-1"></div>
      <FONT class=" text-left parrafoBlack"> <div class="col-sm-11 row" id="">1. Ella trabaja muy duro todos los días: She <inputChecked  style="width: 20%; margin-left:10px; margin-right:10px;" :resuelto="false" :esperado="['works']" />very hard every day.  <br> </div>
      <div class="col-sm-11 row" >2. Yo vivo con mi Madre acá: I  <inputChecked style="width: 20%; margin-left:10px; margin-right:10px;" :resuelto="false" :esperado="['live']" /> with my mother here.<br> </div>
      <div class="col-sm-11 row">3. Él tiene que trabajar mañana en la mañana: He <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['has']" /></p>to work tomorrow morning.<br> </div>
      <div class="col-sm-11 row">4. Natalie hace deporte todos los días: Natalie <inputChecked  :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['does']" /></p> sports every day.<br> </div>
      <div class="col-sm-11 row">5. Yo voy a trabajar en bus: I  <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['go']" />to work by bus.<br> </div>
      <div class="col-sm-11 row" >6. Ella va al colegio a pie: She  <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['goes']" /> to school on foot.<br> </div>
      <div class="col-sm-11 row">7. Llueve mucho en New York: It  <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['rains']" />a lot in New York.<br> </div>
      <div class="col-sm-11 row" >8. Amar tiene sentido: Loving  <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['makes']" /></p> sense. </div>
      <div class="col-sm-11 row" >9. Él tiene que trabajar mañana: He <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['has']" />to work tomorrow.<br> </div>
      <div class="col-sm-11 row" >10. Mi novia mira televisión los sábados: My girlfriend  <inputChecked :resuelto="false" style="width: 25%; margin-left:10px; margin-right:10px;" :esperado="['watches']" />tv on Saturdays.<br></div>
      <div class="col-sm-11 row" >11. Ella tiene un carro: She <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['has']" /> a car.<br> </div>
      <div class="col-sm-11 row">12. Ella no tiene un carro: She doesn’t  <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['have']" /> a car.<br> </div>
      <div class="col-sm-11 row" >13. Víctor llora todos los días: Victor <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['cries']" />everyday.<br> </div>
      <div class="col-sm-11 row" >14. El gato tiene cuatro patas: The cat  <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['has']" /> four paws.<br> </div>
      <div class="col-sm-11 row">15. Mi mamá me ama: My mother <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['loves']" /> me.<br> </div>
      <div class="col-sm-11 row" >16. El profesor enseña muy bien: The teacher <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['teaches']" /> very well.<br> </div>
      <div class="col-sm-11 row" >17. Eso huele mal: That  <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['smells']" /> bad.<br> </div>
      <div class="col-sm-11 row">18. Ese niño estudia inglés: That boy<inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['studies']" /> English.<br> </div>
      <div class="col-sm-11 row" >19. Él ama el número mágico: He <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['loves']" /> the magic number.<br> </div>
      <div class="col-sm-11 row" >20. Él tiene que madrugar: He  <inputChecked :resuelto="false" style="width: 20%; margin-left:10px; margin-right:10px;" :esperado="['has']" />to wake up early. </div></FONT>
    </div> <br><br><br>
      <div class="row">
     
      <i class="fa fa-diamond marginn-left" >   </i>
      
        <p class="parrafoBlack marginn-left">&nbsp;<b>ESCRIBA LA TRADUCCIÓN EN INGLES Y COMPLETA LAS ORACIONES. </b> <br></p>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-2 show-grid" v-for="item in $data.tablaUnoPag35">

        <listaIndex :tabla="item"/>
        <br><br><br>
        
      </div>
      </div>
            <div class="row">
      
      <i class="fa fa-diamond marginn-left" >   </i>
      
        <p class="parrafoBlack marginn-left">&nbsp;<b>Aquí hay una lista de los verbos más fáciles del inglés. Reescribe las oraciones con “she” </b> <br></p>
    </div>
      <div class="row">
      <div class="col-sm-1"></div>
      <font class="parrafoBlack ">Recuerda que la <font class="text-danger">S</font> , <font class="text-danger">ES</font> o <font class="text-danger">IES</font> se le agrega a un verbo en presente precedida de SHE, HE o IT</font>
      </div>

       <div class="col-sm-11 row" id="inputText">
                    Un verbo se usa en forma
                    <span
                      class="colorLetraRojo"
                      style="margin-left:4px; margin-right:4px;"
                    >Pasado</span> solo en una
                    <inputChecked
                      :resuelto="false"
                      :esperado='["Afirmación"]'
                      style="width: 15%; margin-left:10px; margin-right:10px;"
                    />; si es regular se agrega
                    “
                    <inputChecked
                      :resuelto="false"
                      :esperado='["ed"]'
                      style="width: 15%; margin-left:10px; margin-right:10px;"
                    />” y si es
                    irregular se aprende.
                  </div>
</div>
 
        
      
</template>
<script>
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
import tablaTraduccionCodigos from "./tablaTraduccionCodigos";
export default {
    components:{
        listaIndex,
        inputChecked,
        tablaTraduccionCodigos
    },
    data(){
        return{
    tablaUnoPag32: [
        {
          camposInput:false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html: '<FONT class=" parrafoBlack">I</FONT>',
            },
             {
              html: '<FONT class=" parrafoBlack">YOU</FONT>',
            },
             {
              html: '<FONT class=" parrafoBlack">WE  </FONT>',
            },
             {
              html: '<FONT class=" parrafoBlack">THEY</FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack" ><strong>SHE</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>IT</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>HE</strong></FONT>',
            },

          ],
          
        },
        {
          camposInput:false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html: '<FONT class=" parrafoBlack">SEE</FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack">SEE</FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack">SEE</FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack">SEE</FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>SEES</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>SEES</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>SEES</strong></FONT>',
            },
          ],
        },
        {
          camposInput:false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html: '<FONT class=" parrafoBlack">Yo veo</FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack">Tu ves</FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack">Nosotros vemos</FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack">Ellos ven</FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>Ella ve</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>Ve</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>El ve</strong></FONT>',
            },
          ],
        },
      ],
        tablaDosPag32: [
          {
            camposInput:false,
            fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" }
          ],
          items:[
            {
                html:  '<FONT class=" parrafoBlack"><strong>SHE______</strong></FONT>',
            },
             {
                html:  '<FONT class=" parrafoBlack"><strong>HE______</strong></FONT>',
            },
             {
                html:  '<FONT class=" parrafoBlack"><strong>IT______</strong></FONT>',
            }
          ]
          },
          {
             camposInput:false,
            fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" }
          ],
          items:[
            {
                html:  '<FONT ><strong>Verbos terminados en<br><FONT class=" parrafoBlack text-danger"> o, x, s, sh, ch, z </FONT>se<br>le agrega</strong></FONT><br><br>',


            },

             {
                html:  '<FONT  class=" parrafoBlack text-danger  p-2   bg-warning"><strong> EN </strong></FONT>',
            }
          ]
          },
           {
             camposInput:false,
            fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" }
          ],
          items:[
            {
                html:  '<FONT class=" parrafoBlack"><strong>Verbos terminados en <FONT class="text-danger">Y</FONT><br>precedida de consonante<br>se cambia la y por <FONT class="text-danger">i</FONT> más<br><FONT class="text-danger ">es</FONT><br></strong></FONT>',


            },

             {
                html:  '<FONT class=" parrafoBlack text-danger  p-2   bg-warning"><strong> IES </strong></FONT>',
            }
          ]
          },
           {
             camposInput:false,
            fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" }
          ],
          items:[
            {
                html:  '<FONT class=" parrafoBlack"><strong>Los demás<br>verbos se les<br>agrega la <br><FONT class="text-danger ">s</FONT><br></strong></FONT>',


            },

             {
                html:  '<FONT  class=" parrafoBlacktext-danger  p-2   bg-warning"><strong> S </strong></FONT>',
            }
          ]
          },
          {
             camposInput:false,
            fields: [
               // A virtual column that doesn't exist in items
               // A column that needs custom formatting
               { key: "html", label: "" }
            ],
          items:[
            {
                html:  '<FONT class=" parrafoBlack"><strong>Y “have” se<br>convierte en<br>“has”<br><br></strong></FONT>',


            },

             {
                html:  '<FONT class=" parrafoBlack" class="text-danger  p-2   bg-warning"><strong> HAS </strong></FONT>',
            }
          ]
          }
          
      ],
        tablaTresPag32: [
        {
          camposInput:false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html: '<FONT class=" parrafoBlack"><strong>I go</strong></FONT>',
            },
             {
              html: '<FONT class=" parrafoBlack"><strong>We have</strong></FONT>',
            },
             {
              html: '<FONT class=" parrafoBlack"><strong>They cry</strong></FONT>',
            },
             {
              html: '<FONT class=" parrafoBlack"><strong>You play</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>I watch</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>We study</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>I do</strong></FONT>',
            },

          ],
          
        },
        {
          camposInput:false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
             {
              html: '<FONT class=" parrafoBlack"><strong>She</strong></FONT>',
            }, {
              html: '<FONT class=" parrafoBlack"><strong> &nbsp; </strong></FONT>',
            }, {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            }, {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>She</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>My sister</strong></FONT>',
            },
          ],
        },
        {
          camposInput:false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            }, {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            }, {
              html: '<FONT class=" parrafoBlack"><strong>She</strong></FONT>',
            }, {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>The boy</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            },
          ],
        },
         {
          camposInput:false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            }, {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            }, {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp;</strong></FONT>',
            }, {
              html: '<FONT class=" parrafoBlack"><strong>He  </strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            },
          ],
        },
                 {
          camposInput:false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" },
          ],
          items: [
            {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            }, {
              html: '<FONT class=" parrafoBlack"><strong>Victor </strong></FONT>',
            }, {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp;</strong></FONT>',
            }, {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class=" parrafoBlack"><strong>&nbsp; </strong></FONT>',
            },
          ],
                 }
        ],
         tablaAPag33: {
        bordered: true,
        
        fields: [
          // A virtual column that doesn't exist in items
          
          // A column that needs custom formatting
          { key: "A", thClass: "Blue  parrafoBlack" },
        ],
        
        items: [
          {A: "1. I"},
          { A: "2. YOU "},
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
          { key: "B", thClass: "Red parrafoBlack" },
        ],
        items: [
          { B: "1. go/goes" },
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
          { key: "C", thClass: "Yelow parrafoBlack" },
        ],
        

        items: [
          { C: "1. there" },
          { C: "2. to admit" },
          { C: "3. movies" },
          { C: "4. a lot" },
          { C: "5. what" },
          { C: "6. here" },
          { C: "7. healthy" },
          { C: "8. sport" },
          
        ],
      },
      tablaDPag33: {
        bordered: true,
       
        fields: [
          // A virtual column that doesn't exist in items
          
          
          // A column that needs custom formatting
          { key: "D", thClass: "Green parrafoBlack" },
        ],
        
        items: [

          { D: "1. on Sundays" },
          { D: "2. it" },
          { D: "3. that" },
          { D: "4. everyday" },
          { D: "5. from time to time" },
          { D: "6. at night" },
          { D: "7. I want" },
          { D: "8. from Monday to Friday" },
          { D: "9. in the morning" },
        ],
      },
       cuestionario1Pag33: {
        fields: [
          { key: "A", thClass: "Blue parrafoBlack" },
          { key: "B", thClass: "Red parrafoBlack" },
          { key: "C", thClass: "Yelow parrafoBlack" },
          { key: "D", thClass: "Green parrafoBlack" },
          {key:"ENGLISH_PHRASE", label:"ENGLISH"},
          {key:"TRADUCCION_ESPAÑOL", label:"SPANISH"},
        ],
        items: [
          {
            A: 1,
            B: 1,
            C: 1,
            D: 1,
            ENGLISH_PHRASE: ['I go there on sundays'],
            TRADUCCION_ESPAÑOL: ['Voy allá los domingos'],
          },
          {
            A: 3,
            B: 2,
            C: 2,
            D: 2,
            ENGLISH_PHRASE: ["She has to admit it"],
            TRADUCCION_ESPAÑOL: ["Ella tiene que admitirlo"],
          },
          {
            A: 6,
            B: 7,
            C: 6,
            D: 4,
            ENGLISH_PHRASE: ["We work here everyday"],
            TRADUCCION_ESPAÑOL: ["Nosotros trabajamos aquí todos los días"],
          },
           {
            A: 1,
            B: 6,
            C: 8,
            D: 9,
            ENGLISH_PHRASE: ["I do sport in the morning"],
            TRADUCCION_ESPAÑOL: ["Yo hago deporte en la mañana"],
          }, {
            A: 4,
            B: 4,
            C: 3,
            D: 6,
            ENGLISH_PHRASE: ["He watches movies at night "],
            TRADUCCION_ESPAÑOL: ["Él ve películas en la noche"],
          }, {
            A: 2,
            B: 9,
            C: 1,
            D: 8,
            ENGLISH_PHRASE: ["You stay there from Monday to Friday"],
            TRADUCCION_ESPAÑOL: ["Tú te quedas allá de lunes a viernes"],
          }, {
            A: 1,
            B: 8,
            C: 4,
            D: 4,
            ENGLISH_PHRASE: ["I eat a lot everyday "],
            TRADUCCION_ESPAÑOL: ["Yo como mucho todos los días"],
          }, {
            A: 3,
            B: 6,
            C: 5,
            D: 7,
            ENGLISH_PHRASE: ["She does what I want"],
            TRADUCCION_ESPAÑOL: [" Ella hace lo que yo quiera"],
          }, {
            A: 7,
            B: 8,
            C: 7,
            D: 9,
            ENGLISH_PHRASE: ["They eat healthy in the morning"],
            TRADUCCION_ESPAÑOL: ["Ellos comen saludable en la mañana"],
          }, {
            A: 3,
            B: 5,
            C: 6,
            D: 5,
            ENGLISH_PHRASE: ["She buys here from time to time"],
            TRADUCCION_ESPAÑOL: ["Ella compra aquí de vez en cuando"],
          }, {
            A: 4,
            B: 4,
            C: 3,
            D: 1,
            ENGLISH_PHRASE: ["He watches movies on Sundays"],
            TRADUCCION_ESPAÑOL: ["Él ve películas los domingos"],
          }, {
            A: 7,
            B: 7,
            C: 4,
            D: 4,
            ENGLISH_PHRASE: ["They work a lot everyday"],
            TRADUCCION_ESPAÑOL: ["Ellos trabajan mucho todos los días"],
          }, {
            A: 1,
            B: 2,
            C: 2,
            D: 3,
            ENGLISH_PHRASE: ["I have to admit that"],
            TRADUCCION_ESPAÑOL: ["Yo tengo que admitir eso"],
          },
           {
            A: 1,
            B: 8,
            C: 5,
            D: 7,
            ENGLISH_PHRASE: ["I eat what I want"],
            TRADUCCION_ESPAÑOL: ["Yo como lo que yo quiero"],
          },
           {
            A: 3,
            B: 3,
            C: 4,
            D: 6,
            ENGLISH_PHRASE: ["She cries a lot at night"],
            TRADUCCION_ESPAÑOL: ["Ella llora mucho en la noche"],
          },
           
        ],
      },      
      tablaUnoPag34: [
          {
            camposInput:false,
            fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" }
          ],
          items:[
            {
                html:  '<FONT  class=" parrafoBlack p-2 bg-warning"><strong>Work</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Trabajar</strong></FONT>',
            },
             
          ]
          },
          {
             camposInput:false,
            fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" }
          ],
          items:[
           {
                html:  '<FONT  class=" parrafoBlack p-2 bg-warning"><strong>Live</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Vivir</strong></FONT>',
            },
             
          ]
          },
           {
             camposInput:false,
            fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" }
          ],
          items:[
            {
                html:  '<FONT  class=" parrafoBlack p-2 bg-warning"><strong>Have</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Tener</strong></FONT>',
            },
             
          ]
          },
           {
             camposInput:false,
            fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "" }
          ],
          items:[
          {
                html:  '<FONT  class=" parrafoBlack p-2 bg-warning"><strong>Do</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Hacer</strong></FONT>',
            },
             
          ]
          },
          {
             camposInput:false,
            fields: [
               // A virtual column that doesn't exist in items
               // A column that needs custom formatting
               { key: "html", label: "" }
            ],
          items:[
           {
                html:  '<FONT  class="p-2 bg-warning parrafoBlack"><strong>Go</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Ir</strong></FONT>',
            },
             
          ]
          },
          {
             camposInput:false,
            fields: [
               // A virtual column that doesn't exist in items
               // A column that needs custom formatting
               { key: "html", label: "" }
            ],
          items:[
           {
                html:  '<FONT class="p-2 bg-warning parrafoBlack"><strong>Rain</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Llover</strong></FONT>',
            },
             
          ]
          },
          {
             camposInput:false,
            fields: [
               // A virtual column that doesn't exist in items
               // A column that needs custom formatting
               { key: "html", label: "" }
            ],
          items:[
           {
                html:  '<FONT class="p-2 bg-warning parrafoBlack"><strong>Make Sense</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Tener Sentido</strong></FONT>',
            },
             
          ]
          },
          {
             camposInput:false,
            fields: [
               // A virtual column that doesn't exist in items
               // A column that needs custom formatting
               { key: "html", label: "" }
            ],
          items:[
           {
                html:  '<FONT class="p-2 bg-warning parrafoBlack"><strong>Watch</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Mirar</strong></FONT>',
            },
             
          ]
          },
          {
             camposInput:false,
            fields: [
               // A virtual column that doesn't exist in items
               // A column that needs custom formatting
               { key: "html", label: "" }
            ],
          items:[
           {
                html:  '<FONT  class="p-2 bg-warning parrafoBlack"><strong>Cry</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Llorar</strong></FONT>',
            },
             
          ]
          },
          {
             camposInput:false,
            fields: [
               // A virtual column that doesn't exist in items
               // A column that needs custom formatting
               { key: "html", label: "" }
            ],
          items:[
           {
                html:  '<FONT class="p-2 bg-warning parrafoBlack"><strong>Love</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Amar</strong></FONT>',
            },
             
          ]
          },{
             camposInput:false,
            fields: [
               // A virtual column that doesn't exist in items
               // A column that needs custom formatting
               { key: "html", label: "" }
            ],
          items:[
           {
                html:  '<FONT class="p-2 bg-warning parrafoBlack"><strong>Teach</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Enseñar</strong></FONT>',
            },
             
          ]
          },{
             camposInput:false,
            fields: [
               // A virtual column that doesn't exist in items
               // A column that needs custom formatting
               { key: "html", label: "" }
            ],
          items:[
           {
                html:  '<FONT  class="p-2 bg-warning parrafoBlack"><strong>Smell</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Oler</strong></FONT>',
            },
             
          ]
          },{
             camposInput:false,
            fields: [
               // A virtual column that doesn't exist in items
               // A column that needs custom formatting
               { key: "html", label: "" }
            ],
          items:[
           {
                html:  '<FONT  class="p-2 bg-warning parrafoBlack"><strong>Study</strong></FONT>',
            },
             {
                html:  '<FONT class="parrafoBlack"><strong>Estudiar</strong></FONT>',
            },
             
          ]
          }
          
      ],
      tablaUnoPag35: [
        {
          camposInput:false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "ORACIÓN EN PRESENTE  AFIRMATIVO (INGLÉS)", thClass:"parrafoBlack"  },
          ],
          items: [
            {
              html: '<FONT class="parrafoBlack"><strong>I walk everyday</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong> You cry a lot</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>They eat here </strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>I cough every now and then</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack" ><strong>I watch TV once in a blue moon</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>I go for a run every morning</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>We dance in the rain</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>I brush my teeth twice a day </strong></FONT> <br><br>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>They speak English very slowly</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>I walk everyday </strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>You cry very much</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>They eat here</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>You cough every now and then</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>I watch TV once in a blue moon</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>We take the kids to the school</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>We dance in the rain</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>I brush my teeth twice a day</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>They speak english very slowly</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>I walk everyday</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>I love you</strong></FONT>',
            },

          ],
          
        },
        {
          camposInput:false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "ORACIÓN AFIRMATIVA EN PRESENTE (ESPAÑOL)", thClass:"parrafoBlack"  },
          ],
          items: [
              {
              html: '<FONT class="parrafoBlack"><strong>Yo camino todos los días</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong> Tu lloras muchot</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>Ellos comen aquí </strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>Yo toso de vez en cuando</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack" ><strong>Yo veo televisión muy rara vez</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>Yo voy a correr en la mañana</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>Nosotros bailamos bajo la lluvia</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>Me cepillo mis dientes dos veces al día </strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>Ellos hablan inglés muy despacio</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>&nbsp;</strong></FONT>',
            },
          ],
        },
        {
          camposInput:false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "html", label: "Si el sujeto es HE, SHE o IT elverbo lleva la s, es o ies", thClass:"parrafoBlack" },
          ],
          items: [
          {
              html: '<FONT class="parrafoBlack"><strong>She walk<font class="text-danger">s </font>every day</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong> He cr<font class="text-danger">ies</font> a lot</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>The dog eat<font class="text-danger">s</font> here </strong></FONT>',
            },
              {
              html: '<FONT class="parrafoBlack"><strong>My mother cough<font class="text-danger">s</font> </strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>She watch<font class="text-danger">es</font> tv</strong></FONT>',
            },
            
            {
              html: '<FONT class="parrafoBlack"><strong>Nobody go <font class="text-danger">es</font> for a run every morning</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>She danc<font class="text-danger">es</font> in the rain</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>He brush<font class="text-danger">es</font> his teeth twice a day</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>My teacher speak<font class="text-danger">s</font> </strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>He______ everyday</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>She _______ vey much</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>The chicken ________ here;</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>The baby _________ every now and then</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>She ___________ tv once in a blue moon</strong></FONT>',
            },
            {
              html: '<FONT class="parrafoBlack"><strong>He __________ the kids to the school</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>It ________ in the rain</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>She _________ her teeth twice a day</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>He _________ English very slowly</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>The dog ________ everyday</strong></FONT>',
            },
             {
              html: '<FONT class="parrafoBlack"><strong>She_______ me</strong></FONT>',
            },
          ],
        },
         
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