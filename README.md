# DevOps Test

Esta es mi implementacion de la aplicacion demo para la prueba de Devops.

## Diseño de infraestructura en AWS
<p align="center">
<img src="https://i.ibb.co/f1fzvrc/Challenge-DS-Racosta-Ideal-page-0001.jpg">
</p>

Diseñe la infraesctura en AWS utilizando las mejores practicas de desplegue de aplicaciones web en la nube de AWS (well architected framework) empleando el uso de varias zonas ded disponibilidad para obtener alta disponibilidad en nuestras cargas de trabajo. Dentro de los servicios utilizados estan: 
EKS para el manejo de nuestro cluster de kubernetes.
EC2 para los nodos workers de nuestro cluster de kubernetes.
Route53 para el manejo de los records DNS para nuestros servicios desplegados.
Elastic Load Balancer para asignar un punto de entrada para nuestro ingress.
RDS para almacenar nuestra base de datos en modo multi-az para que nuestra base de datos sera redundante y aprueba de fallas.
NAT Gateway para el acceso a internet de nuestros nodos workers para descargar las images de docker desde dockerhub.
CloudWatch para monitorear el consumo de los recursos.
SNS para enviar notificaciones para alertar a los adminsitradores de la infraestructura.
AWS WAF para proteger nuestros endpoints de los ataques conocidos.

## Tecnologias Utilizadas
Para la ejecución de este proyecto utilice:
Terraform
Python
Docker
Github
Github Actions
Bash Script
Microk8s como distro de Kubernetes
Nginx ingress

## Repositorios
[Docker image](https://hub.docker.com/r/xkingrd/ds-challenge)
[Terraform IAC Repo](https://github.com/rancesking/Challenge-DS-infra)

## Usage

Refers to source code documentation on
[Devsu demo-devops-python](https://bitbucket.org/devsu/demo-devops-python/src/master/)

## License

Copyright © 2023 Devsu. All rights reserved.
