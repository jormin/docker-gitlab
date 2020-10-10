## 说明

1. 安装前需要先指定 GITLAB_HOME 指定 gitlab 数据映射路径

    ```
    export GITLAB_HOME=/srv/gitlab
    ```

2. 映射文件路径及作用说明

    宿主机路径 | 容器路径 | 作用
    --- | --- | ---
    $GITLAB_HOME/data | /var/opt/gitlab | 应用数据
    $GITLAB_HOME/logs | /var/log/gitlab | 存储日志
    $GITLAB_HOME/config | /etc/gitlab | 配置文件

3. 全局配置说明

    - external_url：配置好后外部访问路径
    - gitlab_rails['gitlab_shell_ssh_port']：外部拉取代码所使用的宿主机端口