# kanata.kbd 说明

这是 Kanata 的键盘映射配置文件，主要用来通过 `CapsLock` 组合键实现高效的导航和编辑操作，常用于提升编码及文本处理效率。下面对常用映射和层进行简要说明：

## 快速说明

- **默认层（Layer 1）：**
  - 按住 `CapsLock`（作为功能键），可进入导航层。
  - `CapsLock + 1`：切换到 Layer 1（默认层）
  - `CapsLock + ikjl`：方向键（上/下/左/右）
  - `CapsLock + df`：Home / End
  - `CapsLock + h;`：Page Up / Page Down
  - `CapsLock + uo`：按单词移动（左/右）
  - `CapsLock + space`：选中整行
  - `CapsLock + y`：退格（Backspace）
  - `CapsLock + m`：截图（PrintScreen）

- **切换层（Layer 2）：**
  - `CapsLock + 2`：切换到 Layer 2
  - Layer 2 的映射类似，但可重新定义方向和编辑键以适应不同需求。

- **技术细节（defalias/deflayer）**
  - `defalias` 定义快捷命令和组合操作，如 `lword`（Ctrl+Left）、`rword`（Ctrl+Right）、`prtsc`（PrintScreen）。
  - `deflayer` 定义每一层的按键布局和导航行为。
  - `nav1`、`nav2` 代表按住 `CapsLock` 的导航层，即临时切换到更便捷的导航/编辑按键映射。
  - `_` 代表该层该键无操作。

- **常用修改建议**
  - 你可以按需修改某一层的功能，或增添自己的快捷/宏组合，只需在相应的 `defalias` 和 `deflayer` 段落按格式书写即可。

## 启动使用

- 建议搭配 systemd 配置（参考 `kanata.service`）随系统自启动。
- 启动命令示例（实际路径需按你的安装修改）：
  ```
  /home/用户/.tools/kanata/kanata --cfg /home/用户/.tools/kanata/kanata.kbd
  ```
- 修改配置文件后，重启 `kanata` 服务即可生效。

---

更多详细语法可参考官方文档或 GitHub 项目说明。

