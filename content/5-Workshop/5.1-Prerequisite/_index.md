---
title: "Environment Setup"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

#### Requirements

| Item | Version / notes |
| --- | --- |
| **Node.js** | 18 or later |
| **npm** | Bundled with Node |
| **AWS CLI** | Configured profile (`aws configure` or `npx ampx configure profile`) |
| **Region** | `ap-southeast-1` (Singapore) |
| **Git** | Clone public repo |

#### Clone source code

```powershell
git clone https://github.com/DHgLang/Movie-Ticket-Booking-Platform.git
cd Movie-Ticket-Booking-Platform
npm install
```

After cloning and installing dependencies, the main folders are `amplify/` (backend), `frontend/` (React), and `scripts/` (deploy).

![Project structure](/images/5-Workshop/5.1-Prerequisite/project-structure.png)

#### Verify environment

```powershell
node -v
aws sts get-caller-identity
```

Run `node -v` to confirm Node.js ≥ 18 — for example `v20.15.0` as shown below.

![Node.js version](/images/5-Workshop/5.1-Prerequisite/node-version.png)

The `aws sts get-caller-identity` command returns Account ID, ARN, and UserId — proof that AWS CLI is logged in with the correct profile.

![AWS CLI identity](/images/5-Workshop/5.1-Prerequisite/aws-cli.png)

Check that the default region in `~/.aws/config` is `ap-southeast-1` (Singapore) to match the sandbox deployment.

![AWS region ap-southeast-1](/images/5-Workshop/5.1-Prerequisite/aws-region.png)

#### Environment variables

After `npm install`, copy the example file:

```powershell
copy .env.example .env
notepad .env
```

| Variable | Purpose |
| --- | --- |
| `VITE_API_URL` | API Gateway URL (after `npm run sandbox`) |
| `VITE_TMDB_API_KEY` | TMDB poster API key |
| `TMDB_API_KEY` | Same key for Lambda |
| `VNPAY_TMN_CODE`, `VNPAY_HASH_SECRET` | VNPay sandbox (payment testing) |
| `FRONTEND_URL`, `VNPAY_RETURN_URL` | Payment callback URLs |

The `.env` file holds API URL, TMDB keys, and VNPay credentials — redact sensitive values before taking screenshots.

![.env file (secrets redacted)](/images/5-Workshop/5.1-Prerequisite/env-file.png)

{{% notice info %}}
**Note:** Do not commit `.env` or `amplify_outputs.json` to GitHub — they are listed in `.gitignore`.
{{% /notice %}}

#### Minimum IAM permissions (guidance)

Your AWS account needs permissions to deploy Amplify sandbox: CloudFormation, Lambda, API Gateway, DynamoDB, SQS, Cognito, S3, IAM (pass role), CloudWatch. FCJ lab accounts typically include a pre-configured policy.

**Next step**

When ready → [5.2 Backend Deployment](../5.2-Backend/)
