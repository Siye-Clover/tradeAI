# tradeAI 项目说明文档


## 项目简介
tradeAI 是一个基于 Ant Design Pro 和 Umi 构建的企业级前端应用，主要提供贸易相关的业务功能案。


## 技术栈
- **核心框架**：React 18、Umi Max（企业级前端框架）
- **UI 组件库**：Ant Design 5、@ant-design/pro-components（Pro 组件库）
- **状态管理**：Zustand
- **类型检查**：TypeScript 5
- **网络请求**：@umijs/max/request
- **样式解决方案**：antd-style、Less（默认）
- **代码规范**：ESLint、Prettier、Husky、lint-staged
- **构建工具**：Umi 构建工具
- **包管理**：pnpm


## 项目结构
```bash
tradeAI/ui/
├── config/               # 项目配置（路由、主题、代理等）
│   ├── config.ts         # 主配置文件
│   ├── routes.ts         # 路由配置
│   └── defaultSettings.ts # 主题等默认设置
├── src/
│   ├── pages/            # 页面组件
│   │   ├── Tool/Gen/     # 代码生成工具（核心模块）
│   │   ├── Tool/Swagger/ # Swagger API文档查看
│   │   └── Monitor/Cache/ # 缓存监控
│   ├── services/         # 接口服务
│   │   ├── yw/           # 业务相关接口（如库存管理）
│   │   ├── ant-design-pro/ # 基础功能接口
│   │   └── swagger/      # Swagger相关接口
│   ├── components/       # 公共组件
│   ├── utils/            # 工具函数（如树形结构处理、下载工具）
│   ├── access.ts         # 权限配置
│   └── app.tsx           # 应用入口配置
├── package.json          # 项目依赖及脚本
└── .gitignore            # Git忽略配置

tradeAI/backend/
├── src/main/java/com/tradeai/
│   ├── controller/        # 接口层（接收前端请求）
│   │   ├── ToolController.java      # 代码生成工具接口
│   │   ├── InventoryController.java # 库存管理接口
│   │   └── MonitorController.java   # 监控数据接口
│   ├── service/           # 业务逻辑层
│   │   ├── impl/          # 业务逻辑实现类
│   │   ├── ToolService.java        # 代码生成业务逻辑
│   │   └── InventoryService.java   # 库存业务逻辑
│   ├── mapper/            # 数据访问层（与数据库交互）
│   ├── model/             # 数据模型（实体类、DTO、VO）
│   │   ├── entity/        # 数据库实体类
│   │   └── dto/           # 前后端数据传输对象
│   ├── config/            # 配置类（数据库、Swagger、安全等）
│   ├── util/              # 工具类（加密、日期处理等）
│   └── TradeAiApplication.java     # 应用入口类
├── src/main/resources/
│   ├── application.yml    # 主配置文件（数据库连接、端口等）
│   ├── application-dev.yml # 开发环境配置
│   └── mapper/            # MyBatis映射文件（XML）
├── src/test/              # 单元测试
└── pom.xml                # Maven依赖配置
