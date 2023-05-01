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
  image: registry.cn-zhangjiakou.aliyuncs.com/jcrose-k8s/nginx:1.18
  port: 80
  domain: nginx.jcrose.com
  project: nginx
```

spec里面的内容解析
1 port 应用自己的端口，例如tomcat 8080,nginx 80,mysql 3306
2 domain ingress使用的域名地址
3 project 应用的名字，用于deployment与svc创建的时候标签选择
