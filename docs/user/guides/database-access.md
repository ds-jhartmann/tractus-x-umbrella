# Database Access

This guide provides instructions to access the Postgres databases deployed as part of the Umbrella Chart.

## Overview

The Umbrella Chart includes a `pgadmin4` instance for easy management of Postgres databases. This service is only accessible within the Kubernetes cluster.

## Accessing pgAdmin4

### URL

You can access pgAdmin4 at the following URL, because it is enabled by default:
```
http://pgadmin4.tx.test
```

### Credentials

Use the following credentials to log in to pgAdmin4:
- **Username**: `pgadmin4@txtest.org`
- **Password**: `tractusxpgadmin4`

## Adding Database Connections

After logging in to pgAdmin4, you need to manually add connections for the databases you want to access.

### Default Postgres Credentials

For all connections:
- **Username**: `postgres`
- **Port**: `5432`

### Database Connection Details

| Component         | Host                              |Password                   |
|-------------------|-----------------------------------|---------------------------|
| Portal            | `umbrella-portal-backend-postgresql` |`dbpasswordportal`         |
| CentralIdP        | `umbrella-centralidp-postgresql`    |`dbpasswordcentralidp`     |
| SharedIdP         | `umbrella-sharedidp-postgresql`    |`dbpasswordsharedidp`      |
| MIW               | `umbrella-miw-postgres`            |`dbpasswordmiw`            |
| Data Provider     | `umbrella-dataprovider-db`         |`dbpasswordtxdataprovider` |
| Data Consumer 1   | `umbrella-dataconsumer-1-db`       |`dbpassworddataconsumerone`|
| Data Consumer 2   | `umbrella-dataconsumer-2-db`       |`dbpassworddataconsumertwo`|
| BPDM              | `umbrella-bpdm-postgres`           |`dbpasswordbpdm`           |

## Verifying Database Access

To verify access, follow these steps:

1. Open pgAdmin4.
2. Add a new server connection for the desired database.
3. Test the connection by browsing schemas and running queries.

For further assistance, refer to the [pgAdmin documentation](https://www.pgadmin.org/docs/).

## NOTICE

This work is licensed under the [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/legalcode).

* SPDX-License-Identifier: CC-BY-4.0
* SPDX-FileCopyrightText: 2024 Contributors to the Eclipse Foundation
* Source URL: <https://github.com/eclipse-tractusx/tractus-x-umbrella>
