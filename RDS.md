# 📘 How to Create a Database in AWS and Link It to an EC2 Instance

1. **Search for “RDS”** in the AWS Management Console.
2. **Choose your preferred database engine**, e.g., **MySQL**.
3. **Select the database version**, e.g., `MySQL 8.0.41`.  
   > ✅ *Tip: Use the latest stable version unless your app requires an older one.*
4. **Choose a template**:
   - Production
   - Dev/Test
   - Free Tier (if eligible)
5. **Select the availability option**:
   - Multi-AZ DB Cluster (3 instances)
   - Multi-AZ DB Instance (2 instances)
   - Single DB Instance (1 instance)
6. **Enter your DB instance identifier** (i.e., database name).
7. **Set the master username**.
8. **Set the master password**, and choose how to manage it (manual or auto-generated).
9. **Choose instance configuration** based on your needs  
   e.g., `t3.micro` for Free Tier.
10. **Select storage type** (e.g., General Purpose SSD)  
    Set storage to at least **20 GB** (required minimum).
11. **Enable storage autoscaling** (optional).
12. **Choose EC2 connectivity option**:
    - Connect automatically to an EC2 instance
    - Or connect manually later
13. **Set public access**:
    - `Yes` to allow external access
    - `No` to restrict to internal VPC access (recommended for production)
14. **Assign a security group** (or create a new one):  
    Ensure port **3306** (MySQL) is allowed from your EC2 instance.
15. **Select database authentication method**:
    - Password
    - Password + IAM DB Authentication
    - Password + Kerberos Authentication (advanced)
16. **Launch the RDS instance.**
17. **SSH into your EC2 instance.**
18. **Update and install the MySQL client**:
    ```bash
    sudo apt update && sudo apt install mysql-client -y
    ```
19. **Connect to your MySQL database** from EC2:
    ```bash
    mysql -u <your-username> -p -h <your-rds-endpoint>
    ```

> ⚠️ Replace `<your-username>` and `<your-rds-endpoint>` with your actual values.
