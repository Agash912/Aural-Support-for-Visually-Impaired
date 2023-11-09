# AWS-backed Aural Assistive System for the Visually Impaired

## Project Overview

This project "AWS-backed Aural Assistive System for the Visually Impaired", showcases the seamless integration of Amazon Web Services (AWS) into a real-world application, specifically designed to aid the visually impaired. Utilizing cutting-edge technologies like Raspberry Pi 3B, Python, and AWS cloud services, the system converts printed text from documents into audio for enhanced accessibility.

## AWS Cloud Technologies Utilized

### Hardware Components:

- Raspberry Pi 3B
- Raspberry Pi Camera Module
- IR Sensor
- Earphone

### AWS Services:

1. **Amazon S3 (Simple Storage Service):**
    - **Usage:** Object-oriented storage service.
    - **Role:** Stores images captured by the Raspberry Pi camera.
    - **Integration:** On image upload, triggers Lambda function.

2. **Lambda:**
    - **Usage:** Serverless compute service.
    - **Role:** Executes Python code triggered by S3 events.
    - **Integration:** Triggers Textract service on image upload.

3. **Textract:**
    - **Usage:** Machine learning service for image-to-text conversion.
    - **Role:** Extracts text from images stored in S3.
    - **Integration:** Outputs text back to the S3 bucket.

4. **IAM (Identity and Access Management):**
    - **Usage:** Manages access control.
    - **Role:** Ensures fine-grained access control for secure data access.

5. **CloudWatch:**
    - **Usage:** Logging and monitoring service.
    - **Role:** Facilitates efficient issue identification and resolution.

## Working Methodology

The system follows a streamlined process for converting printed text from documents into audio for the visually impaired:


1. **Raspberry Pi Configuration with AWS:**
    - The Raspberry Pi is configured with AWS using the `Boto3` library in Python.
    - `Boto3` enables communication between the Raspberry Pi and AWS services.
     
2. **Image Capture and Logging:**
   - The Raspberry Pi captures images using the attached camera.
   - AWS S3 is utilized for object-oriented storage, logging, and efficient data management.

3. **AWS Lambda Trigger on Image Upload:**
   - Upon image upload to the S3 bucket, an AWS Lambda function is triggered.
   - The Lambda function initiates the next step in the workflow.

4. **Textract Service Execution:**
   - AWS Textract, a machine learning service, processes the uploaded image.
   - It automatically extracts text from the image, considering various parameters for optimal results.

6. **Raspberry Pi as a Listener:**
   - The Raspberry Pi acts as a listener for the S3 bucket containing the processed text.
   - It continuously monitors the bucket for any new text uploads from textract.

7. **Text-to-Audio Conversion and Playback:**
   - Upon detecting new text, the Raspberry Pi converts it into audio using Python scripts.
   - The audio output is played through the user's earphones, enabling them to access the content seamlessly.

8. **S3 Bucket Security Configurations:**
   - The S3 bucket is configured with strict access controls.
   - Access is restricted to only the configured Raspberry Pi and the Textract service.
   - This ensures a secure and controlled environment for data transmission.

This systematic approach ensures an end-to-end process, leveraging AWS cloud services and Raspberry Pi's capabilities to provide an efficient aural assistive system.

## Project Objective

This project serves as a demonstration of the practical application of Amazon cloud services in a real-world scenario for the greater good. By providing an aural assistive system for the visually impaired, it showcases how AWS technologies can be harnessed to address societal challenges and enhance accessibility.

### AWS Services in Action 

## S3 Bucket

![S3 Bucket](https://github.com/Agash912/Aural-Support-for-Visually-Impaired/assets/112348271/fa3f4ad8-63bf-4b41-8de9-9493ab59c809)

## IAM Users, Roles & Policies

![IAM Users](https://github.com/Agash912/Aural-Support-for-Visually-Impaired/assets/112348271/b2a0d0a3-8987-408d-91ec-97cfa3c7d5bd)
![IAM Roles](https://github.com/Agash912/Aural-Support-for-Visually-Impaired/assets/112348271/12e0b7b2-c430-4006-a2ac-d8f7da1d876e)
![IAM Policies](https://github.com/Agash912/Aural-Support-for-Visually-Impaired/assets/112348271/8a1e6686-d540-430a-9462-8889476e4c90)

## Lambda Function

![Lambda Function 1](https://github.com/Agash912/Aural-Support-for-Visually-Impaired/assets/112348271/a8dcc6ce-40dd-4381-8f82-188b0e1bde59)
![Lambda Function 2](https://github.com/Agash912/Aural-Support-for-Visually-Impaired/assets/112348271/545bd663-404e-4736-8285-7c9dfcb2a3be)

## Cloud Watch

![Cloud Watch 1](https://github.com/Agash912/Aural-Support-for-Visually-Impaired/assets/112348271/e592565f-53dd-41c0-8369-6b0b99913ddf)
![Cloud Watch 2](https://github.com/Agash912/Aural-Support-for-Visually-Impaired/assets/112348271/99dcd88c-ca2f-4844-ad7c-ffa23f44f524)
![Cloud Watch 3](https://github.com/Agash912/Aural-Support-for-Visually-Impaired/assets/112348271/ad266540-338f-4a21-8e28-2fbdff523031)

## Sample Input & Output

![Sample Input & Output](https://github.com/Agash912/Aural-Support-for-Visually-Impaired/assets/112348271/76426f90-ad70-4b29-8815-8e4a05e0add4)
![Sample Input & Output 2](https://github.com/Agash912/Aural-Support-for-Visually-Impaired/assets/112348271/a6b5bec3-3fab-4cb7-a544-3dff0e64b50c)


## Additional Info

Explore the [Slides] and [Report] present in the repo for detailed information, diagrams and technical insights into the architecture.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

