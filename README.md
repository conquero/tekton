#安装tekton  
kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml  
#示例应用  
java-api-gateway、java-test  
#代码仓库  
gitlab.domain  
#镜像仓库  
core.harbor.domain  
#认证方式  
通过serviceaccount的方式与gitlab、harbor、k8s进行认证，涉及的文件名为serviceaccount.yaml、tekton-basic-user-pass-gitlab-secret.yaml、tekton-basic-user-pass-harbor-secret.yaml、clusterrolebinding.yaml  
#参数传入  
task.yaml、deploy.yaml、dockerfile为标准化模板，通过taskrun.yaml、gitlab-java-api-gateway-pipelineresource.yaml、harbor-java-api-gateway-pipelineresource.yaml传入相应的参数即可  
#rancher  
rancher的流水线配置文件在rancher目录下  
#参考文档  
https://github.com/tektoncd/pipeline 
https://docs.rancher.cn/rancher2x/  
