# Application Load Balancer (ALB) Setup

## Step 1: Create ALB
1. Go to **EC2 → Load Balancers → Create Load Balancer**.
2. Select **Application Load Balancer**.
3. Name: `my-alb`
4. Scheme: **Internet-facing**
5. IP Address Type: **IPv4**
6. Select at least **two public subnets** in different AZs.

---

## Step 2: Configure Listeners
- Add **HTTP (80)** listener.
- (Optional) Add **HTTPS (443)** listener if SSL certificate is available.

---

## Step 3: Configure Security Group
- Attach ALB security group (allows inbound **HTTP/HTTPS** from the internet).

---

## Step 4: Create Target Group
1. Go to **Target Groups → Create target group**.
2. Choose **Instances** as target type.
3. Name: `my-tg`
4. Protocol: **HTTP**, Port: **80**
5. Health checks:
   - Protocol: HTTP  
   - Path: `/`  
   - Healthy threshold: 2  
   - Unhealthy threshold: 2  

---

## Step 5: Register Targets
- Add backend EC2 instances to the target group.  
- Ensure health check passes before routing traffic.

---

## Step 6: Test ALB
- Copy **DNS name** of ALB from console.
- Paste into browser → should display EC2 web page.
