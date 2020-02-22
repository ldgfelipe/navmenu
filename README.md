
Se agrega la etiqueta importada, con los props 

-menulista: Pasa el Array con los datos que trabajara el menú
-lvl:Administra permisos estos deben ir en el array del menu para poder validarlos
-pre:Si lleva algo mas antes del enlace como por ejemplo [pre][key.href] = #/linkenlace
-estilo:indica el estilo que desea utilizar  style1, style2 


< navmenu  :menulista='listamenu' :lvl='permisos' ></ navmenu>

var listamenu:[
                {
                    title:"Inicio",
                    href:"./?u=tablero",
                    lvl:[0,2,1]
                },
                {
                    title:"Lotes",
                    href:"/",
                    lvl:[2,1],
                    submenu:[
                    {
                        title:'Administrar',
                        href:'./?u=tablero&ad=administrar-obsoletos',
                        lvl:[2,1],
                    },
                    {
                        title:"Subir Lotes",
                        href:"./?u=tablero&ad=listas-obsoletos",
                        lvl:[2,1]
                    },
                    {
                        title:"CRM",
                        href:"./?u=tablero&ad=mi-crm",
                        lvl:[2,1]
                        
                        },
                    
                    ]

                },
             ]
