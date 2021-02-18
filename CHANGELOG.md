<a name="v2.19.0"></a>
## [v2.19.0] - 2021-02-18
### Bug Fixes
- replacement for deadlink linter
- cannot create resource "newrelic_infra_alert_condition" of type "infra_host_not_reporting"
- replacement for deadlink linter
- **alert_channel:** avoid config drift with sensitive values not returned by the API
- **alert_channel:** avoid drift with config.auth_password
- **alert_condition:** remove conditional to fix drift when using 'user_defined' attributes
- **alert_muting_rule:** condition tag validation
- **alert_muting_rule:** update test expectation to match input
- **alert_policy:** avoid drift due to account_id inheritance in resource and data source
- **alerts:** Unify how alert policy selects an account_id
- **alerts:** flatten condition scope properly for APM JVM metrics
- **alerts:** require at least one violation time limit attr
- **alerts:** ensure threshold_occurrences case fold comparison
- **alerts:** avoid bad index reference
- **alerts:** improve nil handling for alert_channel
- **build:** update version.ProviderVersion via ldflags during release process
- **changelog:** ensure proper branch to base from
- **changelog:** update changelog on release only, drop reviewer spec
- **dashboard:** use state migration to fix 500 error when upgrading from v2.7.5 to v2.8 and beyond
- **docs:** extra whitespace below table
- **docs:** Alert Channels do not manage Policies
- **docs:** better table header rendering
- **entity:** add VIZ domain
- **infra:** avoid nil pointer reference
- **infra:** avoid nil pointer reference
- **infra_alert_condition:** fix integration tests
- **infra_alert_condition:** support zero-value thresholds for infra_alert_condition resource
- **newrelic_alert_condition:** allow instance scope for JVM app metrics
- **newrelic_entity:** include additional ID attr for browser apps
- **nrql_alert_condition:** fix fill_option DiffSuppressFunc
- **nrql_alert_condition:** avoid drift due to account_id inheritance in NRQL alert condition
- **nrql_alert_condition:** fix drift with threshold_occurrences - store lowercase in terraform state
- **nrql_alert_condition:** avoid drift using computed value
- **nrql_alert_condition:** reverse attribute detection for migration
- **nrql_alert_condition:** add missing zeros to violation_time_limit_seconds to the new:old map
- **nrql_alert_condition:** validate operator based on condition type
- **nrql_alert_condition:** use better term operator
- **nrql_alert_condition:** Fixed an issue with extrapolation (gap filling) settings
- **nrql_alert_condition:** update validation for nrql conditions
- **one_dashboard:** Table Widget should have filter on them
- **one_dashboard:** Inherit nrql_query account_id from dashboard by default

### Documentation Updates
- update infra alert condition api key type
- update changelog
- communicate that most but not all keys have prefixes
- fix broken links in api_access_key.html.markdown
- fix broken links
- fix broken links
- fix broken links
- update changelog
- change personal API key to user api key
- update API key instructions for getting started guide
- update getting started guide with a link to EU graphiql
- fix broken links
- include note about API key access
- update process running example
- update changelog
- update changelog
- add instructions for New Relic One users to get an api key
- replace uses of APM conditions with NRQL conditions
- add website documentation for nrql_alert aggregation_window
- remove admin key from documentation
- remove admin API key from docs and various other updates
- update authentication table
- fix references to newrelic_entity data sources
- update changelog
- update changelog
- update changelog
- update changelog
- update changelog
- update development instructions for new TF version
- DEPRECATION notice for newrelic_alert_condition
- update supported Go information and test config
- change slack integration documentation
- update changelog
- **README:** update provider configuration pin version examples
- **alert_channel:** add note to import section regarding handling of sensitive data
- **alert_condition:** document apm_jvm_metric
- **alert_muting_rule:** Added docs for alert muting rule.
- **alert_policy:** update alert_policy import section, add  default to arg ref
- **alert_policy_channel:** update example reference
- **alerts:** update documentation for newrelic_nrql_alert_condition
- **alerts:** include account_id attribute for alert_policy
- **dashboard:** Improve docs for limit and order_by widget attributes
- **dashboard:** update docs regarding cross-account widget config drift
- **dashboard:** add cross-account example
- **dashboard:** fix some broken links
- **dashboard:** update docs with info regarding widget.account_id and cross-account widgets
- **newrelic_synthetics_monitor_script:** Use file method instead of template_file data source
- **nrql_alert_condition:** Amends threshold_duration constraints for NRQL alert conditions
- **nrql_alert_condition:** include notes about upgrading from 1.x
- **nrql_condition:** add clarity around choosing between new and old/deprecated attributes
- **nrql_condition:** clarify when value_function attr is 'required' vs 'not required'
- **one_dashboard:** Add overview doc for one_dashboard resource
- **one_dashboard:** remove unused entity reference in example
- **one_dashboard:** add linked_entity_guids to newrelic_one_dashboard resource docs
- **provider:** additional v2 updates, migration guide updates
- **provider:** update getting started example to reflect v2 updates
- **provider:** add environment variables and schema attribute table
- **provider:** add getting started guide to the quick links
- **provider:** fix incorrect newrelic_application reference in some examples
- **provider:** add account_id to argument reference, move argument reference above the fold
- **readme:** update title, add link to latest documentation
- **synthetics:** remove newrelic_synthetics_label resource
- **synthetics_monitor_location:** Adding docs for Synthetics monitor location data source.

### Features
- add a newrelic_account data source
- **aggregation_window:** add support for nrql signal aggregationWindow
- **alert_muting_rule:** Creating alert muting rule resource.
- **alert_muting_rule:** add schedule support
- **alerts:** allow a 30 day violation limit for nrql conditions
- **alerts:** deprecate plugins conditions and un-deprecate APM alert conditions
- **alerts:** new newrelic_alerts_location_failure_condition resource
- **client:** update newrelic-client-go (retry on nerdgraph timeouts)
- **dashboard:** enable Personal API Key auth for dashboards and some sythentics resources
- **dashboard:** support cross-account widgets :)
- **infra_alert_condition:** add description attribute
- **newrelic_api_access_key:** Implement new resource: newrelic_api_access_key
- **nrql_alert_condition:** Added support for expiration (loss of signal) and extrapolation (gap filling) settings
- **nrql_alert_condition:** swap deprecation of violation_time_limit fields
- **one_dashboard:** Add support for widget_funnel
- **one_dashboard:** Add widget_heatmap
- **one_dashboard:** add linked entities to widget schema
- **one_dashboard:** Add support for widget_bullet
- **one_dashboard:** Testing out one_dashboard resource
- **one_dashboard:** Add support for widget_histogram
- **synthetics:** replace REST API calls with Nerdgraph calls
- **synthetics_monitor_location:** Add data source newrelic_synthetics_monitor_location.

<a name="v2.1.1"></a>
## [v2.1.1] - 2020-06-23
### Features
- update the release process to prepare for repo handoff

<a name="v2.1.0"></a>
## [v2.1.0] - 2020-06-22
### Documentation Updates
- include information on pinning a version
- include sidebar link for 2.x upgrade

### Features
- **eventstometrics:** add an events to metrics rule resource ([#690](https://github.com/newrelic/terraform-provider-newrelic/issues/690))

<a name="v2.0.0"></a>
## [v2.0.0] - 2020-06-18
### Bug Fixes
- Require condition_scope = `instance` for validation_close_timer
- Add validation to newrelic_alert_condtion condition_scope
- **alerts:** remove DiffSuppressFunc on TypeSet to avoid test drift
- **alerts:** infra alert condition zero value detection
- **alerts:** handle a nil reference with more grace
- **application_settings:** Remove delete, as it is not possible
- **deps:** Revert terraform sdk to 1.10.0
- **newrelic:** fix the failing integration tests ([#519](https://github.com/newrelic/terraform-provider-newrelic/issues/519))
- **nrql_alert_condition:** threshold_occurrences is case insensitive, attribute description updates

### Documentation Updates
- add callout to top of each v1.x doc page
- tidy up after review
- DEPRECATION notice for 1.x
- update index header with improved words
- update getting started guide to reference new material
- update README with new pointers
- add table for current endpoint in use per resource
- include documentation about upgrading the provider to 2.x
- update API key references to match desires
- include v1 index.html in sidebar
- prep for v2.x, isolate v1.x docs
- **alert_channel:** fix broken 'nested config' anchor link
- **alerts:** include caveat about NRQL alerts condition operator usage with outliers
- **alerts:** update wording to avoid implementation details
- **alerts:** include deprecation notice for "terms"
- **alerts:** update examples to reflect deprecation
- **getting started:** fix resource naming
- **nrql_alert_condition:** add outlier example, add new attributes, deprecate old attributes, update import section
- **nrql_alert_condition:** update docs to reflect version 2.0 changes
- **provider:** add region to provider docs, removing references to API base URLs
- **provider:** add provider configuration guide page
- **workloads:** fix api key attribute name ([#489](https://github.com/newrelic/terraform-provider-newrelic/issues/489))

### Features
- **alerts:** convert Alerts Policies to nerdgraph
- **application:** implement newrelic_application resource
- **dashboard:** add grid_column_count to dashboard schema
- **entity_tags:** add an entity tag resource ([#679](https://github.com/newrelic/terraform-provider-newrelic/issues/679))
- **nrql_alert_condition:** integrate nerdgraph for nrql alert conditions
- **provider:** add region to provider schema, handle API URLs based off region

<a name="v1.19.0"></a>
## [v1.19.0] - 2020-06-05
### Bug Fixes
- **test:** Workloads returns ordered list of scope account IDs, update test

### Documentation Updates
- **application_settings:** add application settings resource to sidebar ([#582](https://github.com/newrelic/terraform-provider-newrelic/issues/582))

<a name="v1.18.0"></a>
## [v1.18.0] - 2020-05-15
### Bug Fixes
- **alerts:** infra alert condition zero value detection

### Features
- **application:** implement newrelic_application resource ([#558](https://github.com/newrelic/terraform-provider-newrelic/issues/558))

<a name="v1.17.1"></a>
## [v1.17.1] - 2020-05-04
### Bug Fixes
- **client:** update the client for pagination URL fix

<a name="v1.17.0"></a>
## [v1.17.0] - 2020-05-01
### Features
- **dashboard:** add grid_column_count to dashboard schema

<a name="v1.16.0"></a>
## [v1.16.0] - 2020-03-24
### Documentation Updates
- use correct default synthetics_api_url in config docs, remove inaccessible alert condition type
- Update getting started guide

### Features
- **workloads:** add a workloads resource ([#474](https://github.com/newrelic/terraform-provider-newrelic/issues/474))

<a name="v1.15.1"></a>
## [v1.15.1] - 2020-03-18
### Bug Fixes
- import condition terms regardless of threshold format ([#469](https://github.com/newrelic/terraform-provider-newrelic/issues/469))

### Documentation Updates
- ensure consistency ([#458](https://github.com/newrelic/terraform-provider-newrelic/issues/458))
- **examples:** add a golden signal alerting module example ([#450](https://github.com/newrelic/terraform-provider-newrelic/issues/450))

<a name="v1.15.0"></a>
## [v1.15.0] - 2020-03-04
### Bug Fixes
- **application_label:** use correct type assertions for applications and servers attributes
- **nrql_alert_condition:** terms should be a TypeSet

### Documentation Updates
- **alert_policy_channel:** include sorting recommendation for channel_ids

### Features
- **alert_policy_channels:** add ability to add multiple channels to a policy

<a name="v1.14.0"></a>
## [v1.14.0] - 2020-02-20
### Bug Fixes
- **provider:** deprecate and re-enable the use of infra_api_url ([#411](https://github.com/newrelic/terraform-provider-newrelic/issues/411))

### Features
- **alert_policy:** add ability to add multiple channels to a policy ([#398](https://github.com/newrelic/terraform-provider-newrelic/issues/398))
- **synthetics:** add secure credentials resource ([#409](https://github.com/newrelic/terraform-provider-newrelic/issues/409))
- **synthetics:** add labels resource ([#407](https://github.com/newrelic/terraform-provider-newrelic/issues/407))

<a name="v1.13.1"></a>
## [v1.13.1] - 2020-02-12
### Bug Fixes
- **alert_channel:** validate payload also has payload_type specified
- **alert_channels:** allow complex headers & payloads with new attributes
- **alert_condition:** mark condition_scope optional
- **newrelic_alert_channel:** Force new resource for all config fields

### Documentation Updates
- **alert_channel:** add payload_type details to docs

<a name="v1.13.0"></a>
## [v1.13.0] - 2020-02-06
### Documentation Updates
- Make a note about community resources and support
- Make note about ignoring secrets

### Features
- replace provider backend with newrelic-client-go ([#358](https://github.com/newrelic/terraform-provider-newrelic/issues/358))
- **infra_alert_condition:** add violation_close_timer to newrelic_infra_alert_condition resource ([#370](https://github.com/newrelic/terraform-provider-newrelic/issues/370))

<a name="v1.12.2"></a>
## [v1.12.2] - 2020-01-25
### Bug Fixes
- **alert_channels:** handle more complex JSON structures in payload or headers ([#361](https://github.com/newrelic/terraform-provider-newrelic/issues/361))

<a name="v1.12.1"></a>
## [v1.12.1] - 2020-01-22
### Bug Fixes
- **newrelic-client-go:** Fix API Key passing to provider

### Documentation Updates
- update alert-channel examples

<a name="v1.12.0"></a>
## [v1.12.0] - 2020-01-16
### Bug Fixes
- **dashboards:** include application_breakdown as a valid visualization

### Documentation Updates
- **alerts:** update documentation for newrelic_alert_channel
- **dashboards:** include application_breakdown in docs

### Features
- **alerts:** deprecate alerts channel configuration and add config block

<a name="v1.11.0"></a>
## [v1.11.0] - 2020-01-09
### Documentation Updates
- update docs for consistency
- document the new synthetics_api_url variable

### Features
- release 1.11.0
- update CHANGELOG for v1.11.0

<a name="v1.10.0"></a>
## [v1.10.0] - 2019-12-18
### Bug Fixes
- make event a computed attribute
- loosen validation for threshold duration
- add attribute validation for infra condition types

### Documentation Updates
- update documentation for newrelic_infra_alert_condition
- update newrelic_synthetics_monitor docs
- add missing resources and data source to sidebar
- updates for consistency

### Features
- add ability to import resource_newrelic_synthetics_monitor, update acceptance tests and add coverage

<a name="v1.9.0"></a>
## [v1.9.0] - 2019-12-05
### Bug Fixes
- use name as filter in application lookup
- fix newrelic_infra_alert imports and backfill acc testing

### Documentation Updates
- update for clarity and consistency
- update nrql_alert_condition docs to reference violation_time_limit_seconds
- update docs for newrelic_nrql_alert_condition
- refresh the infra alert condition docs
- add docs for newrelic_plugin_component
- update docs for newrelic_alert_channel resource and data source
- fix formatting in dashboard docs

### Features
- allow importing of violation_time_limit_seconds, add validation, remove inline docs
- add ability to import nrql_alert_condition for types static and outlier
- update newrelic_synthetics_alert_condition  acceptance tests
- update newrelic_synthetics_monitor_script acceptance tests
- add a plugin component data source
- create importer for alert policy channels
- add ability to import newrelic_alert_channel data source

<a name="v1.8.0"></a>
## [v1.8.0] - 2019-11-22
### Bug Fixes
- appease golangci-lint when running make

### Documentation Updates
- add Getting Started section

### Features
- add import functionality for newrelic_alert_policy data source

<a name="v1.7.0"></a>
## [v1.7.0] - 2019-11-13
### Bug Fixes
- align alert condition duration constraints to NR's API constraints
- align alert policy validation with NR's API validation
- lint issue, update modules
- merge conflicts
- typos

<a name="v1.6.0"></a>
## [v1.6.0] - 2019-11-07
<a name="v1.5.2"></a>
## [v1.5.2] - 2019-10-23
<a name="v1.5.1"></a>
## [v1.5.1] - 2019-07-11
<a name="v1.5.0"></a>
## [v1.5.0] - 2019-03-26
<a name="v1.4.0"></a>
## [v1.4.0] - 2019-02-27
<a name="v1.3.0"></a>
## [v1.3.0] - 2019-02-07
<a name="v1.2.0"></a>
## [v1.2.0] - 2018-11-02
<a name="v1.1.0"></a>
## [v1.1.0] - 2018-10-16
<a name="v1.0.1"></a>
## [v1.0.1] - 2018-06-06
<a name="v1.0.0"></a>
## [v1.0.0] - 2018-02-12
<a name="v0.1.1"></a>
## [v0.1.1] - 2017-08-02
<a name="v0.1.0"></a>
## v0.1.0 - 2017-06-21
[Unreleased]: https://github.com/newrelic/terraform-provider-newrelic/compare/v2.19.0...HEAD
[v2.19.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v2.1.1...v2.19.0
[v2.1.1]: https://github.com/newrelic/terraform-provider-newrelic/compare/v2.1.0...v2.1.1
[v2.1.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v2.0.0...v2.1.0
[v2.0.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.19.0...v2.0.0
[v1.19.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.18.0...v1.19.0
[v1.18.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.17.1...v1.18.0
[v1.17.1]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.17.0...v1.17.1
[v1.17.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.16.0...v1.17.0
[v1.16.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.15.1...v1.16.0
[v1.15.1]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.15.0...v1.15.1
[v1.15.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.14.0...v1.15.0
[v1.14.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.13.1...v1.14.0
[v1.13.1]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.13.0...v1.13.1
[v1.13.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.12.2...v1.13.0
[v1.12.2]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.12.1...v1.12.2
[v1.12.1]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.12.0...v1.12.1
[v1.12.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.11.0...v1.12.0
[v1.11.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.10.0...v1.11.0
[v1.10.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.9.0...v1.10.0
[v1.9.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.8.0...v1.9.0
[v1.8.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.7.0...v1.8.0
[v1.7.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.6.0...v1.7.0
[v1.6.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.5.2...v1.6.0
[v1.5.2]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.5.1...v1.5.2
[v1.5.1]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.5.0...v1.5.1
[v1.5.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.4.0...v1.5.0
[v1.4.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.3.0...v1.4.0
[v1.3.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.2.0...v1.3.0
[v1.2.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.1.0...v1.2.0
[v1.1.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.0.1...v1.1.0
[v1.0.1]: https://github.com/newrelic/terraform-provider-newrelic/compare/v1.0.0...v1.0.1
[v1.0.0]: https://github.com/newrelic/terraform-provider-newrelic/compare/v0.1.1...v1.0.0
[v0.1.1]: https://github.com/newrelic/terraform-provider-newrelic/compare/v0.1.0...v0.1.1
