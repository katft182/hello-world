# hello-world

Run ansible in colaboratory

%cd /content
%rm -rf hello-world
!pip3 install --user ansible
!git clone -l -s https://github.com/katft182/hello-world.git hello-world
%cd hello-world/ansible
!/root/.local/bin/ansible-playbook main.yml

Get the aws instance ip
aws ec2 describe-instances --query 'Reservations[*].Instances[*].PublicIpAddress' --filters "Name=tag:Project,Values=KatyUdacity" --output text >> inventory 