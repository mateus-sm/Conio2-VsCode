# Conio2-VsCode
### Será necessário utilizar o compilador TDM-GCC 4.7.1 (x86) (Versão Modificada).
### Obter o compilador através de um dos métodos: 
### 1. Usar o compilador incluído com os arquivos do Dev-C++ (Fornecido pela faculdade) + Configuração do Conio2. *Caso queira desinstalar o Dev, retire o compilador de dentro dos arquivos para utilizar na compilação.
### 2. Usar o compilador incluído neste repositório (MinGW64.7z). O compilador incluso já contém a biblioteca Conio2 inserida e configurada. Será necessário alterar os caminhos fornecidos ao longo do tutorial baseado em onde o arquivo for colocado no seu PC.

***

## I. Instalar e configurar a extensão - Code Runner <a href="https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner"><img src = "https://github.com/mateus-sm/Images/blob/main/CodeRunner.png"></a>
> ### A extensão servirá para definir como o VsCode irá executar o código em questão, nesse caso será configurado para arquivos .cpp
#### 1. Instale a extensão.
#### 2. Configurações da extensão -> Executor Map(Editar em Json).
![Config](https://github.com/mateus-sm/Images/blob/main/Config.png)
#### 3. Substitua a instrução ["cpp": " ..... ",] da extensão pela instrução abaixo. Substitua (...) de acordo com o caminho da sua máquina.

    "code-runner.executorMap": {  

      "cpp": "cd $dir && g++ $fileName -o $fileNameWithoutExt -I\"C:\\ ... \\Dev-Cpp\\MinGW64\\x86_64-w64-mingw32\\include\" -L\"C:\\ ... \\Dev-Cpp\\MinGW64\\x86_64-w64-mingw32\\lib32\" -static-libgcc -lconio -m32 && start $fileNameWithoutExt.exe",  

    }

#### Exemplo:
![Gif Demonstração](https://github.com/mateus-sm/Images/blob/main/Exemplo-CodeRunner.gif)  

***
 
## II. Configurar o PATH
> ### É necessário que o compilador seja adicionado a variável de ambiente. O vscode irá chamar o compilador g++ então é necessário que ele esteja no PATH.
#### 1. Acesse e edite o PATH ([Tutorial](https://www.youtube.com/watch?v=ing2pLCrvxo)).
#### 2. Adicione o caminho abaixo. Substitua (...) de acordo com o caminho da sua máquina.

    C:\ ... \Dev-Cpp\MinGW64\bin

#### Para testar, abra o cmd, digite: "g++ --version" e verifique se obtem o retorno: "g++ (tdm64-1) 4.7.1"
![CMD](https://github.com/mateus-sm/Images/blob/main/cmd.png)

### Caso queira manter outro compilador no path, basta manter abaixo do recém colocado, quando quiser usar o antigo coloque o mesmo por cima. Os caminhos são priorizados de cima para baixo.
![PATH](https://github.com/mateus-sm/Images/blob/main/path.png)

***

## III. Instalar e configurar a extensão - C/C++ Extension Pack <a href="https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-extension-pack"><img src = "https://github.com/mateus-sm/Images/blob/main/C-C%2B%2B.png" width = "70"></a>
> ### A extensão servirá para as correções em tempo real do código, Intelisense.
#### 1. Abra uma pasta(não abra apenas o arquivo) que contenha um código que importa o conio2.h (#include <conio2.h>).
> ### É necessário que seja feito em uma pasta pois, ao configurar os passos abaixo, a extensão criará uma pasta .vscode dentro da pasta que você estiver trabalhando, essa pasta irá conter as configurações que farão com que o código funcione corretamente, então, toda vez que uma pasta nova for criada que não contenha esse .vscode, será necessario seguir os passos abaixo para que ela seja criada. Desta forma recomendo que, crie uma pasta geral para todos os códigos de C (Ex: ATP2), qualquer pasta dentro desta já estará configurada (Ex: Aula1, Aula2, Aula3...).
#### 2. A linha do include provavelmente estará sublinhada em vermelho, clique nessa linha e logo após na lampada a esquerda.
![Imagem Demonstração](https://github.com/mateus-sm/Images/blob/main/IncludePath.png) 
#### *Quando quiser entrar na tela de configuração do intelisense é posível escrever um include incorreto e entrar nas configurações por meio da lampada novamente. Ex: escrever #include <xxx.h>
#### 3. Clique em "Editar a configuração de IncludePath" -> Selecione a pasta do arquivo caso o vscode pergunte.
![Imagem Demonstração](https://github.com/mateus-sm/Images/blob/main/IncludePath2.png)  
#### 3.1. Também é possível chegar nas configurações pela aba de problemas.
![Imagem Demonstração](https://github.com/mateus-sm/Images/blob/main/IncludePath3.png)  
#### 4. Substitua "Caminho do compilador" por um dos caminhos abaixo. Substitua (...) de acordo com o caminho da sua máquina.

    C:\ ... \Dev-Cpp\MinGW64\bin\gcc.exe 
    C:\ ... \Dev-Cpp\MinGW64\bin\g++.exe 
    
 #### 5. Em "Modo do IntelliSense" coloque ${default}.
 #### 6. Em "Incluir caminho" apague todo o conteúdo.

#### Exemplo:
 ![Gif Demonstração](https://github.com/mateus-sm/Images/blob/main/Exemplo-C++.gif)  

***

 ### Como executar o arquivo : 
#### Opção 1. Botão direitro do mouse + Run Code  
#### Opção 2. CTRL + ALT + N
 
 ## Reinicie o VsCode.

#### Caso tenha sido útil para você, não se esqueça de deixar uma ☆
