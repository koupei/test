# 恢复备份<a name="TOPIC_0142028410"></a>

## 操作场景<a name="section58860356172215"></a>

华为云关系型数据库服务支持使用已有的自动和手动备份恢复实例数据，可恢复到手动备份被创建时的状态。

账户余额大于等于0元，才可恢复到新实例。

## 操作步骤<a name="section56693485162629"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/region.png)，选择区域和项目。

    您可选择自己的专属计算集群（Dedicated Computing Cluster，简称DCC）。

3.  选择“数据库  \>  关系型数据库“，进入关系型数据库信息页面。
4.  在实例管理页面，选择目标实例，单击实例名称，进入实例的“基本信息“页签。
5.  在“备份管理”页签，选择需要恢复的备份文件，单击操作列中的“恢复”。

    根据该手动备份所在实例是否存在，进行操作：

    -   存在，继续[6](#li3991847815249)。
    -   不存在，跳过[6](#li3991847815249)，执行[7](#li5799021015249)。

6.  <a name="li3991847815249"></a>选择需要的恢复方式，单击“确定”。
    -   新实例

        跳转到“恢复到新实例”的服务选型页面，为用户重新创建一个和该备份数据相同的实例。恢复成功的新实例是一个独立的实例，与原有实例没有关联。如果需要使用只读实例，请重新创建。

        -   数据库引擎和数据库版本，与原实例相同，数据库端口默认为5432，以上参数皆不可重置。
        -   其他参数，用户需设置，请参见[购买实例](https://support.huaweicloud.com/qs-rds/zh-cn_topic_0046585384.html)。
        -   创建成功后，系统会自动执行一次全量备份。

    -   当前实例

        >![](public_sys-resources/icon-notice.gif) **注意：**   
        >恢复到当前实例会导致实例数据被覆盖，且恢复过程中实例将不可用。  

        在“实例管理”页面，可查看该实例状态为“恢复中”。无需执行[7](#li5799021015249)。

        恢复成功后，若当前实例已开启自动备份策略，系统会自动执行一次全量备份。反之则不会执行全量备份。

    -   已有实例

        >![](public_sys-resources/icon-notice.gif) **注意：**   
        >-   恢复到已有实例会导致实例数据被覆盖，且恢复过程中实例将不可用。  
        >-   请确保目标实例的存储空间不小于当前实例，否则会导致任务下发失败。  

        选择目标实例，单击“确定“。

        **图 1**  恢复到已有实例<a name="fig123128437496"></a>  
        ![](figures/恢复到已有实例.png "恢复到已有实例")

        对于开启自动备份策略的实例，恢复成功后，会执行一次全量备份。 反之则不会执行全量备份。


7.  <a name="li5799021015249"></a>恢复到新实例。

    跳转到“恢复到新数据库实例”的服务选型页面，为用户重新创建一个和该备份数据相同的实例。恢复成功的新实例是一个独立的实例，与原有实例没有关联。如果需要使用只读实例，请在新实例上重新创建。

    -   数据库引擎、数据库版本，与原实例相同，数据库端口默认为5432，以上参数皆不可重置。
    -   其他参数，用户需设置，请参见[购买实例](https://support.huaweicloud.com/qs-rds/zh-cn_topic_0046585384.html)。

    创建成功后，系统会自动执行一次全量备份。


