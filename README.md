# ML_Logistica

Desenvolvimento de Machine Learning para a área de Logística. Este projeto visa prever o tipo de produto baseado no peso e no tipo de embalagem.

<details>
  <summary>Introdução</summary>
  
  ## Estrutura do Projeto

  ![Explicação dos Arquivos](imagens/explicacaoarquivos.png)
  
  - A pasta `modelo` contém os dados dos modelos treinados.
  - A pasta `templates` contém o template da página *HTML*.
  - O arquivo `p1_deploy.py` contém o desenvolvimento do software para deployment.
  - O arquivo `p1_modelo.py` contém o desenvolvimento do modelo de *Machine Learning*.
  - O arquivo `versoes.py` contém o código para verificar as versões dos pacotes utilizados.
  
</details>

<details>
  <summary>versoes.py</summary>
  
  ## Executando o arquivo `versoes.py`

  ![versoes.py](imagens/versoes.png)
  
  Este script verifica os pacotes e versões instalados para este projeto.
  
</details>

<details>
  <summary>p1_modelo.py</summary>
  
  ## Executando o arquivo `p1_modelo.py`

  Este script realiza as seguintes etapas:

  1. **Importação dos Pacotes e Preparação dos Dados**
     - Importa os pacotes necessários.
     - Carrega os dados de entrada e saída.
     - Separa os dados.

     ![Preparação dos Dados](imagens/p1_modelo_1.png)
  
  2. **Divisão dos Dados**
     - Divide os dados em conjuntos de treino e teste.
     - Aprende os parâmetros categóricos para convertê-los em numéricos.
     
     ![Divisão dos Dados](imagens/p1_modelo_2.png)
  
  3. **Transformação dos Dados**
     - Transforma os dados categóricos em numéricos com base no ajuste (`fit`).

     ![Transformação dos Dados](imagens/p1_modelo_3.png)
  
  4. **Treinamento e Avaliação do Modelo**
     - Treina o modelo de Machine Learning.
     - Realiza previsões (inferência).
     - Verifica a acurácia do modelo.
     - Gera um relatório de desempenho.
     - Salva o modelo treinado e os transformadores.

     ![Treinamento e Avaliação](imagens/p1_modelo_4.png)

  ### Resultado do Treinamento:
  - **Acurácia**: 67%
  - **Precisão**:
    - Classe 0 (Caixa de Papelão): 50%
    - Classe 1 (Plástico Bolha): 100%
  - **Recall**:
    - Classe 0 (Caixa de Papelão): 100%
    - Classe 1 (Plástico Bolha): 50%
  - **F1-Score**: Média harmônica da precisão e recall, equilibrada em 67%.
  - **Macro Average**: Média aritmética das métricas para todas as classes (não ponderada).
  - **Weighted Average**: Média ponderada das métricas para todas as classes, considerando o suporte de cada classe.
  
  ![Resultado do Treinamento](imagens/p1_modelo_5.png)
  
</details>

<details>
  <summary>p1_deploy.py</summary>
  
  ## Executando o arquivo `p1_deploy.py`

  Este script realiza as seguintes etapas:

  1. **Importação e Inicialização**
     - Importa os pacotes necessários.
     - Instancia o Flask.
     - Carrega o modelo e os transformadores salvos.

     ![Inicialização](imagens/p1_deploy_1.png)
  
  2. **Renderização da Página e Previsão**
     - Renderiza a página inicial.
     - Extrai a previsão do produto a partir dos dados de entrada.

     ![Renderização e Previsão](imagens/p1_deploy_2.png)
  
  3. **Execução e Uso**
     - Executa o código Python.
     - Utiliza via navegador, inserindo os dados e obtendo o resultado.

     ![Execução e Uso](imagens/p1_deploy_3.png)
  
</details>


Esta estrutura fornece uma visão detalhada do projeto e facilita a compreensão e a execução dos scripts para desenvolvimento, avaliação e deployment do modelo de Machine Learning.