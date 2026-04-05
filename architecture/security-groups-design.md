# Security Group Design Architecture

1. **bastion-sg**: Allows SSH (22) from My IP.
2. **web-tier-sg**: Allows HTTP (80) from anywhere. Allows SSH (22) from bastion-sg.
3. **app-tier-sg**: Allows TCP (8080) from web-tier-sg. Allows SSH (22) from bastion-sg.
4. **database-sg**: Allows MySQL (3306) from app-tier-sg. Allows SSH (22) from bastion-sg.
