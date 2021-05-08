![img](https://i.imgur.com/upK2IkS.png)

**Contextualização**
-----
As bases a serem explorada nesse estudo foram disponibilizada pela Alura, na 3ª edição da Imersão Dados, e esse projeto foi inspirado em um desafio do Laboratory for Innovation Science at Harvard (https://www.kaggle.com/c/lish-moa).  As análises aqui apresentadas são extraídas de bases com experimentos e resultados de estudos de compostos químicos aplicados em diferentes genes e tipos celulares. 



-----
**Objetivo**
-----
O principal objetivo é explorar a possibilidade de criar modelos de machine learning que possam prever informações que sirvam de auxílio ao processo de descoberta de novos fármacos.

------
Variáveis de interesse
------

Os modelos desenvolvidos nesse projeto tem como objetivo prever as variáveis:

Se algum mecanismo de ação é ativado ou não:
- 0 ou 1 | [ativo_moa]

Compostos:
- '87d714366', '9f80f3f77', '8b87a7a83' ou '5628cb3ee' | [composto] (teste de machine learning controlado, há mais de 3000 compostos na base)

Se o tratamento é com_controle:
- 0 ou 1 | [com_controle]

------
**Base de dados**
------
A base de dados se encontra nesse mesmo diretório e está separada em dois arquivos:

- Dados de experimento (comprimido em zip)

- Dados de resultados (csv)

-----

**Entenda as variáveis**
-----
**Dados de experimentos**

**id** | identificador único do experimento;

**tratamento [com_controle, com_droga]** | com_controle: grupo não afetado por composto químico, serve de referência para os que são afetados. com_droga: grupo afetado por compostos químicos;

**g's [g0 até g771]**: genes utilizados para experimento;

**c's [c0 até c99]**: tipos celulares utilizados para experimento.

Os valores disponíveis nas colunas de genes são referentes a variabilidade normalizada das expressões gênicas. Já os valores disponíveis nas colunas de tipos celulares, são referentes a viabilidade celular.

-----

**Dados de resultados**

**id** | identificador único do resultado;

**demais colunas** | as demais colunas são mecanismos de ação ou, como serão mencionados nesse projeto: Mechanism of Action (MoA).

Os mecanismos de ação são registrados como não ativados ou ativados [0, 1]. Temos diversos tipos de MoA na análise de resultados a serem apresentados no decorrer das análises.

-----
Referências
-----

[1] Drug Discovery: passado, presente e futuro
(https://docs.google.com/document/d/10EhrQBChlyYIcff3to7PrCQi5HcNk2r-zd2ZCKPtcz8/edit)

[2] Expressão gênica: o caminho da informação biológica (https://drive.google.com/file/d/1VNP08ffCiGD8cqaBkdHATWSX8Yxfm3dj/view)

[3] Grupo de controle (https://pt.wikipedia.org/wiki/Grupo_de_controle#:~:text=Um%20grupo%20de%20controle%20cient%C3%ADfico,dois%20experimentos%20id%C3%AAnticos%20s%C3%A3o%20conduzidos)

[4] Regressão logística (http://www.portalaction.com.br/analise-de-regressao/regressao-logistica#:~:text=O%20modelo%20de%20regress%C3%A3o%20log%C3%ADstica,e%20%22sucesso%22%2C%20respectivamente.&text=O%20modelo%20de%20regress%C3%A3o%20log%C3%ADstica,e%20%22sucesso%22%2C%20respectivamente)

[5] Dummy classifier (https://scikit-learn.org/stable/modules/generated/sklearn.dummy.DummyClassifier.html)

[6] Árvores de Decisão (https://medium.com/machine-learning-beyond-deep-learning/%C3%A1rvores-de-decis%C3%A3o-3f52f6420b69)

[7] Sobreajuste (Overfitting) (https://pt.wikipedia.org/wiki/Sobreajuste)

[8] Supporting Vector Classifier (SVC) (https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html)

[9] SciKit Learn (https://scikit-learn.org/stable/)

[10] Alura (https://www.alura.com.br/)
