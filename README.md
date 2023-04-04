# CIÊNCIA DE DADOS APLICADA AO PISA 2018

## Introdução 🇧🇷
A presente pesquisa foi desenvolvida no Programa de Mestrado Profissional em Educação em Ciências Matemática e Tecnologia da Universidade Federal dos Vales do Jequitinhonha e Mucuri, com o objetivo de utilizar técnicas da Ciência de Dados para extrair conhecimento dos dados do PISA 2018. O estudo buscou identificar quais características, coletadas pelo questionário aplicado aos professores, têm mais impacto sobre o desempenho dos alunos nas avaliações de matemática e ciências, aplicando dois modelos de aprendizado supervisionado, o Decision Tree e o Random Forest. A seleção de atributos foi realizada com o método Recursive Feature Elimination, e os resultados mostraram que características relacionadas à tecnologia, incentivo dado aos alunos pelos professores, motivação e valorização do aprendizado e capacitação dos professores foram as principais influenciadoras de desempenho
## Considerações iniciais ☕
Ao executar os códigos, é importante ressaltar que os resultados podem variar minimamente a cada execução devido ao fator da aleatoriedade em algumas partes do código, como por exemplo, o parâmetro "random_state" que é utilizado por padrão pela função "train_test_split".

### Configurando o ambiente no LINUX 🐧
Abra o terminal e atualize a lista de pacotes disponíveis:
``` 
sudo apt update
```
Instale os pacotes do Python:

``` 
sudo apt install python3-pip
sudo apt install python3-dev
``` 

Instale os Ambientes Virtuais do Python:
``` 
sudo -H pip3 install --upgrade pip
sudo -H pip3 install virtualenv
``` 
Crie um ambiente virtual Python:

``` 
virtualenv pisa-env
``` 
Ative o ambiente virtual:

``` 
source pisa-env/bin/activate
``` 
Instale o Jupyter Notebook:
``` 
pip install jupyter
``` 
Instale as bibliotecas utilizadas no projeto:

``` 
pip install pandas numpy matplotlib seaborn sklearn pyreadstat
``` 
### Adquirindo os códigos 📥

``` 
sudo apt install git
git clone https://github.com/Rochelly/CIENCIA-DE-DADOS-APLICADA-AO-PISA-2018.git

``` 

#### Adquirindo a base de dados
As bases de dados utilizadas já estão presentes no repositório do projeto dentro da pasta "00-Basesde-dados", mas ainda podem ser adquiridas no site oficial da OCDE:

https://www.oecd.org/pisa/data/

### Executando os códigos 👨‍💻
Para executar os códigos, navegue pelo terminal até a pasta que contém os arquivos de códigos com o comando "cd":


``` 
cd CIENCIA-DE-DADOS-APLICADA-AO-PISA-2018/

``` 
Execute o Jupyter Notebook:


``` 
jupyter-notebook --ip=0.0.0.0 --port=8888

``` 
Após esse comando, você será redirecionado ao seu navegador padrão.

Antes de executar os códigos, configure caminho para a base de dados de acordo com seu ambiente:
```
professoresDF, infoProfessores=ps.read_sav('CY07_MSU_TCH_QQQ.sav')
```
Em alguns arquivos, existe uma variável que aponta para base de dados que também deve ser
configurada de acordo com o seu ambiente:
```
path='00-Bases-de-dados/Professores/CY07_MSU_TCH_QQQ.sav'
```
Após a configuração dos caminhos para as bases de dados, os arquivos poder ser executados clicando
em "Cell"e depois em "Run All".

Leia mais em: https://cienciadedadospisa.wordpress.com/
