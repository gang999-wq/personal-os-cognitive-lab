# Personal OS Cognitive Lab

当前版本：**v0.6.0**

这是 Personal OS「认知功能恢复支持」板块使用的手机优先认知训练工具。它不是独立系统，也不是医疗诊断或治疗工具。

## MVP

- Reading Recall & Expression：读完文章后脱稿写 1–3 句摘要、1 句观点、1 个反问/推理点。
- Stroop：抑制控制与处理速度。
- Visual Search：视觉搜索与注意分配。
- Digit Span：短时保持与工作记忆。
- Low-dose 1-back：低剂量工作记忆更新。

每天由 Personal OS 根据状态只选择需要的训练；明显不适时允许 **0 分钟**，不补债。

## 数据与边界

- 训练记录默认只保存在当前浏览器 localStorage。
- 支持 JSON / CSV 导出、JSON 恢复与 Personal OS Markdown 摘要。
- 不把任务成绩、反应时、span 或 N-back 表现等同于医学意义上的认知恢复。
- 浏览器反应时只适合同设备、相近条件下看粗趋势。
- Reading Recall 不保存文章全文，也不做伪“AI 质量分”。

## v0.6.0

当前仓库先部署经过自动校验的 **single-file build** 作为 `index.html`，减少首轮手机验收的文件依赖。完整版源码与 PWA 资源在验收后继续补齐到本仓库。

固定外部依赖：
- jsPsych 8.3.0
- @jspsych/plugin-html-button-response 2.1.0
- @jspsych/plugin-html-keyboard-response 2.2.0
- @jspsych/plugin-survey-text 2.1.1

## iPhone 验收

1. 首页可打开；
2. 5 个任务都能进入并完成；
3. “停止本次训练”可正常退出且不保存；
4. 本地历史可保存；
5. JSON / CSV 可导出；
6. Personal OS 摘要可复制；
7. 切后台/锁屏后会记录中断提示。

代码仓库只存应用代码，不提交个人训练 JSON / CSV。
