<template>
<nav :class="estilo">
   <ul>
       <li  v-for="(key,index) in menulista" :key="index" v-if="validador(key.lvl)" :style="'float:'+direccion+';'" >

       <a  v-if="!key.submenu" :href="pre+key.href" >{{key.title}}</a>
       
       <div v-if="key.submenu && validador(key.lvl)" class="_submenu" >
       {{key.title}}
      
           <ul v-if="key.submenu" >
               <li v-for="(skey,index) in key.submenu" v-if="validador(skey.lvl)">
                  <a :href="pre+skey.href">{{skey.title}}</a>
               </li>
           </ul>

        </div>
       </li>
   </ul>
</nav>
</template>
<style>

/**--style1----**/
.style1 ul{
    list-style:none;
     
     padding:1%;
       z-index:99999999999999999999999999999999;
}
.style1 ul li{
    top:-20px;
    padding: 10px;
    background-color: rgb(0, 87, 163);
    color:#fff;
    position:relative;
   
    

}
.style1 ul li a {
    width:100%;
       text-decoration: none; 
       color:#fff;
}
.style1 ul li:hover {
        background-color:#FF4000;;
}

/**--submenu---**/


._submenu{
    cursor:pointer;
    position:relative;
}
._submenu ul{
  top:35px;
  display:none;
  position:absolute;
  left:0px;
  
}
._submenu ul li a{
    width:100%;
    
}
._submenu ul li {
    width:180px;
    background-color: rgb(0, 87, 163);
    /*border:solid #000 1px;*/
    box-shadow: 0 0 5px #000;
}

._submenu ul li:hover {
   background-color:#FF4000;
    
}
._submenu:hover ul{
  display:block;
}
</style>
<script>
module.exports={
    data(){
        return {
        
        }
    },
    methods:{
        validador(p){
            
            if(p.indexOf(this.lvl)>-1){
                return true
            }else{
                return false
            }
        }
    },
    props:{
        menulista:{},
        direccion:{
            default:"left"
        },
        estilo:{
          default:"style1"
        },
        pre:{
            default:""
        },
        lvl:{
            default:0
        }
    },
    mounted(){
        
    }
}
</script>
