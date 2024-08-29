# Conio2-VsCode
### Será necessário utilizar o compilador TDM-GCC 4.7.1 (x86) (Versão Modificada).
### Compilador incluído com os arquivos do Dev-C++(Fornecido pela faculdade) + Configuração do Conio2. Caso queira desinstalar o Dev-C++ retire o compilador de dentro dos arquivos para utilizar na compilação.
### Compilador incluído neste repositório. O compilador incluso já contém a biblioteca Conio2 inserida e configurada. Será necessário alterar os caminhos fornecidos ao longo do tutorial baseado em onde o arquivo for colocado no seu PC.

*** 

## I. Instalar e configurar a extensão - Code Runner <a href="https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner"><img src = "https://github.com/mateus-sm/Images/blob/main/CodeRunner.png"></a>
```bash
A extensão servirá para definir como o VsCode irá executar o código em questão, nesse caso será configurado para arquivos .cpp
```
#### 1. Instale a extensão.
#### 2. Configurações da extensão -> Executor Map(Editar em Json).
![Config](https://github.com/mateus-sm/Images/blob/main/Config.png)
#### 3. Substitua a instrução ["cpp": " ..... ",] da extensão pela instrução abaixo, Substitua (...) de acordo com o caminho da sua máquina.

    "code-runner.executorMap": {  

      "cpp": "cd $dir && g++ $fileName -o $fileNameWithoutExt -I\"C:\\ ... \\Dev-Cpp\\MinGW64\\x86_64-w64-mingw32\\include\" -L\"C:\\ ... \\Dev-Cpp\\MinGW64\\x86_64-w64-mingw32\\lib32\" -static-libgcc -lconio -m32 && start $fileNameWithoutExt.exe",  

    }

***
 
## II. Configurar o PATH
```bash
É necessário que o compilador seja adicionado a variavel de ambiente, caso já exista outro é necessária remoção.
O vscode irá chamar o compilador g++ então é necessário que ele esteja no PATH.
```
#### 1. Acesse e edite o PATH ([Tutorial](https://www.youtube.com/watch?v=ing2pLCrvxo)).
#### 2. Adicione os caminhos abaixo, Substitua (...) de acordo com o caminho da sua máquina.

    C:\ ... \Dev-Cpp\MinGW64\bin
    C:\ ... \Dev-Cpp\MinGW64\x86_64-w64-mingw32\bin

#### Para testar abra o cmd e digite: "g++ --version" e verifique se obtem o retorno: "g++ (tdm64-1) 4.7.1"
![CMD](https://github.com/mateus-sm/Images/blob/main/cmd.png)

***

## III. Instalar e configurar a extensão - C/C++ Extension Pack <a href="https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-extension-pack"><img src = "https://github.com/mateus-sm/Images/blob/main/C-C%2B%2B.png" width = "70"></a>
```bash
A extensão servirá para as correções em tempo real do código, Intelisense.
```  
#### 1. Abra uma pasta(não abra apenas o arquivo) que contenha um código que importa o conio2.h (#include <conio2.h>).
#### 2. A linha do include provavelmente estará sublinhada em vermelho, clique nessa linha e logo após na lampada a esquerda.
![Imagem Demonstração](https://github.com/mateus-sm/Images/blob/main/IncludePath.png) 
#### 3. Clique em "Editar a configuração de IncludePath".
![Imagem Demonstração](https://github.com/mateus-sm/Images/blob/main/IncludePath2.png)
#### 4. Substitua "Caminho do compilador" por um dos caminhos abaixo, Substitua (...) de acordo com o caminho da sua máquina.

    C:\ ... \Dev-Cpp\MinGW64\bin\gcc.exe 
    C:\ ... \Dev-Cpp\MinGW64\bin\g++.exe 
    
 #### 5. Em "Modo do IntelliSense" coloque ${default}.
 #### 6. Em "Incluir caminho" apague todo o conteúdo.
 
 ## Reinicie o VsCode.
 
