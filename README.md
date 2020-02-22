
Se agrega la etiqueta importada, con los props 

-menulista: Pasa el Array con los datos que trabajara el menú
-lvl:Administra permisos estos deben ir en el array del menu para poder validarlos
-pre:Si lleva algo mas antes del enlace como por ejemplo [pre][key.href] = #/linkenlace
-estilo:indica el estilo que desea utilizar  style1, style2 

Props

menulista=Recibe el array con la estructura del menú
           ejemplo 
           Array = [
                  {
                    titulo:"", ///agrega al titulo al menu
                    href:"", // el link de destino 
                    lvl:"", // permisos de comparación 
                    submenu: [  //// SUB MENU ---------------
                        titulo:"", ///agrega al titulo al menu
                        href:"", // el link de destino
                    ]
                  }
           ]
                  

lvl=recibe el nivel de permiso se compara con el lvl del array de menu

estilo= Puede elegir 3 estilos de menu style1, style2 y style3 /// [desarrollo pendiente]
