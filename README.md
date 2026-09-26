Docker
Python is an interpreted language.

Your source file is app.py
Python reads that file at runtime
It interprets the code line by line
It uses the Python runtime installed in the container

Go
Go is a compiled language.

You write Go source code
You run go build
That generates a native binary executable for the target OS/architecture
The binary can then be run directly
No runtime dependencies needed inside the container

service.yaml
port: x other Pods/services in the cluster reach this Service at my-service:x (or its ClusterIP on port x)
targetPort: y means: when the Service receives that traffic on port x, it forwards it to port y on the Pod's container — because that's the actual port your application inside the container is listening on