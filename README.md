# 天王星占星 · uranian core

汉堡学派八虚星与中点计算。从 [知几排盘](https://github.com/weihaoyang/qimen-llm-chart) 提取 TypeScript 实现、共享依赖模块与回归测试；暂未发布 npm 包。

## 运行

需要 Node.js 20 或更高版本。

```sh
npm install
npm run patch:3meta
npm test
npm run typecheck
```

运行前的补丁会修正本地依赖中的计算口径。入口位于 `src/lib/uranian/`。

## 资料与案例

[研究论文：古籍、现代模型与待核事项](https://github.com/weihaoyang/qimen-llm-chart/blob/main/docs/research/calculation-audit-paper.md)

- places the epoch and the eight trans-Neptunian bodies（`src/lib/uranian/chart.test.ts`）
- matches the independent Matrix geometry for all eight points at JD 2488069.5（`src/lib/uranian/chart.test.ts`）
- solves Cupido on its circular orbit at epoch（`src/lib/uranian/chart.test.ts`）
- keeps the earth elements usable for the geocentric step（`src/lib/uranian/chart.test.ts`）
- returns eight distinct geocentric longitudes（`src/lib/uranian/chart.test.ts`）

案例验证具体输出字段，不验证占断效果。

## 授权与来源

本仓代码按 [GPL-3.0-only](LICENSE) 发布，源自知几排盘。轨道要素移植自 [Astrolog](https://github.com/CruiserOne/Astrolog)，Copyright © 1991–2026 Walter D. Pullen，GPL-2.0-or-later；源码保留署名。 其他随仓代码及依赖许可见 `LICENSES/`。不附古籍影像，其授权另按[影像权利记录](https://github.com/weihaoyang/qimen-llm-chart/blob/main/docs/research/sources/RIGHTS.md)核查。
