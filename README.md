# springboot-jwt-authr
sprinboot REST service using jwt for authorization and not for authentication.
This service read the jwt token coming as a Bearer token header and parse it.
{
  "sub": "1234567890",
  "name": "John Doe",
  "roles":"ROLE_ADMIN",
  "iat": 1516239022
}

Above JWT value will be parsed as the current request and ADMIN role.
sample jwt as bearer token
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwicm9sZXMiOiJST0xFX0FETUlOIiwiaWF0IjoxNTE2MjM5MDIyfQ.nzoTXU6kVPfv_P9_BHA4cB_SkCDvuRwRRhisEARDyfM


run in docker:
docker build -t springboot-jwt-authr .
docker run -p 127.0.0.1:8090:8090 springboot-jwt-authr


run in k8s (minikube):
eval $(minikube docker-env)
docker build -t springboot-jwt-authr .
kubectl apply -f k8s.yaml



