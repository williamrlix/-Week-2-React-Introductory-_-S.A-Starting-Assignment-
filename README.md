# TIL 21/10/2022

# 1. What are the characteristics of JavaScript - data type and JavaScript?
Javascript is the language we are going to learn from now on. So today, we will have spend some time digging deeper into what this language is and what qualities it has. if we input numerik number mede variabel become integer, if we input true/false it become boolean, and etc

loosely typed dynamic language
JavaScript is a loosely typed language, meaning you don’t have to specify what type of information will be stored in a variable in advance. JavaScript automatically types a variable based on what kind of information you assign to it (e.g., that '' or " " to indicate string values).
    
JavaScript Type Casting
Typecasting in JavaScript means converting one data type to another data type i.e., the conversion of a string data type to Boolean or the conversion of an integer data type to string data type. The typecasting in JavaScript is also known as type conversion or type coercion.

==, ===

== is a equal operator that use for check an equal on javascript

=== is a identical operator that check the variable if contains same information and same data types in javascript 

example:

#1 typeof

whenever a variable’s type is in doubt, you can employ the typeof operator:

typeof 1 //> “number”

typeof “1” //> “string”

typeof [1,2,3] //> “object”

typeof {name: “john”, country: “usa”} //> “object”

typeof true //> “boolean”

typeof (1 === 1) //> “boolean”

typeof undefined //> “undefined”

typeof null //> “object”

const f = () => 2

typeof f //> “function”

#2 Double Equals Versus Triple Equals

The === mean “equality without type coercion”. Using the triple equals, the values must be equal in type as well.

1 == “1” //> true

1 === “1” //> false

null == undefined //> true

null === undefined //> false

‘0’ == false //> true

‘0’ === false //> false

0 == false //> true

0 === false //> false, because they are of a different type

Note, you can use !== for checking inequality with type coercion:

1 != "1" //> false

1 !== "1" //> true

#3 Checking for Falsiness

Using the ! operator (called the “bang” operator) to check for falsiness, we notice the following:

!null //> true

!undefined //> true

!0 //> true

!"" //> true

!false //> true

![] //> false

!42 //> false

!"hello world" //> false


Answer the following questions:
What is the **problem** of a loosely typed dynamic language, and what are the ways to **supplement** it?
in javascript we don’t have to specify what type of information will be stored in a variable in advance, that made us cant make the method, so we need the define the type of data waht that variable contain to made the method.

Compare the difference between undefined and null.
The difference between undefined and null is, null is an object so er can add number to it, but undefined is not an object so if we add number it will results NaN

# 2. What is JavaScript object and Immutability?
Primitive type data, and Reference type data.
Primitive data types are simple and at lowest level of implementation, its not object and doesn't have any methods, such as strings, booleans, null and unified. javascript will converts primitives strings into objects, so we can using methods
Refrence data in javascript is dynamic so it no have fixed size, most of them are objects and have methods, such as arrays, collections.
Primitive data is treated something like this

![will3](https://user-images.githubusercontent.com/63656243/197225909-5a3220ef-42ce-4d74-8ace-86f0c7bd6fb1.png)

while reference data will treated like this

![will4](https://user-images.githubusercontent.com/63656243/197226224-a9fcb458-654f-4b75-af3f-330ae9fbe3c1.png)

How to make Immutable Object?
mutability means ability to change overtime, iimutability meaning the object will not change overtime, when immutability we cannot add new property, modify or delete it, wo make immutability we can use const function like this

![willjpeg](https://user-images.githubusercontent.com/63656243/197227160-c216aa08-32de-4dfa-83c9-7b4316c23d6d.jpeg)

What are shallow copy and deep copy. What are the differences?
shallow copy is when we copy data, the original is object is stored and only the reference address is copied, in deep copy both original and repetitive copies are stored.

# 3.Hoisting and TDZ
Scope, Hoisting and TDZ
Scope is current context of cide, Hoisting is mechanism that makes variables usable before they declared and execute, TDZ or temporal dead zone is region of scope which variable is defined but cant be used because variable didn't exist.

![will5](https://user-images.githubusercontent.com/63656243/197228046-f589167e-e68c-4f5a-b114-2fe87f3a8d87.png)


Different ways of hoisting in Function Declarations and Function Expressions.
in hoisting on function declaration, it must be begin with function statement, must have name and executing on compilation phase. in function expression it must be stored on variable, no need name and executing on execution phase of javascript engine, both of them are hoisted function declaration hoisted first and function expression hoisted fully, usually variable declarations get hoisted but their assignment expression dont.

Execution Context and Call Stack
execution context is environment to handle the transformation and execution of JS code, the execution stack or call stack keeps track of all execution context during life cycle of a script. both oof the process carried out under the hood to let our code run

Scope Chain and Information Hiding
Scope is context environment created when function is written, this context defines whatother data has access to, closure are functions that have access to variables from another functions scope, it will return another function, encapsulation or information hiding is key for object oriented programming (OOT) means separating desrtiption of how to use a class from the implementation details, it is to hide our method.

# 4. Let’s do some Exercise: 
What would be the “b” value printed on the console?

![will](https://user-images.githubusercontent.com/63656243/197222083-41f70ffd-5420-426f-a8a8-8d69997aca38.png)

Variable “b” will be printed as 1 in console.log as it was assigned.
There are 3 console lines that print “b”.

Which “b” value would be printed from which line of console.log? Explain why.
based on my text editor, it was : line 10, line 7, and line 13
line 10 : printed as 1 because the variable “b” is assigned as 1
line 7 : printed as 101 because there is an incrementation (b++) in the function hi(), and it’s going to adding 1 to the variable b when the function is called
line 13 : printed as 1 because the variable “b” was declared as 1 before the hi() function was created.

What would be //console.log(a); in the comment? If there’s an error, explain why and fix the error.

![erorwill](https://user-images.githubusercontent.com/63656243/197222613-77930e5a-211f-400f-9f92-493be6d6be70.png)

For the error part, “a” is a constant with a value is 1, which is defined and declare in the hi() function, so the constant “a” has a limited scope in the hi() function. That’s why the console give an alert ‘a is not defined’.
The way to fix this easily is turn const a into global scope variable by replace it to outside of the hi() function and const a is already global scope variable then you can access it from anywhere.

![will2](https://user-images.githubusercontent.com/63656243/197223020-6e450822-9c3c-4fd2-bfea-e6a2e56582b9.png)

# 7 I'm using the Amazon S3 static website feature but getting an Access Denied error. Why is this happening?

- Short description

#If you're trying to host a static website using Amazon S3, but you're getting an Access Denied error, check the following requirements:
Objects in the bucket must be publicly accessible.

S3 bucket policy must allow access to the s3:GetObject action.

The AWS account that owns the bucket must also own the object.

Objects can't be encrypted by AWS Key Management Service (AWS KMS).

Objects that are requested must exist in the S3 bucket.

Amazon S3 Block Public Access must be disabled on the bucket and account level.

- Resolution
Objects in the bucket must be publicly accessible

S3 static website endpoint supports only publicly accessible content. To verify whether an object in your S3 bucket is publicly accessible, open the object's URL in a 

web browser. Or, you can run a cURL command on the URL.

The following is an example URL of an S3 object:

http://doc-example-bucket.s3-website-us-east-1.amazonaws.com/index.html
    
If an Access Denied error is returned by the web browser or cURL command, then the object isn't publicly accessible. To allow public read access to your S3 object, create a bucket policy that allows public read access for all objects in the bucket.

- 3 bucket policy must allow access to the s3:GetObject action
Review your bucket policy, and make sure that there aren't any deny statements that block public read access to the s3:GetObject action. Even if you have an explicit allow statement for s3:GetObject in your bucket policy, confirm that there isn't a conflicting explicit deny statement. An explicit deny statement will always override an explicit allow statement.

To review your bucket policy for s3:GetObject, perform the following steps:

1.    Open the Amazon S3 console.

2.    Choose the Permissions tab.

3.    Choose Bucket Policy.

4.    Review the bucket policy for statements with "Action": "s3:GetObject" or "Action": "s3:*".

5.    (Optional) Modify the bucket policy. For example, you can remove or edit statements that block public read access to s3:GetObject.

- the AWS account that owns the bucket must also own the object
To allow public read access to objects, the AWS account that owns the bucket must also own the objects. A bucket or object is owned by the account of the AWS Identity and Access Management (IAM) identity that created the bucket or object.

Note: The object-ownership requirement applies to public read access granted by a bucket policy. It doesn't apply to public read access granted by the object's access control list (ACL).

To check if your Amazon S3 bucket and objects are owned by the same AWS account, perform the following steps:

1.    To retrieve the S3 canonical ID of the bucket owner, use the following command:

aws s3api list-buckets --query Owner.ID
    
2.    To retrieve the S3 canonical ID of the object owner, use the following command:

aws s3api list-objects --bucket DOC-EXAMPLE-BUCKET --prefix index.html

Note: This example shows a single object. To check several objects, use the list command.

3.    Confirm whether the canonical IDs of the bucket owner and object owner match. If they don't match, then the bucket and object have different owners.

Note: You can also use the Amazon S3 console to check the bucket and object owners. The owners are found in the Permissions tab of the respective bucket or object.

4.    If the canonical IDs of the bucket and object owner don't match, change the object's owner to the bucket owner.

From the object owner's account, run the following command to retrieve the ACL permissions assigned to the object:

aws s3api get-object-acl --bucket DOC-EXAMPLE-BUCKET --key object-name

If the object doesn't have bucket-owner-full-control ACL permissions, then run the following command from the object owner's account:

aws s3api put-object-acl --bucket DOC-EXAMPLE-BUCKET --key object-name --acl bucket-owner-full-control

If the object has bucket-owner-full-control ACL permissions, run the following command from the bucket owner's account. This command changes the owner of the object by copying the object over itself:

aws s3 cp s3://DOC-EXAMPLE-BUCKET/index.html s3://DOC-EXAMPLE-BUCKET/index.html --storage-class STANDARD

You can also use S3 Object Ownership to grant the bucket owner automatic ownership of any objects uploaded by anonymous users or other AWS accounts.

- ojects in the bucket can't be AWS KMS-encrypted
AWS KMS doesn't support anonymous requests. As a result, any Amazon S3 bucket that allows anonymous or public access will not apply to objects that are encrypted with AWS KMS. You must remove KMS encryption from the objects that you want to serve using the Amazon S3 static website endpoint.

Note: Instead of using AWS KMS encryption, use AES-256 to encrypt your objects.

You can check if an object in your bucket is KMS encrypted using the following methods:

Use the Amazon S3 console to view the properties of the object. Review the Encryption dialog box. If AWS-KMS is selected, then the object is KMS-encrypted

Run the head-object command using the AWS Command Line Interface (AWS CLI). If the command returns ServerSideEncryption as aws:kms, then the object is KMS-encrypted.

Note: If you receive errors when running AWS CLI commands, make sure that you’re using the most recent version of the AWS CLI.

To change the object's encryption settings using the Amazon S3 console, see Specifying Amazon S3 encryption.

To change the object's encryption settings using the AWS CLI, verify that the object's bucket doesn't have default encryption. If the bucket doesn't have default encryption, then remove the object's encryption by copying the object over itself:

aws s3 cp s3://DOC-EXAMPLE-BUCKET/index.html s3://DOC-EXAMPLE-BUCKET/index.html --storage-class STANDARD

Warning: Copying the object over itself removes settings for storage-class and website-redirect-location. To maintain these settings in the new object, make sure to explicitly specify storage-class or website-redirect-location values in the copy request.

- bjects that are requested must exist in the S3 bucket
If a user performing the request doesn’t have s3:ListBucket permissions, then the user gets an Access Denied error for missing objects.

You can run the head-object AWS CLI command to check if an object exists in the bucket.

Note: S3 object names are case-sensitive. If the request doesn't have a valid object name, then Amazon S3 will report that the object is missing.

If the object exists in the bucket, then the Access Denied error isn't masking a 404 Not Found error. Verify other configuration requirements to resolve the Access Denied error.

If the object doesn't exist in the bucket, then the Access Denied error is masking a 404 Not Found error. Resolve the issue related to the missing object.

Note: It's not a security best practice to enable public s3:ListBucket access. Enabling public s3:ListBucket access allows users to see and list all objects in a bucket. This access exposes object metadata details (for example, key and size) to users even if the users don't have permissions for downloading the object.

- amazon Block Public Access must be disabled on the bucket
Amazon S3 Block Public Access settings can apply to individual buckets or AWS accounts. Confirm that there aren't any Amazon S3 Block Public Access settings applied to either your S3 bucket or AWS account. These settings can override permissions that allow public read access.
