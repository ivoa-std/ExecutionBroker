The vospace-storage type describes a resource in VOSpace storage system.

A vospace-storage resource may include the following properties:

```
resources:
  storage:
  - name: # The name of the resource.
    type: "https://www.purl.org/ivoa.net/storage-types/vospace-storage"
    spec:

      lifecycle: # One of "managed" or "unmanaged".
      # If lifecycle is set to managed, then the lifetime can also be set.
      minlifetime: # The minimum time that the resource will be available after the job completes.
      maxlifetime: # The maximum time that the resource will be available after the job completes.

      minsize: # The minimum size require to perform the task, specified in GiB.
      maxsize: # The maximum size that will be available, specified in GiB.

      endpoint: # The main endpoint of the VOSpace service.
      ivorn: # The IVOA registry URI of the VOSpace service.
      type: # The node type within the VOSpace service.
      path: # The node path within the VOSpace service.

