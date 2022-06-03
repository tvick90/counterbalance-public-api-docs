# Permissions & Roles

## Roles

Roles are logical groupings of permission scopes that define what platform objects and operations a user is permitted to access.

### Role Types
| Type | Description |
|:-|:-|
| **System-Assigned Roles** |  |
| **Position-Based Roles**  |  |

### Predefined Roles
| Role ID | Name/Description | Permissions | 
|:-|:-|:-|
| **System-Assigned Roles** |
| `rol_mAdN91g5jh41yrwO` | **Tenant Owner** <br> All-access permissions for tenant owner assigned when tenant account is created | `*`
| `rol_BjYA2HwGRnfaFhuV` | **Console User** <br> Base permissions for console users assigned when account is created | `tenant:account:read` <br> `tenant:preferences:read` <br> `tenant:quota:read` <br> `user:permissions:read` <br> `user:roles:read` <br> `user:self:read`
| **Position-Based Roles**
| `rol_9t7sUEmXhoXG0JIn` |  **Automation Technician** <br> Permissions suitable for an automation/field/service technician | `infrastructure:*` <br> `sites:*` <br> `telemetry:*` 
| `rol_CxegVC5SoEeAUa6E` |  **Building Engineer** <br> Permissions suitable for a building engineer | `tenant:account:read` <br> `tenant:preferences:read`
| `rol_t0duC3p8gZbzhZ5a` |  **Energy Manager** <br> 	Permissions suitable for an energy manager | `tenant:account:read` <br> `tenant:preferences:read`

## Permissions

### All Permision Scopes
| **Permission Scope** | **Description** |
|:-|:-|
| **Absolute Wildcard**
| `*`                                  |	All access to literally everything
| **Automation Wildcard** 
| `automation:*`                       |	All access to automation component
| **Automation Resets** 
| `automation:reset:*`                 |	All access to setpoint resets
| `automation:reset:read`              |	View existing setpoint resets
| `automation:reset:create`            |	Create new setpoint resets
| `automation:reset:update`            |	Update existing setpoint resets
| `automation:reset:delete`            |	Delete existing setpoint resets
| **Automation Routines** 
| `automation:routine:*`               |	All access to routines
| `automation:routine:create`          |	Create new routines
| `automation:routine:read`            |	View existing routines
| `automation:routine:update`          |	Update existing routines
| `automation:routine:delete`          |	Delete existing routines
| **Automation Setbacks** 
| `automation:setback:*`               |	All access to equipment setbacks
| `automation:setback:create`          |	Create new equipment setbacks
| `automation:setback:read`            |	View existing equipment setbacks
| `automation:setback:update`          |	Update existing equipment setbacks
| `automation:setback:delete`          |	Delete existing equipment setbacks
| **Automation Triggers** 
| `automation:trigger:*`               |	All access to triggers
| `automation:trigger:create`          |	Create new triggers
| `automation:trigger:read`            |	View existing triggers
| `automation:trigger:update`          |	Update existing triggers
| `automation:trigger:delete`          |	Delete existing triggers
| **Billing Wildcard** 
| `billing:*`                          |	All access to billing & subscriptions
| **Billing Account** 
| `billing:account:*`                  |	All access to billing account
| `billing:account:create`             |	Activate billing account
| `billing:account:read`               |	View billing account
| `billing:account:update`             |	Update billing account
| `billing:account:delete`             |	Delete billing account
| **Invoice** 
| `billing:invoice:*`                  |	All access to invoices
| `billing:invoice:read`               |	View invoices
| **Payment Sources** 
| `billing:sources:*`                  |	All access to payment sources
| `billing:sources:create`             |	Create new payment sources
| `billing:sources:read`               |	View existing payment sources
| `billing:sources:update`             |	Update existing payment sources
| `billing:sources:delete`             |	Delete existing payment sources
| **Subscription** 
| `billing:subscription:*`             |	All access to subscriptions
| `billing:subscription:create`        |	Create new subscriptions
| `billing:subscription:read`          |	View existing subscriptions
| `billing:subscription:update`        |	Update existing subscriptions
| `billing:subscription:delete`        |	Delete existing subscriptions
| **Equipment Wildcard** 
| `equipment:*`                        |	All access to equipment component
| **Equipment Node** 
| `equipment:node:*`                   |	All access to equipment nodes
| `equipment:node:read`                |	View existing equipment nodes
| `equipment:node:create`              |	Create new equipment nodes
| `equipment:node:update`              |	Update existing equipment nodes
| `equipment:node:delete`              |	Delete existing equipment nodes
| **Equipment Node Telemetry** 
| `equipment:telemetry:*`              |	All access to equipment telemetry relationships
| `equipment:telemetry:create`         |	Create new equipment telemetry relationships
| `equipment:telemetry:read`           |	View existing equipment telemetry relationships
| `equipment:telemetry:update`         |	Update existing equipment telemetry relationships
| `equipment:telemetry:delete`         |	Delete existing equipment telemetry relationships
| **Infrastructure Wildcard** 
| `infrastructure:*`                   |	All access to connectivity component
| **Gateway Device** 
| `infrastructure:gateway:*`           |	All access to gateway devices
| `infrastructure:gateway:register`    |	Register new gateway devices
| `infrastructure:gateway:list`        |	List existing gateway devices <br> *__Deprecated__, use `*:read`*
| `infrastructure:gateway:read`        |	View existing gateway devices
| `infrastructure:gateway:manage`      |	Administer existing gateway devices
| `infrastructure:gateway:update`      |	Update existing gateway devices
| `infrastructure:gateway:delete`      |	Delete existing gateway devices
| **BACnet Device** 
| `infrastructure:controller:*`        |	All access to controller devices
| `infrastructure:controller:register` |	Register new controller devices
| `infrastructure:controller:list`     |	List existing controller devices <br> *__Deprecated__, use `*:read`*
| `infrastructure:controller:read`     |	View existing controller devices
| `infrastructure:controller:manage`   |	Administer existing controller devices
| `infrastructure:controller:update`   |	Update existing controller devices
| `infrastructure:controller:delete`   |	Delete existing controller devices
| **Intelligence Wildcard** 
| `intelligence:*`                     |	All access to building intelligence component
| **Intelligence FDD Rules** 
| `intelligence:rule:*`                |	All access to FDD rules
| `intelligence:rule:read`             |	View existing FDD rules
| `intelligence:rule:create`           |	Create new FDD rules
| `intelligence:rule:update`           |	Update existing FDD rules
| `intelligence:rule:delete`           |	Delete existing FDD rules
| **Intelligence Alarms** 
| `intelligence:alarm:*`               |	All access to alarms
| `intelligence:alarm:create`          |	Create new alarms
| `intelligence:alarm:read`            |	View existing alarms
| `intelligence:alarm:update`          |	Update existing alarms
| `intelligence:alarm:delete`          |	Delete existing alarms
| **Reporting Wildcard** 
| `reporting:*`                        |	All access to reporting component
| **Report Definition** 
| `reporting:report:*`                 |	All access to report definitions
| `reporting:report:read`              |	View existing report definitions
| `reporting:report:create`            |	Create new report definitions
| `reporting:report:update`            |	Update existing report definitions
| `reporting:report:delete`            |	Delete existing report definitions
| **Report Group** 
| `reporting:group:*`                  |	All access to report groups
| `reporting:group:create`             |	Create new report groups
| `reporting:group:read`               |	View existing report groups
| `reporting:group:update`             |	Update existing report groups
| `reporting:group:delete`             |	Delete existing report groups
| **Trend Plot Definition** 
| `reporting:plot:*`                   |	All access to plots
| `reporting:plot:create`              |	Create new plots
| `reporting:plot:read`                |	View existing plots
| `reporting:plot:update`              |	Update existing plots
| `reporting:plot:delete`              |	Delete existing plots
| **Sites Wildcard** 
| `sites:*`                            |	All access to sites component
| **Site Object** 
| `sites:site:*`                       |	All access to site objects
| `sites:site:read`                    |	View existing site objects
| `sites:site:create`                  |	Create new site objects
| `sites:site:update`                  |	Update existing site objects
| `sites:site:delete`                  |	Delete existing site objects
| **Site Address** 
| `sites:address:*`                    |	All access to address objects
| `sites:address:create`               |	Create new address objects
| `sites:address:read`                 |	View existing address objects
| `sites:address:update`               |	Update existing address objects
| `sites:address:delete`               |	Delete existing address objects
| **Site Floor** 
| `sites:floor:*`                      |	All access to floor objects
| `sites:floor:create`                 |	Create new floor objects
| `sites:floor:read`                   |	View existing floor objects
| `sites:floor:update`                 |	Update existing floor objects
| `sites:floor:delete`                 |	Delete existing floor objects
| **Site Room** 
| `sites:room:*`                       |	All access to room objects
| `sites:room:create`                  |	Create new room objects
| `sites:room:read`                    |	View existing room objects
| `sites:room:update`                  |	Update existing room objects
| `sites:room:delete`                  |	Delete existing room objects
| **Telemetry Wildcard** 
| `telemetry:*`                        |	All access to telemetry component
| **Collector** 
| `telemetry:collector:*`              |	All access to datapoint collector objects
| `telemetry:collector:create`         |	Create new datapoint collector objects
| `telemetry:collector:list`           |	List existing datapoint collectorobjects <br> *__Deprecated__, use `*:read`*
| `telemetry:collector:read`           |	View existing datapoint collector objects
| `telemetry:collector:update`         |	Update existing datapoint collector objects
| `telemetry:collector:delete`         |	Delete existing datapoint collector objects
| `telemetry:collector:sample`         |	Sample existing datapoint collector object data
| **BACnet Point** 
| `telemetry:datapoint:*`              |	All access to controller point objects
| `telemetry:datapoint:create`         |	Create new controller point objects
| `telemetry:datapoint:list`           |	List existing controller point objects <br> *__Deprecated__, use `*:read`*
| `telemetry:datapoint:read`           |	View existing controller point objects
| `telemetry:datapoint:command`        |	Command/relinquish existing controller point objects
| `telemetry:datapoint:update`         |	Update existing controller point objects
| `telemetry:datapoint:delete`         |	Delete existing controller point objects
| **BACnet Schedule** 
| `telemetry:schedule:*`               |	All access to controller schedule objects
| `telemetry:schedule:create`          |	Create new controller schedule objects
| `telemetry:schedule:list`            |	List existing controller schedule objects <br> *__Deprecated__, use `*:read`*
| `telemetry:schedule:read`            |	View existing controller schedule objects
| `telemetry:schedule:command`         |	Command/relinquish existing controller schedule objects
| `telemetry:schedule:update`          |	Update existing controller schedule objects
| `telemetry:schedule:delete`          |	Delete existing controller schedule objects
| **Tenant Wildcard** 
| `tenant:*`                           | All access to tenant account management
| **Tenant Account** 
| `tenant:account:*`                   |	All access to tenant account
| `tenant:account:read`                |	View tenant account
| `tenant:account:update`              |	Update tenant account
| `tenant:account:delete`              |	Delete tenant account
| **Tenant Preferences** 
| `tenant:preferences:*`               |	All access to tenant preferences
| `tenant:preferences:read`            |	View tenant preferences
| `tenant:preferences:update`          |	Update tenant preferences
| **Tenant Quota** 
| `tenant:quota:read`                  |	View tenant quotas
| **Tenant Licensing** 
| `tenant:licensing:*`                 |	All access to tenant licensing
| `tenant:licensing:add`               |	Add SKUs to tenant account
| `tenant:licensing:read`              |	View SKUs assigned to tenant account
| `tenant:licensing:remove`            |	Remove SKUs assigned to tenant account
| `tenant:licensing:assign`            |	Assign licensing to existing user accounts
| **Users Wildcard** 
| `user:*`                             |	Access to all user management
| **User Accounts** 
| `user:account:*`                     |	All access to user accounts
| `user:account:create`                |	Create new user accounts
| `user:account:list`                  |	List existing user accounts <br> *__Deprecated__, use `*:read`*
| `user:account:read`                  |	View existing user accounts
| `user:account:update`                |	Update existing user accounts
| `user:account:delete`                |	Delete existing user accounts
| **User Groups** 
| `user:group:*`                       |	All access to user groups
| `user:group:create`                  |	Create new user groups
| `user:group:list`                    |	List existing user groups <br> *__Deprecated__, use `*:read`*
| `user:group:read`                    |	View existing user groups
| `user:group:update`                  |	Update existing user groups
| `user:group:delete`                  |	Delete existing user groups
| **User Roles** 
| `user:roles:*`                       |	All access to user roles
| `user:roles:read`                    |	View roles assigned to existing user accounts
| `user:roles:update`                  |	Update roles assigned to existing user accounts
| `user:roles:remove`                  |	Remove roles from existing user accounts
| **User Permisions** 
| `user:permissions:read`              |	View user permissions
| **User Self-Service** 
| `user:self:*`                        |	All access to own user account
| `user:self:update`                   |	Update own user account
| `user:self:password`                 |	Update own user password
| `user:self:read`                     |	View own user account

