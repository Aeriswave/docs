| Heading | Description |
| ---------- | --------- |
| `x-amz-acl` | Sets a [predefined ACL](../concepts/acl.md#predefined_acls) for an object. |
| `x-amz-grant-read` | Grants the access grantee object read permission. |
| `x-amz-grant-read-acp` | Grants the access grantee object ACL read permission. |
| `x-amz-grant-write-acp` | Grants the access grantee object ACL write permission. |
| `x-amz-grant-full-control` | Grants the access grantee the following permissions: `READ`, `WRITE`, `READ_ACP`, and `WRITE_ACP` for an object. |

The value for a `x-amz-grant-*` header is a comma-separated list of access grantees. Each access grantee is identified in a structure like: `<access grantee type>:<access grantee ID>`. {{ objstorage-name }} supports the following types of access grantees:

- `id` — access grantee — Yandex.Cloud user.
- `uri` — access grantee — system group.

Example:

```
x-amz-grant-read: uri="http://acs.amazonaws.com/groups/s3/AuthenticatedUsers"
```

