# 数据库安全设置<a name="TOPIC_0142028541"></a>

## 帐户密码等级设置<a name="section5980155415126"></a>

华为云关系型数据库服务Console端数据库密码复杂度，请参见[购买实例](https://support.huaweicloud.com/qs-rds/zh-cn_topic_0046585334.html)中的数据库配置表格。

华为云关系型数据库对在客户端新创建的数据库用户，设置了密码安全策略：

-   口令长度至少8个字符。
-   口令至少包含大写字母、小写字母、数字和特殊字符各一个。

创建实例时，为用户提供了密码复杂度校验，由于root用户可以修改密码复杂度，安全起见，建议修改后的密码复杂度不低于华为云关系型数据库的初始化设置。

## 帐户说明<a name="section25975919145551"></a>

为了给MySQL数据库实例提供管理服务，您在创建数据库实例时，系统会自动为实例创建rdsAdmin、rdsRepl、rdsBackup和rdsMetric帐户。如果试图删掉、重命名、修改这些帐户的密码和权限，会导致出错。

