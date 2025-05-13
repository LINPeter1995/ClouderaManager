# ClouderaManager

| 工具                          | 類型      | 功能簡述   

| --------------------------- | ------- | --------------------------------------|

| **Cloudera Manager**        | 管理工具    | Hadoop 生態系的 GUI 管理後台，部署與監控  

| **Hue**                     | 使用者介面工具 | 給開發者/分析師用的 Web 介面（查詢資料、操作 Hive、Spark 等） 

| **Hadoop/Spark/Hive/Kafka** | 核心運算框架  | 真正負責資料儲存、運算、串流、查詢等工作                    

Cloudera Manager定義：

Cloudera Manager 是一個 Web 介面管理平台，用來 管理整個 Hadoop 叢集的部署、設定、監控與資源分配。

可以做的事：

安裝 Hadoop、Hive、Spark、Kafka 等套件

設定服務（像是 Hive Server2、HDFS 節點等）

監控 CPU/記憶體/磁碟使用率

重啟或調整各個服務

管理使用者權限、資源池（YARN）

和誰有關？

它是 Cloudera 提供的整套「企業級 Hadoop 套件」的一部分，專門讓你管理：

Hadoop (HDFS、MapReduce、YARN)

Hive

Impala

Spark

Kafka

HBase

等等...

---------------------------------------------------------------------------------------------------------------------------------------------------------------

Hue 定義：

Hue（Hadoop User Experience）是一個 Web 介面，提供 圖形化的 SQL 編輯器與資料操作工具，讓你可以不用打指令，就查詢 Hadoop 資料。

可以做的事：

查詢 Hive、Impala、Spark SQL 資料（類似 SQL 開發介面）

瀏覽 HDFS 中的檔案

操作 Kafka Topics（用額外 Plugin）

提交 Spark Job、建立視覺化 Dashboard

幫助他們快速：查資料、看結果、建報表

          [使用者]
              ↓
          ┌───────┐
          │  Hue  │ ←—— 使用者操作 Web GUI 查資料
          └──┬────┘
             ↓
        [Hive / Spark SQL] ←—— 真正查詢執行層
             ↓
        [HDFS / Kafka] ←—— 資料來源（儲存 or 串流）

管理整個系統 ——→ [Cloudera Manager]
                     ↑
         安裝/配置/監控 Hive、Spark、Kafka 等

| 名稱                          | 誰用？       | 做什麼？           

| **Cloudera Manager**          | 系統管理員     | 部署、設定、監控所有大數據服務 

| **Hue**                       | 分析師 / 開發者 | 查詢資料、寫 SQL、看結果  

| **Hadoop/Hive/Spark/Kafka**   | 系統本體      | 實際執行資料儲存與運算任務   

如果你在用的 Docker 映像（像 semicolon1709/cdh5.13.0:v1.0）有啟動好 Cloudera Manager 和 Hue，那你就可以：

用 Cloudera Manager 看你的 Hive、Spark 有沒有啟動成功

用 Hue 在網頁上寫 SQL 查 Hive 中的資料


