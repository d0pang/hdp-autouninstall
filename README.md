# hdp-autouninstall
前置条件：
1.脚本基于HDP3.1版本的一键自动卸载程序，基于如下环境
2.HDP安装方式为离线模式
3.脚本需要在Ambari server服务器上运行
4.脚本仅支持RHEL System

脚本输入参数说明：
脚本执行需要root用户或者具有免密sudo, 并且服务器打通免密ssh
$ sh autouninstall.sh

目录文件说明（以下文件不能重命名，否则会导致不脚本不能正常使用）：
autouninstall.sh 卸载脚本
components.list  集群中包含的所有组件
node.list  集群所有节点的hostname，必须为hostname,Ambari server服务器不需要配置
user.list  集群中所有启动服务的用户
group.list 集群中所有启动服务的组
delete.list 集群中所有需要删除的目录和文件
doall.sh   ssh远程简单执行命令

此脚本改编自：https://github.com/fayson/cdh-autouninstall
感谢原创者！