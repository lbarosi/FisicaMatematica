# Instalação do Python

Estas instruções são para um sistema Linux de 64 bits. Mas pode ser realizada em Windows ou MacOs, fazendo as alterações adequadas ao seu sistema operacional.

1. Baixe o `miniconda`
2. Crie um ambiente
3. Inicie seu ambiente
4. Abra o Jupyter

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

Você deve acessar a página da http://wolfram.com e fazer o download de um arquivo chamado **wolframscript**. Você precisará fazer uma conta para isso.

## wolframscript Install

Copie o aplicativo que você acabou de baixar em um lugar sensato em seu computador e instale da forma apropriada ao seu sistema operaçcional.

## Publicando o Kernel

1. Ative o env do Python que deseja utilizar. (Se você está seguindo as instruçṍes deste curso será **cursos** )

````bash
conda activate cursos
````

2. Clone o repositório (em uma pasta sensata):

````bash
git clone https://github.com/WolframResearch/WolframLanguageForJupyter.git
````

3. Ative o Kernel

````bash
git clone https://github.com/WolframResearch/WolframLanguageForJupyter.git
````
## Teste sua instalação

````bash
jupyter kernelspec list
````
Você deve ver uma lista, uma das linhas será alguma coisa assim, com os seus diretórios indicados.

````
  wolframlanguage12    /home/lbarosi/.local/share/jupyter/kernels/wolframlanguage12
````
