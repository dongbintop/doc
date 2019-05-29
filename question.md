namespace delete is not work

kubectl patch crd clusters.rook.io -p '{"metadata":{"finalizers": []}}' --type=merge