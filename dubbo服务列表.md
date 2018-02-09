## 1. [余额类型](dubbo_srv_list/acct_res.md)

#### 1.账目类型查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.acct.service.AcctItemTypeRemoteService>`
1.1 查询所有账目类型
>
`List<AcctItemTypeData> qryAllAcctItemType()`
  
1.2 根据账目类型id查询账目类型
>
`AcctItemTypeData qryAcctItemTypeById(Long acctItemTypeId)`

1.3 根据余额类型ID查询账目类型
>
`List<AcctItemTypeData> qryAcctItemTypeByAcctResId(Long acctResId)`

#### 2.属性查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.attr.service.AttrRemoteService>`
2.1 根据目录查询属性基本信息
>
`List<AttrData> queryAttrByCatg(String attrCatg)`

2.2 根据属性标识（多个）查询属性基本信息
>
`List<AttrData> queryAttrByAttrIds(Long[] attrIds)`

2.3 根据属性标识（多个）查询属性基本信息（给ZTP测试用）
>
`List<AttrData> queryAttrByAttrIds4Ztp(AttrIdData4Ztp attrIdData)`

2.4 根据入参条件查询属性信息列表(QueryAttrListReq目前包含attrIds、attrCodes、attrCatg和objAttrId字段，查询顺序为先根据ids查询；ids为空则根据codes查询；codes为空根据catg查询，根据catg查询时，过滤掉子属性，即objAttrId字段不为空的属性；catg为空时根据objAttrId字段查询，查询objAttrId等于传入值的属性)
>
`QueryAttrListResp queryAttrList(QueryAttrListReq queryAttrListReq)`

#### 3.域类型数据查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.DomainRemoteService>`
3.1 根据域类型编码查询域表数据
> 
`List<DomainData> queryPublicDimList(String domainTypeCode)`

#### 4.账期查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.BillingCycleRemoteService>`
4.1 查询所有账期类型
>
`List<BillingCycleTypeData> queryAllBillingCycleType()`

4.2 根据账期类型id，账期日期，偏移量查询账期
>
`BillingCycleData qryBillingCycle(Long billingCycleTypeId, Date startDate, Integer offset)`

4.3 根据账期类型id，账期日期，偏移量查询账期（给ZTP测试用）
>
`BillingCycleData qryBillingCycle4Ztp(Parm4QryBillCyc parm4QryBillCyc)`

4.4 issue#245 根据入参中的条件查询账期类型列表（QueryBillingCycleTypeListReq中包含postpaid字段，可选值为"Y"和"N",匹配先付费和后付费的账期类型，如果入参为null或postpaid字段为null，则返回全部账期类型）
>
`QueryBillingCycleTypeListResp qryBillingCycleTypeList(QueryBillingCycleTypeListReq req)`

#### 5.支付方式查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.pay.service.PaymentMethodRemoteService>`
5.1 查询所有支付方式
>
`List<PaymentMethodData> queryAllPaymentMethod()` 

#### 6.交互事件查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.InterEventRemoteService>`
6.1 根据事件id查询交互事件
>
`InterEventData qryInterEventById(Long eventId)`

6.2 查询符合事件使用范围的所有交互事件
>
`List<InterEventData> qryInterEventsByScope(String scope)`

#### 7.供应商查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.VenderRemoteService>`
7.1 查询查询所有供应商
>
`List<VenderData> queryAllVender()`
 
#### 8.业务配置项查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.busiparam.service.ConfigItemRemoteService>`
8.1 根据业务模型编码，业务配置项编码，业务配置项参数编码查询业务配置项
>
`ConfigItemParamData qryConfigItemParamValue(String moduleCode, String itemCode, String paramCode)`
 
#### 9.接触渠道查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.channel.service.ContactChannelRemoteService>`
9.1 查询所有接触渠道数据
>
`List<ContactChannelData> qryAllContactChannel()`

9.2 根据渠道类型查询接触渠道
>
`List<ContactChannelData> qryContactChannelByChannelType(String channelType)`

9.3 根据接触渠道id查询接触渠道
>
`ContactChannelData qryContactChannelById(Long contactChannelId)`
 
#### 11.货币类型查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.CurrencyTypeRemoteService>`
11.1 查询所有货币类型
>
`List<CurrencyTypeData> qryAllCurrencyType()`

11.2 根据货币类型编码查询货币类型
>
`CurrencyTypeData qryCurrencyTypeByCode(String currencyCode)`

11.3 根据条件查询货币类型(QueryCurrencyTypeReq目前包含currencyTypeId和currencyTypeCode字段，查询顺序为先根据id查询，id为空则根据code查询)
>
`QueryCurrencyTypeResp queryCurrencyType(QueryCurrencyTypeReq request)`

#### 12.单位类型查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.UnitTypeRemoteService>`
12.1 查询所有单位类型
>
`List<UnitTypeData> qryAllUnitType()`

12.2 根据unitTypeId查询单位类型
>
`UnitTypeData qryUnitTypeById(Long unitTypeId)`
 
#### 13.保证金类型查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.DepositTypeRemoteService>`
13.1 查询所有保证金类型
>
`List<DepositTypeData> qryAllDepositType()`

13.2 根据idList查询保证类型
>
`List<DepositTypeData> qryDepositTypeByIdList(List<Long> depositTypeIdList)`

13.3 根据idList查询保证类型（给ZTP测试用）
>
`List<DepositTypeData> qryDepositTypeByIdList4Ztp(DepositTypeIdList4Ztp depositTypeIdList)`

#### 14.渠道关联单位查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.channel.service.ChannelUnitRemoteService>`
14.1 根据条件查询适用渠道关联单位集合，QueryChannelUnitListReq包含contactChannelID字段和unitTypeId字段。只有contactChannelID时查询该渠道下的所有关联单位；有unitTypeId再根据其过滤
>
`QueryChannelUnitListResp queryChannelUnitList(QueryChannelUnitListReq req)`

#### 15.银行查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.BankRemoteService>`
15.1 查询所有银行
>
`List<BankData> qryAllBank()`

15.2 根据银行编码查询银行
>
`BankData qryBankByCode(String bankCode)`

15.3 根据银行id查询银行
>
`BankData qryBankById(Long bankId)`

#### 16.分期付款类型查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.pay.service.InstalmentTypeRemoteService>`
16.1 根据账目类型（AcctItemTypeId）查询适用的分期付款类型（基本信息，只返回cbec_instalment_type表信息）
>
`List<InstalmentTypeData> qryInstalmentTypeByAcctItemTypeId(Long acctItemTypeId)`

16.2 查询所有分期付款类型（基本信息，只返回cbec_instalment_type表信息）
>
`List<InstalmentTypeData> qryAllInstalmentType()`

16.3 根据分期付款类型ID查询分期付款详情（返回cbec_instalment_type, cbec_instalment_type_item, cbec_instalment_item三张表信息）
>
`InstalmentTypeData qryInstalmentTypeById(Long instalmentTypeId)`

#### 17.物理、网络小区查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.zone.service.HomeZoneRemoteService>`
17.1 查询所有物理小区
>
`List<GeoHomeZoneData> qryAllGeoZones()`

17.2 查询所有网络小区
>
`List<HomeZoneData> qryAllHomeZones()`

17.3 根据物理小区ID查询网络小区
>
`List<HomeZoneData> qryHomeZonesByGeoZoneId(Long geoZoneId)`

#### 18.MVNO查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.mvno.service.MvnoRemoteService>`
18.1 查询指定MVNO拥有的数据权限
>
`QueryMvnoDataAuthListResp queryMvnoDataAuthList(QueryMvnoDataAuthListReq req)`

#### 19.余额类型组查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.acct.service.AcctResGroupRemoteService>`
19.1 查询余额类型组集合(QueryAcctResGroupListReq暂无条件字段，默认为查询全量)
>
`QueryAcctResGroupListResp queryAcctResGroupList(QueryAcctResGroupListReq request)`

#### 20.业务进程查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.BusinessProcessorRemoteService>`
20.1 根据入参条件查询业务进程列表(QueryBusinessProcessorListReq中有processorIds字段，为空则查询全量)
>
`QueryBusinessProcessorListResp queryBusinessProcessorList(QueryBusinessProcessorListReq request)`

#### 21.信控类型查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.ClTypeRemoteService>`
21.1 根据入参条件查询信控类型列表(QueryClTypeListReq暂无字段，默认为查询全量)
>
`QueryClTypeListResp queryClTypeList(QueryClTypeListReq request)`

#### 22.单位查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.UnitRemoteService>`
22.1 根据入参条件查询单位列表(QueryUnitListReq为null则查询全量，QueryUnitListReq中有unitIds和defaultUnit字段)
>
`QueryUnitListResp queryUnitList(QueryUnitListReq req)`

#### 23.信用额度类型查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.CcTypeRemoteService>`
23.1 根据条件查询信用额度类型列表(QueryCcTypeListReq为null则查询全量)
>
`QueryCcTypeListResp queryCcTypeList(QueryCcTypeListReq req)`

#### 24.单位兑换率查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.common.service.UnitRateRemoteService>`
23.1 根据条件查询单位兑换率列表(QueryUnitRateListReq包含srcUnitId和objUnitId两个字段。只传srcUnitId时查询源单位为其的所有单位兑换率；如果有objUnitId，再根据它过滤)
>
`QueryUnitRateListResp queryUnitRateList(QueryUnitRateListReq request)`
