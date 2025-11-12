# Study-C-
# C-Linked-List | C语言指针深度实践

> 用C实现带头节点链表，**通过valgrind验证无内存泄漏**（含调试过程）

## 关键技术
- **指针操作**：`struct Node* head` 实现链表遍历
- **动态内存**：`malloc`/`free` 管理节点（避免内存泄漏）
- **内存验证**：`valgrind --leak-check=full ./list` 无泄漏报告

## 设计思考
> 为什么不用C++ STL？  
> - 二本学生需证明**C基础**（STL会掩盖指针理解）  
> - 用C指针实现链表，**直接关联C语言核心考点**（面试常问“链表如何用指针实现”）

## 运行验证
```bash
gcc -o list list.c
valgrind --leak-check=full ./list
