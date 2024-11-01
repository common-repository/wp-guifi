=== wp-guifi ===
Contributors: Albert Sarle
Donate link: http://blog.albertsarle.com/wp-guifi
Tags: guifi.net,freenetwork,zone,summary
Requires at least: 2.7
Tested up to: 3.1.2
Stable tag: 4.3

Visualitza una llista de nodes operatius i la seva disponibilitat en una zona de guifi(http://guifi.net,la xarxa lliure oberta, alternativa i neutral)

== Description ==

Visualitza una llista de nodes operatius i la seva disponibilitat en una zona de guifi(http://guifi.net,la xarxa lliure oberta, alternativa i neutral)

== Installation ==

1. Descarrega el plugin
2. Descomprimeix la carpeta del plugin wp-guifi i copia-la a la carpeta wp-content/plugins de la teva instalació de WordPress
3. Activa el plugin des del panell d’administració de WordPress
4. Des del panell d’administració de plantilles de WordPress , a l’apartat de Widgets veuràs que ha aparegut WP-guifi. Afegeix-lo a la columna que vulguis
5. Introdueix el títol del widget al que s’afegirà automàticament el nom de la zona triada, Introdueix l’identificador de la zona de guifi.net que vols mostrar, selecciona quin tipus de node i tria si vols veure l’estat o el percentatge de connectivitat, el limit, l’estat i l’ordre en que volem mostrar els nodes de la zona.

El temps d’actualització en segons és el temps en que es recarrega tota la informació que mostra el plugin, conve que aquest valor no sigui massa baix ja que genera peticions a guifi.net i en el moment de refer la catxe pot alentir el nostre blog.

Si seleccionem mostrar la connectivitat, en el cas dels supernodes ens mostrarà el status general del node i despres la connectivitat de cadascun dels seus devices.

La opció de resum de zona ens mostra una taula resum amb el total de nodes per estat, amb el mateix estil i colors que apareix a guifi.net


== Frequently Asked Questions ==

= Com obtinc el identificador de zona ?=

El identificador de zona de guifi.net vol dir el id del node drupal que correspòn a la zona. Així per exemple Terrassa te el identificador de manera que http://guifi.net/node/8802 és la seva pàgina de zona. Si la zona te definit un alias com http://guifi.net/Terrassa, caldra buscar aquest id a algun dels enllaços de gestió

== Screenshots ==

1. Aquesta captura correspòn al widget que permet configurar les opcions des de Appearance / Widgets 
2. Aquesta segona captura correspòn a la opció de "mostrar connectivitat", on a més de treure la connectivitat del node, també mostra l'estat de cadascuna de les radios
3. Aquesta captura correspòn a la opció de "mostrar connectivitat"

== Changelog ==

= 0.5 - 11/10/2012 =
Corretgit el bug de ordenació dels nodes
Corretgit bug que deixava buida la catxe del plugin si no podia connectar a guifi.net
Afegits els estats de nodes reservat i esborrat
Afegida descripció de nodes en catala (malgrat que del cnml venen en anglès) 
Afegides nous criteris de ordenació : per clients i links

 = 0.4 - 9/6/2010 =
 Corretgit identificador de zona per defecte (88022->8802 Terrassa)
 Eliminar cestrencades del codi $enllaços -> $enllacos
 
 = 0.3 - 27/8/2009 =
 Afegida opcio per ordenar descendent els nodes (per id, alfabetic, per # de aps , per # de devices)
 Afegit logo i enllaç a guifi.net encapçalant el formulari de gestió del widget
 Passat html de li a table per ajustar amplades de celes (al cap i a la fi es un llistat)
 Igualades l'amplada de les celes del resum amb les de la llista de nodes.
 Per als supernodes , quan connectivitat es mostren tots els seus devices
 Remaquetacio HTML de la llista de nodes, status sempre alineat a la dreta
 Afegit parametre call=availability a les imatges de connectivitat per evitar  problemes amb versions diefrents de servidors de grafiques.
 Corretgida deteccio de supernodes afegint restriccio al xpath (access_points>1) && (devices>1)
 Afegit enllaç a la gestió del widget des del llistat de plugins
 
 = v 0.2 =
 Afegit Temps de catxe configurable
 Afegida opció per anar a buscar la disponibilitat  dels servidors de gràfiques o no. Estalviant consultes HTTP
 Afegida taula de Resum de Zona
 Inicialitzacio de variables per defecte
 Afegit Limit de nodes al llistat
 Afegit filtre de supernodes
 Neteja de cache al actualitzar opcions.
 
 = 0.1 =
 show me the code!!

== Upgrade Notice ==
La versió 0.4 no incorpora el codi per fer la ordenació, es recomana actualitzar a la 0.5

== Whishlist  ==
Afegir comprovacions de rangs de zona (zona 10000?)
Llistat de Serveis Operatius de la zona
Comprovar funcionament de la web de guifi.net abans de generar el html
Enllaçar el titol amb la pagina de la zona de guifi.net 

== Known Issues == 
register_widget_control DEPRECATED!  
si la zona hereda el servidor de gràfiques dels pares no treu res al seleccionar connectivitat.
