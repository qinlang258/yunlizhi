# yunlizhi
一个yam文件创建deployment，svc，ingress

文件如下
```yaml
apiVersion: infra.yunlizhi.cn/v1
kind: App
metadata:
  namespace: dev
  name: yunlizhi-sample
spec:
  # Add fields here
  replicas: 2
  image: registry.cn-zhangjiakou.aliyuncs.com/jcrose-k8s/tomcat:8
  port: 8080
  domain: tomcat.jcrose.com
  project: tomcat
```

spec里面的内容解析  
1 port 应用自己的端口，例如tomcat 8080,nginx 80,mysql 3306  
2 domain ingress使用的域名地址  
3 project 应用的名字，用于deployment与svc创建的时候标签选择  
