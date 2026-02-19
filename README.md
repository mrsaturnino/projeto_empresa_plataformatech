Utilizando o CISCO PACKET TRACER você vai criar a rede lógica com as seguintes informações:


A empresa Super Tech, precisa criar a estrutura de sua rede de computadores, de maneira que atenda as seguintes necessidades.



São 4 departamentos: Engenharia, Compras, TI Interno e Infraestrutura. 



* Cada departamento deve conter: 20 estações, 2 servidores e 2 impressoras, totalizando 24 hosts. 



* Deve ser usada uma máscara de sub-rede que atenda a necessidade apresentada. 



* A rede é de Classe C e deve-se usar a topologia estrela. 



* Para a numeração IPs, deve-se usar uma sequência nas sub-redes de acordo com a máscara adotada. 



* Como são 24 hosts em cada sub-rede, devemos usar uma máscara que permita está configuração: neste caso a rede seria de /27, o host de 24.

  *máscara padrão: 255.255.255.22*
  *máscara CIDR: /27*



* Descreva a rede, seu 1º IP válido, ultimo IP valido e o broadcast de cada Sub-Rede.



|*REDE*|*HOSTS*|*BROADCAST*|
|-|-|-|
|*192.168.0.0*|*.1 ao .30*|*192.168.0.31*|
|*192.168.0.32*|*.33 ao .62*|*192.168.0.63*|
|*192.168.0.64*|*.63 ao .94*|*192.168.0.95*|
|*192.168.0.96*|*.95 ao .126*|*192.168.0.127*|





* Utilize o switch 2950-24 da Cisco para cada departamento, interligando eles entre si.

  *Nota: para interligar os departamentos da forma mais fácil e objetiva, foi necessário remover um dos computadores para ter uma porta sobrando, visto que, seguindo o enunciado, não haveria portas sobrando para conectar mais um switch (que foi utilizado para interligar as redes existentes).*



* Cada departamento deve estar em uma sub-rede. Configure uma Vlan nas subs-rede. 



* Configure uma VLAN nas sub-redes. Em cada Sub-rede crie 2 vlans com 12 portas cada. Da 1-12 VLAN1 e da 13 a 24 VLAN2. Cada VLAN vai ter 10 estações, 1 impressora e um Servidor.



* Os departamentos são: Engenharia, Compras, T.I. Interno e Infraestrutura.



* Os departamentos de Engenharia e T.I. Interno devem ser colocados IPs estáticos, já nos departamentos de compras e Infraestrutura devem ser colocados IPs dinâmicos, de maneira que siga a sequência dos IPs estáticos.


<img width="1883" height="657" alt="image" src="https://github.com/user-attachments/assets/49753088-c755-452c-bb55-37764dc00f74" />

