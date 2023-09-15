# DevOps Test

Esta es mi implementación de la aplicación demo para la prueba de DevOps.

## Diseño de infraestructura en AWS

![Diagrama de Infraestructura](https://i.ibb.co/f1fzvrc/Challenge-DS-Racosta-Ideal-page-0001.jpg)

Diseñé la infraestructura en AWS utilizando las mejores prácticas de despliegue de aplicaciones web en la nube de AWS (Well-Architected Framework), empleando el uso de varias zonas de disponibilidad para obtener alta disponibilidad en nuestras cargas de trabajo. Dentro de los servicios utilizados están:

- EKS para el manejo de nuestro clúster de Kubernetes.
- EC2 para los nodos workers de nuestro clúster de Kubernetes.
- Route53 para el manejo de los registros DNS para nuestros servicios desplegados.
- Elastic Load Balancer para asignar un punto de entrada para nuestro Ingress.
- RDS para almacenar nuestra base de datos en modo multi-zona de disponibilidad para que nuestra base de datos sea redundante y a prueba de fallos.
- NAT Gateway para el acceso a Internet de nuestros nodos workers para descargar las imágenes de Docker desde Docker Hub.
- CloudWatch para monitorear el consumo de los recursos.
- SNS para enviar notificaciones para alertar a los administradores de la infraestructura.
- AWS WAF para proteger nuestros endpoints de los ataques conocidos.

## Tecnologías Utilizadas

Para la ejecución de este proyecto utilicé:

- Terraform
- Python
- Docker
- Github
- Github Actions
- Bash Script
- Microk8s como distribución de Kubernetes
- Nginx Ingress

Diseñé 2 pipelines en github actions, uno para el CI donde se prueba el codigo y se realiza el escanero de voulnerabilidades y se crea la imagen de docker luego es subida al repositorio en docker hub. Otro para el CD donde se aplican los cambios en el manifiesto via kubectl.

## Repositorios y Documentos

- [Docker Image](https://hub.docker.com/r/xkingrd/ds-challenge)
- [Terraform IAC Repo](https://github.com/rancesking/Challenge-DS-infra)
- [Manifiesto de K8s](https://github.com/rancesking/Challenge-DS-infra/blob/main/kube/deploy.yml)
- [CI Github Action](https://github.com/rancesking/Challenge-DS/blob/main/.github/workflows/CI.yml)
- [CD Github Action](https://github.com/rancesking/Challenge-DS-infra/blob/main/.github/workflows/deploy.yml)

## Uso

Consulta la documentación del código fuente en
[Devsu demo-devops-python](https://bitbucket.org/devsu/demo-devops-python/src/master/)

## Licencia

Copyright © 2023 Devsu. Todos los derechos reservados.
