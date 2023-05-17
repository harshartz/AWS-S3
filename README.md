# Static Website Hosting Using AWS S3


# Step 1: 

-Sign in to the AWS Management Console and navigate to the S3 service by searching for "S3" in the AWS Management Console search bar.

![1ss](https://github.com/harshartz/AWS-EC2/assets/130890384/c504a03a-e3a0-449b-aa9d-7f42f061dff3)


 # Step 2:  

-Click on the "Create bucket" button to start the bucket creation process. 

![2ss](https://github.com/harshartz/AWS-EC2/assets/130890384/3006499b-704a-4551-828d-0c475e4d1426)


# Step 3: 

-Provide a unique name for your bucket. This name will be part of the website URL, so it should be globally unique.

-Choose the region where you want your bucket to be located.  

![3ss](https://github.com/harshartz/AWS-EC2/assets/130890384/c4d78163-f5eb-4f8c-a755-2a37e11bd0da)

-Leave all other settings as their default values and click on the "Create" button to create the bucket.

![4ss](https://github.com/harshartz/AWS-EC2/assets/130890384/0d3f22fe-c7ab-42aa-9828-61cddd604005)


# Step 4: 

-Navigate to bucket "Properties"

![5ss](https://github.com/harshartz/AWS-EC2/assets/130890384/71750dcc-69f7-4d18-a445-a1015d15b2a9)


-Under "Static website hosting," click on the "Edit" button. 

![6ss](https://github.com/harshartz/AWS-EC2/assets/130890384/fbdcc380-b7cb-44f5-b742-be863ac49ad7)


-Select the option "Enable". 

-In the "Index document" field, enter the name of your main HTML file (e.g., "index.html"). 

-Optionally, you can provide a custom error document for handling 404 errors. 

-Click on the "Save changes" button.

![7ss](https://github.com/harshartz/AWS-EC2/assets/130890384/7de5505c-4f4f-4638-b3d5-753b4f784259)


# Step 5: 

Upload Website Files 

Open Notepad or any text editor and create a new file.

Write the desired content that you want to display on the website.

![8ss](https://github.com/harshartz/AWS-EC2/assets/130890384/f44d65f6-0178-4ef7-9a9b-9de327d4262a)


Go to the "File" menu and click on "Save As".

Enter a file name for your webpage, ensuring that you include the ".html" extension, such as "index.html".

Click on the "Save" button to save the file.

![9ss](https://github.com/harshartz/AWS-EC2/assets/130890384/1bc58441-7c14-4769-8915-67de7f2350b2)


-Navigate to bucket "Object"

-Go to the "Upload" button or and click on it

![10ss](https://github.com/harshartz/AWS-EC2/assets/130890384/3bebf641-607d-472f-9af6-64b6a0f2cde5)


-Go to the "Add files" select the "index.html" file and then click on the "Upload" button

![11ss](https://github.com/harshartz/AWS-EC2/assets/130890384/9bea4563-c6ba-440f-8a71-d82c7144f714)


-Once the upload is complete, you will see a confirmation message indicating that the file has been successfully uploaded.

![12ss](https://github.com/harshartz/AWS-EC2/assets/130890384/5b018d98-c9b5-4995-a29c-669f6f9930ce)


# Step 6

-Enable Public Access 

-Go to the bucket settings and select "Permissions."

-Locate the section titled "Block public access (bucket settings)" and click on "Edit."

![13ss](https://github.com/harshartz/AWS-EC2/assets/130890384/edeaefb1-e7df-498b-b735-b5bd2e7b34ab)


-Uncheck the box labeled "Block all public access" to allow public access to the bucket.

![14ss](https://github.com/harshartz/AWS-EC2/assets/130890384/eeaf7b6f-2ddb-4d29-b1c8-f7c09a28c408)


-In the designated field, type "confirm" to confirm your changes.

-this will will effectively enable public access for the bucket

![15ss](https://github.com/harshartz/AWS-EC2/assets/130890384/0fc81a19-7eac-4f9a-96f1-d0b5ca8450a9)


# Step 7

-Go to the bucket settings and select "Permissions."

-Locate the section titled "Bucket policy" and click on "Edit."

![16ss](https://github.com/harshartz/AWS-EC2/assets/130890384/33343d96-3066-4c82-9d35-fb52d164761e)


-Click on "Policy Generator" it will open in a new window.

![17ss](https://github.com/harshartz/AWS-EC2/assets/130890384/8c2a1ca0-9f7f-4ba9-8117-8c06d156d97f)


-Select the type of policy as "S3" and set the effect to "Allow."

-In the "Principal" field, enter "*" to allow all the resourses.

-In the "Action" field, select "GetObject" to grant read access to the objects in the bucket.

-Paste the ARN (Amazon Resource Name) from the earlier tab into the "ARN" field.

-Click on "Add Statement" to include the generated policy.

![18ss](https://github.com/harshartz/AWS-EC2/assets/130890384/b20da9cb-c5dd-4c7e-aa93-9e7ff4df02a8)


-Copy the generated policy and paste it into the policy editor tab.

![19ss](https://github.com/harshartz/AWS-EC2/assets/130890384/232a17ab-2752-46e9-b0ec-1c3a18363b82)


-Add "/*" at the end of the resource to allow access to all files under the bucket.

-Click on "Save Changes" to apply the bucket policy.

![20ss](https://github.com/harshartz/AWS-EC2/assets/130890384/9d8b06bb-1838-4a38-8af7-4c2ef3adff7e)


-Navigate to the bucket's website endpoint and copy the provided link.

![21ss](https://github.com/harshartz/AWS-EC2/assets/130890384/2ac47666-0f5a-40a7-8ecd-f90e8783fb15)


-Open the link in a browser to verify if the website is functioning correctly.

-You should now see your static website live and accessible through the provided URL.

![22ss](https://github.com/harshartz/AWS-EC2/assets/130890384/4ae35226-5047-4bad-aed1-cdde36f6e7f1)



# That's it! You have successfully hosted a static website using AWS S3.
