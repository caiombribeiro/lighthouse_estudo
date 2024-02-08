# Relatório do Banco Vitória (BanVic)

## Introdução

O Banco Vitória (BanVic), instituição financeira de caráter inovador, tem consolidado sua posição no mercado financeiro. Com uma gama diversificada de produtos e serviços, o BanVic se destaca pela sua abordagem personalizada na gestão de relações com clientes e na oferta de soluções financeiras.

Porém, agora estamos em uma era tecnológica em que geramos milhões de dados a todo momento. Por conta desse grande volume, muitas vezes se torna desafiador conseguir extrair informações úteis com tantos dados a disposição. Por isso, o ato de lidar adequadamente com esse montante de fatos apenas aumentará pelos próximos anos.

Enxergando esse cenário, fica clara a importância de se ter a melhor gestão desses dados. Desde as formas como eles são coletados e tratados, até como eles gerarão insights valiosos por meio de visualizações, quanto mais informações forem extraídas dessas bases maior será a clareza na tomada de decisão pelos colaboradores.

Com isso em mente, esse presente relatório tem como finalidade principal demonstrar quais as possibilidades podem ser geradas quando se há uma tratativa e exposição dos dados clara e trazer certas tomadas de decisão com base nas tabelas obtidas da BanVic.

## Processo de Análise

### Definição da Análise:

A primeira etapa da análise está ligada aos interesses que a Análise deseja alcançar e isso é feito pelas perguntas. Pensando na BanVic, algumas perguntas são importantes para o entendimento da eficiência do negócio, tais como: 

- Quais ações podem ser tomadas para a aquisição de novos clientes? 
- O banco digital traz mais ou menos retorno do que o banco físico? 
- Quais produtos do banco são mais rentáveis? 
- Pode ser aplicados indicadores para cada uma dessas e outras perguntas.

Sobre novos clientes, é possível trazer a visualização de quais estados possuem clientes mais ativos para focar o marketing de atração. Sobre as agências, é possível trazer a taxa de clientes ativos pelo total, assim como quantidade de colaboradores por tipo de agência. Por fim, sobre a rentabilidade, é possível comparar se os empréstimos geram mais ou menos retorno do que as transações.

Ainda é viável fazer mais perguntas. Quanto melhores elas forem elaboradas, mais fácil será os processos de limpeza, análise e visualização, assim como alcançar um melhor resultado no geral.

### Transformação e tratamento de dados

Obtendo o direcionamento por meios das perguntas, a limpeza ajudará tanto em ver se os dados estão consolidados e precisos, assim como garantir que apenas os dados de interesse ao projeto serão utilizados. 

Primeiramente, foi checada se as tabelas estão concisas, sem elementos faltantes e bem estruturadas. Tendo aval positivo, foram delimitados os atributos de cada uma das tabelas que precisavam ser realocados.

Para tratar os dados, foi utilizado o Jupyter Notebook junto com o Python/Pandas por conta da facilidade do uso dessas ferramentas, tanto pela versatilidade quanto pela recorrência delas no processo de tratamento. 

Mas, essa etapa pode ser feita também por SQL ao trabalhar com banco de dados ou Excel/Sheets caso seja melhor. Também é possível trabalhar com um pipeline de dados e data Warehouse no sistema em nuvem Azure ou AWS caso tenha interesse em segurança extra.

Sobre esse processo, algumas alterações formam feitas nas planilhas, dentre elas:

- Separação do UF dos clientes e colaboradores do endereço para análise por estado;
- Normalização das datas em um formado possível de ser compreendido pelo Power Bi;
- Normalização do CEP, deixando todos sem o hífen;
- Criação de uma coluna de tipo de Transação, para facilitar o filtro no Dashboard;
- Seleção de colunas de interesse, para melhorar a performance do Dashboard;

O arquivo do notebook com todas essas informações está presente neste [link](https://github.com/caiombribeiro/lighthouse_estudo/blob/main/consulta_planilhas.IPYNB).

### Visualização dos dados

Após o tratamento adequado, entra a fase de dispor esses dados em Dashboards de uma forma clara e objetiva, sempre respeitando os interesses levantados já na primeira etapa das perguntas.

Para isso, foi confeccionado um dashboard com 4 abas distintas, sendo elas acessadas pelos botões dispostos no canto superior central, feitos por meio da guia Indicadores do Power BI. Cada uma dessas abas dispõe sobre um determinado interesse em específico.

A primeira aba está relacionada a indicativos das agências. Aqui é disposto o número de contas ativas (considerando a utilização da conta nos últimos 2 anos), número de colaboradores, soma total do saldo final das contas em formato de KPI. Há também um gráfico sobre contagem de contas por agências e um mapa demonstrando a quantidade de colaboradores espalhados pelo Brasil.

Para filtro, foi disponibilizado no canto superior direito a opção de selecionar por conta Ativa ou Inativa. E é possível fazer o filtro selecionando uma das colunas de Contagem de Contas por Agência ou o círculo na UF dos colaboradores.

![](Aspose.Words.f79437d1-da27-4c09-9cfe-9331b6765f0b.001.jpeg)Fonte: Dashboard BanVic	

A segunda aba está relacionada aos clientes da BanVic. Nesse, também temos como indicadores presentes o número total de clientes, a soma total de contas e o mapa com a quantidade de clientes pelo Brasil.  As maiores diferenças aqui se devem a existência da taxa de clientes ativos, o gráfico de faixa etária dos clientes e o filtro de agência.

![](Aspose.Words.f79437d1-da27-4c09-9cfe-9331b6765f0b.002.jpeg)

Fonte: Dashboard BanVic





![](Aspose.Words.f79437d1-da27-4c09-9cfe-9331b6765f0b.003.jpeg)A terceira aba é referente às propostas de crédito. Aqui os indicadores analisados são o número de propostas, taxa de aprovação das propostas, média das propostas, média da entrada, número de parcelas média e média do financiamento. Para filtro, temos o status da proposta e a data inicial, assim como a agência que recebeu a proposta. 

Fonte: Dashboard BanVic

A quarta aba e última é referente as transações presentes na BanVic. Aqui temos o número de contas, total de valores das transações e quantidade de transações feitas. Os gráficos são referentes, da esquerda para a direita, sobre o valor total de transações por período e a contagem de transações por tipo. Pode ser filtrado pelo estado do cliente e data inclusive.

![](Aspose.Words.f79437d1-da27-4c09-9cfe-9331b6765f0b.004.jpeg)

Fonte: Dashboard BanVic

## Insights e Resultados

### Análise para entendimento do negócio

Agora que o dashboard foi apresentado, o processo de extração de alguns insights sobre o funcionamento do negócio se torna mais palpável e claro para entendimento.

Considerando a aba de agência, é perceptível a diferença nítida de resultado entre as agências físicas e a digital. O total de contas ativas é de 787, sendo 396 filiadas a agência digital. Sobre saldo final das contas, a agência digital possui 12 dos 26 milhões totais. 

Ou seja, a agência digital possui um potencial muito maior do que as agências físicas e com menor custo laboral, por ter apenas 7 dos 100 colaboradores em sua gestão.

Seguindo o estudo, na aba Clientes, o número de clientes em diferentes faixas etárias é bem distribuído. Contudo, é possível considerar que a quantidade de clientes acima de 60 anos é bastante alta, o que poderia render um marketing focado nessa faixa etária, incluindo para crédito consignado. 

Agora, sobre a questão do crédito, 935 das 2000 propostas foram feitas pela agência digital, sendo que houve 1,1% a mais de aprovação delas em comparação a média de todas as agências. Isso mostra que investir em crédito pela agência digital traz bastante retorno e melhora a chance do cliente de conseguir a respostas esperada.

Por fim, compreendendo a aba transações, fica nítido o quanto o pix se tornou uma importante forma de transferência monetária, mas que a transferência bancária ainda é o tipo de transação que mais movimenta dinheiro, mesmo a quantidade de transações ser apenas maior do que a do boleto.

### Conclusão e recomendações


Com base nas análises apresentadas e nos insights obtidos do dashboard do Banco Vitória (BanVic), a conclusão aponta para um cenário promissor, com oportunidades claras de otimização e crescimento em relação as agências digitais.

Elas demonstram um potencial significativo em termos de contas ativas, número de colaboradores para operacional funciona e rentabilidade, sugerindo uma reavaliação da distribuição de recursos entre canais digitais e físicos. 

Inclusive, a eficácia das propostas de crédito digitais indica que investimentos adicionais em canais digitais podem aumentar a satisfação do cliente e a rentabilidade. 

Outro ponto a ser considerado é diversidade etária dos clientes, pois ela destaca a possibilidade de estratégias de marketing personalizadas, especialmente para a população acima de 60 anos que detém boa parte das contas no banco. 

Inclusive, é bom ressaltar a importância da obtenção de uma tabela sobre serviços e produtos disponibilizados pela empresa para que se possa compreender quais são os mais rentáveis e importantes para cultivo do banco. 

Por fim, caso almeje o aprimoramento da compreensão das tabelas do negócio, ter em vista a expansão do uso de análises de dados para refinar a oferta de produtos e serviços garantirá que o BanVic permaneça na vanguarda da inovação financeira.

## Documentação

GitHub com todos os arquivos: <https://github.com/caiombribeiro/lighthouse_estudo>
