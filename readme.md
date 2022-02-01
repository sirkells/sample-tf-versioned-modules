source https://blog.gruntwork.io/how-to-create-reusable-infrastructure-with-terraform-modules-25526d65f73d

'module "webserver" {
  source = "git::git@github.com:sirkells/sample-tf-versioned-modules.git//modules/services/webserver?ref=v0.0.1"
  cluster_name  = "webservers-prod"
  instance_type = "m4.large"
  min_size      = 2
  max_size      = 10
}'