# 数据字典规范

## 必读

请仔细阅读并遵循以下规则：

1. 本文档保存所有标准名词、英译和缩写
2. 适用于所有微服务接口定义、数据库定义、代码中方法名称、常量变量名称
3. 按照字母表顺序排列



## 命名规则

### 驼峰法与下划线连字符

与阿里开发规范保持一致：

* 在接口定义和代码中，均使用驼峰法命名；
* 在数据库表结构定义，均使用下划线连字符法命名；

### 区分不同客户

数据定义中将常见的客户按以下方式定义英文名词：

1. customer，特指C端的个人客户，如连锁的门店客户，电商客户
2. client，特指B端的企业客户，如批发客户
3. user，特指系统中需要登录业务系统后台的账号，如：电商客服、财务、会员运营岗位人员
4. seller，特指商户，即入驻平台的卖家

### 区分号码(No)和内码(Id)

数据定义中，用No表示<u>号码</u>，Id表示<u>内码</u>。如：
* member**No**：会员卡号
* member**Id**：会员卡内码
* order**No**：订单号
* order**Id**：订单内码
* refund**No**：退款单号
* refund**Id**：退款单内码



### 不区分单、复数

所有名词均以单数为准，不使用复数形式表述。

### 不区分动词被动时态

所有动词均已原始形态表述。

### 总数

包含总数、总量、合计等含义的字段，以amount开头。

### 时间

* 仅详细到天的用Date，作为后缀；
* 详细到天内具体时间的用Time，作为后缀；
* 所有起止时间，均用begin、end作为前缀，不使用start、stop前缀；



## 名词表

| 接口名词 | Java代码定义 | 数据库名词 | MySQL标准定义 | 含义和应用场景，应用项目，以下为示例，请删除后重新编辑，请保留Markdown格式 |
|---|---|---|---|---|
| abscentDuration |  | abscent_duration |  | 未消费时间 |
| accountAmount | String | account_amount |  | 下账金额 |
| advancedFilterName | String | advanced_filter_name |  | 高级筛选名称 |
| age |  | age |  | 年龄 |
| alipayOpenId | String | alipay_openid |  | 支付宝ID：发送支付宝消息目标用户的支付宝 openid |
| amountDedicatedMember |  | amount_dedicated_member |  | 专属会员数 |
| amountIncomingAnswer |  | amount_incoming_answer |  | 呼入接听量 |
| amountIncomingAnswerRate |  | amount_incoming_answer_rate |  | 呼入接听率 |
| amountIncomingCall |  | amount_incoming_call |  | 呼入量 |
| amountIssue |  | amount_issue |  | 发送次数 |
| amountManualTagCustomer |  | amount_manual_tag_customer |  | 人工标签人数 |
| amountMember |  | amount_member |  | 会员数 |
| amountOperator |  | amount_operator |  | 话席数 |
| amountOutgoingAnswer |  | amount_outgoing_answer |  | 呼出接听量 |
| amountOutgoingAnswerRate |  | amount_outgoing_answer_rate |  | 呼出接听率 |
| amountOutgoingCall |  | amount_outgoing_call |  | 呼出量 |
| amountOutgoingTask |  | amount_outgoing_task |  | 外呼任务量 |
| amountRedeem |  | amount_redeem |  | 已核销数 |
| amountSendCustomer |  | amount_send_customer |  | 已发人数 |
| amountSendSms |  | amount_send_sms |  | 已发条数 |
| amountSendTask |  | amount_send_task |  | 已发送任务数 |
| amountSuccessIssue |  | amount_success_issue |  | 下推成功总数 |
| amountSystemTagCustomer |  | amount_system_tag_customer |  | 系统标签人数 |
| amountTagCustomer |  | amount_tag_customer |  | 标签总人数 |
| amountTargetCustomer |  | amount_target_customer |  | 目标人数 |
| amountTask |  | amount_task |  | 目标任务数 |
| appliedGoods |  | applied_goods |  | 适用商品 |
| appliedShop |  | applied_shop |  | 适用门店 |
| associatedGoods |  | associated_goods |  | 关联商品 |
| averageDuration |  | average_duration |  | 平均通话时长 |
| averagePrice |  | average_price |  | 均摊价格 |
| bankName |  | bank_name |  | 银行 |
| beginTime |  | begin_time |  | 开始时间 |
| callDetail |  | call_detail |  | 通话明细 |
| callDuration |  | call_duration |  | 通话时间 |
| callStatus |  | call_status |  | 通话结果 |
| cardNo |  | card_no |  | 卡号 |
| cart |  | cart |  | 购物车 |
| collectionSize |  | collection_size |  | 群人数 |
| collectionSource |  | collection_source |  | 生成方式 |
| collectionTag |  | collection_tag |  | 群标签 |
| consignee |  | consignee |  | 收货人 |
| consumeAmount |  | consume_amount |  | 消费金额 |
| contact |  | contact |  | 联系人 |
| control |  | control |  | 控件，一些业务控件 如：导航、分类 |
| corporateNo |  | corporate_no |  | 企业号 |
| corporatePhone |  | corporate_phone |  | 企业号码 |
| coupon |  | coupon |  | 优惠券，商品下单时用到 |
| couponName |  | coupon_name |  | 优惠券名称 |
| couponNo |  | coupon_no |  | 优惠券编号 |
| couponPassword |  | coupon_password |  | 优惠券密码 |
| couponTaskName |  | coupon_task_name |  | 优惠券任务名称 |
| couponType |  | coupon_type |  | 券类型 |
| createTime |  | create_time |  | 创建时间 |
| creator |  | creator |  | 创建人 |
| customer |  | customer |  | 个人客户，平台对应的个人客户，个人买家 |
| customerAddr |  | customer_addr |  | 客户收货地址 |
| customerArea |  | customer_area |  | 区域：客户所属大区 |
| customerLevel |  | customer_level |  | 客户等级：相关等级配置 |
| customerName |  | customer_name |  | 客户姓名 |
| dailyUsage |  | daily_usage |  | 每日用量 |
| decimalPlace |  | decimal_place |  | 小数位数 |
| delaySend |  | delay_send |  | 延时发送 |
| deliveryType |  | delivery_type |  | 配送（方式） |
| device |  | device |  | 设备：特殊商品上的设备 |
| deviceGroup |  | device_group |  | 设备组：设备的分组 |
| deviceRelation |  | device_relation |  | 设备关联关系：主从设备 |
| discount |  | discount |  | 折扣 |
| discountPrice |  | discount_price |  | 折后价格 |
| documentCreateTime |  | document_create_time |  | 建档时间 |
| dosage |  | dosage |  | 剂型 |
| duration |  | duration |  | 时间范围 |
| effectiveDate |  | effective_date |  | 有效日期 |
| electricFence |  | electric_fence |  | 电子围栏：设备可活动的范围 |
| enabled |  | enabled |  | 启停用 |
| endTime |  | end_time |  | 结束时间 |
| enterAccount |  | enter_account |  | 下账 |
| executeMode |  | execute_mode |  | 执行方式 |
| expectArrivalTime |  | expect_arrival_time |  | 期望送达时间 |
| expressName |  | express_name |  | 物流公司 |
| expressServieRegion |  | express_service_region |  | 物流对应的配送地区 |
| fenceDevice |  | fence_device |  | 电子围栏和设备的关系 |
| filter |  | filter |  | 筛选条件 |
| filterName |  | filter_name |  | 筛选条件名称 |
| goods |  | goods |  | 商品：包括普通商品、租借商品、共享商品等； |
| goodsAttribute |  | goods_attribute |  | 商品包含的对应属性 |
| goodsCategory |  | goods_category |  | 商品分类信息 |
| goodsFirstCategory |  | goods_first_category |  | 一级分类 |
| goodsFourthCategory |  | goods_fourth_category |  | 四级分类 |
| goodsHabitat |  | goods_habitat |  | 产地 |
| goodsName |  | goods_name |  | 商品名称 |
| goodsNo |  | goods_no |  | 货号 |
| goodsPicture |  | goods_picture |  | 商品相册 |
| goodsRentAttribute |  | goods_rent_attribute |  | 商品对应的租借属性：特殊商品的属性 |
| goodsSecondCategory |  | goods_second_category |  | 二级分类 |
| goodsSpecs |  | goods_specs |  | 规格 |
| goodsSubCategory |  | goods_sub_category |  | 子类 |
| goodsTag |  | goods_tag |  | 商品的标签 |
| goodsThirdCategory |  | goods_third_category |  | 三级分类 |
| goodsType |  | goods_type |  | 商品类型 |
| goodsUnit |  | goods_unit |  | 单位 |
| grossProfitRate |  | gross_profit_rate |  | 毛利率 |
| homepageConfig |  | homepage_config |  | 首页配置 |
| homepageControl |  | homepage_control |  | 首页包含的控件 |
| homepageControlDtl |  | homepage_control_dtl |  | 首页控件明细 |
| integral |  | integral |  | 积分 |
| lastModifiedTime |  | last_modified_time |  | 最后维护时间 |
| lifeTime |  | life_time |  | 消亡时长 |
| manualTagBy |  | manual_tag_by |  | 可手动标记范围 |
| manufacturer |  | manufacturer |  | 生产厂家 |
| memberCollection |  | member_collection |  | 会员群名称 |
| memberGroup |  | member_group |  | 会员群组名称 |
| memberGroupNo |  | member_group_no |  | 会员群所属会员群组 |
| memberNo |  | member_no |  | 会员编号：发送消息目标用户的会员编号 |
| memberValue |  | member_value |  | 会员价值 |
| monitorPhone |  | monitor_phone |  | 监控手机号 |
| msgPlaceholder |  | msg_placeholder |  | 扩展字段：微信、支付宝消息模板的占位字段 |
| msgSendNo |  | msg_send_no |  | 消息活动编号：发送消息的活动 |
| note |  | note |  | 备注 |
| operator |  | operator |  | 话席 |
| operatorName |  | operator_name |  | 话席人员名称 |
| orderGoods |  | order_goods |  | 订单商品明细 |
| orderInfo |  | order_info |  | 订单信息表 |
| orderTime |  | order_time |  | 订单相关时间属性配置 |
| orderType |  | order_type |  | 订单类型 |
| originalAmount |  | original_amount |  | 原始金额 |
| originalPrice |  | original_price |  | 原始价格 |
| outgoingTaskName |  | outgoing_task_name |  | 外呼任务名称 |
| packingAmount |  | packing_amount |  | 单位包装量 |
| packingFee |  | packing_fee |  | 包装费 |
| paymentRecord |  | payment_record |  | 系统支付记录 |
| paymentType |  | payment_type |  | 付款类型 |
| perCustomerTransaction |  | per_customer_transaction |  | 客单价 |
| phone |  | phone |  | 手机号/电话号码 |
| phoneBar |  | phone_bar |  | 电话条 |
| picking |  | picking |  | 拣货 |
| pinyinInitial |  | pinyin_initial |  | 助记码 |
| platformCode |  | platform_code |  | 平台编码 |
| platformPrice |  | platform_price |  | 平台价格 |
| pointAddCondition |  | point_add_condition |  | 加分条件 |
| pointAddValue |  | point_add_value |  | 加分值 |
| pointDeductionCondition |  | point_deduction_condition |  | 减分条件 |
| pointDeductionValue |  | point_deduction_value |  | 减分值 |
| progress |  | progress |  | 呼叫进度 |
| randomPasswordWidth |  | randow_password_width |  | 随机密码位数 |
| redeemPercentage |  | redeem_percentage |  | 核销进度 |
| reduceCoupon |  | reduce_coupon |  | 满减券 |
| region |  | region |  | 地区：和所属地区有关的设置 |
| registerShop |  | register_shop |  | 办卡门店 |
| relatedTask |  | related_task |  | 相关任务 |
| rentAttribute |  | rent_attribute |  | 租借商品属性 |
| retailPrice |  | retail_price |  | 零售价 |
| seller |  | seller |  | 商家：下面有门店 |
| sendTime |  | send_time |  | 发送时间 |
| sendTo |  | send_to |  | 发送范围 |
| sendDate |  | send_date |  | 发送日期 |
| sex |  | sex |  | 性别 |
| shop |  | shop |  | 门店 |
| shopArea |  | shop_area |  | 场地：对应门店的区域 |
| smsContent |  | sms_content |  | 短信内容 |
| smsTemplateGroupName |  | sms_template_group_name |  | 短信模板分组 |
| smsTemplateName |  | sms_template_name |  | 短信模板名称 |
| status |  | status |  | 状态 |
| tagCategory |  | tag_category |  | 所属标签类 |
| tagGroupName |  | tag_group_name |  | 标签组名称 |
| tagName |  | tag_name |  | 标签名称 |
| taskExecutionStatus |  | task_execution_status |  | 任务执行状态 |
| taskGroupName |  | task_group_name |  | 任务组名称 |
| taskName |  | task_name |  | 任务名称 |
| taskNo |  | task_no |  | 任务编号 |
| timeLimitationType |  | time_limitation_type |  | 时限类型 |
| timeSlot |  | time_slot |  | 时间段 |
| valueModel |  | value_model |  | 价值条件 |
| valueModelName |  | value_model_name |  | 价值模型名称 |
| visibleBy |  | visible_by |  | 可见范围 |
| wechatOpenId |  | wechat_openid |  | 微信ID：发送微信模板消息目标用户的微信 openid |
| workgroupNo |  | workgroup_no |  | 工作组编号 |
| workgroupName |  | workgroup_name |  | 工作组名称 |







