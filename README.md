Credit Card Fraud Detection
Wilson Azer Junior
Hist�rico do assunto
Pode-se dizer com toda certeza que para o bem ou para o mau, a vontade humana de levar vantagem sempre moveu a humanidade, partindo da�, pode-se afirmar tamb�m que a necessidade de evitar e descobrir fraudes sempre estiveram presentes em n�ssa hist�ria. Com institui��es financeiras isso n�o � diferente. Segundo pesquisa da PwC, de crimes econ�micos globais de 2016, indica que aproximadamente 36% das organiza��es sofreram com crimes econ�micos. O que nos leva ao tema do presente trabalho, descobrir fraudes financeiras em cart�es de cr�dito usando Data Science e Machine Learning.
O que torna esse assunto relevante, mesmo nos dias atuais, � que � uma �rdua tarefa se conseguir equil�brio entre conceder cr�dito e n�o tomar preju�zo. Outro fato � que o desempenho da descoberta desse tipo fraude em transa��es de cart�o de cr�dito � muito afetado pela abordagem de amostragem no conjunto de dados, sele��o de vari�veis e t�cnica (s) de detec��o utilizada. N�o existe bala de prata quando o assunto � prevenir fraudes financeiras, mas com toda certeza, pode-se conseguir resultados animadores, aplicando-se t�cnicas adequadas.
Solu��o encontrada (Detec��o de aproximadamente 83% de transa��es fraudulentas)
Detec��o de Fraude em Cart�es de Cr�dito pode ser considerado um dos cl�ssicos desafios que apredizagem supervisionada, mais especificamente � um problema de classifica��o. Onde dado uma s�rie de infoma��es hist�ricas de diversos clientes, j� previamente classificados entre bons e maus pagadores, tenta-se criar um modelo que possa corretamente identificar em qual dos dois grupos, dado um novo cliente. O mais importante aqui � evitar ao m�ximo os maus pagadores sem restringir demais para n�o perder bons.
Ao final de nossa an�lise, podemos afirmar que encontramos um classificador que identifica, em m�dia, aproximadamente 81% de transa��es fraudulentas, target 1, e errando muito pouco  falsos positivos.

Com esses resultados podemos argumentar sobre nosso estimador final:
Comparado nosso modelo com outros encontrados na Internet para o mesmo dataset, nossos resultados s�o razo�velmente bons. Enquanto que em algumas an�lises se encontrou um Recall de 0.61-0.63, nossa an�lise atingiu um Recall de 0.80. Outro trabalho muito bom desenvolvido em R atingiu valores m�dios de AUPRC de 0.95-0.96, o nosso modelo atinge m�dias de 0.96-0.97 para situa��o similar.
Estrat�gias empregadas em nossa an�lise:
n�o remover nenhum outlier: o que se mostrou eficiente para nosso caso.
Sele��o de Caracter�sticas mais importantes: para essa tarefa foi usado ExtraTreeCassifier, selecionando-se as 8 principais caracter�sticas.
Escalonamento das caracter�sticas:  Usando StandardScaler.
AUC final no conjunto de testes: 0.92% usando-se cross validation com cv= 10.
classificador final: Gaussian Naive Bayes 
Instala��o
Este projeto requer Python 3.6 e as seguintes bibliotecas Python instaladas:
NumPy
Pandas
scikit-learn
Voc� tamb�m precisar� ter software instalado para rodar e executar um Jupyter Notebook
Execu��o
Em um terminal ou janela de comando, navegue at� o diret�rio raiz de projeto e execute os seguintes comandos:

jupyter notebook Credit_card_fraud_detection.ipynb
Isso abrir� o o software e arquivo de projeto Jupyter Notebook em seu navegador.
Dados
O Dataset cont�m transa��es realizadas com cart�es de cr�dito em setembro de 2013 pelos detentores de cart�o europeus. Este conjunto de dados apresenta transa��es ocorridas em dois dias, onde temos 492 fraudes de 284.807 transa��es. Os dados usados neste projeto est�o inclu�dos em creditcard.csv. O conjunto de dados pode ser baixado em https://www.kaggle.com/mlg-ulb/creditcardfraud/data.

