# iTerm2 配置

## 文件说明

- `com.googlecode.iterm2.plist` - 原始 plist 配置文件
- `iterm2-config.xml` - XML 格式配置（便于版本对比）

## 如何使用

### 恢复配置

```bash
# 复制配置文件到系统目录
cp com.googlecode.iterm2.plist ~/Library/Preferences/

# 重启 iTerm2 使配置生效
```

### 导出当前配置

```bash
# 复制当前配置
cp ~/Library/Preferences/com.googlecode.iterm2.plist .

# 转换为 XML 格式（便于查看差异）
plutil -convert xml1 -o iterm2-config.xml com.googlecode.iterm2.plist
```

## 配置亮点

- AI 功能已启用 (GPT-5.2)
- 自定义配色方案：12-bit Rainbow 等
- 已优化字体渲染设置

## 同步时间

- 最后更新: 2026-03-24
