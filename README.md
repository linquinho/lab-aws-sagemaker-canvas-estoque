# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas. Neste Lab DIO, você aprenderá a usar o SageMaker Canvas para criar previsões de estoque baseadas em Machine Learning (ML). Siga os passos abaixo para completar o desafio!

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira nosso repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).


## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)

- Dê um fork neste projeto e reescreva este `README.md`. Sinta-se à vontade para detalhar todo o processo de criação do seu Modelo de ML para uma "Previsão de Estoque Inteligente".
- Para isso, siga o [passo a passo] descrito a seguir e evolua as suas habilidades em ML no-code com o Amazon SageMaker Canvas.
- Ao concluir, envie a URL do seu repositório com a solução na plataforma da DIO.


## 🚀 Passo a Passo

### 1. Selecionar Dataset

-   Navegue até a pasta `datasets` deste repositório. Esta pasta contém os datasets que você poderá escolher para treinar e testar seu modelo de ML. Sinta-se à vontade para gerar/enriquecer seus próprios datasets, quanto mais você se engajar, mais relevante esse projeto será em seu portfólio.
-   Escolha o dataset que você usará para treinar seu modelo de previsão de estoque.
-   Faça o upload do dataset no SageMaker Canvas.

### 2. Construir/Treinar

-   No SageMaker Canvas, importe o dataset que você selecionou.
-   Configure as variáveis de entrada e saída de acordo com os dados.
-   Inicie o treinamento do modelo. Isso pode levar algum tempo, dependendo do tamanho do dataset.

### 3. Analisar

-   Após o treinamento, examine as métricas de performance do modelo.
-   Verifique as principais características que influenciam as previsões.
-   Faça ajustes no modelo se necessário e re-treine até obter um desempenho satisfatório.

### 4. Prever

-   Use o modelo treinado para fazer previsões de estoque.
-   Exporte os resultados e analise as previsões geradas.
-   Documente suas conclusões e qualquer insight obtido a partir das previsões.

## 🤔 Dúvidas?

Esperamos que esta experiência tenha sido enriquecedora e que você tenha aprendido mais sobre Machine Learning aplicado a problemas reais. Se tiver alguma dúvida, não hesite em abrir uma issue neste repositório ou entrar em contato com a equipe da DIO.

## Entendendo as Métricas de Modelos de ML no SageMaker Canvas

- P10 (10º Percentil): Representa um valor abaixo do qual 10% das previsões estão. Em termos de estoque, este valor indica um cenário de baixa demanda. É útil para identificar períodos em que a demanda é mais baixa do que o esperado, ajudando a evitar excessos de estoque que podem resultar em custos adicionais de armazenamento ou perdas.
- P50 (50º Percentil): Este é o valor mediano nas previsões, mostrando a demanda média esperada. Para o controle de estoque, entender o P50 é crucial para planejamento médio de compras e reposição de produtos. Ele representa a situação mais comum de demanda que você deve considerar como base para suas decisões.
- P90 (90º Percentil): Indica um valor acima do qual 10% das previsões estão. Reflete um cenário de alta demanda, útil para planejar períodos de picos ou campanhas de vendas. Com essa informação, você pode assegurar que seu estoque está preparado para atender à demanda máxima esperada sem faltar produtos.
- Avg. wQL (Média da Perda Quantil Ponderada): Essa métrica mede o erro nas previsões, ponderado pela importância de cada item. Um valor menor indica maior precisão nas previsões. Em um cenário de estoque, isso ajuda a entender quais previsões estão mais próximas da realidade e onde podem estar os maiores riscos de erro, possibilitando ajustes mais precisos.
- MAPE (Erro Percentual Médio Absoluto): Calcula a média da porcentagem de erro das previsões em relação aos valores reais. Um MAPE menor indica maior precisão nas previsões. Por exemplo, se o MAPE for 5%, significa que, em média, as previsões de demanda estão erradas em 5% em relação à demanda real, o que é um bom indicador da eficiência do modelo.
- WAPE (Erro Percentual Absoluto Ponderado): Similar ao MAPE, mas leva em consideração a importância de cada item no estoque. Isso significa que itens de maior valor ou importância terão um impacto maior na métrica. Um WAPE menor é desejável, pois indica que o modelo está prevendo com mais precisão para os itens mais críticos, o que é essencial para uma gestão eficiente do estoque.
- RMSE (Raiz do Erro Quadrático Médio): Mede a diferença média entre os valores previstos e os valores reais, dando mais peso a grandes erros. Um RMSE menor é melhor, pois indica que as previsões estão, em média, próximas dos valores reais. No contexto de estoque, isso ajuda a minimizar grandes discrepâncias que podem levar a super ou subestimativas críticas.
- MASE (Erro Escalado Médio Absoluto): Compara o erro da previsão com um modelo simples. Um valor de MASE menor que 1 indica que o modelo está fazendo previsões mais precisas do que simplesmente usar a média histórica. Para controle de estoque, um MASE menor que 1 é um bom sinal de que o modelo está efetivamente melhorando a previsão em comparação com métodos mais básicos.

## Treinamento realizado com base em um DataSet com preço promocional e renovação de estoque:

![image](https://github.com/user-attachments/assets/578155c4-1815-44e0-9e64-52be3992afa9)

## Predição realizada para Item específico com histórico de demanda e predições Pesimista, Mediana e Otimista conforme explicado acima:

  <img width="584" alt="image" src="https://github.com/user-attachments/assets/e671aca9-094d-4f31-811e-5cacdf5e8fb4">


