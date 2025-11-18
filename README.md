## Stage 1: 项目骨架与依赖
**Goal**: 初始化前后端目录，配置 Vite + Vue3、Express + Socket.IO、Node.js（后端），并建立共享类型定义。
**Success Criteria**: 
- 前后端可分别启动开发服务器
- 统一的环境变量与 .editorconfig/.eslint 配置生效
- 基础 MySQL 连接与迁移脚本可运行
**Tests**: 
- `npm run lint` (前后端)
- `npm run test:db-connection`
**Status**: Not Started

## Stage 2: 身份认证与基础接口
**Goal**: 实现用户注册、登录、JWT 鉴权中间件以及用户/机器人基础数据表。
**Success Criteria**:
- 注册/登录接口具备参数校验与错误处理
- JWT 可在 Socket.IO 握手与 REST API 中复用
- 数据库迁移生成用户、机器人、禁言等表
**Tests**:
- `npm run test:auth` 覆盖成功/失败场景
- 集成测试验证鉴权保护路由
**Status**: Not Started

## Stage 3: 实时通讯与消息持久化
**Goal**: 构建多人聊天室消息流、Socket.IO 房间逻辑、消息持久化以及 AI 管理机器人（A 类）回复。
**Success Criteria**:
- 用户可发送/接收实时消息并写入 MySQL
- A 类机器人基于本地策略回应并能触发禁言
- 消息节流/限频策略可配置
**Tests**:
- WebSocket 集成测试模拟多用户
- 单元测试校验机器人策略函数
**Status**: Not Started

## Stage 4: 后台管理与虚假机器人（B 类）
**Goal**: 提供后台面板，支持 robot_setting.json CRUD、B 类机器人定时/随机发言与禁言管理。
**Success Criteria**:
- 后台可增删改 robot_setting.json 中的配置并热加载
- 管理员可手动禁言/解禁用户
- B 类机器人可按配置发言且受全局禁言控制
**Tests**:
- 后台 API 集成测试
- 机器人调度器单元测试
**Status**: Not Started

## Stage 5: 前端界面与系统状态管理
**Goal**: 构建聊天室 UI、Pinia 状态管理、系统状态面板（禁言、限频、发言控制）以及消息监控视图。
**Success Criteria**:
- 聊天室界面显示消息列表、在线用户、机器人标签
- 后台面板可实时查看系统状态并操作
- 与 Socket.IO 客户端集成，状态变更实时生效
**Tests**:
- 端到端测试覆盖登录→聊天→后台操作流程
- 组件测试验证 Pinia store 行为
**Status**: Not Started
