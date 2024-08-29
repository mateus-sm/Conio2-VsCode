# Conio2---VsCode
### Será necessário utilizar o compilador TDM-GCC 4.7.1 (x86) (Versão Modificada).
### Compilador incluso com os arquivos do Dev-C++(Fornecido pela faculdade) caso queira desinstalar o Dev-C++ retire o compilador de dentro dos arquivos para utilizar na compilação.
### Compilador incluso neste repositório.

## I. Instalar e configurar a extensão - [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
```bash
A extensão servirá para definir como o VsCode irá executar o código em questão, nesse caso será configurado para arquivos .cpp
```
#### 1. Instale a extensão.
#### 2. Configurações da extensão -> Executor Map(Editar em Json).
#### 3. Substitua a instrução "cpp" da extensão pela instrução abaixo, Substitua (...) de acordo com o caminho da sua máquina.

    "code-runner.executorMap": {  

        "cpp": "cd $dir && g++ $fileName -o $fileNameWithoutExt -I\"C:\\ ... \\Dev-Cpp\\MinGW64\\x86_64-w64-mingw32\\include\" -L\"C:\\ ... \\Dev-Cpp\\MinGW64\\x86_64-w64-mingw32\\lib32\" -static-libgcc -lconio -m32 && start $fileNameWithoutExt.exe",  

    }

***
 
## II. Configurar o PATH
```bash
É necessário que o compilador seja adicionado a variavel de ambiente, caso já exista outro é necessária remoção.
O vscode irá chamar o compilador g++ então é necessário que ele esteja no PATH.
```
#### 1. Acesse e edite o PATH.
#### 2. Adicione os caminhos abaixo, Substitua (...) de acordo com o caminho da sua máquina.

    C:\ ... \Dev-Cpp\MinGW64\bin
    C:\ ... \Dev-Cpp\MinGW64\x86_64-w64-mingw32\bin

#### Para testar abra o cmd e digite: "g++ --version" e verifique se obtem o retorno: "g++ (tdm64-1) 4.7.1"
***

## III. Instalar e configurar a extensão - [C/C++ Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-extension-pack)
```bash
A extensão servirá para as correções em tempo real do código, Intelisense.
```  
#### 1. Abra uma pasta(não abra apenas o arquivo) que contenha um código que importa o conio2.h (#include <conio2.h>).
#### 2. A linha do include provavelmente estará sublinhada em vermelho, clique nessa linha e logo após na lampada a esquerda.
#### 3. Clique em "Editar a configuração de IncludePath".
#### 4. Substitua "Caminho do compilador" por um dos caminhos abaixo, Substitua (...) de acordo com o caminho da sua máquina.

    C:\ ... \Dev-Cpp\MinGW64\bin\gcc.exe 
    C:\ ... \Dev-Cpp\MinGW64\bin\g++.exe 
    
 #### 5. Em "Modo do IntelliSense" coloque ${default}.
 #### 6. Em "Incluir caminho" apague todo o conteúdo.
 
 ## Reinicie o VsCode.
 
