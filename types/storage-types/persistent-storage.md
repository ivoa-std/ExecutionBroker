A persistent-storage resource is available beyond the lifetime of the job.

A persistent-storage resource may include the following properties:

```
resources:
  storage:
  - name: # The name of the resource.
    type: "https://www.purl.org/ivoa.net/storage-types/persistent-storage"
    spec:

      lifecycle: # One of "managed" or "unmanaged".
      # If lifecycle is set to managed, then the lifetime can also be set.
      minlifetime: # The minimum time that the resource will be available after the job completes.
      maxlifetime: # The maximum time that the resource will be available after the job completes.

      minsize: # The minimum size require to perform the task, specified in GiB.
      maxsize: # The maximum size that will be available, specified in GiB.
```

The lifecycle of a managed resource is handled by the ExecutionPlanner service, creating
and deleting the resource automatically.
It is up to the ExecutionPlanner service to decide where the storage is allocated.

The lifecycle of an unmanaged resource is handled by an external entity.
The ExecutionPlanner service does not play any part in creating or deleting the resource.

