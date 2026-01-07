# 📸 Screenshots Guide

## How to Add Your Screenshots

Place your screenshots in this folder with the following names:

### Required Screenshots:

1. **01-ec2-instance-running.png**
   - EC2 Dashboard showing your running instance
   - Should show instance ID, state (running), instance type (t2.micro)

2. **02-stress-test-terminal.png**
   - Terminal/SSH session showing stress command running
   - Command: `stress --cpu 2`

3. **03-cloudwatch-cpu-spike.png**
   - CloudWatch metrics graph showing CPU utilization spike
   - Should show the graph going above 70%

4. **04-cloudwatch-alarm-created.png**
   - CloudWatch Alarms page showing your created alarm
   - Should show alarm name, state, and threshold (70%)

5. **05-alarm-email-notification.png**
   - Email screenshot showing SNS notification received
   - Shows alarm triggered message

6. **06-cost-explorer-analysis.png**
   - AWS Cost Explorer dashboard
   - Shows daily/monthly cost breakdown

7. **07-s3-bucket-created.png**
   - S3 console showing your created bucket
   - Shows bucket name and region

8. **08-s3-lifecycle-rule.png**
   - S3 Lifecycle rule configuration
   - Shows transition to Glacier after 30 days

9. **09-ec2-stopped.png**
   - EC2 Dashboard showing instance in stopped state
   - Demonstrates cost-conscious practice

---

## Screenshot Tips:

✅ **DO:**
- Use clear, high-resolution screenshots
- Crop unnecessary parts (browser tabs, personal info)
- Highlight important sections if needed
- Use PNG format for better quality

❌ **DON'T:**
- Include sensitive information (AWS Account ID, Access Keys)
- Use blurry or low-quality images
- Include personal email addresses (blur if needed)

---

## How to Take Screenshots:

### Windows:
- **Full Screen:** Press `Windows + PrtScn`
- **Snipping Tool:** Press `Windows + Shift + S`
- **Specific Window:** Press `Alt + PrtScn`

### After Taking Screenshot:
1. Save with the correct filename (e.g., 01-ec2-instance-running.png)
2. Place in this `screenshots` folder
3. Verify the image appears in the README.md

---

## Alternative: If You Don't Have Screenshots Yet

You can:
1. Re-do the scenario and take screenshots
2. Use placeholder text in README until you have images
3. Add screenshots gradually as you practice

---

**Note:** Screenshots make your GitHub repository more impressive and show recruiters that you actually did the hands-on work!
