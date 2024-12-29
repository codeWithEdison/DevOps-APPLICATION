
# DevOps Environment Preparation and Linux System Administration

## Part 1: Key Terms and Concepts

### Key Definitions

1. **Server**: A computer or system that provides resources, services, or data to other computers (clients) over a network. Servers can be physical machines or virtual instances.

2. **Linux**: An open-source operating system kernel that forms the foundation of many distributions (distros). It's widely used in server environments due to its stability, security, and flexibility.

3. **DevOps**: A set of practices combining software development (Dev) and IT operations (Ops) to shorten the development lifecycle while delivering high-quality software continuously.

4. **DevSecOps**: An extension of DevOps that integrates security practices throughout the development pipeline, making security an active consideration from the start rather than an afterthought.

5. **Container**: A lightweight, standalone package that includes everything needed to run a piece of software, including code, runtime, system tools, and libraries.

6. **Node**: A machine (physical or virtual) in a network that can run containers or services. In container orchestration, nodes form clusters that work together.

7. **Infrastructure as Code (IaC)**: Managing and provisioning infrastructure through code rather than manual processes. Popular tools include Terraform and Ansible.

8. **IaaS (Infrastructure as a Service)**: Cloud computing service providing virtualized computing resources over the internet, like AWS EC2 or Google Compute Engine.

9. **CI/CD**: Continuous Integration and Continuous Delivery/Deployment - automated practices for frequently integrating code changes and delivering them to production.

## Part 2: Linux Distributions and Installation

### Common Linux Distributions

1. **Ubuntu Server**
   - Popular for cloud deployments
   - Large community support
   - Regular LTS (Long Term Support) releases

2. **Red Hat Enterprise Linux (RHEL)**
   - Enterprise-grade distribution
   - Excellent support and security
   - Popular in corporate environments

3. **CentOS**
   - Free alternative to RHEL
   - Stable and reliable
   - Common in web hosting

### Installation Steps
1. Choose installation media (USB/ISO)
2. Configure partitioning
3. Set up networking
4. Configure base system
5. Install required packages

## Part 3: Essential Linux Commands

### System Information
```bash
uname -a          # System and kernel information
lsb_release -a    # Distribution information
df -h             # Disk usage
free -h           # Memory usage
top               # Process monitoring
```

### File and Directory Management
```bash
ls -la            # List files with details
mkdir dirname     # Create directory
cp source dest    # Copy files
mv source dest    # Move/rename files
rm -rf dirname    # Remove directory
chmod 755 file    # Change permissions
```

### Text Processing
```bash
cat file          # Display file content
grep pattern file # Search for pattern
sed 's/old/new/g' # Stream editor
awk '{print $1}'  # Text processing
vim filename      # Text editor
```

### Process Management
```bash
ps aux            # List processes
kill pid          # Terminate process
systemctl status  # Service status
htop              # Process monitor
```

## Part 4: Server Services Management

### Web Server (Apache/Nginx)
```bash
# Apache installation
sudo apt install apache2
sudo systemctl start apache2

# Basic configuration
sudo vim /etc/apache2/apache2.conf
```

### SSH Server
```bash
# Installation
sudo apt install openssh-server

# Configuration
sudo vim /etc/ssh/sshd_config

# Key management
ssh-keygen -t rsa -b 4096
```

### DNS Server (BIND)
```bash
# Installation
sudo apt install bind9

# Configuration
sudo vim /etc/bind/named.conf
```

### Mail Server (Postfix)
```bash
# Installation
sudo apt install postfix

# Basic configuration
sudo vim /etc/postfix/main.cf
```

