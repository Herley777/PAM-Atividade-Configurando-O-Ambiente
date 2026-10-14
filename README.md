Etapa 1 — Verificação inicial dos pré-requisitos

Objetivo: verificar se as ferramentas necessárias para o desenvolvimento mobile estavam instaladas no computador.

Procedimento realizado: foram executados os comandos node -v, npm -v, java -version e code --version no PowerShell do Windows.

Resultados obtidos: o Node.js apresentou a versão 24.22.0, o npm apresentou a versão 11.19.1, o Java apresentou a versão 21.0.9 LTS e o Visual Studio Code apresentou a versão 1.108.1.

Conclusão: todos os comandos foram reconhecidos pelo terminal e retornaram suas respectivas versões. Não foram encontrados erros nesta etapa.

Evidência: captura de tela do PowerShell com os resultados dos comandos.

------------------------------------------------------------------------------------------------------------------------


### Etapa 2 — Verificação das ferramentas do Android

**Objetivo:** verificar a disponibilidade do Android SDK e de suas ferramentas de linha de comando.

**Procedimento realizado:** foram executados os comandos `$env:ANDROID_HOME`, `adb --version` e `sdkmanager --version` no PowerShell.

**Resultados obtidos:** a variável `ANDROID_HOME` não apresentou nenhum valor. Os comandos `adb` e `sdkmanager` retornaram mensagens informando que não foram reconhecidos pelo terminal.

**Dificuldade encontrada:** as ferramentas do Android não estão acessíveis pelo PowerShell. Ainda é necessário verificar se estão instaladas e configurar as variáveis de ambiente, caso necessário.

**Evidência:** captura de tela do PowerShell mostrando os resultados e as mensagens de erro.

------------------------------------------------------------------------------------------------------------------------

### Etapa 3 — Localização do Android SDK

**Objetivo:** verificar se o Android SDK já estava presente no computador.

**Procedimento realizado:** foram utilizados os comandos `Test-Path "C:\Android\sdk"` e `Test-Path "$env:LOCALAPPDATA\Android\Sdk"` no PowerShell.

**Resultados obtidos:** o primeiro comando retornou `False`, indicando que a pasta `C:\Android\sdk` não foi encontrada. O segundo retornou `True`, confirmando a existência da pasta do SDK no diretório local do usuário.

**Conclusão:** foi identificado um possível local de instalação do Android SDK. A próxima etapa consiste em verificar se as ferramentas necessárias estão presentes nessa pasta.

**Evidência:** captura de tela do PowerShell com os resultados dos dois comandos.


------------------------------------------------------------------------------------------------------------------------


### Etapa 4 — Inspeção do Android SDK

**Objetivo:** verificar quais ferramentas do Android já estavam instaladas.

**Procedimento realizado:** foi utilizado o PowerShell para examinar as pastas do Android SDK e verificar a existência dos executáveis `adb.exe`, `emulator.exe` e `sdkmanager.bat`.

**Resultados obtidos:** foram encontradas as pastas `build-tools`, `emulator`, `platform-tools`, `platforms` e `system-images`, entre outras. O arquivo `adb.exe` foi localizado, assim como o executável do emulador. Entretanto, o arquivo `sdkmanager.bat` não foi encontrado no caminho `cmdline-tools\latest\bin`.

**Conclusão:** o computador já possui componentes importantes do Android SDK. É necessário verificar as ferramentas de linha de comando e configurar o acesso pelo terminal.

**Evidência:** captura de tela dos resultados dos comandos de verificação.




