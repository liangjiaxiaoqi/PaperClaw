<div align="center">
  <img src="./docs/paperclaw-mark.svg" alt="PaperClaw 论文雷达标志" width="132" />

  <h1>PaperClaw</h1>

  <p><strong>面向 VLM/VLA、USV、多模态视觉与 EEG/BCI 的个人论文雷达</strong></p>
  <p>四个核心方向＋拓展阅读 · 交叉标签 · 每日论文卡片</p>

  <p>
    <a href="https://liangjiaxiaoqi.github.io/PaperClaw/"><img src="https://img.shields.io/badge/研究门户-在线访问-0D6B66?style=flat-square" alt="研究门户" /></a>
    <a href="https://github.com/liangjiaxiaoqi/PaperClaw/issues"><img src="https://img.shields.io/badge/论文卡片-GitHub_Issues-24292F?style=flat-square&logo=github" alt="论文卡片" /></a>
    <img src="https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python 3.10+" />
    <a href="https://github.com/liangjiaxiaoqi/PaperClaw/actions/workflows/rs-pipeline-schedule-reset.yml"><img src="https://github.com/liangjiaxiaoqi/PaperClaw/actions/workflows/rs-pipeline-schedule-reset.yml/badge.svg" alt="定时流水线" /></a>
  </p>

  <p><a href="https://liangjiaxiaoqi.github.io/PaperClaw/">网页</a> · <a href="./daily_reports/">日报</a> · <a href="https://github.com/liangjiaxiaoqi/PaperClaw/issues">论文库</a> · <a href="./skills/rs-paper-pipeline/CUSTOMIZATION_GUIDE.md">定制说明</a></p>
</div>

---

> 每天追踪值得读的新论文，把零散论文整理成可检索、可回看的研究线索。  
> 核心目标不是收集尽可能多的论文，而是减少噪声，保留与当前研究项目真正相关的工作。

## 研究雷达

本仓库面向四个核心方向，允许论文拥有多个方向标签；另设“拓展阅读”展示相邻方法。所有方向都由标题、摘要和日报概括中的明确证据生成，关键词命中本身不代表论文质量。

### 1. VLM 与 VLA

关注视觉语言模型、视觉语言动作模型、具身智能，以及机器人从感知到动作的完整链路。

| 子方向 | 代表关键词 |
|---|---|
| VLA 动作生成范式 | discrete action token · flow matching VLA · diffusion policy · world model |
| VLM/VLA 架构与高效适配 | end-to-end VLA · hierarchical VLA · parameter-efficient · visual token pruning |
| 跨本体与泛化 | cross-embodiment · sim-to-real · zero-shot manipulation · generalization |

优先保留与机器人操作、具身决策、动作生成或可迁移 VLA 方法有明确关系的论文。纯 OCR、图表问答、文档理解或图像描述工作，如果没有方法迁移价值，通常不纳入每日雷达。

### 2. 无人水面艇（USV）

关注 USV/ASV 的自主感知、环境理解、导航和控制。

| 子方向 | 代表关键词 |
|---|---|
| USV 感知与环境理解 | maritime object detection · water surface segmentation · USV visual perception |
| USV 导航与路径规划 | USV path planning · collision avoidance · maritime navigation |
| USV 控制与多艇协同 | USV control · multi-USV cooperation · swarm · formation |
| 自动驾驶技术跨界迁移 | BEV perception · end-to-end driving · autonomous driving adaptation |

自动驾驶、BEV 和端到端驾驶方法只有在摘要中能看出可迁移到 USV 时才进入核心方向，否则放入拓展阅读或排除。

### 3. 多模态视觉感知

关注多模态融合、跨模态表征，以及显著目标和伪装目标感知。

| 子方向 | 代表关键词 |
|---|---|
| 显著目标检测（SOD） | salient object detection · saliency detection · multimodal saliency |
| 伪装目标检测（COD） | camouflaged object detection · concealed object detection · RGB-D/RGB-T COD |
| 融合与跨模态表征 | multimodal fusion · cross-modal learning · sensor fusion |
| 对齐与非对齐建模 | alignment · unaligned · asynchronous · registration |
| 缺失模态与鲁棒学习 | missing modality · modality completion · robust fusion |
| 多模态检测、分割与跟踪 | multimodal detection · multimodal segmentation · multimodal tracking |

论文必须包含明确的视觉任务、视觉模态或可迁移的视觉方法贡献，不能只使用“multimodal”措辞。

### 4. 脑电信号（EEG）

关注 EEG/BCI 的解码、表征学习和多模态融合。

| 子方向 | 代表关键词 |
|---|---|
| EEG 信号解码与表征学习 | EEG decoding · representation learning · self-supervised EEG |
| 脑机接口应用 | motor imagery · SSVEP · EEG emotion recognition |
| EEG 与多模态融合 | EEG-fMRI · EEG-visual fusion · multimodal EEG |

优先保留具有明确信号处理、表征学习或解码方法的工作。纯临床观察、数据采集或硬件设计，如果没有可迁移方法贡献，通常不进入每日雷达。

### 5. 拓展阅读

与核心方向相关性较弱，但在方法、实验协议或应用上具有借鉴价值的论文。

重点关注：

- 强化学习与模仿学习
- 基础模型与大语言模型的可迁移方法
- 域泛化、域适应与鲁棒学习
- 与 VLA/USV 相关的自动驾驶感知、规划和 BEV 方法

拓展阅读不是低质量论文收容区。只有能从摘要指出具体可借鉴方法时才保留。

### 交叉标签示例

| 研究内容 | 归属方向 |
|---|---|
| 面向机器人操作的端到端 VLA | VLM 与 VLA |
| USV 水面目标检测与多传感器融合 | 无人水面艇（USV）＋多模态视觉感知 |
| 可迁移到 USV 的 BEV 感知方法 | 无人水面艇（USV）＋拓展阅读 |
| EEG 与视觉刺激联合表征学习 | 脑电信号（EEG）＋多模态视觉感知 |

## 项目做什么

每天自动完成以下流程：

1. 从 arXiv 和其他元数据来源抓取候选论文
2. 使用标题、摘要和关键词进行硬过滤
3. 调用 LLM 进行研究方向精筛
4. 检查刊会准入、日期和重复记录
5. 下载论文并生成前三页预览图
6. 生成摘要翻译、标签、TL;DR 和 10 问分析
7. 为每篇入选论文创建 GitHub Issue
8. 生成当天日报 Issue
9. 将日报同步到 Markdown 归档
10. 构建并发布 GitHub Pages 网站

## 在线入口

- 研究门户：https://liangjiaxiaoqi.github.io/PaperClaw/
- 论文库：https://github.com/liangjiaxiaoqi/PaperClaw/issues
- 日报归档：https://github.com/liangjiaxiaoqi/PaperClaw/tree/main/daily_reports
- Actions：https://github.com/liangjiaxiaoqi/PaperClaw/actions

## 以 Issue 为核心

- 一篇论文对应一个 Issue，便于搜索、评论和回看
- 每天生成一个日报 Issue，记录当天检索和入选情况
- Issue、Markdown 和网站数据保持同步
- 已收录论文不会重复创建，后续只在必要时刷新

## 快速开始

### 1. Fork 或克隆仓库

~~~bash
git clone https://github.com/liangjiaxiaoqi/PaperClaw.git
cd PaperClaw
~~~

### 2. 配置 GitHub Actions

在仓库页面进入：

~~~text
Settings → Secrets and variables → Actions
~~~

#### Secrets

必需：

~~~text
LLM_API_KEY
~~~

可选：

~~~text
OPENALEX_API_KEY
SEMANTIC_SCHOLAR_API_KEY
IEEE_API_KEY
ELSEVIER_API_KEY
SPRINGER_NATURE_API_KEY
DINGTALK_WEBHOOK
~~~

#### Variables

~~~text
RS_GITHUB_REPO=liangjiaxiaoqi/PaperClaw
LLM_MODEL=你的模型名
LLM_API_URL=你的 OpenAI-compatible Chat Completions 地址
~~~

GitHub Actions 会自动提供 <code>GITHUB_TOKEN</code>，不需要把它保存为 Actions Secret。

如果暂时只使用 arXiv，可以把工作流中的：

~~~yaml
RS_MULTISOURCE_ENABLED: "true"
~~~

改为：

~~~yaml
RS_MULTISOURCE_ENABLED: "false"
~~~

确认流程稳定后，再开启其他论文来源。

### 3. 启用 GitHub Pages

进入：

~~~text
Settings → Pages
~~~

将 Source 设置为：

~~~text
GitHub Actions
~~~

### 4. 先手动运行

进入：

https://github.com/liangjiaxiaoqi/PaperClaw/actions/workflows/rs-pipeline-manual.yml

点击 **Run workflow**，填写：

~~~text
Command to run: run_no_notify
Optional target date: YYYYMMDD
arXiv IDs: 留空
Force replay: 不勾选
~~~

推荐先运行：

~~~text
command: doctor
~~~

再选择一个有论文的日期运行：

~~~text
command: run_no_notify
date: 20261022
~~~

运行结束后检查：

- Issues 中是否出现单篇论文卡片
- Issues 中是否出现“日报 YYYYMMDD”
- <code>daily_reports/YYYYMM/YYYYMMDD.md</code> 是否生成
- GitHub Pages 是否更新

## 本地运行

### Windows PowerShell

~~~powershell
git clone https://github.com/liangjiaxiaoqi/PaperClaw.git
cd PaperClaw\\skills\\rs-paper-pipeline
.\\bootstrap.ps1
notepad .env
~~~

本地 <code>.env</code> 至少填写：

~~~dotenv
GITHUB_TOKEN=你的个人访问令牌
LLM_API_KEY=你的模型密钥
RS_GITHUB_REPO=liangjiaxiaoqi/PaperClaw
LLM_MODEL=你的模型名
LLM_API_URL=你的接口地址
~~~

本地运行时，<code>GITHUB_TOKEN</code> 需要目标仓库的 Contents 和 Issues 写权限。

Windows 还需要安装 Poppler，并保证以下命令可用：

~~~text
pdftoppm
pdftotext
~~~

### Linux / macOS

~~~bash
git clone https://github.com/liangjiaxiaoqi/PaperClaw.git
cd PaperClaw/skills/rs-paper-pipeline
./bootstrap.sh
cp .env.example .env
~~~

安装 Poppler：

~~~bash
# Ubuntu / Debian
sudo apt-get install -y poppler-utils

# macOS
brew install poppler
~~~

### 常用命令

~~~bash
cd skills/rs-paper-pipeline

python3 scripts/cli.py doctor
python3 scripts/cli.py filter --dry-run --date YYYYMMDD
python3 scripts/cli.py run --date YYYYMMDD --no-notify
python3 scripts/cli.py reconcile --date YYYYMMDD --dry-run
~~~

## 筛选与更新时间

### 手动运行

<code>date</code> 只接受单个日期：

~~~text
20261022
~~~

日期留空时：

- 工作日检索前一天
- 周六、周日补扫最近 7 天

目前不支持在 Actions 表单中填写任意起止日期区间。需要多天时，可以逐日运行，或扩展工作流增加 lookback 参数。

### 定时运行

定时工作流默认在 fork 中被 GitHub 禁用。运行稳定后，可以启用：

~~~text
Actions → PaperClaw Scheduled Pipeline → Enable workflow
~~~

启用后的默认策略：

- 北京时间周一至周五 13:17：检索前一天
- 北京时间周一至周五 22:17：再次检索前一天
- 北京时间周日 13:17：补扫最近 7 天

GitHub Actions 的 cron 可能有几分钟延迟。工作日第二轮会复用已有结果，只补充新出现的论文。

自动定时流程默认不发送钉钉或飞书通知；需要通知时，可使用手动命令：

~~~text
command: run_notify
~~~

## 配置说明

| 文件 | 作用 |
|---|---|
| <code>skills/rs-paper-pipeline/scripts/config/filter_keywords.json</code> | 查询词、硬过滤正则、排除规则和 AI 信号 |
| <code>skills/rs-paper-pipeline/scripts/prompts/filter_cross_prompt.md</code> | LLM 论文精筛标准 |
| <code>skills/rs-paper-pipeline/scripts/config/research_taxonomy.json</code> | 网页方向、子方向和分类规则 |
| <code>skills/rs-paper-pipeline/scripts/config/venue_policy.json</code> | 期刊和会议准入白名单 |
| <code>skills/rs-paper-pipeline/scripts/prompts/summarize_prompt.md</code> | 单篇论文 10 问分析 |
| <code>skills/rs-paper-pipeline/scripts/prompts/translate_prompt.md</code> | 摘要翻译 |
| <code>skills/rs-paper-pipeline/scripts/prompts/tags_prompt.md</code> | 标签提取 |

修改研究方向时，建议同时检查：

1. <code>filter_keywords.json</code>
2. <code>filter_cross_prompt.md</code>
3. <code>research_taxonomy.json</code>
4. <code>venue_policy.json</code>

只改关键词而不改 Prompt 或分类，容易出现抓取、筛选和网页展示不一致。

## 论文来源

当前代码支持以下来源：

- arXiv
- OpenAlex
- Crossref
- Semantic Scholar
- Springer Nature
- IEEE Xplore
- Elsevier Scopus

每个来源独立降级。未配置密钥的来源会被标记为未参与检索，不会阻断其他来源。Semantic Scholar 会限制请求频率；Elsevier 使用 Scopus 元数据接口。

## 产出说明

### 单篇论文 Issue

包含：

- 标题、作者、单位、日期
- arXiv / DOI 链接
- 来源和出版物
- 开源代码链接
- 中文摘要
- TL;DR
- 标签
- 论文前三页预览
- 10 问深度分析

### 日报

包含：

- 当日候选数量
- 各来源运行状态
- 刊会准入和 LLM 筛选统计
- 最终入选论文列表
- 运行时间和异常说明
- 零结果时的心跳日报

## 项目结构

~~~text
PaperClaw/
├── .github/workflows/             # 定时检索、手动运行、Pages 发布
├── daily_reports/                 # 每日 Markdown 日报
├── papers/
│   ├── issue_index.json           # 论文 ID 到 Issue 编号的索引
│   └── previews/                  # 论文预览图
├── scripts/
│   └── build_pages_site.py        # 从日报构建静态网站
├── site/                          # GitHub Pages 前端
├── skills/rs-paper-pipeline/      # 检索、筛选、分析和发布流水线
│   ├── scripts/clients/           # arXiv、GitHub、LLM、通知客户端
│   ├── scripts/services/          # 筛选、分析、日报和分类服务
│   ├── scripts/config/            # 关键词、分类和刊会白名单
│   ├── scripts/prompts/           # LLM Prompt
│   └── scripts/cli.py             # 统一命令行入口
└── README.md
~~~

## Fork 后首次清理

从上游 fork 时，仓库会复制历史日报、论文预览图和 Issue 索引，但这些历史数据不属于你的论文库。

建议首次使用时：

1. 将 <code>papers/issue_index.json</code> 重置为 <code>{}</code>
2. 删除继承的 <code>daily_reports/</code> 历史文件，保留 <code>README.md</code>
3. 删除继承的 <code>papers/previews/</code>
4. 确认 <code>scripts/build_pages_site.py</code> 的 <code>REPO_URL</code> 指向当前仓库
5. 确认 <code>site/index.html</code> 中的 GitHub 链接指向当前仓库
6. 重新运行 PaperClaw Pages

否则网站会继续显示上游历史论文，论文链接也可能跳转到原仓库。

## 已知限制

- GitHub Contents API 对单文件读取存在约 1 MB 限制。Issue 索引超过限制时，需要改用 Git Data API。
- 每篇论文会保存前三页预览图，长期运行需要定期清理或改用对象存储。
- GitHub Actions 定时任务不能保证精确到分钟。
- 外部论文来源可能限流、维护或要求机构授权。
- LLM 筛选和论文分析会产生 API 成本，建议先限制每日入选数量。

## 维护建议

- 先运行 <code>doctor</code>，再运行 <code>filter --dry-run</code>
- 先用单日测试，再启用定时任务
- 每周抽查误选和漏选，持续调整关键词与 Prompt
- 优先提高精筛质量，不要单纯扩大检索词
- 及时清理失败运行和无效 Issue 索引

## 相关项目

- thinson/RS-PaperClaw：https://github.com/thinson/RS-PaperClaw
- zitalk/PaperClaw：https://github.com/zitalk/PaperClaw
- papers.cool：https://papers.cool/

## 致谢

本项目的 Issue 驱动论文追踪思路来源于 thinson/RS-PaperClaw，并在 zitalk/PaperClaw 的基础上继续重构，适配 VLM/VLA、USV、多模态视觉感知和 EEG/BCI 的个人研究方向。

流水线代码目录中包含上游的 MIT License。使用、修改或再分发前，请同时确认上游项目和相关论文元数据来源的授权与使用条款。
