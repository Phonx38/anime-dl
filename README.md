# anime-dl

Search and download anime from the terminal.

## Install

```bash
# Dependencies
brew install aria2
pip3 install --user --break-system-packages rich

# Install
curl -o ~/bin/anime-dl https://raw.githubusercontent.com/Phonx38/anime-dl/main/anime-dl
chmod +x ~/bin/anime-dl

# Make sure ~/bin is in your PATH
echo 'export PATH="$HOME/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

## Usage

```bash
anime-dl "attack on titan"
anime-dl "azazel"
anime-dl                     # prompts for search
```

## How it works

1. Search by name — shows results in a table
2. Pick an anime — lists all episodes with file sizes
3. Select episodes — `all`, `1-5`, `1,3,7`, or single number
4. Downloads via aria2c (16 parallel connections)

Skips already-downloaded files. Saves to `~/Downloads/<anime-name>/`.
