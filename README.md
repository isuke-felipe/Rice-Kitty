# Rice-Kitty
An Rice for Your Kitty

![AssemblyScript](https://img.shields.io/badge/assembly%20script-%23000000.svg?style=for-the-badge&logo=assemblyscript&logoColor=white)
![Status](https://img.shields.io/static/v1?label=STATUS&message=COMPLETO&color=green&style=for-the-badge)

> Consiste em um repositório destinado a .

## 💻 Pré-requisitos

Antes de começar, verifique se você atendeu aos seguintes requisitos:

- Você tem uma máquina `Linux`.

## 🚀 Instalando o repositorio

Para clonar o código na sua maquina Linux, basta abrir o terminal e colar o seguinte comando:

```
git clone https://github.com/isuke-felipe/Rice-Kitty.git
```

## 📫 Contribuindo para a manutenção

Para contribuir com projeto final e nos auxiliar a continuar desenvolvendo melhor, aprimorando e torna-lo mais eficientes, siga estas etapas:

1. Bifurque este repositório.
2. Crie um branch: `git checkout -b <nome_branch>`.
3. Faça suas alterações e confirme-as: `git commit -m '<mensagem_commit>'`
4. Envie para o branch original: `git push origin <nome_do_projeto> / <local>`
5. Crie a solicitação de pull.

Como alternativa, consulte a documentação do GitHub em [como criar uma solicitação pull](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).


## Comandos padrão para execução do programa no terminal

> Cada código neste repositório tem sua própria linha de comando, que deve ser executado no terminal para que compile e execute em sua máquina.

```
sudo pacman -S kitty |
sudo apt install kitty |
sudo dnf install kitty
```
Este comando é para instalar o Kitty pelo Terminal.

Abra o Kitty.

Adicione as configuraćões de fonte e transparencia.

`cd ~/.config/kitty/`

Baixe a configuracão 

`wget https://raw.githubusercontent.com/isuke-felipe/Rice-Kitty/refs/heads/main/kitty.conf`

Instale o ˋFastFetchˋ em sua distro:

```
sudo pacman -S fastfetch
sudo apt install fastfetch
sudo dnf install fastfetch
```

Após isso configure o `FastFetch`.

Vá para o seu diretório `.config`

`cd ~/.config`

Se você não ver uma pasta chamada `fastfetch `, crie uma usando este comando: 

`mkdir -p fastfetch`

Gere a configuração padrão:

`fastfetch --gen-config`

Remova o arquivo de configuração padrão: 

`rm fastfetch/config.jsonc`

Baixe minha versao de configuração customizada:

```
wget https://raw.githubusercontent.com/isuke-felipe/Rice-Kitty/refs/heads/main/config.jsonc
```

Feche seu terminal e abra-o novamente.

Abra o `config.jsonc` e edite adicione o diretório da sua `logo.png`:

`sudo nano nano ~/.config/kitty/kitty.conf`

Agora, execute o `fastfetch`.

Adicione o `FastFetch `na entrada do seu Shell.


## 🤝 Colaboradores

Agradecemos às seguintes pessoas que contribuíram para este projeto:

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/isuke-felipe" title="Autor">
        <img src="https://avatars.githubusercontent.com/u/111601155?v=4" width="100px;" alt="Foto do Felipe"/><br>
        <sub>
          <b>Felipe Iglesias</b>
    </td>
  </tr>
</table>

## 😄 Seja um dos contribuidores

Quer fazer parte desse projeto? Clique [AQUI](CONTRIBUTING.md) e leia como contribuir.

## 📝 Licença

Esse projeto está sob licença. Veja o arquivo [LICENÇA](https://github.com/isuke-felipe/Rice-Kitty/blob/18714b635e7c40013805f04fc64ad0fbb522cb09/LICENSE) para mais detalhes.

