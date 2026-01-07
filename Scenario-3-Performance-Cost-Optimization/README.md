# 🔥 Application Performance & Cost Optimization Using AWS

## 📋 Real-World Problem

Startup ka website chal raha hai, but:
- ❌ Slow response aa raha hai
- ❌ AWS bill badh raha hai
- ❌ Monitoring nahi hai

**Client:** "Performance improve karo aur cost kam karo"

## 🎯 Solution

AWS services use karke monitoring aur cost optimization implement kiya:

1. **CloudWatch** se CPU monitoring
2. **CloudWatch Alarms** se automated alerts
3. **Cost Explorer** se cost analysis
4. **S3 Lifecycle** se storage cost 82% reduce
5. **SNS** se email notifications

## 🧰 AWS Services (All Free Tier)

| Purpose | Service | Cost |
|---------|---------|------|
| Compute | EC2 (t2.micro) | Free |
| Monitoring | CloudWatch | Free |
| Alerting | CloudWatch Alarms + SNS | Free |
| Cost Analysis | Cost Explorer | Free |
| Storage Optimization | S3 + Lifecycle | Free |

**Total Cost: $0**

---

## 🛠️ Step-by-Step Implementation

### Step 1: EC2 Instance Launch Kiya

**Kya kiya:**
- EC2 Dashboard open kiya
- New instance launch kiya:
  - AMI: Amazon Linux 2
  - Type: t2.micro (Free Tier)
  - Security: SSH (22) + HTTP (80) allow kiya
- Key pair download kiya

**Screenshot:**

![EC2 Running](./screenshots/01-ec2-instance-running.png)

**Learning:** t2.micro Free Tier mein rehta hai

---

### Step 2: Performance Issue Simulate Kiya

**Kya kiya:**
- SSH se EC2 connect kiya
- Stress tool install kiya:
  ```bash
  sudo yum install stress -y
  ```
- CPU load create kiya:
  ```bash
  stress --cpu 2
  ```

**Screenshot:**

![Stress Test](./screenshots/02-stress-test-terminal.png)

**Purpose:** Real-world high CPU usage test karne ke liye

---

### Step 3: CloudWatch Se Monitor Kiya

**Kya kiya:**
- CloudWatch Console open kiya
- Metrics → EC2 → Per-Instance Metrics
- CPUUtilization metric check kiya
- CPU spike dekha stress test se

**Screenshot:**

![CloudWatch CPU Spike](./screenshots/03-cloudwatch-cpu-spike.png)

**Learning:** CloudWatch 5-minute intervals mein metrics deta hai (Free Tier)

---

### Step 4: CloudWatch Alarm Create Kiya

**Kya kiya:**
- CloudWatch mein new alarm banaya
- Settings:
  - Metric: CPUUtilization
  - Condition: Greater than 70%
  - Period: 5 minutes
  - Action: SNS email notification
- Email subscription verify kiya

**Screenshots:**

![Alarm Created](./screenshots/04-cloudwatch-alarm-created.png)

![Email Notification](./screenshots/05-alarm-email-notification.png)

**Learning:** Proactive monitoring se problems pehle pata chal jati hain

---

### Step 5: Cost Analysis Kiya

**Kya kiya:**
- AWS Billing Dashboard open kiya
- Cost Explorer access kiya
- Check kiya:
  - Daily costs
  - Service-wise breakdown
  - Free Tier usage

**Screenshot:**

![Cost Explorer](./screenshots/06-cost-explorer-analysis.png)

**Learning:** Regular cost monitoring zaroori hai

---

### Step 6: S3 Storage Optimize Kiya

**Kya kiya:**
- S3 bucket create kiya
- Sample files upload kiye
- Lifecycle Rule banaya:
  - 30 days baad Glacier mein move
  - 90 days baad delete (optional)

**Screenshots:**

![S3 Bucket](./screenshots/07-s3-bucket-created.png)

![Lifecycle Rule](./screenshots/08-s3-lifecycle-rule.png)

**Cost Savings:**
- S3 Standard: $0.023 per GB
- S3 Glacier: $0.004 per GB
- **Savings: 82%**

---

### Step 7: Resources Cleanup (IMPORTANT!)

**Kya kiya:**
- EC2 instance stop kiya
- Unused resources check kiye
- Documentation kiya

**Screenshot:**

![EC2 Stopped](./screenshots/09-ec2-stopped.png)

**Learning:** Unused resources stop karna = Cost-conscious DevOps mindset

---

## 📊 Results

### Performance
- ✅ Real-time monitoring enabled
- ✅ CPU > 70% par automated alert
- ✅ Proactive issue detection

### Cost Optimization
- ✅ 82% storage cost reduction
- ✅ Proper resource management
- ✅ Free Tier maximize kiya

### Skills Demonstrated
- ✅ Monitoring & Observability
- ✅ Cost Awareness
- ✅ Automation
- ✅ Problem-solving
- ✅ Documentation

---

## 🎓 Key Learnings

1. **Monitoring First** - Measure karo tabhi optimize kar sakte ho
2. **Automate Everything** - Alarms aur lifecycle policies manual work reduce karte hain
3. **Cost Conscious** - Practice ke baad resources cleanup karo
4. **Free Tier is Powerful** - Real projects bina paisa kharch kiye ban sakti hain
5. **Documentation Matters** - Learning aur showcase dono ke liye zaroori

---

## 📝 Commands Reference

```bash
# Stress tool install
sudo yum install stress -y

# CPU load create (2 cores)
stress --cpu 2

# Stop stress test
Ctrl + C

# CPU usage check
top
```

---

## 🔗 AWS Documentation Links

- [CloudWatch Documentation](https://docs.aws.amazon.com/cloudwatch/)
- [Cost Optimization Best Practices](https://aws.amazon.com/pricing/cost-optimization/)
- [S3 Lifecycle Policies](https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html)

---

**Date:** [Apni date add karo]

**Status:** ✅ Completed

---

[← Back to Main](../README.md)
