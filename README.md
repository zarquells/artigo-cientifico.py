## **Analisando a correlação entre o crescimento do PIB nacional e a população graduada de 2000 a 2025**

---

### **Resumo**

O Produto Interno Bruto (PIB) é um indicador de crescimento econômico composto por atividades produtivas, sendo empregado para entender as potências de um país como uma economia emergente ou melhor o índice de desenvolvimento humano em comparação ao resto do mundo. O Brasil é um país com uma forte desindustrialização que acaba não alavancando profissionais necessários no mundo como um todo, que alterariam significativamente o PIB se houvesse incentivo nacional para estes estudos. Este estudo tem como objetivo analisar e responder a hipóteses relacionadas à correlação entre educação, força de trabalho e o PIB do Brasil, tendo como foco o nível educacional brasileiro, para compreender o impacto de uma população qualificada sobre a economia. Para este projeto, foi utilizado o banco de dados público com levantamentos dos anos 2000 à 2024 no World Bank Data, Instituto Brasileiro de Geografia e Estatística (IBGE) e Organização das Nações Unidas (ONU). Serão analisadas as causas da ausência de incentivo nacional para que profissionais em áreas como tecnologia, ciência e inovação possam alavancar a indústria nacional e entender a ausência deste impacto de forma direta, ou indireta, no PIB nacional.

---
### **Passo a passo**

Para realizar esta análise, utilizei arquivos públicos principalmente do worldbank buscando informações relevantes que permitissem correlacionar as varíaveis principais (PIB e população qualificada). Explorei os anos 2000 à 2024 devido a maior quantidade de informações disponíveis e, quando havia varíaveis com pequenos 'gaps', complementei com informações externas (IBGE). E comecei a aplicar duas visões para os dados: temporal e taxa diferencial.

A primeiro momento, tive dados com alta taxa de correlação devido a relação orgânica de crescimento populacional e valorização do PIB:
<img width="972" height="665" alt="image" src="https://github.com/user-attachments/assets/106ec925-8cc5-4c90-9cdd-3177ce78e2b5" />

Para resolver isto, criei um novo dataframe baseado nas diferenças entre cada ano em porcentagem e, ao aplicar a correlação, tive melhores resultados:
<img width="918" height="626" alt="image" src="https://github.com/user-attachments/assets/626f12ea-02fd-4557-914e-8590bbe6738f" />

Com estes resultados, foi possível concluir que somente com estas varíaveis não era possível observar correlação entre a população nacional que ingressa em universidades ou, ao menos, finalizam o ensino médio. Entretanto, para enfatizar nossa indagação, buscamos artigos e revistas internacionais que observam esta relação em países mais desenvolvidos e demonstram que há uma taxa positiva e orgânica das varíaveis. 
Na lógica de mercado, o PIB positivo demonstra o investimento interno para qualificação da população e empregabilidade que, posteriormente, resulta em melhores produções nacionais.

---

### **Requisitos para execução**

Linguagem utilizada

Python 3.13.0

Bibliotecas necessárias

Pandas (pandas-2.3.2)
Numpy (numpy-2.1.2)

---

### **Como reproduzir a análise**

1. Extraía as bases de dados do https://www.worldbank.org/en/country/brazil sobre os KPIs de trabalho. Existem filtros de assuntos determinados voltados para o PIB e também mercado de trabalho.
2. Faça o download da base como .xlsx e aplique o caminho dos arquivos no começo do código.
3. A partir disso, ocorrerá diversas aplicações de limpeza e tratamento de dados assim como exibição e afins.
4. Para que os gráficos e filtros funcione é importante validar a nomenclatura das varíaveis (colunas).
