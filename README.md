
Se agrega la etiqueta importada, con los props 

-menulista: Pasa el Array con los datos que trabajara el menú
-lvl:Administra permisos estos deben ir en el array del menu para poder validarlos
-pre:Si lleva algo mas antes del enlace como por ejemplo [pre][key.href] = #/linkenlace
-estilo:indica el estilo que desea utilizar  style1, style2 



<navmenu  :menulista='listamenu' :lvl='permisos' ></navmenu>


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
                {
                    title:"Cuenta",
                    href:"/",
                    lvl:[0,2,1],
                    submenu:[
                       {
                        title:"Mi Cuenta",
                         href:"./?u=tablero&ad=mi-cuenta",
                        lvl:[0,2,1]
                    },      
                        
                    {
                        title:"Editar Datos",
                        href:"./?u=tablero&ad=datos-usuario",
                        lvl:[0,2,1]
                    },
                    {
                        title:"Realizar Pagos",
                        href:"./?u=comienza-venta",
                        lvl:[0,2,1]
                    },  
                    {
                        title:'Empresa',
                        href:'./?u=tablero&ad=alta-empresa',
                        lvl:[2,1]
                    }
                   
                    ]
                    
                },
                {
                    title:"Buzon",
                    lvl:[2,1],
                    submenu:[
                         {
                        title:"Mensajes",
                        href:"./?u=mensajes",
                        lvl:[2,1]
                        
                        },
                    {
                        title:"Chat",
                        href:"./?u=tablero&ad=mensajero-service",
                        lvl:[2,1]
                        
                        }
                    ]
                },
                
                {
                    title:'Administrador',
                    href:'/',
                    lvl:[1],
                    submenu:[
                        {
                            title:'Revisión Lotes',
                            href:'./?u=tablero&ad=administrador&tp=0',
                            lvl:[1]                        },
                         {
                            title:'Usuarios',
                            href:'./?u=tablero&ad=administrador&li=busuario',
                            lvl:[1]                        },
                        {
                             title:'Sitemap',
                            href:'./?u=tablero&ad=administrador&li=sitemap_tools' ,
                            lvl:[1]  
                        },
                        {
                             title:'Gifcard',
                            href:'./?u=tablero&ad=administrador&li=GiftCard' ,
                            lvl:[1]  
                        },
                        {
                             title:'Alta de Lista',
                            href:'./?u=tablero&ad=administrador&li=altaLista'  ,
                            lvl:[1] 
                        },
                        {
                             title:'Metricas Empresa',
                            href:'./?u=tablero&ad=administrador&li=listaEstat' ,
                            lvl:[1]  
                        },
                        {
                             title:'Buzon',
                            href:'./?u=tablero&ad=administrador&li=lista-newsletter' ,
                            lvl:[1]  
                        },
                        {
                             title:'Mailing',
                            href:'./?u=tablero&ad=administrador&li=mailingServer'  ,
                            lvl:[1] 
                        },
                        {
                             title:'Estadisticas',
                            href:'./?u=tablero&ad=administrador&li=estadisticas-del-sitio',
                            lvl:[1]
                        },
                        {
                             title:'Elementos',
                            href:'./?u=tablero&ad=administrador&li=Elementos',
                            lvl:[1]
                        },
                        {
                            title:'Pruebas',
                            href:'./?u=tablero&ad=administrador&li=testSection',
                            lvl:[1]
                        },
                        {
                            title:'Admin Banners',
                            href:'./?u=tablero&ad=administrador&li=publicityadmin',
                            lvl:[1]                        
                            },
                        {
                            title:'Admin Contactos',
                            href:'./?u=tablero&ad=administrador&li=Admincontactos',
                            lvl:[1]                        
                            }
                    ]
                },
