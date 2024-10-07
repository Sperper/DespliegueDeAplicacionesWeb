# DNS
## Resolución
Es un sitema que se encarga de traducir los nombres de dominios a direcciones IP para que los navegadores puedan cargar los recursos de internet, suprimiendo así la necesidad de memorizar cada dirección IP. 

#### Nombre de dominio
Es una cadena de texto que se asigna a una dirección IP numérica.

## Niveles de dominio
### Primer nivel
Los servidores de nombre de dominio de primer nivel mantiene la información de todos los nombre de dominio que comparten una **extensión común**, tal como .com, .net, etc.
Existen dos tipos de dominios de primer nivel.
- Dominios de primer nivel genéricos: Son aquellos dominios que no son específicos de paises, los más conocidos son .com, .org, .net, .edu y .gov.
- Dominios de primer nivel de código de país: Son todos los dominios específicos de cada país. Un ejemplo de este tipo de dominios sería .es.

### Nombres autoritativos
Suele ser el último paso del solucionador en el recorrido de una dirección IP. El servidor de nombres autoritativos incluye información específica para el nombre de dominio al que sirve y puede ofrecer un solucionador recursivo con la dirección IP de ese servidor encontrada en el registro DNS A.

## Zona de busqueda
Una zona DNS es una parte del espacio de nombres DNS que está gestionada por una organización específica o un administrador. La zona DNS es un espacio administrativo que permite más control granular de los componentes de DNS, como los servidores de nombres autoritativos. El espacio de nombres de dominio es un árbol jerárquico, con el dominio raíz DNS en la parte superior. La zona DNS empieza en un dominio dentro del árbol y se puede extender hacia abajo en subdominios para que una entidad pueda gestionar múltiples subdominios.

## Registros
Registros de recurso básicos
Registro A (Address): Muestra la dirección IP IPv4 para un nombre de host o dominio específico 1.
Registro AAAA (IPv6 Address): Similar al registro A, pero se dirige a direcciones IP IPv6 1.
Registro CNAME (Canonical Name): Permite crear alias para un nombre de host 1.
Registro NS (Name Server): Indica el servidor DNS autorizado para un dominio 1.
Registro MX (Mail Exchange): Indica dónde deben dirigirse los correos electrónicos de un dominio

## Funcionamiento
### DNS recursivo
El DNS recursivo es el tipo más común y utilizado por la mayoría de los usuarios finales. Funciona como sigue:

El cliente envía una consulta al servidor DNS local.
Si el servidor local no tiene la respuesta en caché, realiza consultas a servidores autoritarios apropiados.
Recibe las respuestas de los servidores autoritarios y las devuelve al cliente.
Almacena la respuesta para futuras consultas rápidas
### DNS iterativo
El DNS iterativo es un método de resolución que permite que el servidor DNS recorra múltiples niveles jerárquicos hasta encontrar la información solicitada. Es diferente del recursivo porque:

No sigue siempre el camino más corto hacia la respuesta.
Puede consultar múltiples servidores antes de devolver una respuesta.
Permite una mayor flexibilidad en la búsqueda de información

### Recursos
[DNS](https://www.cloudflare.com/es-es/learning/dns/what-is-dns/)