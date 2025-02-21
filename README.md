# Conio2-VsCode
### Este tutorial utiliza o compilador TDM-GCC 4.7.1 (x86) (Versão Modificada).

## 📦 Pré-requisitos
- ###  Instalar o Compilador
    - Baixe o arquivo `Compilador-Conio2.rar` deste repositório. 
    - Extraia o conteúdo para **C:\\**

- ### Instalar o [VsCode](https://code.visualstudio.com/)

## ⚠️ Limitações do Ambiente
- Compilação em **32 bits** por padrão.
- Versão do GCC **(4.7.1)**
> Ao finalizar a configuração, os códigos gerados utilizando o VsCode serão compilados em um compilador de versão antiga, gerando executáveis em 32 bits. Caso necessite trabalhar em um projeto que exige um compilador atualizado ou código compilado para 64 bits, será necessário ajustar o processo de compilação.

***

## 🚩 Usar apenas o compilador (Opicional).
> Com o compilador instalado é possível compilar códigos em C/C++ sem precisar utilizar uma IDE. Para compilar va até a pasta onde está seu código através de um terminal de sua preferência e execute o comando abaixo.

    "C:\Compilador-Conio2\MinGW64\bin\g++.exe" Exemplo.c -o Exemplo -I"C:\Compilador-Conio2\MinGW64\x86_64-w64-mingw32\include" -L"C:\Compilador-Conio2\MinGW64\x86_64-w64-mingw32\lib32" -static-libgcc -lconio -m32
#### A instrução acima compila um arquivo chamado Exemplo.c em um arquivo chamado Exemplo.exe
    
***

## 🔧 Configuração do VS Code
## I. Instale e configure a extensão - [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
> Essa extensão serve para definir o que o VsCode irá fazer com determinado arquivo baseado em sua extensão.
#### 1. Abra as configurações (Atalho: aperte CTRL + Virgula)
#### 2. Na caixa de texto procure pela configuração code-runner.executorMap
#### 3. Clique em editar em settings.json
> Você será direcionado para a condiguração: "code-runner.executorMap". 
#### 4. Existirão diversas siglas para extensões de arquivos diferentes, nosso interesse é em "cpp": e "c": Coloque a string a frente dessas extensões conforme segue abaixo.
> Caso queira usar conio2 apenas com arquivos .cpp coloque a instrução apenas na frente de "cpp": e vice versa.

    "code-runner.executorMap": {  

      "cpp": "cd $dir && \"C:\\Compilador-Conio2\\MinGW64\\bin\\g++.exe\" $fileName -o $fileNameWithoutExt -I\"C:\\Compilador-Conio2\\MinGW64\\x86_64-w64-mingw32\\include\" -L\"C:\\Compilador-Conio2\\MinGW64\\x86_64-w64-mingw32\\lib32\" -static-libgcc -lconio -m32 && start $fileNameWithoutExt.exe",

      "c": "cd $dir && \"C:\\Compilador-Conio2\\MinGW64\\bin\\gcc.exe\" $fileName -o $fileNameWithoutExt -I\"C:\\Compilador-Conio2\\MinGW64\\x86_64-w64-mingw32\\include\" -L\"C:\\Compilador-Conio2\\MinGW64\\x86_64-w64-mingw32\\lib32\" -static-libgcc -lconio -m32 && start $fileNameWithoutExt.exe",

    }

## II. Instalar e configurar a extensão - [C/C++ Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-extension-pack)
> A extensão servirá para as correções em tempo real do código, Intelisense.

### Compilador Padrão
> Aqui estaremos definindo que toda vez que um código em C/C++ for aberto que seja usado um compilador de nossa preferencia para corrigir o código.
#### 1. Abra as configurações (Atalho: aperte CTRL + Virgula)
#### 2. Na caixa de texto procure pela configuração C_Cpp.default.compilerPath 
#### 3. Clique em editar em settings.json
#### 4. Entre as aspas da direita coloque o caminho para o compilador gcc ou g++ conforme segue a string abaixo.
    "C_Cpp.default.compilerPath": "C:/Compilador-Conio2/MinGW64/bin/g++.exe",

***

## 🚀 Executando o Código

 ### Como executar o arquivo : 
> ⚠️ Reinicie o VS Code antes de tentar executar pela primeira vez.
#### Opção 1. Botão direitro do mouse + Run Code  
#### Opção 2. CTRL + ALT + N

#### Caso tenha sido útil para você, não se esqueça de deixar uma ☆
