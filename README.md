helm create service-bus


kubectl create secret docker-registry regcred --docker-server=lopez.azurecr.io --docker-username=lopez --docker-password=SECRET_PASSWORD --docker-email=USER_EMAIL
# kubectl delete secret regcred

helm install -n service-bus service-bus .
helm uninstall -n service-bus service-bus .


command: ["dotnet"]
args: ["/app/Platform.Api/Platform.Api.dll"]




command: ["/bin/sh", "-ec", "while :; do echo '.'; sleep 5 ; done"]