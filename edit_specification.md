# 编写约定


## 任务树
### 文件组织
1. 任务树文件命名为`KS_{国家名}_missions.txt`。
2. 欲覆盖或更改原版任务树时，建立一个与其同名的文件。
### 命名
一棵任务树的结构如下。
```
{任务树名称} = {
    ...
    {任务名称} = {

    }
}
```
1. 任务树名称命名为`ks.{国家名}.missions.{简略描述}`，如
   ```
   ks.ottoman.missions.conquerors_of_the_near_east
   ```
2. 任务名称命名为`ks.{国家名}.mission.{简略描述}`，如
   ```
   ks.ottoman.mission.defeat_the_byzantine_empire
   ```


## 事件
### 文件组织
1. 事件文件命名为`KS_{国家名/领域}_event_{triggered/routine}.txt`。
### 命名
1. 每个事件文件必须指定`namespace`，`namespace`命名为`ks_{国家名/领域}_event_{t/r}`，如
   ```
   ks_ottoman_event_t
   ```
2. 事件编号在各`namespace`下简单递增。
3. `title`命名为`{namespace}.{事件简略描述}.title`，如
   ```
   ks_ottoman_event.conquer_rome.title
   ```
4. `desc`命名为`{namespace}.{事件简略描述}.description`，如
   ```
   ks_ottoman_event.conquer_rome.description
   ```
5. 各选项的`name`命名为`{namespace}.{事件简略描述}.option.{选项简略描述}`，如
   ```
   ks_ottoman_event.conquer_rome.option.ok
   ```

## 本地化
### 文件组织
1. 每个本地化文件对应一个源文件，为了文件按字典序排序时对应相同类型文件的本地化文件归在同一处，文件类型写在国家名或领域之前。如，`KS_events_t_ottoman_l_english.yml`对应`KS_ottoman_events_t.txt`。

## 语法结构
1. 总是在左大括号后换行，如
    ```
    trigger = {
        owns = 118
    }
    ```
2. 注释时，`#`后接一个空格。
3. 所有的游戏文件的换行符使用`LF`。