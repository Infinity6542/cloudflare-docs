---
_build:
  publishResources: false
  render: never
  list: never
---

Terraform functions through a working directory that contains configuration files. You can store your configuration in multiple files or just one — Terraform will evaluate all of the configuration files in the directory as if they were in a single document.

1. Create a folder for your Terraform configuration:

   ```sh
   $ mkdir cloudflare-tf
   ```

2. Change into the directory:

   ```sh
   $ cd cloudflare-tf
   ```