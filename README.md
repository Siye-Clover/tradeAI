# tradeAI 项目说明文档

## 项目简介
tradeAI 是一个基于 Ant Design Pro 和 Umi 构建的企业级前端应用，主要提供贸易相关的业务功能案。

## 技术栈
| 类别         | 技术选型                                  |
|--------------|-------------------------------------------|
| 核心框架     | React 18、Umi Max（企业级前端框架）       |
| UI 组件库    | Ant Design 5、@ant-design/pro-components（Pro 组件库） |
| 状态管理     | Zustand                                   |
| 类型检查     | TypeScript 5                              |
| 网络请求     | @umijs/max/request                        |
| 样式解决方案 | antd-style、Less（默认）                  |
| 代码规范     | ESLint、Prettier、Husky、lint-staged      |
| 构建工具     | Umi 构建工具                              |
| 包管理       | pnpm                                      |

## 项目结构
| 后端（tradeAI/backend/）                                                                 | 前端（tradeAI/ui/）                                                                 |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **层级符号说明**                                                                        | **层级符号说明**                                                                     |
| ┌──：表示某级目录的第一个子项（非最后一项）                                             | ┌──：表示某级目录的第一个子项（非最后一项）                                          |
| ├─：表示某级目录的中间子项（非第一个且非最后一个）                                       | ├─：表示某级目录的中间子项（非第一个且非最后一个）                                    |
| └─：表示某级目录的最后一个子项                                                           | └─：表示某级目录的最后一个子项                                                        |
| │  ：表示父目录下仍有后续子项时的竖线连接（用于保持层级对齐）                             | │  ：表示父目录下仍有后续子项时的竖线连接（用于保持层级对齐）                          |
| **核心目录结构**                                                                        | **核心目录结构**                                                                     |
| ┌── `src/main/java/com/tradeai/` （后端主代码目录）                                     | ┌── `config/` （项目配置目录）                                                       |
| │  ├─ `controller/` （接口层：接收前端请求）                                             | │  ├─ `config.ts` （主配置文件）                                                     |
| │  │  ├─ `ToolController.java` （代码生成工具接口）                                      | │  ├─ `routes.ts` （路由配置文件）                                                   |
| │  │  ├─ `InventoryController.java` （库存管理接口）                                     | │  └─ `defaultSettings.ts` （主题等默认设置）                                        |
| │  │  └─ `MonitorController.java` （监控数据接口）                                       | ├─ `src/` （前端主代码目录）                                                        |
| │  ├─ `service/` （业务逻辑层）                                                        | │  ├─ `pages/` （页面组件目录）                                                     |
| │  │  ├─ `impl/` （业务逻辑实现类目录）                                                 | │  │  ├─ `Tool/Gen/` （代码生成工具：核心模块）                                       |
| │  │  ├─ `ToolService.java` （代码生成业务逻辑）                                        | │  │  ├─ `Tool/Swagger/` （Swagger API文档查看）                                     |
| │  │  └─ `InventoryService.java` （库存业务逻辑）                                       | │  │  └─ `Monitor/Cache/` （缓存监控页面）                                           |
| │  ├─ `mapper/` （数据访问层：与数据库交互）                                            | │  ├─ `services/` （接口服务目录）                                                  |
| │  ├─ `model/` （数据模型目录：实体类、DTO、VO）                                         | │  │  ├─ `yw/` （业务相关接口：如库存管理）                                           |
| │  │  ├─ `entity/` （数据库实体类目录）                                                 | │  │  ├─ `ant-design-pro/` （基础功能接口）                                          |
| │  │  └─ `dto/` （前后端数据传输对象目录）                                               | │  │  └─ `swagger/` （Swagger相关接口）                                              |
| │  ├─ `config/` （配置类目录：数据库、Swagger等）                                        | │  ├─ `components/` （公共组件目录）                                                |
| │  ├─ `util/` （工具类目录：加密、日期处理等）                                           | │  ├─ `utils/` （工具函数目录：树形结构处理、下载工具等）                             |
| │  └─ `TradeAiApplication.java` （应用入口类）                                          | │  ├─ `access.ts` （权限配置文件）                                                   |
| ├─ `src/main/resources/` （资源配置目录）                                                | │  └─ `app.tsx` （应用入口配置文件）                                                 |
| │  ├─ `application.yml` （主配置文件：数据库连接、端口等）                               | ├─ `package.json` （项目依赖及脚本配置）                                             |
| │  ├─ `application-dev.yml` （开发环境配置文件）                                        | └─ `.gitignore` （Git忽略配置文件）                                                  |
| │  └─ `mapper/` （MyBatis映射文件目录：XML）                                             |                                                                                      |
| ├─ `src/test/` （单元测试目录）                                                         |                                                                                      |
| └─ `pom.xml` （Maven依赖配置文件）                                                     |                                                                                      |
