<a name="unreleased"></a>
## [Unreleased]


<a name="v1.75.0"></a>
## [v1.75.0] - 2022-09-07
### Feat
- Allow running container as non-root UID/GID for ownership issues (docker) ([#433](https://github.com/sandatech/terraform/issues/433))


<a name="v1.74.2"></a>
## [v1.74.2] - 2022-09-02
### Fix
- Fixed url for wrappers in generated README (terraform_wrapper_module_for_each) ([#429](https://github.com/sandatech/terraform/issues/429))


<a name="v1.74.1"></a>
## [v1.74.1] - 2022-07-13
### Fix
- Passed scenario in `terraform_docs` hook now works as expected


<a name="v1.74.0"></a>
## [v1.74.0] - 2022-07-12
### Feat
- Suppress color for all hooks if `PRE_COMMIT_COLOR=never` set ([#409](https://github.com/sandatech/terraform/issues/409))
- Add support for set env vars inside hook runtime ([#408](https://github.com/sandatech/terraform/issues/408))
- Allow `terraform_providers_lock` specify terraform init args ([#406](https://github.com/sandatech/terraform/issues/406))

### Fix
- Add `--env-vars`, deprecate `--envs` ([#410](https://github.com/sandatech/terraform/issues/410))
- Add `--tf-init-args`, deprecate `--init-args` ([#407](https://github.com/sandatech/terraform/issues/407))


<a name="v1.73.0"></a>
## [v1.73.0] - 2022-06-27
### Feat
- Add __GIT_WORKING_DIR__ to terraform_checkov ([#399](https://github.com/sandatech/terraform/issues/399))


<a name="v1.72.2"></a>
## [v1.72.2] - 2022-06-21
### Fix
- Pre-commit-terraform terraform_validate hook ([#401](https://github.com/sandatech/terraform/issues/401))


<a name="v1.72.1"></a>
## [v1.72.1] - 2022-05-25
### Fix
- Fixed `terraform_fmt` with `tfenv`, when `terraform` default version is not specified ([#389](https://github.com/sandatech/terraform/issues/389))


<a name="v1.72.0"></a>
## [v1.72.0] - 2022-05-25
### Feat
- When a config file is given, do not specify formatter on cli (terraform_docs) ([#386](https://github.com/sandatech/terraform/issues/386))


<a name="v1.71.0"></a>
## [v1.71.0] - 2022-05-02
### Feat
- Added terraform_wrapper_module_for_each hook ([#376](https://github.com/sandatech/terraform/issues/376))


<a name="v1.70.1"></a>
## [v1.70.1] - 2022-04-28
### Fix
- Fixed `tfupdate` to work in all cases, not only `pre-commit run --all` ([#375](https://github.com/sandatech/terraform/issues/375))


<a name="v1.70.0"></a>
## [v1.70.0] - 2022-04-28
### Feat
- Add support for `pre-commit/pre-commit-hooks` in Docker image ([#374](https://github.com/sandatech/terraform/issues/374))


<a name="v1.69.0"></a>
## [v1.69.0] - 2022-04-26
### Feat
- Allow env vars expansion in `--args` section for all hooks ([#363](https://github.com/sandatech/terraform/issues/363))


<a name="v1.68.1"></a>
## [v1.68.1] - 2022-04-20
### Fix
- Fixed git fatal error in Dockerfile ([#372](https://github.com/sandatech/terraform/issues/372))


<a name="v1.68.0"></a>
## [v1.68.0] - 2022-04-18
### Feat
- Removed `coreutils` (realpath) from dependencies for MacOS ([#368](https://github.com/sandatech/terraform/issues/368))


<a name="v1.67.0"></a>
## [v1.67.0] - 2022-04-15
### Feat
- Added `terraform_checkov` (run per folder), deprecated `checkov` hook ([#290](https://github.com/sandatech/terraform/issues/290))


<a name="v1.66.0"></a>
## [v1.66.0] - 2022-04-13
### Feat
- Added support for `tfupdate` to update version constraints in Terraform configurations ([#342](https://github.com/sandatech/terraform/issues/342))


<a name="v1.65.1"></a>
## [v1.65.1] - 2022-04-13
### Fix
- Improve `tflint --init` command execution ([#361](https://github.com/sandatech/terraform/issues/361))


<a name="v1.65.0"></a>
## [v1.65.0] - 2022-04-13
### Feat
- Adding init to terraform_tflint hook ([#352](https://github.com/sandatech/terraform/issues/352))


<a name="v1.64.1"></a>
## [v1.64.1] - 2022-03-31
### Fix
- Make hooks bash 3.2 compatible ([#339](https://github.com/sandatech/terraform/issues/339))


<a name="v1.64.0"></a>
## [v1.64.0] - 2022-02-10
### Feat
- Improved speed of `pre-commit run -a` for multiple hooks ([#338](https://github.com/sandatech/terraform/issues/338))


<a name="v1.63.0"></a>
## [v1.63.0] - 2022-02-10
### Feat
- Improve performance during `pre-commit --all (-a)` run ([#327](https://github.com/sandatech/terraform/issues/327))


<a name="v1.62.3"></a>
## [v1.62.3] - 2021-12-22
### Fix
- Check all directories with changes and pass all args in terrascan hook ([#305](https://github.com/sandatech/terraform/issues/305))


<a name="v1.62.2"></a>
## [v1.62.2] - 2021-12-21
### Fix
- Speedup `terrascan` hook up to x3 times in big repos ([#307](https://github.com/sandatech/terraform/issues/307))
- Properly exclude .terraform directory with checkov hook ([#306](https://github.com/sandatech/terraform/issues/306))


<a name="v1.62.1"></a>
## [v1.62.1] - 2021-12-18

<a name="v1.62.0"></a>
## [v1.62.0] - 2021-12-12
### Feat
- Added semantic release ([#296](https://github.com/sandatech/terraform/issues/296))


<a name="v1.61.0"></a>
## [v1.61.0] - 2021-12-11
### Feat
- Pass custom arguments to terraform init in `terraform_validate` hook ([#293](https://github.com/sandatech/terraform/issues/293))

### Fix
- analyse all folders with tflint and don't stop on first execution ([#289](https://github.com/sandatech/terraform/issues/289))


<a name="v1.60.0"></a>
## [v1.60.0] - 2021-12-08
### Fix
- pre-build docker image ([#292](https://github.com/sandatech/terraform/issues/292))


<a name="v1.59.0"></a>
## [v1.59.0] - 2021-12-06
### Fix
- Fixed docker build ([#288](https://github.com/sandatech/terraform/issues/288))


<a name="v1.58.0"></a>
## [v1.58.0] - 2021-11-20

<a name="v1.57.0"></a>
## [v1.57.0] - 2021-11-17
### Fix
- typo in arg name for terraform-docs ([#283](https://github.com/sandatech/terraform/issues/283))


<a name="v1.56.0"></a>
## [v1.56.0] - 2021-11-08
### Feat
- Updated Docker image from Ubuntu to Alpine ([#278](https://github.com/sandatech/terraform/issues/278))


<a name="v1.55.0"></a>
## [v1.55.0] - 2021-10-27
### Fix
- Fixed 1.54.0 where `terraform_docs` was broken ([#272](https://github.com/sandatech/terraform/issues/272))


<a name="v1.54.0"></a>
## [v1.54.0] - 2021-10-27
### Feat
- Add support for quoted values in `infracost_breakdown` `--hook-config` ([#269](https://github.com/sandatech/terraform/issues/269))

### Fix
- Fixed args expand in terraform_docs ([#260](https://github.com/sandatech/terraform/issues/260))


<a name="v1.53.0"></a>
## [v1.53.0] - 2021-10-26
### Feat
- Add infracost_breakdown hook ([#252](https://github.com/sandatech/terraform/issues/252))
- Set up PR reviewers automatically ([#258](https://github.com/sandatech/terraform/issues/258))
- add __GIT_WORKING_DIR__ to tfsec ([#255](https://github.com/sandatech/terraform/issues/255))
- Add `terraform_docs` hook settings ([#245](https://github.com/sandatech/terraform/issues/245))
- Add support for specify terraform-docs config file ([#244](https://github.com/sandatech/terraform/issues/244))
- Allow passing of args to terraform_fmt ([#147](https://github.com/sandatech/terraform/issues/147))

### Fix
- command not found ([#251](https://github.com/sandatech/terraform/issues/251))
- execute tflint once in no errors ([#250](https://github.com/sandatech/terraform/issues/250))
- terrafrom_tflint ERROR output for files located in repo root ([#243](https://github.com/sandatech/terraform/issues/243))
- TFSec outputs the same results multiple times ([#237](https://github.com/sandatech/terraform/issues/237))


<a name="v1.52.0"></a>
## [v1.52.0] - 2021-10-04
### Feat
- Add new hook for `terraform providers lock` operation ([#173](https://github.com/sandatech/terraform/issues/173))
- Add PATH outputs when TFLint found any problem ([#234](https://github.com/sandatech/terraform/issues/234))

### Fix
- terraform_tflint hook executes in a serial way to run less often ([#211](https://github.com/sandatech/terraform/issues/211))
- Dockerfile if INSTALL_ALL is not defined ([#233](https://github.com/sandatech/terraform/issues/233))
- remove dead code from terraform-docs script ([#229](https://github.com/sandatech/terraform/issues/229))


<a name="v1.51.0"></a>
## [v1.51.0] - 2021-09-17
### Feat
- Add GH checks and templates ([#222](https://github.com/sandatech/terraform/issues/222))
- Add mixed line ending check to prevent possible errors ([#221](https://github.com/sandatech/terraform/issues/221))

### Fix
- trigger terraform-docs on changes in lock files ([#228](https://github.com/sandatech/terraform/issues/228))
- label auto-adding after label rename ([#226](https://github.com/sandatech/terraform/issues/226))
- Dockerized pre-commit-terraform ([#219](https://github.com/sandatech/terraform/issues/219))


<a name="v1.50.0"></a>
## [v1.50.0] - 2021-04-22
### Feat
- Adds support for Terrascan ([#195](https://github.com/sandatech/terraform/issues/195))


<a name="v1.49.0"></a>
## [v1.49.0] - 2021-04-20
### Fix
- Fix and pin versions in Dockerfile ([#193](https://github.com/sandatech/terraform/issues/193))


<a name="v1.48.0"></a>
## [v1.48.0] - 2021-03-12

<a name="v1.47.0"></a>
## [v1.47.0] - 2021-02-25
### Fix
- remove sed postprocessing from the terraform_docs_replace hook to fix compatibility with terraform-docs 0.11.0+ ([#176](https://github.com/sandatech/terraform/issues/176))


<a name="v1.46.0"></a>
## [v1.46.0] - 2021-02-20
### Fix
- Terraform validate for submodules ([#172](https://github.com/sandatech/terraform/issues/172))


<a name="v1.45.0"></a>
## [v1.45.0] - 2020-11-12
### Fix
- Correct deprecated parameter to terraform-docs ([#156](https://github.com/sandatech/terraform/issues/156))


<a name="v1.44.0"></a>
## [v1.44.0] - 2020-11-02
### Feat
- Make terraform_validate to run init if necessary ([#158](https://github.com/sandatech/terraform/issues/158))


<a name="v1.43.0"></a>
## [v1.43.0] - 2020-09-24
### Fix
- Fix regex considering terraform-docs v0.10.0 old ([#151](https://github.com/sandatech/terraform/issues/151))


<a name="v1.42.0"></a>
## [v1.42.0] - 2020-09-24
### Fix
- make terraform_docs Windows compatible ([#129](https://github.com/sandatech/terraform/issues/129))


<a name="v1.41.0"></a>
## [v1.41.0] - 2020-09-23
### Fix
- terraform-docs version 0.10 removed with-aggregate-type-defaults ([#150](https://github.com/sandatech/terraform/issues/150))


<a name="v1.40.0"></a>
## [v1.40.0] - 2020-09-22
### Feat
- Add possibility to share tflint config file for subdirs ([#149](https://github.com/sandatech/terraform/issues/149))


<a name="v1.39.0"></a>
## [v1.39.0] - 2020-09-08
### Feat
- Add checkov support ([#143](https://github.com/sandatech/terraform/issues/143))


<a name="v1.38.0"></a>
## [v1.38.0] - 2020-09-07
### Fix
- Correctly handle arrays in terraform_docs.sh ([#141](https://github.com/sandatech/terraform/issues/141))


<a name="v1.37.0"></a>
## [v1.37.0] - 2020-09-01
### Fix
- make terraform_tfsec.sh executable ([#140](https://github.com/sandatech/terraform/issues/140))


<a name="v1.36.0"></a>
## [v1.36.0] - 2020-09-01
### Feat
- have option for terraform_tfsec hook to only run in relevant modified directories ([#135](https://github.com/sandatech/terraform/issues/135))


<a name="v1.35.0"></a>
## [v1.35.0] - 2020-08-28
### Fix
- Squash terraform_docs bug ([#138](https://github.com/sandatech/terraform/issues/138))


<a name="v1.34.0"></a>
## [v1.34.0] - 2020-08-27

<a name="v1.33.0"></a>
## [v1.33.0] - 2020-08-27
### Fix
- Pass args and env vars to terraform validate ([#125](https://github.com/sandatech/terraform/issues/125))


<a name="v1.32.0"></a>
## [v1.32.0] - 2020-08-19
### Feat
- add terragrunt validate hook ([#134](https://github.com/sandatech/terraform/issues/134))


<a name="v1.31.0"></a>
## [v1.31.0] - 2020-05-27
### Fix
- Updated formatting in README (closes [#113](https://github.com/sandatech/terraform/issues/113))


<a name="v1.30.0"></a>
## [v1.30.0] - 2020-04-23
### Feat
- Support for TFSec ([#103](https://github.com/sandatech/terraform/issues/103))


<a name="v1.29.0"></a>
## [v1.29.0] - 2020-04-04
### Fix
- Change terraform_validate hook functionality for subdirectories with terraform files ([#100](https://github.com/sandatech/terraform/issues/100))


<a name="v1.28.0"></a>
## [v1.28.0] - 2020-04-04

<a name="v1.27.0"></a>
## [v1.27.0] - 2020-03-02

<a name="v1.26.0"></a>
## [v1.26.0] - 2020-02-21

<a name="v1.25.0"></a>
## [v1.25.0] - 2020-01-30

<a name="v1.24.0"></a>
## [v1.24.0] - 2020-01-21

<a name="v1.23.0"></a>
## [v1.23.0] - 2020-01-21

<a name="v1.22.0"></a>
## [v1.22.0] - 2020-01-13

<a name="v1.21.0"></a>
## [v1.21.0] - 2019-11-16

<a name="v1.20.0"></a>
## [v1.20.0] - 2019-11-02

<a name="v1.19.0"></a>
## [v1.19.0] - 2019-08-20

<a name="v1.18.0"></a>
## [v1.18.0] - 2019-08-20

<a name="v1.17.0"></a>
## [v1.17.0] - 2019-06-25

<a name="v1.16.0"></a>
## [v1.16.0] - 2019-06-18

<a name="v1.15.0"></a>
## [v1.15.0] - 2019-06-18

<a name="v1.14.0"></a>
## [v1.14.0] - 2019-06-17

<a name="v1.13.0"></a>
## [v1.13.0] - 2019-06-17

<a name="v1.12.0"></a>
## [v1.12.0] - 2019-05-27

<a name="v1.11.0"></a>
## [v1.11.0] - 2019-03-01

<a name="v1.10.0"></a>
## [v1.10.0] - 2019-02-21

<a name="v1.9.0"></a>
## [v1.9.0] - 2019-02-18

<a name="v1.8.1"></a>
## [v1.8.1] - 2018-12-15

<a name="v1.8.0"></a>
## [v1.8.0] - 2018-12-14

<a name="v1.7.4"></a>
## [v1.7.4] - 2018-12-11

<a name="v1.7.3"></a>
## [v1.7.3] - 2018-05-24

<a name="v1.7.2"></a>
## [v1.7.2] - 2018-05-20

<a name="v1.7.1"></a>
## [v1.7.1] - 2018-05-16

<a name="v1.7.0"></a>
## [v1.7.0] - 2018-05-16

<a name="v1.6.0"></a>
## [v1.6.0] - 2018-04-21

<a name="v1.5.0"></a>
## [v1.5.0] - 2018-03-06

<a name="v1.4.0"></a>
## [v1.4.0] - 2018-01-24

<a name="v1.3.0"></a>
## [v1.3.0] - 2018-01-15

<a name="v1.2.0"></a>
## [v1.2.0] - 2017-06-08

<a name="v1.1.0"></a>
## [v1.1.0] - 2017-02-04

<a name="v1.0.0"></a>
## v1.0.0 - 2016-09-27

[Unreleased]: https://github.com/sandatech/terraform/compare/v1.75.0...HEAD
[v1.75.0]: https://github.com/sandatech/terraform/compare/v1.74.2...v1.75.0
[v1.74.2]: https://github.com/sandatech/terraform/compare/v1.74.1...v1.74.2
[v1.74.1]: https://github.com/sandatech/terraform/compare/v1.74.0...v1.74.1
[v1.74.0]: https://github.com/sandatech/terraform/compare/v1.73.0...v1.74.0
[v1.73.0]: https://github.com/sandatech/terraform/compare/v1.72.2...v1.73.0
[v1.72.2]: https://github.com/sandatech/terraform/compare/v1.72.1...v1.72.2
[v1.72.1]: https://github.com/sandatech/terraform/compare/v1.72.0...v1.72.1
[v1.72.0]: https://github.com/sandatech/terraform/compare/v1.71.0...v1.72.0
[v1.71.0]: https://github.com/sandatech/terraform/compare/v1.70.1...v1.71.0
[v1.70.1]: https://github.com/sandatech/terraform/compare/v1.70.0...v1.70.1
[v1.70.0]: https://github.com/sandatech/terraform/compare/v1.69.0...v1.70.0
[v1.69.0]: https://github.com/sandatech/terraform/compare/v1.68.1...v1.69.0
[v1.68.1]: https://github.com/sandatech/terraform/compare/v1.68.0...v1.68.1
[v1.68.0]: https://github.com/sandatech/terraform/compare/v1.67.0...v1.68.0
[v1.67.0]: https://github.com/sandatech/terraform/compare/v1.66.0...v1.67.0
[v1.66.0]: https://github.com/sandatech/terraform/compare/v1.65.1...v1.66.0
[v1.65.1]: https://github.com/sandatech/terraform/compare/v1.65.0...v1.65.1
[v1.65.0]: https://github.com/sandatech/terraform/compare/v1.64.1...v1.65.0
[v1.64.1]: https://github.com/sandatech/terraform/compare/v1.64.0...v1.64.1
[v1.64.0]: https://github.com/sandatech/terraform/compare/v1.63.0...v1.64.0
[v1.63.0]: https://github.com/sandatech/terraform/compare/v1.62.3...v1.63.0
[v1.62.3]: https://github.com/sandatech/terraform/compare/v1.62.2...v1.62.3
[v1.62.2]: https://github.com/sandatech/terraform/compare/v1.62.1...v1.62.2
[v1.62.1]: https://github.com/sandatech/terraform/compare/v1.62.0...v1.62.1
[v1.62.0]: https://github.com/sandatech/terraform/compare/v1.61.0...v1.62.0
[v1.61.0]: https://github.com/sandatech/terraform/compare/v1.60.0...v1.61.0
[v1.60.0]: https://github.com/sandatech/terraform/compare/v1.59.0...v1.60.0
[v1.59.0]: https://github.com/sandatech/terraform/compare/v1.58.0...v1.59.0
[v1.58.0]: https://github.com/sandatech/terraform/compare/v1.57.0...v1.58.0
[v1.57.0]: https://github.com/sandatech/terraform/compare/v1.56.0...v1.57.0
[v1.56.0]: https://github.com/sandatech/terraform/compare/v1.55.0...v1.56.0
[v1.55.0]: https://github.com/sandatech/terraform/compare/v1.54.0...v1.55.0
[v1.54.0]: https://github.com/sandatech/terraform/compare/v1.53.0...v1.54.0
[v1.53.0]: https://github.com/sandatech/terraform/compare/v1.52.0...v1.53.0
[v1.52.0]: https://github.com/sandatech/terraform/compare/v1.51.0...v1.52.0
[v1.51.0]: https://github.com/sandatech/terraform/compare/v1.50.0...v1.51.0
[v1.50.0]: https://github.com/sandatech/terraform/compare/v1.49.0...v1.50.0
[v1.49.0]: https://github.com/sandatech/terraform/compare/v1.48.0...v1.49.0
[v1.48.0]: https://github.com/sandatech/terraform/compare/v1.47.0...v1.48.0
[v1.47.0]: https://github.com/sandatech/terraform/compare/v1.46.0...v1.47.0
[v1.46.0]: https://github.com/sandatech/terraform/compare/v1.45.0...v1.46.0
[v1.45.0]: https://github.com/sandatech/terraform/compare/v1.44.0...v1.45.0
[v1.44.0]: https://github.com/sandatech/terraform/compare/v1.43.0...v1.44.0
[v1.43.0]: https://github.com/sandatech/terraform/compare/v1.42.0...v1.43.0
[v1.42.0]: https://github.com/sandatech/terraform/compare/v1.41.0...v1.42.0
[v1.41.0]: https://github.com/sandatech/terraform/compare/v1.40.0...v1.41.0
[v1.40.0]: https://github.com/sandatech/terraform/compare/v1.39.0...v1.40.0
[v1.39.0]: https://github.com/sandatech/terraform/compare/v1.38.0...v1.39.0
[v1.38.0]: https://github.com/sandatech/terraform/compare/v1.37.0...v1.38.0
[v1.37.0]: https://github.com/sandatech/terraform/compare/v1.36.0...v1.37.0
[v1.36.0]: https://github.com/sandatech/terraform/compare/v1.35.0...v1.36.0
[v1.35.0]: https://github.com/sandatech/terraform/compare/v1.34.0...v1.35.0
[v1.34.0]: https://github.com/sandatech/terraform/compare/v1.33.0...v1.34.0
[v1.33.0]: https://github.com/sandatech/terraform/compare/v1.32.0...v1.33.0
[v1.32.0]: https://github.com/sandatech/terraform/compare/v1.31.0...v1.32.0
[v1.31.0]: https://github.com/sandatech/terraform/compare/v1.30.0...v1.31.0
[v1.30.0]: https://github.com/sandatech/terraform/compare/v1.29.0...v1.30.0
[v1.29.0]: https://github.com/sandatech/terraform/compare/v1.28.0...v1.29.0
[v1.28.0]: https://github.com/sandatech/terraform/compare/v1.27.0...v1.28.0
[v1.27.0]: https://github.com/sandatech/terraform/compare/v1.26.0...v1.27.0
[v1.26.0]: https://github.com/sandatech/terraform/compare/v1.25.0...v1.26.0
[v1.25.0]: https://github.com/sandatech/terraform/compare/v1.24.0...v1.25.0
[v1.24.0]: https://github.com/sandatech/terraform/compare/v1.23.0...v1.24.0
[v1.23.0]: https://github.com/sandatech/terraform/compare/v1.22.0...v1.23.0
[v1.22.0]: https://github.com/sandatech/terraform/compare/v1.21.0...v1.22.0
[v1.21.0]: https://github.com/sandatech/terraform/compare/v1.20.0...v1.21.0
[v1.20.0]: https://github.com/sandatech/terraform/compare/v1.19.0...v1.20.0
[v1.19.0]: https://github.com/sandatech/terraform/compare/v1.18.0...v1.19.0
[v1.18.0]: https://github.com/sandatech/terraform/compare/v1.17.0...v1.18.0
[v1.17.0]: https://github.com/sandatech/terraform/compare/v1.16.0...v1.17.0
[v1.16.0]: https://github.com/sandatech/terraform/compare/v1.15.0...v1.16.0
[v1.15.0]: https://github.com/sandatech/terraform/compare/v1.14.0...v1.15.0
[v1.14.0]: https://github.com/sandatech/terraform/compare/v1.13.0...v1.14.0
[v1.13.0]: https://github.com/sandatech/terraform/compare/v1.12.0...v1.13.0
[v1.12.0]: https://github.com/sandatech/terraform/compare/v1.11.0...v1.12.0
[v1.11.0]: https://github.com/sandatech/terraform/compare/v1.10.0...v1.11.0
[v1.10.0]: https://github.com/sandatech/terraform/compare/v1.9.0...v1.10.0
[v1.9.0]: https://github.com/sandatech/terraform/compare/v1.8.1...v1.9.0
[v1.8.1]: https://github.com/sandatech/terraform/compare/v1.8.0...v1.8.1
[v1.8.0]: https://github.com/sandatech/terraform/compare/v1.7.4...v1.8.0
[v1.7.4]: https://github.com/sandatech/terraform/compare/v1.7.3...v1.7.4
[v1.7.3]: https://github.com/sandatech/terraform/compare/v1.7.2...v1.7.3
[v1.7.2]: https://github.com/sandatech/terraform/compare/v1.7.1...v1.7.2
[v1.7.1]: https://github.com/sandatech/terraform/compare/v1.7.0...v1.7.1
[v1.7.0]: https://github.com/sandatech/terraform/compare/v1.6.0...v1.7.0
[v1.6.0]: https://github.com/sandatech/terraform/compare/v1.5.0...v1.6.0
[v1.5.0]: https://github.com/sandatech/terraform/compare/v1.4.0...v1.5.0
[v1.4.0]: https://github.com/sandatech/terraform/compare/v1.3.0...v1.4.0
[v1.3.0]: https://github.com/sandatech/terraform/compare/v1.2.0...v1.3.0
[v1.2.0]: https://github.com/sandatech/terraform/compare/v1.1.0...v1.2.0
[v1.1.0]: https://github.com/sandatech/terraform/compare/v1.0.0...v1.1.0
