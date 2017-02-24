# aws-equivalent-gcp-cloud-config

Use this snippet of [BOSH Cloud Config](https://bosh.io/docs/cloud-config.html) to allow you to spin up GCP VMs that are roughly equivalent to [AWS EC2 instance types](https://aws.amazon.com/ec2/instance-types/).

Pull requests for additional types are most welcome.

## Example

```yaml
- name: t2.micro
  cloud_properties:
    machine_type: f1-micro
    root_disk_size_gb: 10
    root_disk_type: pd-ssd
    ephemeral_external_ip: true
    preemptible: true
```