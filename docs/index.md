---
layout: ""
page_title: "Provider: Pi-hole"
description: A Terraform provider to manage Pi-hole resources
---

# Pi-hole Provider

The [Pi-hole](https://pi-hole.net) provider is used to manage Pi-hole resources. The provider should be configured with the Pi-hole URL and the admin password (not the hashed web password).

Use the navigation to the left to read about the available resources.

## Example Usage

```terraform
terraform {
  required_providers {
    pihole = {
      source = "ryanwholey/pihole"
    }
  }
}

provider "pihole" {
  url      = "https://pihole.domain.com" # PIHOLE_URL
  password = var.pihole_password         # PIHOLE_PASSWORD
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- **password** (String) The admin password used to login to the admin dashboard
- **url** (String) URL where Pi-hole is deployed