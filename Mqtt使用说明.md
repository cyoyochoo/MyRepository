##  依赖Mqtt-release-V1.0.aar
将Mqtt-release-V1.0.aar放到libs目录
```
repositories {
    flatDir {dirs 'libs'}
}
```
```
dependencies {
    implementation(name: 'Mqtt-release-V1.0', ext: 'aar')
}
```

##  Mqtt使用
1. **创建mqtt**
```
Mqtt mqtt = new Mqtt.Builder()
                    .serverUri("") //服务器地址
                    .userName("") //用户名，可选
                    .password("") //用户密码，可选
                    .clientId("") //客户端唯一标识，不能重复
                    .withCaInputStream(null) //服务端证书校验，可选
                    .withClientInputStream(null) //客户端证书，可选
                    .withClientPassword("") //客户端证书密码，可选
                    .....
                    .build(context);
```
2. **连接mqtt**
