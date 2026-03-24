# Zsh 配置

## 文件说明

| 文件 | 说明 |
|------|------|
| `zshrc` | 主配置文件 → 复制到 `~/.zshrc` |
| `zshenv` | 环境变量 → 复制到 `~/.zshenv` |
| `zshrc.local.example` | 本地敏感信息模板 |

## 安装步骤

### 1. 安装依赖

```bash
# 安装 Oh My Zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# 安装 Powerlevel10k 主题
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

# 安装插件
git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions
git clone https://github.com/zdharma-continuum/fast-syntax-highlighting ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting
git clone https://github.com/agkozak/zsh-z ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/zsh-z

# 安装 brew 插件
brew install zsh-autosuggestions
```

### 2. 安装命令行增强工具

```bash
brew install eza bat fd ripgrep duf btop fzf lazygit tmux pngpaste
```

### 3. 复制配置文件

```bash
# 备份原有配置
[ -f ~/.zshrc ] && mv ~/.zshrc ~/.zshrc.backup
[ -f ~/.zshenv ] && mv ~/.zshenv ~/.zshenv.backup

# 复制新配置
cp zshrc ~/.zshrc
cp zshenv ~/.zshenv

# 创建本地配置（敏感信息）
cp zshrc.local.example ~/.zshrc.local
# 编辑 ~/.zshrc.local 填入你的敏感信息
```

### 4. 重新加载

```bash
source ~/.zshrc
```

## 插件列表

- **git** - Git 别名
- **zsh-z** - 智能目录跳转
- **zsh-completions** - 额外补全
- **fast-syntax-highlighting** - 语法高亮
- **colored-man-pages** - 彩色 man
- **sudo** - 双击 esc 加 sudo
- **web-search** - 命令行搜索
- **history** - 历史别名
- **extract** - 智能解压
- **copypath/copyfile** - 复制路径/文件
- **dirhistory** - 目录历史

## 快捷别名

### 文件操作
- `ls`, `ll`, `lt` - eza 增强版
- `cat` → bat
- `find` → fd
- `grep` → rg

### Git
- `gs` - git status
- `ga` - git add
- `gc` - git commit
- `gp` - git push
- `gl` - git log 图形化
- `gpp` - git pull -p

### Claude Code
- `cc` - claude
- `cdp` - claude (skip permissions)
- `pi` / `paste-image` - 粘贴剪贴板图片
- `cc-img` / `ccc` - 保存图片供 Claude 查看

### 其他
- `lg` - lazygit
- `fz` - fzf
- `reload` - 重载配置

## 同步时间

- 最后更新: 2026-03-24
