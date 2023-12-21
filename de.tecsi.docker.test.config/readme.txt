
test deployment
---------------
kubectl port-forward svc/test-service -n docker-test-dev 8001:8080
kubectl port-forward svc/test-service -n docker-test-dev 50505:50505

curl http://localhost:8001/test-data
