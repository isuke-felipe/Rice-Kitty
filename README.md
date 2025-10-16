# Rice-Kitty
An Rice for Your Kitty

Instale o Kitty Terminal

sudo pacman -S kitty
sudo apt install kitty
sudo dnf install kitty

Abra o Kitty.

Adicione as configuraćões de fonte e transparencia.

cd ~/.config/kitty/

Baixe a configuraćão 

wget https://raw.githubusercontent.com/isuke-felipe/Rice-Kitty/refs/heads/main/kitty.conf

Instale o FastFetch em sua distro/

sudo pacman -S fastfetch
sudo apt install fastfetch
sudo dnf install fastfetch

Após isso configure o FastFetch.

Vá para o seu diretório .config 

cd ~/.config

Se você não vir uma pasta fastfetch , crie uma 

mkdir -p fastfetch

Gere a configuração padrão

fastfetch --gen-config

Remova o arquivo de configuração padrão 

rm fastfetch/config.jsonc

Baixe minha configuração 

wget https://raw.githubusercontent.com/isuke-felipe/Rice-Kitty/refs/heads/main/config.jsonc

Feche seu terminal e abra-o novamente.

Abra o vonfig.jsonc e edite adicione o diretório da sua logo .PNG

sudo nano nano ~/.config/kitty/kitty.conf

Agora, execute → fastfetch

Adicione o FastFetch na entrada do seu Shell

