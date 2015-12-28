# summingbird-hybrid-example-china

1.开启zookeeper   <br /> 
	进入zookeeper的bin目录下使用命令行 ./zkServer.sh start   <br /> 
2.开启kafka   <br /> 
	进入kafka的bin目录下使用命令行 ./kafka-server-start.sh ../config/server.properties &   <br /> 
3.开启memcached 开启12000端口   <br /> 
	进入memcached目录下使用命令行 ./memcached -d -m 10 -u root -l 127.0.0.1 -p 12000 -c 256 -P /tmp/memcached.pid   <br /> 
4.进入summingbird-hybrid-example-china主目录下使用命令行    <br /> 
	sbt compile   <br /> 
	sbt run 选择2运行hybrid.Main   <br /> 
	
一段时间后可以看到如下的结果：   <br /> 

2640724 [pool-5-thread-1] INFO  summingbird.proto.RunHybrid$ - lookupDebug(7)   <br /> 
2640731 [pool-5-thread-1] INFO  summingbird.proto.HybridRunner$ - Offline: Some((BatchID.4828433,229))   <br /> 
2640735 [pool-5-thread-1] INFO  summingbird.proto.HybridRunner$ - Online: (BatchID.4828433,Some(25))     <br /> 
2640748 [pool-5-thread-1] INFO  summingbird.proto.HybridRunner$ - Hybrid: Some(254)    <br /> 
2640748 [pool-5-thread-1] INFO  summingbird.proto.RunHybrid$ - Events Produced: 2635   <br /> 
2640748 [pool-5-thread-1] INFO  summingbird.proto.RunHybrid$ - Events Ingested: 2634   <br /> 

成功！
