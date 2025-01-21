# MegaAgent

#### 目前LLM-MA存在以下三个问题

1.未考虑到大规矩规模agent的管理

2.这些系统在协做上仍表现出局限性，使其在多学科任务解决中没有足够的泛化性

3.SOPs and prompt局限了MA的发展

#### 应解决的关键挑战

1.在并行的情况下组织MA之间以及与外界服务之间的通信问题

2.现有的Agent的自主能力不足

#### MegaAgent核心思想

1.为大规模MA管理而设计，其中的MA可以实现自主的通信

2.可以将大任务切分为子任务并交由下层子任务解决

3.由最上层的BossAgent将任务切分并交由下一层的Agent组进行处理

4.每个Agent组都由1个admin和多个agent

5.BossAengt监控整个agent组的输出规范

**（思考：在agent组数量足够大时监控任务是否会发生阻塞？）**

**（解决方法1.为每一个agent层设置监控agent 2.若BossAgent检测到agent层数超过阈值生成新的监控agent ）**

#### MegaAgent进行的实验

1.Gobanggame

2.an industry-wide national policy simulation