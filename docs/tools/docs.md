# iGEM Wiki 专用工具

> https://github.com/marketplace/actions/igem-wikisync

## WikiSync
- **简介**：
  - Python 包，用于自动上传 iGEM Wiki
  - 自动替换本地 URL 为 igem.org URL
  - 支持批量文件上传

#### 安装配置
```bash
pip install igem-wikisync
```

#### GitHub Actions 集成
```yaml
name: Deploy Wiki
on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: igembitsgoa/wikisync-action@v1
        with:
          team: 'your_team'
          username: ${{ secrets.IGEM_USERNAME }}
          password: ${{ secrets.IGEM_PASSWORD }}
```

#### 本地使用
```python
from igem_wikisync import WikiSync

sync = WikiSync(
    team='your_team',
    year=2024,
    build_dir='path/to/build'
)

sync.run()
```

## 链接检查工具
- **官方工具**：[External Content Checker](https://tools.igem.org/wiki/external-content-check)
  - 检查 Wiki 页面外部链接
  - 验证链接有效性
  - 确保符合 iGEM 规范

### 使用建议
1. 定期运行检查
2. 部署前完整扫描
3. 及时修复失效链接
