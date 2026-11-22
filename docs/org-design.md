# Security Group Design
## Naming scheme

Group naming follows a [GROUP TYPE]-[DIMENSION]-[VALUE] pattern.

This helps differentiate between group types (Security/Distribution/M365), and allows for flexibility when grouping by location, role, department and other dimensions.

###### Examples

    SEC-DEPT-IT
    SEC-ROLE-LEADERSHIP
    SEC-LOC-TAMPA

### Grouped By

At Northwind, groups are primarily grouped by department. 

However, not all groups are. See:

```
SEC-ROLE-LEADERSHIP
```

This group contains members from various departments.

### Trade-Offs

The flexibility does come at the risk of various overlapping groups. 
Someone in an IT leadership role in the Tampa region may belong to:

```
SEC-DEPT-IT
SEC-ROLE-LEADERSHIP
SEC-LOC-TAMPA
```

Without clear governance and policies managing group creation, it may become difficult to administer groups and audit their individual purposes.

## Non-Employee Identities

Contractors at Northwind are members of:

```
SEC-DEPT-CTR
```

### Trade-Offs
This scales poorly as contractors across all departments, roles, and regions will share this group.

## Potential Improvements
### Grouping Contractors
Growth at Northwind may require additional groups that step out of the traditional naming scheme like:

```
CTR-[DIMENSION]-[VALUE]
```

This will allow grouping contractors across several dimensions without lengthening group names.

### Grouping Leadership
As the organizational hierarchy evolves, there may be a need to group executives by:

```
SEC-DEPT-EXEC
```
While maintaining non-executives in a separate group like:

`SEC-DEPT-MGMT` or `SEC-DEPT-LEADERSHIP`

### Obstacles in Northwind Identity Provisioning
I added most users via a Bulk Create operation in Entra ID, using the downloaded template provided. 

I added a '[manager]' attribute/column to the spreadsheet and manually entered each users' manager.

After upload and processing, I realized this attribute isn't considered or populated via Bulk creation.
