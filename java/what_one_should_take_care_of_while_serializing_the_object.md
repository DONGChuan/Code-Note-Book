# 序列化时要注意什么?

One should make sure that all the included objects are also serializable. If any of the objects is not serializable then it throws a NotSerializableException.
