# Conio2-VsCode
### Este tutorial utiliza o compilador TDM-GCC 4.7.1 (x86) (Versão Modificada).

## 📦 Pré-requisitos
### 1. Instalar o Compilador
- Baixe o arquivo `Compilador-Conio2.rar` deste repositório (Compilador-Conio2.rar). 
> O compilador já contém a biblioteca Conio2 inserida e configurada. 
- Extraia o conteúdo para **C:\\**
### ⚠️ Limitações do Ambiente
- Compilação em **32 bits** por padrão
- Versão antiga do GCC (4.7.1)
> Ao finalizar a configuração, seus códigos que utilizam conio2.h serão compilados em um compilador de versão considerada antiga, gerando executáveis em 32 bits. Tenha em mente que: Se seu projeto exigir um compilador atualizado ou código compilado para 64 bits, será necessário ajustar o processo de compilação.

***

## 🔧 Configuração do VS Code
## I. Instale e configure a extensão - Code Runner <a href="https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner"><img src = "https://github.com/mateus-sm/Images/blob/main/CodeRunner.png"></a>
> Essa extensão serve para que seja definido o que você quer que o VsCode irá fazer com determinado arquivo baseado em sua extensão.
#### 1. Abra as configurações (Atalho: aperte CTRL + Virgula)
#### 2. Na caixa de texto procure pela configuração code-runner.executorMap
#### 3. Clique em editar em settings.json
> Você será direcionado para a condiguração: "code-runner.executorMap". 
#### 4. Existirão diversas siglas para extensões de arquivos diferentes, nosso interesse é em "cpp": e "c": Coloque a string a frente dessas extensões conforme segue abaixo.
> Caso queira usar conio2 apenas com arquivos .cpp coloque a instrução apenas na frente de "cpp": e vice versa.

    "code-runner.executorMap": {  

      "cpp": "cd $dir && \"C:\\Compilador-Conio2\\MinGW64\\bin\\g++.exe\" $fileName -o $fileNameWithoutExt -I\"C:\\Compilador-Conio2\\MinGW64\\x86_64-w64-mingw32\\include\" -L\"C:\\Compilador-Conio2\\MinGW64\\x86_64-w64-mingw32\\lib32\" -static-libgcc -lconio -m32 && start $fileNameWithoutExt.exe",

      "c": "cd $dir && \"C:\\Compilador-Conio2\\MinGW64\\bin\\g++.exe\" $fileName -o $fileNameWithoutExt -I\"C:\\Compilador-Conio2\\MinGW64\\x86_64-w64-mingw32\\include\" -L\"C:\\Compilador-Conio2\\MinGW64\\x86_64-w64-mingw32\\lib32\" -static-libgcc -lconio -m32 && start $fileNameWithoutExt.exe",

    }

## 🚀 Executando o Código
## II. Instalar e configurar a extensão - C/C++ Extension Pack <a href="https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-extension-pack"><img src = "https://github.com/mateus-sm/Images/blob/main/C-C%20%20.png" width = "70"></a>
> A extensão servirá para as correções em tempo real do código, Intelisense.

## Configuração global
> Aqui estaremos definindo que toda vez que um código em C/C++ for aberto que seja usado um compilador de nossa preferencia para corrigir o código.
#### 1. Abra as configurações (Atalho: aperte CTRL + Virgula)
#### 2. Na caixa de texto procure pela configuração C_Cpp.default.compilerPath 
#### 3. Clique em editar em settings.json
#### 4. Entre as aspas coloque o caminho para o compilador gcc ou g++ incluidos na pasta do Compilador.
#### Exemplo:
    "C_Cpp.default.compilerPath": "C:/Compilador-Conio2/MinGW64/bin/g++.exe",

***

 ### Como executar o arquivo : 
#### Opção 1. Botão direitro do mouse + Run Code  
#### Opção 2. CTRL + ALT + N
 
> ⚠️ Reinicie o VS Code após as configurações.

#### Caso tenha sido útil para você, não se esqueça de deixar uma ☆
