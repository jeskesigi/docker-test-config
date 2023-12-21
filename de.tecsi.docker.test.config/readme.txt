	
argocd applications
-------------------	
	applications
	- docker-test-dev : values.yaml + values-dev.yaml
	- docker-test-prod : values.yaml + values-prod.yaml

	git configuration repo : https://github.com/jeskesigi/docker-test-config.git
	path to helm deployment : de.tecsi.docker.test.config/docker-test-config

test deployment
---------------
kubectl port-forward svc/test-service -n docker-test-dev 8001:8080
kubectl port-forward svc/test-service -n docker-test-dev 50505:50505

curl http://localhost:8001/test-data
