# zsh-no-windows

Primeiro, vá na windows store e procure pro ubuntu, instale-o

Abra o powershell e com a setinha para escolher o terminal, escolha o terminal do ubuntu.

Abrindo ele, irá pedir para criar usuário e senha, crie.

Caso aconteça um erro que não te deixe criar nem usuario nem senha, abre o power shell como administrador e execute o comando: 
```powershell
wsl --install
```
Após isso, tente abrir novamente e terá sucesso,

Então conseguimos instalar o Linux no Windows, agora você irá procurar algum tutorial de como instalar oh my zsh no seu terminal, indico o video do Otávio Mirando https://www.youtube.com/watch?v=y-w-gamp4U0.

Assim que fizer os passos, você verá que tem uma coisa diferente com o video dele no seu terminal, o Ubuntu fica puchando a pasta home/usuario_criado e nós queremos usar nosso C:/Desktop,

Encontrei duas maneiras para fazer funcionar o C:/, uma seria para caso você queria usar somente o power shell para criação e a outra seria para o uso no VSCode, que eu recomendo.

Abra o VSCode e instale a extensão "WSL" com a foto do Linux,

Então caso queira usar o power shell, você irá abrir o terminal do ubuntu e usará o comando: 
```ps1
cd /mnt/c/
```
 e irá entrar no seu disco C:/, basta procurar Users e ser feliz,

Porém se quiser usar no VSCode, você abrirá o power shell e apertará Shift+Crtl+, para abrir o json de configurações no code, basta procurar por 

```json
{

    "guid": "{2c4de342-xxx-xxx-xxx-2309a097f518}",

    "hidden": false,

    "name": "Ubuntu",

    "source": "Windows.Terminal.Wsl",



},
```

e alterar a sessão desse código por:
```json
{

    "guid": "{2c4de342-xxx-xxx-xxx-2309a097f518}",

    "hidden": false,

    "name": "Ubuntu",

    "source": "Windows.Terminal.Wsl",
    
    "startingDirectory":"C:/Users/seuusuario"


},
```

Apenas troque o "seuusuario" pelo usuario da sua máquina e está tudo feito, poderá usar oh my zsh no terminal do seu VSCode
