provider "aws" {
  region = "us-east-1"
}

resource "aws_instance" "example_instance" {
  ami = "ami-04e914639d0cca79a"
  instance_type = "t2.micro"
  key_name = "user1"
  monitoring = true
  vpc_security_group_ids = ["sg-12345678"]
  subnet_id = "subnet-eddcdzz4"
  tags = {
    Terraform = "true"
    Environment = "dev"
  }
}