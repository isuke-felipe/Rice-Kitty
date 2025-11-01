# 🐱 Rice-Kitty

<div align="center">

**Uma configuração elegante e minimalista para o terminal Kitty com FastFetch**

[Instalação](#-instalação) • [Configuração](#-configuração) • [Capturas de Tela](#-capturas-de-tela) • [Contribuir](#-contribuindo)

</div>

---

## 📋 Sobre o Projeto

Rice-Kitty é uma configuração personalizada (_rice_) para o emulador de terminal **Kitty**, combinado com **FastFetch** para criar uma experiência visual atraente e funcional. Este projeto oferece:

- ✨ Transparência e efeitos visuais suaves
- 🎨 Esquema de cores cuidadosamente selecionado
- ⚡ Performance otimizada
- 🖼️ Integração com FastFetch customizado
- 🔤 Suporte a fontes personalizadas

## 🖼️ Capturas de Tela

> 💡 **Adicione aqui screenshots do seu terminal configurado!**

# Exemplo de visualização do FastFetch
![Kitty](https://github.com/isuke-felipe/Rice-Kitty/blob/d34ff82d3aaac0b57b2bd764d04f72bd7a712855/Kitty.jpg)


## 💻 Pré-requisitos

Antes de começar, certifique-se de ter:

- 🐧 Sistema operacional Linux (qualquer distribuição)
- 📦 Gerenciador de pacotes funcionando (`pacman`, `apt`, ou `dnf`)
- 🔧 Git instalado
- 📁 Acesso ao diretório `~/.config`

## 🚀 Instalação

### 1️⃣ Clone o Repositório

```bash
git clone https://github.com/isuke-felipe/Rice-Kitty.git
cd Rice-Kitty
```

### 2️⃣ Instale o Kitty

Escolha o comando de acordo com sua distribuição:

**Arch Linux / Manjaro:**
```bash
sudo pacman -S kitty
```

**Debian / Ubuntu:**
```bash
sudo apt install kitty
```

**Fedora / RHEL:**
```bash
sudo dnf install kitty
```

### 3️⃣ Instale o FastFetch

**Arch Linux / Manjaro:**
```bash
sudo pacman -S fastfetch
```

**Debian / Ubuntu:**
```bash
sudo apt install fastfetch
```

**Fedora / RHEL:**
```bash
sudo dnf install fastfetch
```

## ⚙️ Configuração

### Configurando o Kitty

1. **Navegue até o diretório de configuração:**
```bash
cd ~/.config/kitty/
```

2. **Faça backup da configuração anterior (se existir):**
```bash
mv kitty.conf kitty.conf.bak 2>/dev/null
```

3. **Baixe a configuração personalizada:**
```bash
wget https://raw.githubusercontent.com/isuke-felipe/Rice-Kitty/refs/heads/main/kitty.conf
```

### Configurando o FastFetch

1. **Acesse o diretório de configuração:**
```bash
cd ~/.config
```

2. **Crie a pasta do FastFetch (se não existir):**
```bash
mkdir -p fastfetch
```

3. **Gere a configuração padrão:**
```bash
fastfetch --gen-config
```

4. **Substitua pela configuração personalizada:**
```bash
cd fastfetch
rm config.jsonc
wget https://raw.githubusercontent.com/isuke-felipe/Rice-Kitty/refs/heads/main/config.jsonc
```

5. **Personalize a logo (opcional):**
```bash
nano ~/.config/fastfetch/config.jsonc
```
> Edite o caminho da imagem `logo.png` para o local da sua imagem personalizada.

### Ativando o FastFetch no Shell

Adicione o FastFetch ao arquivo de inicialização do seu shell:

**Para Bash (~/.bashrc):**
```bash
echo "fastfetch" >> ~/.bashrc
```

**Para Zsh (~/.zshrc):**
```bash
echo "fastfetch" >> ~/.zshrc
```

**Para Fish (~/.config/fish/config.fish):**
```bash
echo "fastfetch" >> ~/.config/fish/config.fish
```

### 🎉 Finalizando

Feche e reabra o terminal ou execute:
```bash
source ~/.bashrc  # ou ~/.zshrc, dependendo do seu shell
```

## 🎨 Personalização

### Modificando Cores e Transparência

Edite o arquivo de configuração do Kitty:
```bash
nano ~/.config/kitty/kitty.conf
```

Principais configurações:
- `background_opacity`: Ajusta a transparência (0.0 a 1.0)
- `foreground`: Cor do texto
- `background`: Cor de fundo
- `cursor`: Cor do cursor

### Alterando Informações do FastFetch

Edite o arquivo de configuração:
```bash
nano ~/.config/fastfetch/config.jsonc
```

Você pode customizar:
- Módulos exibidos
- Cores dos módulos
- Logo/imagem
- Layout das informações

## 📦 Estrutura do Projeto

```
Rice-Kitty/
├── kitty.conf          # Configuração do terminal Kitty
├── config.jsonc        # Configuração do FastFetch
├── logo.png            # Logo personalizada (opcional)
├── LICENSE             # Licença do projeto
└── README.md           # Este arquivo
```

## 🤝 Contribuindo

Contribuições são sempre bem-vindas! Para contribuir:

1. 🍴 Faça um fork do projeto
2. 🌿 Crie uma branch para sua feature (`git checkout -b feature/MinhaFeature`)
3. 💾 Commit suas mudanças (`git commit -m 'Adiciona MinhaFeature'`)
4. 📤 Push para a branch (`git push origin feature/MinhaFeature`)
5. 🔃 Abra um Pull Request

Veja nosso guia completo em [CONTRIBUTING.md](CONTRIBUTING.md)

### 📝 Diretrizes de Contribuição

- Mantenha a consistência com o estilo existente
- Teste suas alterações em diferentes distribuições Linux
- Documente novas features ou mudanças
- Atualize o README se necessário

## 👥 Autor

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/isuke-felipe" title="Autor">
        <img src="https://avatars.githubusercontent.com/u/111601155?v=4" width="100px;" alt="Foto do Felipe"/><br>
        <sub>
          <b>Felipe Iglesias</b>
        </sub>
      </a>
    </td>
  </tr>
</table>

## ⭐ Agradecimentos

- Comunidade [Kitty Terminal](https://sw.kovidgoyal.net/kitty/)
- Projeto [FastFetch](https://github.com/fastfetch-cli/fastfetch)
- Comunidade r/unixporn por inspiração

## 🐛 Reportando Problemas

Encontrou um bug? Tem uma sugestão? 

1. Verifique se já não existe uma [issue aberta](https://github.com/isuke-felipe/Rice-Kitty/issues)
2. Crie uma nova issue com:
   - Descrição clara do problema
   - Passos para reproduzir
   - Screenshots (se aplicável)
   - Informações do sistema (distro, versão do Kitty, etc.)

## 📜 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

<div align="center">

**Feito com ❤️ para a comunidade Linux**

Se este projeto te ajudou, considere dar uma ⭐!

[⬆ Voltar ao topo](#-rice-kitty)

</div>
