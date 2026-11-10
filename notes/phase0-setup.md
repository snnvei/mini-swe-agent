# Phase 0 环境与 Git 基线

- [x] snnvei / Jangev 双 SSH key
- [x] gh 双配置目录
- [x] fork 与 remote 布局
- [x] includeIf 身份隔离
- [x] Jangev collaborator 权限


## 测试基线

```bash
LITELLM_LOCAL_MODEL_COST_MAP=True uv run pytest -n auto -m "not slow" \
  --ignore=tests/environments/extra/test_contree.py

结果：520 passed, 29 skipped。

## 网络注意事项

- HuggingFace 不通：`-m "not slow"` 跳过数据集下载测试。
- `raw.githubusercontent.com` 不通：`LITELLM_LOCAL_MODEL_COST_MAP=True`
使用本地价格表。
- `contree-sdk` 0.5.1 与项目代码不兼容：暂时
`--ignore=tests/environments/extra/test_contree.py`。
