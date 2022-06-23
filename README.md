### Instruction on how to build VPC 

### Please copy paste below code 
```
module "vpc" {
    source  = "yiitkarakaya/vpc-5/aws"
    cidr_block      = "10.0.0.0/16"
    public_subnet1  = "10.0.1.0/24"
    public_subnet2  = "10.0.2.0/24"
    public_subnet3  = "10.0.3.0/24"
    private_subnet1 = "10.0.101.0/24"
    private_subnet2 = "10.0.102.0/24"
    private_subnet3 = "10.0.103.0/24"
    region          = "us-east-1"
    tags = {
        Name = "main"
    }
}
```
### To get the output, please add the following code 
```

output  vpc_id {
    value = module.vpc.vpc_id
}

output  public_subnet1 {
    value = module.vpc.public_subnet1
}

output  public_subnet2 {
    value = module.vpc.public_subnet2
}

output  public_subnet3 {
    value = module.vpc.public_subnet3
}
```