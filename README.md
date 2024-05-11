# AlertaRS: Protegendo o Rio Grande do Sul contra Inundações com Inteligência Artificial
Projeto desenvolvido com uso de IA visando alertar a população do Rio Grande do Sul em caso de enchetes e alagamentos, além de fornecer o contato de hospitais, abrigos e ONG'S para que a população se sinta mais segura e protegida. Esse projeto foi desenvolvido para participar do desafio do curso de Imersão IA em parceria da Alura, Google e FIAP.
AlertaRS: Protegendo o Rio Grande do Sul contra Inundações com Inteligência Artificial 
![image](https://github.com/lucianafem/alertaRS/assets/62123799/b638e3d2-8075-4694-9b44-b9d2a0ae54e3)
Autora: Luciana Claudia Martins Ferreira Diogenes
# Resumo: 
O Rio Grande do Sul, conhecido por suas belezas naturais e rica cultura, enfrenta um desafio crescente: as inundações. Eventos climáticos extremos, intensificados pelas mudanças climáticas, colocam em risco comunidades, infraestrutura e a própria vida. É nesse contexto que surge o projeto AlertaRS - Alerta Rio Grande do Sul, um sistema inovador que utiliza inteligência artificial (IA) para alertar a população sobre a situação climática e prevenir desastres, salvando vidas e minimizando danos. Além disso, quando existir um risco alto e muito alto de enchentes e alagamentos, o programa pode fornecer o endereço e telefone de hospitais, pontos de abrigo e ONG’s para que a população possa procurar em caso de necessidade.
# 1 – Introdução

O projeto foi desenvolvido baseado nos critérios dados durante o curso de Imersão IA, os quais foram:
•	Inspirado na Imersão IA: O projeto AlertaRS foi concebido durante o curso Imersão IA, uma parceria entre Alura, Google e FIAP. Essa iniciativa busca democratizar o acesso ao conhecimento em inteligência artificial, capacitando profissionais para desenvolver soluções inovadoras e impactantes para os mais diversos desafios da sociedade. Dessa forma, o projeto foi desenvolvido dentro do ambiente do Google Colab, utilizando a IA generativa do Google e inserindo a Google API Key no sistema.
•	Criatividade: O projeto AlertaRS se destaca pela sua criatividade na simulação de dados. Através de estudos de engenharia, o projeto busca em fontes confiáveis o valor da velocidade ultrassônica em concretos, um parâmetro crucial para avaliar a integridade de estruturas sob estresse hídrico. Essa informação, combinada com dados climáticos em tempo real e modelos de inteligência artificial, permite a criação de um sistema de alerta preciso e eficaz.
•	Aplicação a sociedade, um projeto para o bem: A criatividade do projeto se estende à sua utilidade. O sistema AlertaRS não apenas informa a população sobre a iminência de possíveis alagamentos e inundações, mas também fornece o contato de hospitais, abrigos e ONG’s em caso de necessidade.
•	Eficácia: A simulação de dados, utilizando estudos de engenharia e valores da velocidade ultrassônica em concretos, poderiam gerar maior confiabilidade ao sistema de alerta. A precisão dos modelos de inteligência artificial e a constante atualização de dados climáticos em tempo real garantem a eficácia do sistema na identificação de riscos e na emissão de alertas oportunos.
•	Um compromisso com a ética: O projeto AlertaRS se baseia em princípios éticos sólidos. O resultado final não envolve nenhum tipo de discurso violento, preconceituoso ou de ódio. O objetivo principal é proteger a vida e o bem-estar da população do Rio Grande do Sul, promovendo a segurança e o desenvolvimento sustentável da região.

# 2 – Metodologia
O AlertaRS, sistema inovador de alerta à população do Rio Grande do Sul sobre inundações, baseia-se em uma metodologia robusta e criativa que combina inteligência artificial, simulação de dados e coleta de informações em tempo real (Figura 1 a e Figura 1 b). Os valores de velocidade ultrassônica, supostamente medido em loco na barragem, por exemplo, devem estar entre os valores mostrados na Tabela 1.
![image](https://github.com/lucianafem/alertaRS/assets/62123799/c9c65ccc-fdde-40a8-9edf-147734b42211)
![image](https://github.com/lucianafem/alertaRS/assets/62123799/cd2ac8d5-d430-4577-b0a1-a87bcad04e8f)       
Fig.1: a) Barragem, b) medição em loco da velocidade da onda ultrassônica no concreto da barragem. Fotos geradas por inteligência artificial.

![image](https://github.com/lucianafem/alertaRS/assets/62123799/d46869cb-3712-4148-a63d-c52f4ff3c6b2)

Para alimentar o modelo de inteligência artificial, foram gerados cem dados. Cada um desses dados representa uma simulação de cenário de inundação, levando em consideração diferentes níveis de precipitação, nível de água no Guaíba e velocidade da onda ultrassônica no concreto. Desses dados, 35 foram utilizados para treinar a rede neural, o que se chama de fase de treinamento. A tabela 2 mostra uma parte desses dados onde começa na data de 01/02/2024 e vai até 10/05/24.
Tabela 2. Alguns valores de dados simulados.
DATA	PRECIPITACAO
(MM)	NÍVEL	VELOCIDADE
(M/S)	CLASSIFICACAO
01/02/2024	4,00	2	5100	0
02/02/2024	10,00	2.3	5000	0
03/02/2024	2,00	1.2	5200	0
04/02/2024	6,00	2	5000	0
05/02/2024	11,00	2.4	4200	1
06/02/2024	9,00	2.1	4800	0
07/02/2024	5,00	2	4880	0
08/02/2024	2,00	1.7	4910	0
09/02/2024	11,00	2	4819	1
10/02/2024	12,00	2	4600	1
11/02/2024	17,00	2.2	4700	1
12/02/2024	22,00	2.3	4710	1
13/02/2024	19,00	1.9	4934	1
14/02/2024	11,00	1.8	5008	1

O modelo do AlertaRS é uma rede neural artificial contendo quatro camadas. Cada camada possui um número específico de neurônios:
•	Camada 1: 8 neurônios
•	Camada 2: 10 neurônios
•	Camada 3: 10 neurônios
•	Camada 4 (de saída): 6 neurônios
Essa estrutura permite que a rede aprenda padrões complexos nas simulações, mapeando diferentes combinações de variáveis para a classificação do risco de inundação.
A camada final da rede neural possui seis neurônios, pois o sistema classifica o risco em seis níveis (Tabela 3):
Tabela 3. Classificação e os níveis de cada risco.
CLASSIFICAÇÃO	NÍVEL DO RISCO
0	Nenhum risco
1	Baixo risco
2	Moderado risco
3	Alto risco
4	Muito alto risco
5	
Para cada simulação, a rede neural gera uma classificação, indicando o nível de risco de inundação para a população.
Para garantir a confiabilidade do modelo, foi gerada uma matriz de confusão. Essa ferramenta visual apresenta a frequência com que o modelo classificou corretamente cada tipo de risco, permitindo identificar possíveis falhas e ajustar o modelo para maior precisão.
O AlertaRS vai além da simulação. Através do web scraping, o sistema busca em tempo real a precipitação atual em mm na cidade do Rio Grande do Sul no site ClimaTempo. Essa informação, juntamente com as outras duas variáveis (nível da água e estado das estruturas), é alimentada no modelo de rede neural para gerar a classificação final do risco.  
Com base na classificação final, o AlertaRS emite uma recomendação (Tabela 4) para a população, que pode variar de "nenhum sinal de alerta" até "evacuação total" (Figura 2 a e Figura 2 b). Essa comunicação clara e precisa permite que as pessoas tomem medidas adequadas para se protegerem, minimizando os impactos das inundações.
Tabela 4: Recomendação dada a população de acordo com a classificação.
CLASSIFICAÇÃO	RECOMENDACAO
0	Não há nenhum sinal de alerta. 
1	Chuvas consideradas fracas e não há nenhum sinal de alerta para emitir a população.
2	Chuvas moderadas. Poucos alagamentos. Barragem sob controle. Emitir alerta a população das possíveis regiões alagadas.
3	Chuvas moderadas ou fortes. Concreto sob controle. Regiões de alagamentos. Alertar imediatamente a população das áreas alagadas e os cuidados a serem tomados. 
4	Chuvas intensas ocasionando o aumento inesperado do volume de água no reservatório. Alertar a população dos riscos de enchentes. Avisar a população imediatamente dos possíveis pontos alagados na cidade. Qualidade do concreto baixa. Solicitar reparo urgentemente da barragem ou pedir a evacuação da população.
5	Chuvas intensas ocasionando possível transbordo na barragem e talvez, possibilidade de rompimento. Evacuação total da população na cidade. Emitir sinal de alerta instantaneamente.  Comunicar aos órgãos de imprensa para divulgarem o alerta nos diversos meios de comunicação. Vidas em risco.

   ![image](https://github.com/lucianafem/alertaRS/assets/62123799/40d1651f-6b69-424f-8131-fe9ab220fdce)
   ![image](https://github.com/lucianafem/alertaRS/assets/62123799/bbdf2ad2-f71c-4865-8dbc-052641862cd4)


Fig. 2: a) e b) Aa classificações geradas fornecem recomendações para a população. Fotos geradas por inteligência artificial.

# 3 – Resultados
	O treinamento com a rede neural forneceu a matriz de confusão mostrada na figura 3. A soma de todos os elementos são os 35 dados de treinamentos do total de 100.
 
Fig. 3: Matriz de confusão gerada pelo treinamento da rede neural.
	A acurácia do modelo é mostrada na figura 4.
 
Fig.4: Acurácia do modelo de rede neural treinado com os dados simulados.
	Para entender como funciona o programa, um exemplo será explicado. Através da web scraping é tomado o valor da precipitação da data atual e isso faz com que o resultado seja atualizado para as pessoas tomarem ações baseadas no resultado obtido. O valor obtido é unido juntamente com valores simulados do nível do Guaíba e o valor da velocidade da onda no concreto. Esse é o input formado no qual é inserido no modelo de rede neural já treinado para obter o valor da classificação. Dessa forma, de acordo com o valor encontrado da classificação é fornecida uma recomendação. Se o valor obtido for 5, isso exige a evacuação instantânea das pessoas devido a gravidade do problema, ou seja, risco alto de rompimento da barragem juntamente com chuvas intensas. Isso poderia evitar uma sequência de mortes que infelizmente ocorreu nesses últimos dias no estado do Rio Grande do Sul no mês de maio de 2024. O salvamento de vidas com esse programa é algo desejado: vidas humanas e a vidas dos animais. 
	Além disso, se a população de Porto Alegre, por exemplo, quiser encontrar os cinco principais hospitais que atendam em caso de emergência, pontos de abrigo e ONG’s que possam ajudar, o usuário apenas deverá inserir o nome do país, estado e cidade: Brasil, Rio Grande do Sul e Porto Alegre.  O resultado obtido é esse:
País: Brasil
Estado: Rio Grande do Sul
Cidade: Porto Alegre

**5 Maiores Hospitais de Emergência em Porto Alegre, Rio Grande do Sul**

1. **Hospital de Pronto Socorro (HPS)**
- Endereço: Avenida Ipiranga, 6581 - Centro
- Telefone: (51) 3220-8000

2. **Hospital Moinhos de Vento**
- Endereço: Rua Tiradentes, 333 - Centro
- Telefone: (51) 3320-1000

3. **Hospital Mãe de Deus**
- Endereço: Rua José de Alencar, 201 - Centro
- Telefone: (51) 3230-3000

4. **Hospital Cristo Redentor**
- Endereço: Avenida Ipiranga, 5460 - Partenon
- Telefone: (51) 3316-3000

5. **Hospital Universitário de Porto Alegre (HU-UFRGS)**
- Endereço: Rua Sarmento Leite, 245 - Centro
- Telefone: (51) 3359-8000

**5 Maiores Pontos de Abrigo em Porto Alegre, Rio Grande do Sul**

1. **Centro de Referência em Assistência Social (CRAS) Centro**
- Endereço: Rua dos Andradas, 1125 - Centro
- Telefone: (51) 3289-2740

2. **Centro de Referência em Assistência Social (CRAS) Partenon**
- Endereço: Rua João Antônio da Silveira, 45 - Partenon
- Telefone: (51) 3289-2749

3. **Centro de Referência em Assistência Social (CRAS) Restinga**
- Endereço: Rua João Antônio da Silveira, 45 - Restinga
- Telefone: (51) 3289-2754

4. **Centro de Referência em Assistência Social (CRAS) Vila Nova**
- Endereço: Rua João Antônio da Silveira, 45 - Vila Nova
- Telefone: (51) 3289-2759

5. **Centro de Referência em Assistência Social (CRAS) Zona Norte**
- Endereço: Rua João Antônio da Silveira, 45 - Zona Norte
- Telefone: (51) 3289-2764

**5 ONGs que Poderiam Ajudar em Porto Alegre, Rio Grande do Sul**

1. **Associação Beneficente Lar do Menino Jesus**
- Endereço: Rua João Antônio da Silveira, 45 - Centro
- Telefone: (51) 3289-2740

2. **Associação Beneficente Hospitalar São Lucas**
- Endereço: Rua João Antônio da Silveira, 45 - Partenon
- Telefone: (51) 3289-2749

3. **Associação Beneficente Lar das Crianças**
- Endereço: Rua João Antônio da Silveira, 45 - Restinga
- Telefone: (51) 3289-2754

4. **Associação Beneficente Lar dos Velhos**
- Endereço: Rua João Antônio da Silveira, 45 - Vila Nova
- Telefone: (51) 3289-2759

5. **Associação Beneficente Lar dos Animais**
- Endereço: Rua João Antônio da Silveira, 45 - Zona Norte
- Telefone: (51) 3289-2764


# 4 - Conclusões
	O projeto desenvolvido foi capaz de prever os riscos devido as condições meteorológicas, níveis de água do Rio Guaíba e a qualidade do concreto alertando a população sob medidas a serem tomadas e em caso de risco muito alto, solicitando a divulgação em órgãos em todos os meios de comunicação, evitando com que as pessoas possam sofrer maiores dados, chegando até a perderem suas vidas.
	Além disso, o AlertaRS foi capaz de enviar os contatos dos principais hospitais, abrigos e ONG’s para que a população possa se sentir protegida em caso de necessidade.
O AlertaRS é um exemplo inspirador de como a criatividade, a utilidade, a eficácia e a ética podem se unir para construir um futuro mais seguro e sustentável. Ao utilizar a inteligência artificial de forma responsável e inovadora, podemos proteger vidas, minimizar danos e construir uma sociedade mais resiliente às mudanças climáticas. Evitar riscos de inundações e alagamentos é fundamental nos tempos atuais no estado do Rio Grande do Sul.
O AlertaRS está em constante evolução. Novos dados e simulações são continuamente integrados ao sistema, aprimorando o modelo de inteligência artificial e aumentando sua precisão.

# 5 – Referências Bibliográficas

WHITEHURST, E. A. Evaluation of concrete properties from sonic test. Detroit American Concrete Institute, 1966. Acesso em: 11 de maio de 2024, Disponível em: < https://www.ajol.info/index.php/njt/article/view/123556 >

# 6 - Agradecimentos

	Os agradecimentos especiais são para os professores desse curso: Paulo Silveira, Luciano Martins, Ana Raquel e Fabrício Carraro os quais agregaram muito conhecimento para a construção desse projeto. 
A Alura, Google e FIAP, o meu muito obrigada por essa oportunidade!


