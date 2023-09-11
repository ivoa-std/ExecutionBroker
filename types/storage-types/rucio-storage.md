The rucio-storage type describes a resource in Rucio storage system.

A rucio-storage resource may include the following properties:

```
resources:
  storage:
  - name: # The name of the resource.
    type: "https://www.purl.org/ivoa.net/storage-types/rucio-storage"
    spec:

      lifecycle: # One of "managed" or "unmanaged".
      # If lifecycle is set to managed, then the lifetime can also be set.
      minlifetime: # The minimum time that the resource will be available after the job completes.
      maxlifetime: # The maximum time that the resource will be available after the job completes.

      minsize: # The minimum size require to perform the task, specified in GiB.
      maxsize: # The maximum size that will be available, specified in GiB.

      endpoint: # The main endpoint of the Rucio service.
      domain:   # The domain within the Rucio service.
      objectid: # The object identifier within the domain.

