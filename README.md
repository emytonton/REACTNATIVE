## Configuração de Ambiente - Windows

- Documentação: https://reactnative.dev

Dependências necessárias:
- Chocolatey;
- Node.js;
- Openjdk17;
- Android Studio

### Instalando Chocolatey

- Abra o Powershell como administrador 

- Agora, execute o seguinte comando para instalar o Chocolatey:

  -Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

- Agora, feche seu powershell e abra normalmente seu CMD e teste se a instalação ocorreu corretamente executando o seguinte comando no seu cmd:

  - choco -v

### Instalando  o Node.js e o openjdk 17

- Abra novamente seu powershell como administrador e rode.

 - choco install -y nodejs-lts microsoft-openjdk17 yarn


### Conferindo se as instalações ocorreram corretamente

- Rode:
 - node -v
 - npm -v
 - java -version

Se todas apresentaram os valores das suas versões, a instalação foi um sucesso.

### Configurando a váriavel de ambiente JAVA_HOME

- Atenção: Geralmente ele fica instalado dentro do seu PC na pasta:

- C:\Program Files\Microsoft\ (E ali dentro tem a pasta do JDK)

- Copie o caminho de instalação

- Pesquise por " Editar as váriaveis de ambiente do sistema" ~

- Clique em variaveis de ambiente

- Clique em Variáveis de usuário, novo

- Nome = JAVA_HOME

- Valor = o caminho de instalação

- Repita o mesmo para Variaveis do sistema

###  Instalando Android Studio

- Acesse a página do Android Studio e clique no botão Download Android Studio.

- Vá até a pasta onde o arquivo foi salvo e execute o instalador.

- A primeira janela que deve aparecer é para escolher o que vai ser instalado. Por padrão, a opção Android Studio já vem selecionada. Selecione também a opção Android Virtual Device e clique em Next.

- Na sequência, será perguntado sobre o local de instalação do Android Studio. Pode deixar o caminho padrão e clicar em Next.

- Em seguida, será perguntado sobre a pasta no menu Iniciar. Deixe o padrão e clique em Install.

- Nessa etapa será realizada instalação. Quando terminar, clique em Next.

- Por fim, será apresentada a janela de fim da instalação. Deixe a opção Start Android Studio marcada e clique em Finish.

### Instalação da SDK. 
- A janela apresentará algumas opções, marque todas.

### Variável ambiente ANDROID_HOME
- Agora vamos voltar as variáveis ambiente do windows e vamos adicionar uma nova variável ANDROID_HOME, primeiro vamos ao Android Studio no SDK manager para pegar o caminho do SDK Manager que foi instalado.

- Siga os mesmos passos que foi para JAVA_HOME, mas com o nome ANDROID_HOME e o seu devido endereço.


## Criando um projeto

- Dentro da sua pasta raiz, rode:
 - npx @react-native-community/cli@latest init nomedoprojeto
 - troquei nomedoprojeto pelo nome do seu projeto

- E depois:
 - npm run android

- Para rodar novamente depois:
 - abra o seu android studio
 - rode seu emulador
 - na pasta do seu projeto:
   - npm run android

- Ops: se quiser rodar apenas o servidor, ou ele não abriu: npm start







