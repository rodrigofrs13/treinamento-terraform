# Treinamentos  Terraform

Colocar ✔ quando concluído. 

##  ✔ Descomplicando o Terraform | HashiWeek
- https://www.youtube.com/watch?v=4FellihAcV8

  

## Lucas de Souza - Terraform além do básico | #FiqueEmCasaConf

- https://www.youtube.com/watch?v=P3aY4_vxzWQ&t=243s

- https://github.com/souzaxx/terraform-alem-do-basico

  

##  Melhores práticas para seu pipeline de Infra as Code
- https://www.youtube.com/watch?v=XGSuK8kyGag

  

## O que é IaaS e IaC e o porquê isso é tão importante para nós! | IaaSWeek
- https://www.youtube.com/watch?v=Tloaql2twe0



## Rafael Gomex - Melhores práticas para seu pipeline de Infra as Code | #FiqueEmCasaConf
- https://www.youtube.com/watch?v=XGSuK8kyGag&t=1s

  

## Descomplicando o Terraform | HashiWeek
- https://www.youtube.com/watch?v=4FellihAcV8&t=4s
- https://www.youtube.com/watch?v=8mRZJcCgoS0
- https://www.youtube.com/watch?v=lrAycU7_XnQ

## LinuxTips
## HASHICORP EXPERT
- https://www.youtube.com/watch?v=c45vNgMphQs

## Oficial
- https://learn.hashicorp.com/terraform

## Acloudguru
- Deploying to AWS with Terraform and Ansible
- HashiCorp Certified Terraform Associate

# Anotações

**Hashicorp Configuration Language** (**HCL**)

**Bloco Data** - coletar uma informação - recurso que já existe no Provider

```yaml
# ---------------------------------------------------------------------------------------------------------------------
data "aws_ami" "consul" {
  most_recent = true  ## Sempre a informação mais recente

  # If we change the AWS Account in which test are run, update this value.
  owners = var.owners ## Pegue a AMI cujo o dono seja "var.owners"

  filter {
    name   = "virtualization-type"
    values = ["hvm"]
  }

  filter {
    name   = "is-public"
    values = ["false"]
  }

  filter {
    name   = "name"
    values = ["consul-ubuntu-*"]
  }
}
```

Local name não é o nome da maquina, mas sim o nome de referencia no terraform

![image-20210531213602994](C:\Users\roee\OneDrive - GFT Technologies SE\Documents\RODRIGO\ESTUDOS\Terraform\terraform\Imagens\image-20210531213602994.png)

# Comandos Terraform



|              Comando              | Descrição                                                    |
| :-------------------------------: | :----------------------------------------------------------- |
|        terraform **init**         | Inicializa o ambiente com o provider utilizado.Por exemplo, se você estiver utilizando o **provider "aws"**, inicializa o plugin para Amazon Web Services. |
|        terraform **apply**        | Este comando que cria e altera as Instâncias/Objetos no Provider de acordo com o seu terraform. |
|        terraform **plan**         | Mostra o plano de execução do terraform.                     |
|       terraform **destroy**       | Este comando para as Instâncias/Objetos em execução e destruindo todos os recursos que foram criados durante o processo de criação. |
|        terraform **show**         | Mostra um resumo do status da sua infraestrutura terraform.  |
|       terraform **output**        | Mostra um valor de uma variável output                       |
|    terraform **init -upgrade**    | UPgrade de pacots                                            |
|    terraform **plan -destroy**    | informa o plano de destruição                                |
| terraform **apply -auto-approve** | Cria infra automático sem perguntar                          |

# Best Pratices

![image-20210531213708639](./Imagens/image-20210531213708639.png)
