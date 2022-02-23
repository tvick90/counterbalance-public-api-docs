# Permission Scopes

## Tenant
| **Permission Scope** | **Description** |
|:-|:-|
| **Tenant Wildcard** 
| `tenant:*`                  | All access to tenant account management |
| **Tenant Account** 
| `tenant:account:*`          |	All access to tenant account
| `tenant:account:read`       |	View tenant account
| `tenant:account:update`     |	Update tenant account
| `tenant:account:delete`     |	Delete tenant account
| **Tenant Preferences** 
| `tenant:preferences:*`      |	All access to tenant preferences
| `tenant:preferences:read`   |	View tenant preferences
| `tenant:preferences:update` |	Update tenant preferences
| **Tenant Quota** 
| `tenant:quota:read`         |	View tenant quotas
| **Tenant Licensing** 
| `tenant:licensing:*`        |	All access to tenant licensing
| `tenant:licensing:add`      |	Add SKUs to tenant account
| `tenant:licensing:read`     |	View SKUs assigned to tenant account
| `tenant:licensing:remove`   |	Remove SKUs assigned to tenant account
| `tenant:licensing:assign`   |	Assign licensing to existing user accounts
