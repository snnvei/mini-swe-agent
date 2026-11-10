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
