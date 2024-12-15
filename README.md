# Event-Driven-Architecture-for-Email-Notifications-on-S3-Uploads
Designed and implemented a robust event-driven architecture using AWS services to automate email notifications for object uploads in Amazon S3. The system is built using Amazon S3, AWS Lambda, Amazon SNS, and CloudWatch, leveraging their capabilities to create a seamless, scalable, and cost-effective solution.

When an object is uploaded to a designated S3 bucket, an S3 Event Notification triggers an AWS Lambda function. This function processes metadata such as the object name, size, and timestamp, and formats it into a message. The Lambda function then publishes this message to an Amazon SNS topic, which acts as the messaging layer. SNS distributes the notification to all subscribed users via email, ensuring stakeholders are promptly informed of the upload event.

CloudWatch enhances the solution by providing comprehensive monitoring and logging. Logs from the Lambda function track execution status and assist in debugging. CloudWatch Alarms are set up to monitor key metrics, including Lambda errors, invocation duration, and throttling, ensuring smooth operations.

This architecture is serverless and scales automatically to handle varying workloads, making it ideal for environments with unpredictable or fluctuating upload activity. The pay-as-you-go model of AWS ensures cost-effectiveness, especially in scenarios with low to moderate activity.

Key features include robust error handling in Lambda for retries and failures, role-based access control for secure interactions between S3, SNS, and Lambda, and customizability to accommodate additional requirements like object tagging, metadata validation, or integration with other AWS services.

This event-driven architecture reduces manual intervention, providing real-time, reliable notifications. It can be easily extended for broader applications, such as triggering data pipelines, monitoring compliance, or auditing uploaded content. By leveraging AWS's suite of services, this solution showcases expertise in designing efficient, scalable, and automated workflows tailored to business needs.

![Screenshot 2024-12-15 203822](https://github.com/user-attachments/assets/eb639727-7795-4bc8-a734-e9b68e91e35f)
![Screenshot 2024-12-15 203845](https://github.com/user-attachments/assets/75ea10c4-cbfb-4c0f-b1fa-0cd6d1fa454a)
![Screenshot 2024-12-15 203913](https://github.com/user-attachments/assets/08aa380a-aa3c-4afc-85bf-376a95009210)
![Screenshot 2024-12-15 203949](https://github.com/user-attachments/assets/c7364460-41f9-464d-a78b-b656871b8cbb)


