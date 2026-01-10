# 📊 AWS Serverless Survey Monitoring Project

> **A Collaborative Project by [Rahul Joshi](https://www.linkedin.com/in/rahul-joshi7) & [Rohini Gusain](https://www.linkedin.com/in/rohini-gusain)**

A cloud-native serverless solution built on AWS infrastructure leveraging S3, API Gateway, Lambda, CloudWatch, and SNS. It captures survey feedback, monitors system metrics, provides data visualization, and dispatches email notifications during high submission activity.

---

## 🔧 Tech Stack

| AWS Service       | Purpose                                                      |
|-------------------|--------------------------------------------------------------|
| Amazon S3         | Hosts static website (survey form)                           |
| API Gateway       | Exposes HTTP endpoint to handle form submissions             |
| AWS Lambda        | Processes submissions, logs custom metrics                   |
| Amazon CloudWatch | Tracks latency, submission count, logs, and dashboards       |
| Amazon SNS        | Sends email alert if more than 5 submissions in 1 minute     |

---

## 🌐 How It Works

1. **User Access** - Survey website hosted on **Amazon S3**
2. **Form Submission** - Request sent via **API Gateway**
3. **Processing** - **AWS Lambda** function triggered
4. **Logging** - Lambda logs submission data and latency to **CloudWatch**
5. **Alerting** - **SNS** sends email if 5+ submissions in 1 minute

---

## 📈 Example Metrics

- `submission_count`: **28**
- `avg_latency`: **0.00006151**
- `invocation_count`: **4**
- Submissions for Yellow: **5** (7.94%)

---

## 📬 Alert Condition

If 5 or more submissions are received in a single minute, **SNS** triggers an email alert to notify potential spamming or peak load activity.

---

## 📁 Project Structure

```
aws-serverless-survey/
├── lambda/                # Lambda function code
│   └── lambda_function.py
├── s3_website/            # Static website files (HTML/CSS/JS)
│   ├── index.html
│   ├── survey.html
│   ├── thankyou.html
│   └── styles.css
├── api_gateway/           # API Gateway configuration or setup notes
│   └── setup.md
├── cloudwatch/            # CloudWatch screenshots (monitoring)
│   ├── Screenshot 2025-06-11 123031.png
│   ├── Screenshot 2025-06-11 123131.png
│   ├── Screenshot 2025-06-11 123204.png
│   └── Screenshot 2025-06-11 144739.png
├── sns/                   # SNS setup steps
│   └── sns_alert_setup.md
└── README.md              # This documentation file
```

---

## 📸 CloudWatch Monitoring Screenshots

Real-time monitoring of the AWS survey website:

| Metric View | Latency Tracking |
|-------------|------------------|
| ![Metric View](cloudwatch/Screenshot%202025-06-11%20123031.png) | ![Latency Tracking](cloudwatch/Screenshot%202025-06-11%20123131.png) |

| Submissions Count | SNS Alert Trigger |
|-------------------|-------------------|
| ![Submissions Count](cloudwatch/Screenshot%202025-06-11%20123204.png) | ![SNS Alert](cloudwatch/Screenshot%202025-06-11%20144739.png) |

---

## ✉️ SNS Email Sample

> 🔔 **Alert:** More than 5 submissions received in the past minute.  
> Please review traffic activity on your survey page.

---

## 🚀 Conclusion

This project demonstrates a fully serverless application using AWS cloud services. It showcases frontend hosting, serverless compute, real-time metrics logging, alerting, and observability — all managed without traditional servers.

---

## 👥 Contributors

<table>
  <tr>
    <td align="center">
      <strong>Rahul Joshi</strong><br>
      📧 <a href="mailto:rahuljoshisg@gmail.com">rahuljoshisg@gmail.com</a><br>
      🔗 <a href="https://www.linkedin.com/in/rahul-joshi7">LinkedIn</a>
    </td>
    <td align="center">
      <strong>Rohini Gusain</strong><br>
      📧 <a href="mailto:gusainrohini@gmail.com">gusainrohini@gmail.com</a><br>
      🔗 <a href="https://www.linkedin.com/in/rohini-gusain">LinkedIn</a> | 
      <a href="https://github.com/Rohini-09">GitHub</a>
    </td>
  </tr>
</table>

---

**⭐ If you found this project helpful, please consider giving it a star!**

