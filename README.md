# Node Exporter Role

这个 Ansible role 用于安装和配置 Node Exporter。

## Variables

以下是这个 role 使用的变量，以及它们的说明：

- `node_exporter_version`: Node Exporter 的版本号。默认值是 "1.7.0"。

- `node_exporter_download_url`: Node Exporter 的下载 URL。默认值是 "https://github.com/prometheus/node_exporter/releases/download/v{{ node_exporter_version }}/node_exporter-{{ node_exporter_version }}.linux-amd64.tar.gz"。

- `node_exporter_install_dir`: Node Exporter 的安装目录。默认值是 "/usr/local/bin"。

- `node_exporter_service_file`: Node Exporter 的 systemd 服务文件路径。默认值是 "/etc/systemd/system/node_exporter.service"。

- `port`: Node Exporter 的监听端口。默认值是 9101。

## Usage

要使用这个 role，你可以在 playbook 中引用它，如下所示：

```yaml
- hosts: node
  become: yes
  roles:
    - role: node-exporter