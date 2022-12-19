# Neste repositório irei upar os Lab's que montei durante o estudo do protocolo OSPF

Para este primeiro LAB, montei um cenário básico e apliquei uma configuração básica de OSPF, onde haverá 3 áreas sendo 1 delas uma área de transito/backbone.
Irei explicar detalhadamente o funcionamento de cada topologia de forma mais detalhada que eu puder e irei disponibilizar todos os comandos utilizados assim como imagens para ilustrar a explicação.

# OSPF - Multi-Area Configuration

Nesta Topologia foi realizada a configuração de 3 áreas OSPF sendo a 245, 367 e a área 0.0.0.0
A Area 245 tem como ABR o roteador 2 e este Anunciar as LSA Tipo 3 para a área 0 (Backbone).

A Area 367 tem como ABR o roteador 3 e este também anuncia os LSA tipo 3 para a area 0.

Os ABR's anunciam suas redes para o R1 e atualizam a LSDB dele.

O R1 Unifica todas as rotas em seu LSDB e é o roteador que tem uma visão geral da rede.

Os roteadores que compõem a Area 245 sabem que para chegar até a rede que está contida na área 367, eles deverão enviar para o ABR e este irá encaminhar o pacote até o R1 que está na área 0, o R1 ao receber o pacote irá consultar a sua LSDB e encaminhar o pacote até o destino.

Abaixo uma imagem descrevendo os tipos de anuncios e a descrição da função de cada Roteador:

<IMAGEM EXPLICANDO A TOPOLOGIA>

A Tabela do roteamento do Roteador 1:

<TABELA DE ROTEAMENTO DO ROTEADOR 1>

e para a configuração deste cenário, a configuração foi feita por meio do EVE-NG utilizando imagens do Huawei NE40, a configuração foi feita com os comandos a seguir:

<COMANDOS>

# OSPF Single-Area Configuration

Nesta outra topologia fiz uma configuração básica de um OSPF em uma configuração de uma única área.

Então é bem simples todos os roteadores compartilham seus LSA e atualizam suas tabelas de roteamentos.

  <IMAGEM EXPLICANDO A TOPOLOGIA>

esta é a tabela de roteamento do R1:
    <TABELA DE ROTEAMENTO DO ROTEADOR 1>

Estes foram os comandos utilizados nos switch's huawei para habilitar o OSPF Single-area.
    
    <COMANDOS>



