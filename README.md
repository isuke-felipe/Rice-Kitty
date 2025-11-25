# 🎨 Customize seu Terminal Linux

Um guia completo para transformar seu terminal em uma experiência visual moderna e produtiva.

---

## 🖼️ Galeria de Personalizações

Veja como seu terminal ficará após a configuração:

### Kitty Terminal
![Kitty Rice](https://github.com/isuke-felipe/Rice-Kitty/blob/1fb99f0298544ff86ce5f4fb49345fb3a70f22c7/kitty-sample.png)
*Terminal Kitty com tema personalizado, Oh My Posh e FastFetch*

### Ghostty Terminal
![Ghostty Rice](https://github.com/isuke-felipe/Rice-Kitty/blob/1fb99f0298544ff86ce5f4fb49345fb3a70f22c7/ghostty-sample.png)
*Terminal Ghostty com configuração moderna*

### Konsole Terminal
![Konsole Terminal](https://github.com/isuke-felipe/Rice-Kitty/blob/1fb99f0298544ff86ce5f4fb49345fb3a70f22c7/konsole-sample.png)
*Terminal Ghostty com configuração moderna*

### FastFetch em Ação
![FastFetch Demo](https://raw.githubusercontent.com/isuke-felipe/Rice-Kitty/main/screenshots/fastfetch-demo.png)
*Informações do sistema com logo personalizada*

### Oh My Posh - Variações de Temas
![Oh My Posh Themes](https://raw.githubusercontent.com/isuke-felipe/Rice-Kitty/main/screenshots/ohmyposh-themes.png)
*Diferentes temas disponíveis para personalização*

> **📌 Nota:** As capturas de tela mostram o resultado final. Seus resultados podem variar dependendo da fonte e tema do sistema.

---

## 📋 Índice

- [Pré-requisitos](#-pré-requisitos)
- [Instalação Rápida](#-instalação-rápida)
- [Configuração Detalhada](#️-configuração-detalhada)
- [Personalização](#-personalização)
- [Solução de Problemas](#-solução-de-problemas)
- [Contribuindo](#-contribuindo)

---

## 💻 Pré-requisitos

Antes de começar, certifique-se de ter:

- **Sistema Operacional:** Linux (testado em Arch, Manjaro, CachyOS, Debian, Ubuntu, Mint, Pop!_OS, Fedora)
- **Gerenciador de Pacotes:** `pacman`, `apt` ou `dnf` funcionando
- **Acesso:** Permissões para instalar pacotes e editar `~/.config`
- **Terminais Compatíveis:** Ghostty, Kitty, Konsole

---

## 🚀 Instalação Rápida

### 1️⃣ Instale as Dependências Básicas

Escolha o comando de acordo com sua distribuição:

```bash
# Arch Linux / Manjaro / CachyOS
sudo pacman -S git wget unzip imagemagick

# Debian / Ubuntu / Mint / Pop!_OS
sudo apt install git wget unzip imagemagick

# Fedora / RHEL
sudo dnf install git wget unzip imagemagick
```

### 2️⃣ Instale o Terminal (escolha um)

#### Kitty Terminal
```bash
# Arch Linux / Manjaro / CachyOS
sudo pacman -S kitty

# Debian / Ubuntu / Mint / Pop!_OS
sudo apt install kitty

# Fedora / RHEL
sudo dnf install kitty
```

#### Ghostty Terminal
```bash
# Arch Linux / Manjaro / CachyOS
sudo pacman -S ghostty

# Debian / Ubuntu / Mint / Pop!_OS
sudo apt install ghostty

# Fedora / RHEL
sudo dnf install ghostty
```

### 3️⃣ Instale o FastFetch

```bash
# Arch Linux / Manjaro / CachyOS
sudo pacman -S fastfetch

# Debian / Ubuntu / Mint / Pop!_OS
sudo apt install fastfetch

# Fedora / RHEL
sudo dnf install fastfetch
```

### 4️⃣ Instale o Oh My Posh

```bash
sudo wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/posh-linux-amd64 -O /usr/local/bin/oh-my-posh
sudo chmod +x /usr/local/bin/oh-my-posh
```

---

## ⚙️ Configuração Detalhada

### 🐱 Configurando o Kitty

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

### 👻 Configurando o Ghostty

1. **Crie o diretório de configuração (se não existir):**
```bash
mkdir -p ~/.config/ghostty
```

2. **Remova a configuração anterior (se existir):**
```bash
rm -f ~/.config/ghostty/config
```

3. **Baixe a configuração personalizada:**
```bash
cd ~/.config/ghostty
wget https://raw.githubusercontent.com/isuke-felipe/Rice-Kitty/refs/heads/main/config
```

### ⚡ Configurando o FastFetch

1. **Crie o diretório e gere a configuração padrão:**
```bash
mkdir -p ~/.config/fastfetch
cd ~/.config/fastfetch
fastfetch --gen-config
```

2. **Substitua pela configuração personalizada:**
```bash
rm -f config.jsonc
wget https://raw.githubusercontent.com/isuke-felipe/Rice-Kitty/refs/heads/main/config.jsonc
wget https://raw.githubusercontent.com/isuke-felipe/Rice-Kitty/refs/heads/main/logo.png
```

3. **Personalize a logo (opcional):**
```bash
nano ~/.config/fastfetch/config.jsonc
```
> Edite o caminho da imagem `logo.png` para apontar para sua imagem personalizada.

4. **Ative o FastFetch no seu shell:**

```bash
# Para Bash
echo 'fastfetch' >> ~/.bashrc

# Para Zsh
echo 'fastfetch' >> ~/.zshrc

# Para Fish
echo 'fastfetch' >> ~/.config/fish/config.fish
```

5. **Aplique as mudanças:**
```bash
# Para Bash/Zsh
source ~/.bashrc  # ou source ~/.zshrc

# Para Fish
source ~/.config/fish/config.fish
```

### 🎨 Configurando o Oh My Posh

1. **Adicione o Oh My Posh ao PATH:**

```bash
# Para Bash
echo 'export PATH="$PATH:$HOME/.local/bin"' >> ~/.bash_profile

# Para Zsh
echo 'export PATH="$PATH:$HOME/.local/bin"' >> ~/.zshenv

# Para Fish
echo 'set -gx PATH $PATH $HOME/.local/bin' >> ~/.config/fish/config.fish
```

2. **Baixe os temas:**
```bash
mkdir -p ~/.poshthemes
cd ~/.poshthemes
wget https://github.com/isuke-felipe/Rice-Kitty/raw/main/themes.zip
unzip themes.zip
chmod u+rw *.json
rm themes.zip
```

3. **Ative o tema no seu shell:**

```bash
# Para Bash
eval "$(oh-my-posh init bash --config ~/.poshthemes/jandedobbeleer.omp.json)"

# Para Zsh
eval "$(oh-my-posh init zsh --config ~/.poshthemes/jandedobbeleer.omp.json)"

# Para Fish
echo 'oh-my-posh init fish --config ~/.poshthemes/jandedobbeleer.omp.json | source' >> ~/.config/fish/config.fish
```

4. **Recarregue o shell:**
```bash
# Bash/Zsh
exec $SHELL

# Ou simplesmente feche e reabra o terminal
```

---

## 🎨 Personalização

### Trocando o Tema do Oh My Posh

1. **Explore os temas disponíveis:**
   - Acesse: https://ohmyposh.dev/docs/themes
   - Escolha seu tema favorito

2. **Edite o arquivo de configuração do seu shell:**

```bash
# Para Bash
sudo nano ~/.bashrc

# Para Zsh
sudo nano ~/.zshrc

# Para Fish
sudo nano ~/.config/fish/config.fish
```

3. **Altere a linha do oh-my-posh:**

```bash
# Sintaxe geral
eval "$(oh-my-posh init [SHELL] --config ~/.poshthemes/[NOME_DO_TEMA].omp.json)"

# Exemplo para Bash com tema "atomic"
eval "$(oh-my-posh init bash --config ~/.poshthemes/atomic.omp.json)"
```

4. **Recarregue a configuração:**
```bash
source ~/.bashrc  # ou ~/.zshrc / ~/.config/fish/config.fish
```

### Personalizando o FastFetch

Edite `~/.config/fastfetch/config.jsonc` para:
- Mudar a logo
- Adicionar/remover módulos de informação
- Alterar cores e formatação

---

## 🔧 Solução de Problemas

### FastFetch não aparece ao abrir o terminal
```bash
# Verifique se foi adicionado corretamente
cat ~/.bashrc | grep fastfetch  # ou ~/.zshrc

# Recarregue manualmente
source ~/.bashrc
```

### Oh My Posh não funciona
```bash
# Verifique se está no PATH
which oh-my-posh

# Verifique permissões
ls -l /usr/local/bin/oh-my-posh

# Reinstale se necessário
sudo chmod +x /usr/local/bin/oh-my-posh
```

### Caracteres estranhos aparecem no prompt
- Instale uma **Nerd Font** (fontes com ícones):
```bash
# Arch
sudo pacman -S ttf-nerd-fonts-symbols

# Debian/Ubuntu
sudo apt install fonts-nerd-font
```

---

## 📦 Estrutura do Projeto

```
Rice-Kitty/
├── kitty.conf          # Configuração do terminal Kitty
├── config              # Configuração do Ghostty
├── config.jsonc        # Configuração do FastFetch
├── logo.png            # Logo personalizada
├── themes.zip          # Temas do Oh My Posh
├── LICENSE             # Licença MIT
└── README.md           # Documentação
```

---

## 🤝 Contribuindo

Contribuições são sempre bem-vindas! Para contribuir:

1. 🍴 Faça um fork do projeto
2. 🌿 Crie uma branch: `git checkout -b feature/MinhaFeature`
3. 💾 Commit suas mudanças: `git commit -m 'Adiciona MinhaFeature'`
4. 📤 Push para a branch: `git push origin feature/MinhaFeature`
5. 🔃 Abra um Pull Request

### 📝 Diretrizes de Contribuição

- Mantenha a consistência com o estilo existente
- Teste suas alterações em diferentes distribuições Linux
- Documente novas features ou mudanças
- Atualize o README se necessário
- Adicione screenshots quando relevante

---

## 👥 Autor

**Felipe Iglesias**  
GitHub: [@isuke-felipe](https://github.com/isuke-felipe)

---

## ⭐ Agradecimentos

- [Kitty Terminal](https://sw.kovidgoyal.net/kitty/)
- [Ghostty Terminal](https://ghostty.org/)
- [FastFetch](https://github.com/fastfetch-cli/fastfetch)
- [Oh My Posh](https://ohmyposh.dev/)
- Comunidade [r/unixporn](https://reddit.com/r/unixporn) por inspiração

---

## 🐛 Reportando Problemas

Encontrou um bug? Tem uma sugestão?

1. Verifique se já não existe uma [issue aberta](https://github.com/isuke-felipe/Rice-Kitty/issues)
2. Crie uma nova issue incluindo:
   - ✅ Descrição clara do problema
   - 📋 Passos para reproduzir
   - 📸 Screenshots (se aplicável)
   - 💻 Informações do sistema (distro, versão do terminal, shell)

---

## 📜 Licença

Este projeto está sob a licença **GLP-3.0**. Veja o arquivo [LICENSE](https://github.com/isuke-felipe/Rice-Kitty/tree/main?tab=GPL-3.0-1-ov-file) para mais detalhes.

---

## 🌟 Gostou?

Se este projeto foi útil para você, considere dar uma ⭐ no repositório!

---

<div align="center">
Feito com ❤️ por Felipe Iglesias
</div>
