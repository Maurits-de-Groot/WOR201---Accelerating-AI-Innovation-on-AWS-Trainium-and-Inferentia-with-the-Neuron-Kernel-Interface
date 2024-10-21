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
7. Navigate to [EC2->Instances](https://us-west-2.console.aws.amazon.com/ec2/home?region=us-west-2#Instances:) and find the instance DNS name
8. Open your terminal and run the following commands:
    
    `cd <whatever folder you saved the key>`

    `chmod 400 "ws-default-keypair.pem"`

    `ssh -i "ws-default-keypair.pem" ubuntu@<instance DNS name> -L 8888:127.0.0.1:8888`

9. (on the instance) run `source /opt/aws_neuron_venv_pytorch/bin/activate`
10. (on the instance) run `python -m pip install --upgrade neuronx-cc==2.* torch-neuronx==1.13.* torchvision`
11. (on the instance) run `git clone <this repo>`
12. (on the instance) run `jupyter-lab` and access the server

### Workshop time
Open `0-setup.ipynb` and follow the notebook
