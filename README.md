# go-improve

## week1 作业

### 作业： 我们在数据库操作的时候，比如 dao 层中当遇到一个 sql.ErrNoRows 的时候，是否应该 Wrap 这个 error，抛给上层。为什么，应该怎么做请写出代码？

#### 答案：不应该抛给上层

#### 原因：
对于上层来说，并不需要知道ErrNoRows，上层只关心查询过程中是否产生错误，如果是空的话，应该返回空slice，空map或nil。
