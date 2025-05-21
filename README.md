# <p align="center">Deployment of Fully Secure and Serverless Static Website Hosting Using AWS S3, CloudFront, Route 53 & ACM</p>
<p align="center"><img src="https://github.com/mfaisal1990/static_website/blob/main/asset/architecture.jpg?raw=true"></p>
<p align="center">Architecture Diagram of Hosting my Professional Portfolio Website using AWS S3, Route 53, Cloudfront and ACM</p>

## Features

<h4>1. Secure and Scalable Static Web Hosting</h4>
Hosted a fully static website using Amazon S3, ensuring high availability and durability.<br>
Utilized S3’s static website hosting feature to serve HTML, CSS, JavaScript, and image files efficiently.

<h4>2. Custom Domain Configuration</h4>
Registered or managed a custom domain using Amazon Route 53.<br>
Mapped the domain to the S3 bucket using Alias or A records for seamless access through a user-friendly URL.

<h4>3. HTTPS Enabled with SSL</h4>
Requested and provisioned a free SSL certificate using AWS Certificate Manager (ACM).<br>
Secured the website with HTTPS, improving user trust and SEO compatibility.

<h4>4. Optimized Content Delivery with CloudFront</h4>
Integrated Amazon CloudFront as a Content Delivery Network (CDN) to cache and distribute website content globally with low latency.<br>
Configured CloudFront origin to point to the S3 bucket with custom error pages and caching rules.

<h4>5. Improved Performance and SEO</h4>
Leveraged CloudFront’s edge locations for faster content delivery across different regions.<br>
Enforced HTTPS and redirected HTTP traffic to secure connections for better search engine optimization and data privacy.

<h4>6. Domain Privacy and WHOIS Protection</h4>
Enabled WHOIS privacy protection to prevent exposure of personal details used during domain registration.

<h4>7. Cache Invalidation and TTL Configuration</h4>
Applied cache settings with defined Time-to-Live (TTL) values in CloudFront to control content freshness.<br>
Performed cache invalidations as needed during website updates to ensure delivery of the latest content.

<h4>8. Cost-Efficient Hosting Solution</h4>
Took advantage of AWS’s pay-as-you-go model for S3 and CloudFront to keep hosting affordable for personal or portfolio projects.

<h4>9. Fully Serverless Architecture</h4>
Achieved a 100% serverless deployment with no need to manage or maintain backend servers, resulting in reduced operational overhead.

## Technologies Used

- AWS S3
- AWS Route 53
- AWS Cloudfront
- AWS Certificate Manager
