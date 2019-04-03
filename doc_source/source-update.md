# Updating the Source of a Flow<a name="source-update"></a>

You can update the source of an existing flow, even when the flow is currently running\.

**To update the source of an existing flow \(console\)**

1. Open the AWS Elemental MediaConnect console at [https://console\.aws\.amazon\.com/mediaconnect/](https://console.aws.amazon.com/mediaconnect/)\.

1. On the **Flows** page, choose the name of the flow that you want to update\.

1. Choose the **Source** tab\.

1. Choose **Update source**\.

1. Make the appropriate changes, and then choose **Update source**\.

**To update the source of an existing flow \(AWS CLI\)**
+ In the AWS CLI, use the update\-flow\-source command:

  ```
  aws mediaconnect update-flow-source --flow-arn "arn:aws:mediaconnect:us-east-1:111122223333:flow:1-23aBC45dEF67hiJ8-12AbC34DE5fG:AwardsShow" --source-arn "arn:aws:mediaconnect:us-east-1:111122223333:source:2-3aBC45dEF67hiJ89-c34de5fG678h:AwardsShowSource" --whitelist-cidr "10.24.34.0/24" --region us-east-1 --profile PMprofile
  ```

  The following example shows the return value:

  ```
  {
    "FlowArn": "arn:aws:mediaconnect:us-east-1:111122223333:flow:1-23aBC45dEF67hiJ8-12AbC34DE5fG:AwardsShow",
    "Source": {
          "IngestIp": "203.0.113.20",
          "Description": "NYC awards show",
          "Transport": {
              "Protocol": "rtp",
              "MaxBitrate": 80000000
          },
          "WhitelistCidr": "10.24.34.0/24",
          "SourceArn": "arn:aws:mediaconnect:us-east-1:111122223333:source:2-3aBC45dEF67hiJ89-c34de5fG678h:AwardsShowSource",
          "IngestPort": 5000,
          "Name": "AwardsShowSource"
      }
  }
  ```