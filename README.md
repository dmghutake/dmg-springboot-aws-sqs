# Spring Boot Application to send and Receive messages to and from AWS SQS service.

  * Create Standard SQS Queue for example: brainupgrade-sqs-queue.
  * Create Group and add add policies to access SQS programmatically with "AdministrativeFullAccess" and "AmazonEC2FullAccess" and add User to this group with programmatic access.
  * Create Spring boot project from spring Initilizer with web and Lombak dependencey.
  * Once you import project into Eclipse , open pom.xml and add below dependencies.
  ```
	<properties>
		<spring-cloud-aws-version>2.2.6.RELEASE</spring-cloud-aws-version>
	</properties>

  <dependency>
		    <groupId>org.springframework.cloud</groupId>
		    <artifactId>spring-cloud-starter-aws</artifactId>
		    <version>${spring-cloud-aws-version}</version>
		</dependency>
		<dependency>
		    <groupId>org.springframework.cloud</groupId>
		    <artifactId>spring-cloud-starter-aws-messaging</artifactId>
		    <version>${spring-cloud-aws-version}</version>
		</dependency>
  ```
  * Create SQSConfiguration class with SQS Message Template Bean with Users access keys, and SQS endpoints.
  * Create Message Sender class to send message to the Queue.
  * Use Rest Client postman to send message.
  * Test on AWS SQS console whether Messages is present.
  * Create Message Receiver class to receive message from the Queue.
  * Test on IDE's console whether Messages is received.
