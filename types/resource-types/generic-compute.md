A generic-compute resources cover a range of resources from bare metal physical machies,
virtual machines, OCI contaniner runtimes to Kubernetes clusters.

A generic-compute resource may include the following properties:

```
resources:
  compute:
  - name: # The name of the resource.
    type: "https://www.purl.org/ivoa.net/resource-types/generic-compute"
    spec:

      mincores:  <float> # The minimum number of CPU cores needed to perform the task.
      maxcores:  <float> # The maximum number of CPU cores that will be available.
      minmemory: <integer> # The minimum amount of memory needed to perform the task, specified in GiB.
      maxmemory: <integer> # The maximum amount of memory that will be available, specified in GiB.

      volumes: # A list of storage volume mounts that link storage resources to locations in the compute resource filesystem.
      - name: # The name of the volume mount.
        resource: # The name or ident of the storage resource.
        path: # The mount location within the compute resource filesystem.
        mode: # The access mode from within the compute resource filesystem, one of 'r' or 'rw'.

      extras:
      # A list of extra components added to the resource.
      # This includes things like GPUs and FPGA accelerators.
      # Each item in the list follows the standard pattern of name, type and spec.
```


