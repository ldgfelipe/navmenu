<template>
<nav :class="style">
   <ul>
       <li v-for="(key,index) in menulista" :key="index" :style="'float:'+direccion+';'" >

       <a  v-if="!key.submenu" :href="'#'+key.href" >{{key.title}}</a>
       
       <div v-if="key.submenu" class="_submenu" >
       {{key.title}}
      
           <ul v-if="key.submenu" >
               <li v-for="(skey,index) in key.submenu">
                  <a :href="'#'+skey.href">{{skey.title}}</a>
               </li>
           </ul>

        </div>
       </li>
   </ul>
</nav>
</template>
<style>
/**--defaul----**/

nav ul{
    list-style:none;
}

nav ul li{
    padding: 10px;
    color:#000
}

nav ul li a:link {
       text-decoration: none; 
}

nav ul li a:hover {
       text-decoration: none; 
}

nav ul li a:focus {
       text-decoration: none; 
}

/**--style1----**/


style1 ul{
    list-style:none;
    background-color:
}

style1 ul li{
    padding: 10px;
    color:#000
}

style1 ul li a:link {
       text-decoration: none; 
}

style1 ul li a:hover {
       text-decoration: none; 
}

style1 ul li a:focus {
       text-decoration: none; 
}   n  nn                                  n                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         nnnnnnnnnnnnnn                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   bb  

/**--style2----**/

/**--style3----**/




._submenu{
    cursor:pointer;
    position:relative;

}
._submenu ul{
  padding:0px;
  display:none;
  position:absolute;
  z-index:99999999999999999999999999999999;
  left:0px;
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
    props:{
        menulista:{},
        direccion:{
            default:"left"
        },
        style:{
          default:"style1"
        }
    },
    mounted(){
        
    }
}
</script>
