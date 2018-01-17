# doc_to_form
从doc等文档中获取表单需要的数据

    搁置很久的一个项目准备启动了，大概思路就是从docx等文档中直接获取基于元数据设计的表单数据，并建立表单与文档附件的关系
    业务场景：用户上传某类附件，比如采购合同.doc，表单定义的原数据里会定义“甲方：”、“乙方：”、“金额：”等等关键字，从单据的元数据定义里拿到这些key，去附件中进行检索，然后再根据一定的逻辑获取相关值，自动放入单据，并提醒相关人进行确认，不用完全准确，能够减少用户80%的录入工作量即可
    用户各自的文档格式不统一，但是会和自己组织定义的表单是一致的，目前我们已经实现了用户组织级的表单定义，结合这个元数据，即可自动进行文档的分析了
   其实这本来是一个伪需求，为什么这么说呢，因为实际如果信息化、互联网化到一定程度，这些数据会直接在系统中产生，而不是先进入word这类的线下文档，这也是之前搁置这个项目的主要原因，另一方面原因就是在线协同文档这个方向的发展，其实石墨、腾讯TIM、百度、金山、office365等的相关文档协作的产品如果能够开放相关接口，就更好了
但是，现实情况发现先有线下文档的情形还会在很长一段时间里大量存在，这都是一个实实在在的需求
