The amazon-s3 storage type describes a resource in an Amazon S3 compatible storage system.

An amazon-s3 resource may include the following properties:

```
resources:
  storage:
  - name: # The name of the resource.
    type: "https://www.purl.org/ivoa.net/storage-types/amazon-s3"
    spec:

      lifecycle: # One of "managed" or "unmanaged".
      # If lifecycle is set to managed, then the lifetime can also be set.
      minlifetime: # The minimum time that the resource will be available after the job completes.
      maxlifetime: # The maximum time that the resource will be available after the job completes.

      endpoint: # The S3 service endpoint.
      template: # The S3 service URL template.
      bucket: # The bucket name.
      object: # The object identifier within the bucket (optional).
```



