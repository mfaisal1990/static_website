# <p align="center">Deployment of Fully Secure and Serverless Static Website Hosting Using AWS S3, CloudFront, Route 53 & ACM</p>
<p align="center"><img src="https://github.com/mfaisal1990/static_website/blob/main/asset/architecture.jpg?raw=true"></p>
<p align="center">Architecture Diagram of Hosting my Professional Portfolio Website using AWS S3, Route 53, Cloudfront and ACM</p>

## Features

<h4>1. Secure and Scalable Static Web Hosting</h4>
Hosted a fully static website using Amazon S3, ensuring high availability and durability.<br>
Utilized S3’s static website hosting feature to serve HTML, CSS, JavaScript, and image files efficiently.

<h4>2. Custom Domain Configuration</h4>
Registered a custom domain using Amazon Route 53.<br>

<h4>3. Domain Privacy and WHOIS Protection</h4>
Enabled WHOIS privacy protection to prevent exposure of personal details used during domain registration.

<h4>4. HTTPS Enabled with SSL</h4>
Requested and provisioned a free SSL certificate using AWS Certificate Manager (ACM).<br>
Set up the corresponding CNAME record and associated it with the ACM-issued SSL certificate to enable secure HTTPS access, improving user trust and SEO compatibility.

<h4>5. Optimized Content Delivery with CloudFront</h4>
Integrated Amazon CloudFront as a Content Delivery Network (CDN) to cache and distribute website content globally with low latency.<br>

<h4>6. Improved Performance and SEO</h4>
Leveraged CloudFront’s edge locations for faster content delivery across different regions.<br>
Enforced HTTPS and redirected HTTP traffic to secure connections for better search engine optimization and data privacy.

<h4>7. Cache Invalidation</h4>
Performed cache invalidations as needed during website updates to ensure delivery of the latest content.

<h4>8. Mapping CNAME and A Records in Route 53</h4>
Configured the domain in the Route 53 Hosted Zone by mapping an Alias (A) record to the CloudFront distribution for seamless global access with low latency. 

<h4>9. Cost-Efficient Hosting Solution</h4>
Took advantage of AWS’s pay-as-you-go model for S3 and CloudFront to keep hosting affordable for personal or portfolio projects.

<h4>10. Fully Serverless Architecture</h4>
Achieved a 100% serverless deployment with no need to manage or maintain backend servers, resulting in reduced operational overhead.

## Tech Stack

- AWS S3 --> Static content hosting
- AWS Route 53 --> DNS management and domain registration
- AWS Cloudfront --> CDN for performance and global distribution
- AWS Certificate Manager --> SSL/TLS for HTTPS support

## Deployment Steps

<h4>1. Create an S3 Bucket</h4>
Go to AWS S3 and create a bucket named exactly as your domain (e.g., example.com)<br>
Uncheck “Block all public access”<br>
Enable Static website hosting<br>
Upload your website files (HTML, CSS, JS)

<h4>2. Set Bucket Policy for Public Access</h4>
Paste the following policy under the bucket permissions:<br>

{<br>
  "Version": "2012-10-17",<br>
  "Statement": [<br>
    {<br>
      "Sid": "PublicReadGetObject",<br>
      "Effect": "Allow",<br>
      "Principal": "*",<br>
      "Action": "s3:GetObject",<br>
      "Resource": "arn:aws:s3:::example.com/*"<br>
    }<br>
  ]<br>
}

<h4>3. Request SSL Certificate</h4>
Navigate to AWS Certificate Manager (ACM)<br>
Select N. Virginia (us-east-1) region<br>
Request a public certificate for your domain (e.g., example.com, www.example.com)<br>
Complete DNS validation via Route 53

<h4>4. Create a CloudFront Distribution</h4>
Origin domain: your S3 bucket static website endpoint (not the REST API endpoint)<br>
Viewer protocol policy: Redirect HTTP to HTTPS<br>
Alternate domain name (CNAME): example.com<br>
Attach the certificate from ACM (N. Virginia)<br>

<h4>5. Set Up Route 53 (DNS)</h4>
Register a domain or use an existing one in Route 53<br>
Create an A record:<br>
Record type: A – IPv4 address<br>
Routing policy: Simple<br>
Alias: Yes<br>
Alias Target: your CloudFront distribution URL

<h4>6. Test the Deployment</h4>
Visit https://your-domain.com<br>
Ensure it loads over HTTPS and serves from CloudFront
