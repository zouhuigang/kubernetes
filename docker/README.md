##docker-镜像构建
###build###

    sudo docker build -t yourname/imagename:yourtagname .

1.构建php images

    sudo docker build -t  registry.cn-hangzhou.aliyuncs.com/zhg_docker_ali_r/php:51tywy .

注：进入php dockerfile文件目录，registry.cn-hangzhou.aliyuncs.com/zhg_docker_ali_r/php为镜像名称,51tywy为tag

起这个名字主要是为了方面推送到阿里云的镜像中心去。

2.推送到阿里云镜像中心,推送前登录
    
    sudo docker login --username=952750120@qq.com registry.cn-hangzhou.aliyuncs.com

    sudo docker push registry.cn-hangzhou.aliyuncs.com/zhg_docker_ali_r/php:51tywy


3.实践编译生成images

1.把workerman上传到linux中，打开目录，运行
     
    sudo docker build -t registry.cn-hangzhou.aliyuncs.com/zhg_docker_ali_r/workerman:51tywy .

2.经过一段漫长的等待，images制作好了。然后提交到我的阿里云镜像库

    sudo docker push registry.cn-hangzhou.aliyuncs.com/zhg_docker_ali_r/workerman:51tywy


3.运行workerman.yaml
