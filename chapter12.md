RAII
通过对象句柄的构造和析构，封装堆资源的分配malloc/new 与 回收 free/delete，避免出函数局部栈前忘记回收或者异常出栈
c99支持动态数组 struct { int arr[]; } 或者 int v; int arr[v]; 编译器不能确认数组分配的长度 unsafe
c++不支持 使用 vector动态数组 或者 array静态数组

智能指针
unique_ptr 独占指针 .get() unsafe
share_ptr 共享指针 引用计数器线程安全 写时拷贝
weak_ptr 避免 share_ptr循环引用死锁
