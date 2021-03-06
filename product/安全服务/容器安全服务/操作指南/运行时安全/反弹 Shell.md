本文档介绍反弹shell功能，以及如何查看事件列表。
## 查看事件列表
### 筛选刷新事件列表
1. 登录 [容器安全服务控制台](https://console.cloud.tencent.com/tcss)，在左侧导航中，单击【运行时安全】>【反弹 Shell】>【事件列表】，进入事件列表页面。
2. 在事件列表页面，单击搜索框，可通过“进程名称、父进程名称和父进程名称”等关键词对反弹 Shell 事件进行查询。
![](https://main.qcloudimg.com/raw/7ad1b5d6b3b8873c527fee57ffe4fc5d.png)
3. 在事件列表页面，单击操作栏右侧![](https://main.qcloudimg.com/raw/84b6cc4d2eabf9ed7fc0bea43503bb1d.png)图标，即可刷新反弹 Shell 事件列表。

### 导出事件列表
1. 登录 [容器安全服务控制台](https://console.cloud.tencent.com/tcss)，在左侧导航中，单击【运行时安全】>【反弹 Shell】>【事件列表】，进入事件列表页面。
2. 在事件列表页面，单击![](https://main.qcloudimg.com/raw/21ff3bd68750cb41c5ce662a24629cb3.png)图标勾选所需的反弹 Shell 事件后，单击![](https://main.qcloudimg.com/raw/24d375a75e4ee95c77910d101f7203dd.png)图标即可导出反弹 Shell 事件。
>?单击操作栏处![](https://main.qcloudimg.com/raw/21ff3bd68750cb41c5ce662a24629cb3.png)图标，可进行批量勾选。
>
![](https://main.qcloudimg.com/raw/3b6377fb6ae599c5a955d3a92d94c69e.png)

### 事件列表处理
1. 登录 [容器安全服务控制台](https://console.cloud.tencent.com/tcss)，在左侧导航中，单击【运行时安全】>【反弹 Shell】>【事件列表】，进入事件列表页面。
2. 在事件列表页面，可对反弹Shell 事件列表进行标记已处理、忽略和删除处理。
 - 标记已处理：单击![](https://main.qcloudimg.com/raw/21ff3bd68750cb41c5ce662a24629cb3.png)图标勾选反弹 Shell 事件后，单击【标记已处理】>【确定】，即可将选中事件标记已处理。
 >?建议您参照事件详情中的“解决方案”，人工对该事件风险进行处理，可将事件标记为已处理。
 - 忽略：单击![](https://main.qcloudimg.com/raw/21ff3bd68750cb41c5ce662a24629cb3.png)图标勾选所需的反弹 Shell 事件后，单击【忽略】>【确定】，即可将选中事件忽略。
>?仅将已选事件进行忽略，若再有相同事件发生依然会进行告警。
 - 删除：单击![](https://main.qcloudimg.com/raw/21ff3bd68750cb41c5ce662a24629cb3.png)图标勾选所需的反弹 Shell 事件后，单击【删除】>【确定】，即可将选中事件删除。
>!删除已选事件记录，控制台将不再显示，无法恢复记录，请慎重操作。

### 自定义列表管理
1. 登录 [容器安全服务控制台](https://console.cloud.tencent.com/tcss)，在左侧导航中，单击【运行时安全】>【反弹 Shell】>【事件列表】，进入事件列表页面。
2. 在事件列表页面，单击![](https://main.qcloudimg.com/raw/d42b27540eef9bf90a9e30f96b500bf3.png)图标，弹出自定义列表管理弹窗，在弹窗中可以自定义设定列表管理。
3. 在自定义列表管理弹窗，选择所需的类型后，单击【确定】，即可完成设置自定义列表管理。
![](https://main.qcloudimg.com/raw/8f1ae8d5fb7dbe9cdd231ee3975d3e6f.png)

### 列表字段说明
在 [事件列表](https://console.cloud.tencent.com/tcss/runtime/reverseShell) 页面，可查看进程名称、父进程名称和目标地址等信息。具体信息如下：
1. 进程名称
2. 父进程名称
3. 目标地址
4. 进程路径
5. 首次生成时间：该 Shell 反向连接事件首次触发告警的时间。系统默认对未处理的相同告警事件进行聚合。
6. 最近生成时间：聚合的告警事件最近触发告警的时间。可单击右侧排序按钮对列表事件按时间正序和时间反序进行排列。
7. 事件数量：聚合时间范围内该 Shell 反向连接事件触发告警的总数量。
8. 容器名称/ID
9. 镜像名称/ID
10. 状态：包括已处理、已忽略、未处理、已加白，支持按状态对列表事件进行快速筛选。
11. 操作
  - 单击查看详情按钮，右侧抽屉展示事件详细信息，包括告警事件详情、进程信息、父进程信息和事件描述。用户确认事件详情后可标记已处理、忽略或删除该事件。
  - 单击立即处理，用户可添加白名单、标记已处理、忽略或删除该告警事件。也可勾选多个告警事件批量标记、忽略或删除。若用户确认该进程属于正常行为，可将该进程添加白名单，后续再出现该进程运行，将直接放行不再告警。勾选添加白名单时，进入新增白名单页面。用户需确认满足条件（目标地址、连接进程）、确认镜像生效范围等。
