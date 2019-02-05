Credit Card Fraud Detection
Wilson Azer Junior
Histórico do assunto
Pode-se dizer com toda certeza que para o bem ou para o mau, a vontade humana de levar vantagem sempre moveu a humanidade, partindo daí, pode-se afirmar também que a necessidade de evitar e descobrir fraudes sempre estiveram presentes em nóssa história. Com instituições financeiras isso não é diferente. Segundo pesquisa da PwC, de crimes econômicos globais de 2016, indica que aproximadamente 36% das organizações sofreram com crimes econômicos. O que nos leva ao tema do presente trabalho, descobrir fraudes financeiras em cartões de crédito usando Data Science e Machine Learning.
O que torna esse assunto relevante, mesmo nos dias atuais, é que é uma árdua tarefa se conseguir equilíbrio entre conceder crédito e não tomar prejuízo. Outro fato é que o desempenho da descoberta desse tipo fraude em transações de cartão de crédito é muito afetado pela abordagem de amostragem no conjunto de dados, seleção de variáveis e técnica (s) de detecção utilizada. Não existe bala de prata quando o assunto é prevenir fraudes financeiras, mas com toda certeza, pode-se conseguir resultados animadores, aplicando-se técnicas adequadas.
Solução encontrada (Detecção de aproximadamente 83% de transações fraudulentas)
Detecção de Fraude em Cartões de Crédito pode ser considerado um dos clássicos desafios que apredizagem supervisionada, mais especificamente é um problema de classificação. Onde dado uma série de infomações históricas de diversos clientes, já previamente classificados entre bons e maus pagadores, tenta-se criar um modelo que possa corretamente identificar em qual dos dois grupos, dado um novo cliente. O mais importante aqui é evitar ao máximo os maus pagadores sem restringir demais para não perder bons.
Ao final de nossa análise, podemos afirmar que encontramos um classificador que identifica, em média, aproximadamente 81% de transações fraudulentas, target 1, e errando muito pouco  falsos positivos.

Com esses resultados podemos argumentar sobre nosso estimador final:
Comparado nosso modelo com outros encontrados na Internet para o mesmo dataset, nossos resultados são razoávelmente bons. Enquanto que em algumas análises se encontrou um Recall de 0.61-0.63, nossa análise atingiu um Recall de 0.80. Outro trabalho muito bom desenvolvido em R atingiu valores médios de AUPRC de 0.95-0.96, o nosso modelo atinge médias de 0.96-0.97 para situação similar.
Estratágias empregadas em nossa análise:
não remover nenhum outlier: o que se mostrou eficiente para nosso caso.
Seleção de Características mais importantes: para essa tarefa foi usado ExtraTreeCassifier, selecionando-se as 8 principais características.
Escalonamento das características:  Usando StandardScaler.
AUC final no conjunto de testes: 0.92% usando-se cross validation com cv= 10.
classificador final: Gaussian Naive Bayes 
Instalação
Este projeto requer Python 3.6 e as seguintes bibliotecas Python instaladas:
NumPy
Pandas
scikit-learn
Você também precisará ter software instalado para rodar e executar um Jupyter Notebook
Execução
Em um terminal ou janela de comando, navegue até o diretório raiz de projeto e execute os seguintes comandos:

jupyter notebook Credit_card_fraud_detection.ipynb
Isso abrirá o o software e arquivo de projeto Jupyter Notebook em seu navegador.
Dados
O Dataset contém transações realizadas com cartões de crédito em setembro de 2013 pelos detentores de cartão europeus. Este conjunto de dados apresenta transações ocorridas em dois dias, onde temos 492 fraudes de 284.807 transações. Os dados usados neste projeto estão incluídos em creditcard.csv. O conjunto de dados pode ser baixado em https://www.kaggle.com/mlg-ulb/creditcardfraud/data.

