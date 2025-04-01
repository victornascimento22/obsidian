 Gerenciamento de Cluster  
kubectl cluster-info → Exibe informações do cluster  
kubectl config → Gerencia configurações do cluster  
kubectl version → Exibe a versão do Kubernetes  
kubectl get nodes → Lista os nós do cluster  
kubectl get pods → Lista os pods em execução  
kubectl get services → Lista os serviços disponíveis  
  
🔹 Gerenciamento de Pods  
kubectl create pod → Cria um novo pod  
kubectl get pods → Lista os pods no cluster  
kubectl describe pod → Exibe detalhes sobre um pod  
kubectl logs → Exibe os logs de um pod  
kubectl exec → Executa um comando dentro de um pod  
kubectl delete pod → Remove um pod  
  
🔹 Monitoramento de Recursos  
kubectl top nodes → Monitora o uso de recursos dos nós  
kubectl top pods → Monitora o uso de recursos dos pods  
kubectl get quota → Exibe cotas de recursos  
kubectl describe → Detalha qualquer recurso do Kubernetes  
  
🔹 Gerenciamento de Serviços  
kubectl create service → Cria um novo serviço  
kubectl get services → Lista os serviços disponíveis  
kubectl expose → Expõe um recurso como serviço  
kubectl describe service → Exibe detalhes sobre um serviço  
kubectl delete service → Remove um serviço  
kubectl port-forward → Encaminha portas para acessar um serviço localmente  
  
🔹 Configuração e Segredos  
kubectl create configmap → Cria um ConfigMap  
kubectl get configmaps → Lista os ConfigMaps  
kubectl create secret → Cria um segredo  
kubectl get secrets → Lista os segredos armazenados  
kubectl describe configmap → Exibe detalhes de um ConfigMap  
kubectl describe secret → Exibe detalhes de um segredo  
  
🔹 Gerenciamento de Deployments  
kubectl create deployment → Cria um deployment  
kubectl get deployments → Lista os deployments  
kubectl scale → Escala um deployment  
kubectl rollout status → Mostra o status do rollout  
kubectl rollout history → Exibe o histórico de rollouts  
kubectl delete deployment → Remove um deployment  
  
🔹 Gerenciamento de Namespaces  
kubectl create namespace → Cria um namespace  
kubectl get namespaces → Lista os namespaces  
kubectl describe namespace → Exibe detalhes de um namespace  
kubectl delete namespace → Remove um namespace  
kubectl apply -n <namespace> → Aplica um recurso em um namespace específico  
kubectl switch -n <namespace> → Alterna entre namespaces