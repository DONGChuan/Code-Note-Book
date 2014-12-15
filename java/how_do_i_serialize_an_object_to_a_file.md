# 如何序列化一个对象到一个文件?

要被序列化的实例所对应的类必须实现 Serializable 接口. 然后你可以把实例传递给 ObjectOutputStream, 同时 ObjectOutputStream 也必须连接至 fileoutputstream. 这样就会把一个对象储存到一个文件里.
