```
kubectl create ns keda
kubectl apply -f jovianx-metering.yaml -n keda
kubectl apply -f dummy-ss.yaml -n keda
helm repo add kedacore https://kedacore.github.io/charts
helm repo update
helm install keda kedacore/keda -n keda
kubectl apply -f keda-scale.yaml -n keda
kubectl apply -f keda-scale1.yaml -n keda
kubectl apply -f keda-scale2.yaml -n keda
kubectl get hpa -n keda
```
