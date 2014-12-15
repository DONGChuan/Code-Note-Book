# 序列化时 static 域的处理?

There are three exceptions in which serialization doesnot necessarily read and write to the stream. These are

1. Serialization ignores static fields, because they are not part of auy particular state state.
2. Base class fields are only hendled if the base class itself is serializable.
3. Transient fields.
