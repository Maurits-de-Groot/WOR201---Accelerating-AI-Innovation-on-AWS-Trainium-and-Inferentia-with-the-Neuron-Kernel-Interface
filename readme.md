WOR201 - Accelerating AI Innovation on AWS Trainium and Inferentia with the Neuron Kernel Interface
---
AWS Deep Dive Days - Generative AI is a three-day in-person event for builders, tech and business leaders that are interested in Generative AI. Let's build connections and learn some practical knowledge together.

### Setup

1. Go to https://catalog.us-east-1.prod.workshops.aws/join
> Ensure to log out of any open AWS accounts or use a private window
2. Enter the event access code (see screen)
3. Carefully review the terms and conditions before joining the event
4. Press `Get EC2 SSH key` on the bottem left
5. Download the key pair
6. Press `Open AWS console (us-west-2)` on the bottem left
7. Navigate to [EC2->Instances](https://us-west-2.console.aws.amazon.com/ec2/home?region=us-west-2#Instances:) and press "Launch Instances"
8. Create an instance with the following settings:

    Name: does not matter (i.e, `NeuronWorkshop`)

    AMI: `Deep Learning AMI Neuron (Ubuntu 22.04)`

    Instance type: `inf2.xlarge`

    Key pair name: `ws-default-keypair`

9. Find the instance DNS name of the instance you just created
10. Open your terminal and run the following commands:
    
    `cd <whatever folder you saved the key>`

    `chmod 400 "ws-default-keypair.pem"`

    `ssh -i "ws-default-keypair.pem" ubuntu@<instance DNS name> -L 8888:127.0.0.1:8888`

11. (on the instance) run `source /opt/aws_neuronx_venv_pytorch_2_1/bin/activate`
12. (on the instance) run `git clone https://github.com/Maurits-de-Groot/WOR201---Accelerating-AI-Innovation-on-AWS-Trainium-and-Inferentia-with-the-Neuron-Kernel-Interface.git`
13. (on the instance) run `jupyter-lab` and access the server

### Workshop time
Open `0-setup.ipynb` and follow the notebook
