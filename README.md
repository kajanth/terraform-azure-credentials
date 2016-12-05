This script uses the `azure-cli` tool to create all the resources required to 
use Terraform with Microsoft Azure.

To follow the instructions by hand, see [this blog post](https://michaelheap.com/using-azure-resource-manager-with-terraform/).

# Usage

```bash
git clone https://github.com/mheap/terraform-azure-credentials.git
cd terraform-azure-credentials
```

Edit `create_credentials` so that it has the correct application name and client
secret at the top. Save the file

Run the following command:
```
bash create_credentials > demo.tf
terraform plan
```

You should see some output that looks like the following:

```
+ azurerm_resource_group.terraform-test
    location: "westus"
    name:     "production"
    tags.%:   "<computed>"
```

This is your starting point for your terraform infrastructure
