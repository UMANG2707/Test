# **Branching Strategy for CI/CD**

This repository follows a structured branching strategy to manage multiple clients, versions, and environments efficiently.

---

## **Branching Structure**

Each **Client (C1, C2, C3, ...)** has a dedicated branch.  
Within each client branch, multiple **Version (V1, V2, V3, ...)** branches exist to manage different software versions.  
Each version contains **Feature directories (Register, Login, Logout)**, and inside each feature, there are **environment-specific directories (PROD, TEST, UAT)** containing configuration files.

![Uploading image.png…]()
