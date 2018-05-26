# spring-cloud-gateway-learn
spring-cloud-gateway-sample项目启动，需要添加注释@EnableAutoConfiguration默认加载spring-could-gateway-core里的spring-factories里的配置默认启动类
org.springframework.boot.autoconfigure.EnableAutoConfiguration=\
org.springframework.cloud.gateway.config.GatewayClassPathWarningAutoConfiguration,\
org.springframework.cloud.gateway.config.GatewayAutoConfiguration,\
org.springframework.cloud.gateway.config.GatewayLoadBalancerClientAutoConfiguration,\
org.springframework.cloud.gateway.config.GatewayRedisAutoConfiguration,\
org.springframework.cloud.gateway.discovery.GatewayDiscoveryClientAutoConfiguration
在以上自动加载配置的类中，GatewayClassPathWarningAutoConfiguration，GatewayRedisAutoConfiguration, GatewayDiscovRibbonAutoConfiguratioeryClientAutoConfiguration
都是在GatewayAutoConfiguration加载之后再加载，GatewayLoadBalancerClientAutoConfiguration加载之后记载RibbonAutoConfiguration类。