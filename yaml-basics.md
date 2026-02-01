# YAML Basics for Operators

*Built for operators. Maintained in the open.*

Essential YAML fundamentals for working safely with Kubernetes and OpenShift manifests.
Focused on structure, indentation, and patterns you will see in real environments.


---

## YAML Survival Rules

 ✔ Use spaces only (never tabs)
 
 ✔ Be consistent with indentation (commonly 2 spaces)
 
 ✔ Indentation defines structure
 
 ✔ Case-sensitive keys
 
 ✔ When in doubt, align with the parent key

 ---

## Basic Key / Value Structure
 
```bash
key: value
string: hello
number: 42
boolean: true
```

## Nested Objects
 
```bash
parent:
  child: value
  another_child: another_value
```

## Lists (Arrays)
 
```bash
ports:
  - 80
  - 443

names:
  - api
  - web
  - worker
```

## Lists of Objects
 
```bash
containers:
  - name: app
    image: nginx
    ports:
      - containerPort: 80
```

## Comments
 
```bash
# This line is ignored by YAML
```

## Multi-line Strings
 
```bash
description: |
  Line one
  Line two
  Line three
```

# ">" folds newlines into spaces
```bash
summary: >
  This becomes
  a single line.
```

## Common Kubernetes / OpenShift Fields
 
```bash
apiVersion: v1
kind: Service
metadata:
  name: hello-service
  labels:
    app: hello

spec:
  selector:
    app: hello
  ports:
    - protocol: TCP
      port: 80
      targetPort: 8080
```

## Indentation Failure Example (DO NOT DO)
 
```bash
  spec:
  selector:
    app: broken
```

---

## Operator Tips

 - YAML errors are usually indentation errors.
   
 - If a manifest won't apply, re-check spacing first.
   
 - Copy working examples and modify incrementally.
   
 - Validate structure with: oc explain <resource>
