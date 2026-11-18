# 合成分析资料契约

所有机构、企业、受访者、交易和事件均为本地合成，不来自新闻所涉真实主体，不声称新闻发生过这些分析问题。

seed.json与同名Parquet是相同原始值的两种载体；actions.json列尚未应用的后续输入动作。inventory.json只记录原件物理摘要和行数，不提供分析结论。时间均含时区或明确日期，金钱字段minor以CNY分计，空值保留未知含义。已有代码只做物理完整性检查，没有估计、预测、方案求解或产品发布功能。

sampling_frame中unit为被抽对象，stratum/psu为分层与整组单位，pi_psu和pi_cond为已知两阶段概率，均大于0且不超过1；target为展期去重成年观众。contacts中attempt按对象递增，status包括refused/absent/answered，answered并不保证每题有值。responses的revisit为yes/no/null，spend_band为分类，null是单题缺答。volunteer的扫码回答缺设计概率，只能独立描述或用于有明确假设的辅助分析。margins每组constraint独立给完整边际，universe/count_unit/date_from/date_to决定适用性，不同名册不保证相容。校准/响应处理方式由实现选择，不能用无观测支持的格子产生确定估计。变化动作是后续补答与名册更正，不是预计算权重。
