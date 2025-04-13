# Consul Crash Course

Deploy HashiCorp Consul service mesh on Amazon EKS with this production-ready setup.

## Quick Start

```bash
cd terraform
terraform init && terraform apply
aws eks update-kubeconfig --name myapp-eks-cluster --region <your-region>
helm install consul hashicorp/consul -f kubernetes/consul-values.yaml
```

## Project Structure

```
.
├── kubernetes/           # Consul and K8s configs
│   ├── config-consul.yaml
│   ├── consul-values.yaml
│   └── intentions.yaml
└── terraform/           # Infrastructure code
    ├── main.tf
    └── variables.tf
```

## Features

- EKS cluster with 3 t2.small nodes
- Multi-AZ VPC with private/public subnets
- Consul service mesh with intentions and service resolution
- EBS CSI Driver for storage

## Prerequisites

- AWS CLI, Terraform >= 1.0, kubectl, Helm 3.x

## License

MIT License
