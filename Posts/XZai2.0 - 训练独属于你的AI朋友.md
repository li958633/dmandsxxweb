---
title: XZai 2.0 - 训练独属于你的AI朋友
date: 2025-08-08 15:14:42
tags: ["程序","AI"]
---

1. # XZai 2.0 - 训练独属于你的AI朋友

   ## 核心升级亮点

   - **本地模型**：基于ChatterBot的增强版本地对话引擎
   - **云API支持**：集成OpenAI/DeepSeek/Kimi/Claude/Gemini五大AI服务
   - **智能路由**：根据查询内容自动选择最优响应来源
   - 历史记录：支持模糊搜索记录

   ## 关键技术栈

   ```
   graph TD
       A[前端界面] --> B[ttkbootstrap主题引擎]
       A --> C[Win32API特效集成]
       B --> D[亚克力/阴影/圆角效果]
       C --> E[系统主题检测]
       F[后端核心] --> G[多模型路由]
       G --> H[本地ChatterBot]
       G --> I[云API适配层]
       H --> J[Levenshtein语义匹配]
       I --> K[HTTP请求池]
   ```

   ## 核心功能模块

   ### 1. 智能对话系统

   - **混合响应引擎**：

     python

     ```
     def get_bot_response(self, message):
         if self.config["api_settings"]["active_model"] == "local":
             # 本地语义匹配
             similar_question = self.find_similar_question(message) 
             return self.qa_mapping.get(similar_question) or str(self.chatbot.get_response(message))
         else:
             # 云API调用
             return self.call_api_model(message)
     ```

   ### 2. 专业训练体系

   - **多格式兼容**：支持标准QA对/分类任务/阅读理解数据
   - **批量导入**：智能JSON解析与错误修复
   - **实时反馈**：训练过程可视化监控

   ### 3. 企业级功能

   - **配置中心**：API密钥管理系统
   - **数据持久化**：自动备份与版本控制
   - **跨会话管理**：对话历史检索与导出

   ## 使用规范

   ### 运行要求

   bash

   ```
   # 基础依赖
   pip install chatterbot==1.0.5 sv-ttk pywin32 ttkbootstrap requests pillow
   
   # 硬件建议
   CPU: i5及以上
   内存: 8GB+
   系统: Windows 10/11
   ```

   ### 数据安全

   1. 配置文件加密存储于`config.json`
   2. 训练数据自动备份机制
   3. API密钥内存隔离处理

   ### 开发接口

   python

   ```
   # 自定义模型接入示例
   def add_custom_model(self, model_name, config):
       self.config["api_settings"][model_name] = config
       self.save_config()
   ```

   ## 性能指标

   | 模块     | 响应时间 | 并发能力 |
   | :------- | :------- | :------- |
   | 本地引擎 | <200ms   | 10+会话  |
   | API调用  | 1-3s     | 异步队列 |
   | 历史检索 | 即时     | 万级数据 |

   ## 注意事项

   1. 云API调用需自行申请密钥
   2. 首次启动会初始化本地数据库
   3. 建议定期清理`win11_chatbot_db.sqlite3`
   4. 暗黑模式需Windows 1903+支持

**下载地址**

[XZai项目仓库](https://github.com/li958633/XZai_Customizeyourfriends)

