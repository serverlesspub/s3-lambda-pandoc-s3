
# S3 Bucket -> Lambda (Pandoc Conversion) -> S3 bucket

## Description

This is a serverless component consisting of:

- an S3 Upload Bucket that accepts files.
- a Lambda function that converts uploaded files using Pandoc
- an S3 Results Bucket where the converted files will be saved

It's a Nuts & Bolts application component for AWS Serverless Application Repository.

## Deployment Parameters

This component has two CloudFormation deployment parameters that can be modified by users:

- `ConversionFileType`: a string with the extension (no starting dot) for the resulting file type. For example, to convert to MS Word, use `docx`.
- `ConversionMimeType`: a string with the MIME type of the result when uploaded to S3. For example, for MS Word files, use `application/vnd.openxmlformats-officedocument.wordprocessingml.document`

If you use a custom [Lambda Layer for Pandoc](https://github.com/effortless-serverless/pandoc-aws-lambda-binary), then also provide the ARN of the layer in the `LambdaLayerArn` parameter. 

## Latest Release - 1.0.0

Initial release.

## Roadmap - Upcoming changes

Here are the upcoming changes that I'll add to this serverless component:

- ESLint
- Tests
