Este repositorio contiene todos los materiales necesarios para crear a "Raúl", un robot autónomo diseñado por la Hermandad del Acero. Este robot participará en la competición WRO Future Engineers 2025.
Los miembros del equipo de la "Hermandad del Acero" son:
1. Mora Contreras, Luis Guillermo.
2. Perez Farkas, Alejandro.
3. Veliz Miguel Antonio
Introducción
Los seres humanos tenemos la necesidad de mejorar cada vez más, y la robótica forma parte de este proceso de mejora, un área fundamental en procesos necesarios para el avance del futuro de la sociedad, que afecta directamente a diferentes disciplinas como la medicina, la industria, la agricultura y el hogar, entre otras. En este contexto, el proyecto de crear el robot "Raúl", además de surgir del propósito de competir en la competencia WRO Future Engineers, también surgió de nuestro deseo de innovar y afrontar nuevos retos.
Así mismo, como estudiantes de segundo semestre de ingeniería informática de la Universidad Católica Andrés Bello, lo vimos como una oportunidad para desarrollar y poner en práctica nuestras habilidades de programación; así como  también, de aprender y experimentar en el área de la robótica, todo en haras de nuestro deseo de al culminar nuestra actual carrera, estudiar la nueva cátedra de mecatrónica, que recientemente ha abierto esta Casa de Estudio. 
Es importante destacar que esta iniciativa ha contado con el apoyo de la universidad desde sus inicios, sobre todo del área social, lo que nos motiva a seguir aprovechando al máximo los recursos que nos ofrece.

Materiales
Nuestro modelo está construido principalmente con componentes y piezas del kit de inventor Nezha para Micro:bit;  y además, con algunas piezas de lego.
Parte electrónica
1 Placa de expansión Nezha
1 Placa Micro:bit
3 PLANETX sensores ultrasónicos
4 cables RJ11
1 cámara Micro:bit Smart AI Lens 
1 batería recargable de 900 mA
Parte mecánica
1 Motor ROJO DC para tracción
1 Servomotor gris de 360 grados para dirección
2 ruedas anchas para la parte trasera
2 ruedas finas para la parte delantera
Bloques de construcción varios de Lego y Nezha V2 compatibles con Lego
Gestión de movilidad:
Tracción: trasera. 
Nuestro vehículo debe su movilidad a un motor rojo DC conectado a dos ruedas anchas traseras a través de dos ejes, uno a cada lado del motor. Además, posee dos ruedas delanteras más estrechas
Dirección: eje delantero.
La dirección utiliza un servomotor gris conectado a la placa, a través de un cable de 3 pines, que controla sus giros en grados. Al servo se conecta un eje central rodeado por un engranaje (circular, a modo de piñon), dispuesto sobre una cremallera (barra dentada), lo cual mueve las ruedas delanteras permitiendo dirigir el vehículo.
Sistema de transmisión y suspensión: 4 ruedas de goma.
Las ruedas traseras son más anchas que las delanteras, emulando a los vehículos de la f1. Esto principalmente proporciona, mayor agarre y tracción al acelerar y en las curvas, debido a que la potencia del motor se trasmite a través de las ruedas traseras, y un mayor contacto con la pista ayuda a transferir dicha potencia de manera más efectiva
Gestión de energía:
Todos los componentes eléctricos están conectados a una batería recargable de 900mA, que se encuentra dentro de la placa de expansión Nezha, incluida en el correspondiente kit de inventor. Ella es cargada a través de un conector miniusb.
Sistema de sensores:
El modelo cuenta con 3 sensores ultrasónicos en la parte delantera del vehículo, uno está dispuesto para que vea de frente y los otros dos están dispuestos en cada esquina de la parte frontal del vehículo, en forma diagonal,  lo que le permite al automóvil tener una visión de 180 grados al frente, emulando así la visión que tendría un conductor de cualquier vehículo sin espejos retrovisores.
Además, nuestro robot cuenta con una cámara Smart AI Lens, programada para reconocimiento de los colores rojo, verde y magenta, a fin de que pueda reconocerlos y girar a derecha o izquierda según las reglas o estacionarse.
Módulos que componen el código:
Dentro de nuestro código hay diferentes módulos encargados de controlar los siguientes componentes:
Motor DC rojo, el cual es responsable de la tracción y la potencia de las ruedas traseras para impulsar el vehículo. Este componente fue ajustado a desarrollar un 30% de su fuerza.
Servomotor gris: Responsable de la dirección, por lo tanto hace torque sobre un eje que mueve los engranajes que giran sobre una cremallera, a diferentes ángulos según el caso.
Cámara IA: detecta los objetos u obstáculos en la vía y esta condicionada a que si detecta un objeto verde, la dirección vehicular gire a la izquierda y si el objeto es rojo, gira a la derecha.
Sensores ultrasónicos: envían señales de sonido las cuales rebotan en los objetos y retornan al sensor, permitiéndole detectar la distancia a dicho  objeto. Esto emula el sistema de ecolocalización de los murciélagos.
