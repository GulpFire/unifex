# concepts 
execution 的各种 concepts 定义及 cpo(custmized point object) 定义

## Receiver
libunifex中的消费者类型，用于接收异步操作结果的对象。
## Sender
libunifex中的生产者类型，会将自己的结果通过其中一种callback方式传递给关联的Receiver(set_value/ set_done/ set_error 中的一个)
## TypedSender
同上，添加了对生产的数值类型的约束
## OperationState
用于持有异步操作状态的对象，一般由connect()产生
## ExecutionContext
并不直接出现的类型，表达一个支持异步任务执行的上下文环境，一般通过Scheduler概念来包装使用，但对于我们理解libunifex的执行模型比较重要。
## Scheduler
libunifex中可以支持异步操作调度的调度器实现。
## TimeScheduler
同上，额外支持特定时间点执行任务的能力。
## StopToken
不同类型的stop-token实现，用于libunifex的取消机制。
## ManySender
Sender的一种扩展，可以传递多个值到Receiver(可以不详细了解，非标准的实现)。
## AsyncStream
类似用于输入范围值，序列中的每个值只会在请求的时候才惰性的去产生(可以不详细了解，非标准的实现)。
