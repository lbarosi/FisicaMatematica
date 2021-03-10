# Instalação do Python

Estas instruções são para um sistema Linux de 64 bits. Mas pode ser realizada em Windows ou MacOs, fazendo as alterações adequadas ao seu sistema operacional.

Primeiro clone o repositório
``` bash
git clone https://github.com/lbarosi/FisicaMatematica.git
```

Você deve instalar o git primeiro, siga os passos apropriados para instalar no seu sistema operacional. (GOOGLE!)

1. Baixe o `miniconda`.
2. Crie um ambiente
3. Inicie seu ambiente
4. Abra o Jupyter

Se o seu sistema operacional é Linux os passos abaixo vão reproduzir os passos 1 a 4 acima. Caso o seu sistema não seja Linux, o passo 1 deve ser adaptado, o que equivale a trocar as linhas 2 - 4 das instruções pelas instruções adequadas ao seu SO em https://docs.conda.io/en/latest/miniconda.html.

Os passos acima são executados com os seguintes comandos:

```` bash
cd MEU_CAMINHO/FisicaMatematica
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
chmod u+x ./Miniconda3-latest-Linux-x86_64.sh
./Miniconda3-latest-Linux-x86_64.sh
conda update conda
conda env create -f environment.yml
conda activate cursos
jupyter notebook &
````

O Jupyter vai abrir em seu navegador, disponível no endereço local http://localhost:8000


# Instalação do Kernel do Mathematica


## Faça o Download do Kernel

Você deve acessar a página da https://www.wolfram.com/engine/ seguir os passos indicados na tela. Você vai precisar criar uma conta, mas o aplicativo é gratuito. O licenciamento será feito com o **wolframscript**.

## wolframscript Install

Acesse https://www.wolfram.com/wolframscript/ e instale o aplicativo que você acabou de baixar em um lugar sensato em seu computador e instale da forma apropriada ao seu sistema operacional.

Rode o **woloframscript** e siga as instruções para realizar o licenciamento.

## Publicando o Kernel

1. Ative o env do Python que deseja utilizar. (Se você está seguindo as instruçṍes deste curso será **cursos** )

````bash
conda activate cursos
````

2. Clone o repositório (em uma pasta sensata):

````bash
git clone https://github.com/WolframResearch/WolframLanguageForJupyter.git
````

3. Registre  o Kernel

````bash
cd WolframLanguageForJupyter
./configure-jupyter.wls add
````
## Teste sua instalação

````bash
jupyter kernelspec list
````
Você deve ver uma lista, uma das linhas será alguma coisa assim, com os seus diretórios indicados.

````
  wolframlanguage12    /home/lbarosi/.local/share/jupyter/kernels/wolframlanguage12
````
