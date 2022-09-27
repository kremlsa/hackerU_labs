# hackerU_labs

https://app.vagrantup.com/debian/boxes/buster64/versions/10.20220912.1/providers/virtualbox.box

https://hackmd.io/1dEZK1JyQFec8-rdAKgw0w?view

https://disk.yandex.ru/d/I7hOKryUURolcg

failed: [master -> node-3(127.0.0.1)] (item=node-3) => {"ansible_loop_var": "item", "changed": true, "cmd": "kubeadm join 192.168.56.10:6443 --token twfda9.o2roxhmqi52k2swy     --discovery-token-ca-cert-hash sha256:a962e7d16deb73aa25f8c65d368ac2279e873f8aa35781c45dc45de26eda67c9 ", "delta": "0:05:02.269155", "end": "2022-09-24 09:29:21.735335", "item": "node-3", "msg": "non-zero return code", "rc": 1, "start": "2022-09-24 09:24:19.466180", "stderr": "\t[WARNING SystemVerification]: this Docker version is not on the list of validated versions: 20.10.18. Latest validated version: 19.03\n\t[WARNING SystemVerification]: missing optional cgroups: hugetlb\nerror execution phase preflight: couldn't validate the identity of the API Server: Get \"https://192.168.56.10:6443/api/v1/namespaces/kube-public/configmaps/cluster-info?timeout=10s\": x509: certificate is valid for 10.96.0.1, 10.0.2.15, not 192.168.56.10\nTo see the stack trace of this error execute with --v=5 or higher", "stderr_lines": ["\t[WARNING SystemVerification]: this Docker version is not on the list of validated versions: 20.10.18. Latest validated version: 19.03", "\t[WARNING SystemVerification]: missing optional cgroups: hugetlb", "error execution phase preflight: couldn't validate the identity of the API Server: Get \"https://192.168.56.10:6443/api/v1/namespaces/kube-public/configmaps/cluster-info?timeout=10s\": x509: certificate is valid for 10.96.0.1, 10.0.2.15, not 192.168.56.10", "To see the stack trace of this error execute with --v=5 or higher"], "stdout": "[preflight] Running pre-flight checks", "stdout_lines": ["[preflight] Running pre-flight checks"]}



TASK [install_charts : add hashicorp helm repo] ********************************
fatal: [master]: FAILED! => {"changed": false, "command": "/usr/local/bin/helm repo add hashicorp https://helm.releases.hashicorp.com", "msg": "Failure when executing Helm command. Exited 1.\nstdout: \nstderr: Error: looks like \"https://helm.releases.hashicorp.com\" is not a valid chart repository or cannot be reached: failed to fetch https://helm.releases.hashicorp.com/index.yaml : 403 Forbidden\n", "stderr": "Error: looks like \"https://helm.releases.hashicorp.com\" is not a valid chart repository or cannot be reached: failed to fetch https://helm.releases.hashicorp.com/index.yaml : 403 Forbidden\n", "stderr_lines": ["Error: looks like \"https://helm.releases.hashicorp.com\" is not a valid chart repository or cannot be reached: failed to fetch https://helm.releases.hashicorp.com/index.yaml : 403 Forbidden"], "stdout": "", "stdout_lines": []}

PLAY RECAP *********************************************************************
master                     : ok=28   changed=20   unreachable=0    failed=1    skipped=0    rescued=0    ignored=0   
node-1                     : ok=13   changed=11   unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
node-2                     : ok=13   changed=11   unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
node-3                     : ok=13   changed=11   unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   

Ansible failed to complete successfully. Any error output should be
visible above. Please fix these errors and try again.
