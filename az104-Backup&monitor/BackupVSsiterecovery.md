## stateful data verses stateless data
- statful data：
    - 应用在处理请求时需要依赖用户的历史状态或上下文，比如登录信息、数据库中的记录等
    - 需长期保存且一致性要求高，通常需要持久化存储（Persistent Storage
    - 例如用户信息，订单信息，redis地session状态，虚拟机的磁盘等等
- stateless data：
    - 不需要记录或者依赖于过去交互的数据，每次请求都是独立的，原子性的
    - 不存储用户状态
    - 例如静态网页，图片，视频，微服务返回的JSON接口响应等。
    - 通常不需要频繁地备份