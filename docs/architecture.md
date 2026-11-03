# Medicalia Infrastructure Architecture

## 1. Overview

Medicalia is a fictional healthcare company whose IT infrastructure is based on a centralized Windows Server environment.

The infrastructure uses Active Directory Domain Services (AD DS) to manage users, organizational units, security groups and domain resources.

## 2. Infrastructure

| Component | Configuration |
|---|---|
| Hypervisor | Oracle VirtualBox |
| Server OS | Windows Server 2022 |
| Domain | medicalia.local |
| NetBIOS name | MEDICALIA |
| Directory Services | Active Directory Domain Services |
| DNS | Windows Server DNS |
| Server IPv4 | 10.0.2.15 |
| DNS address | 127.0.0.1 |

## 3. Active Directory Structure

The domain contains the following Organizational Unit hierarchy:

```text
medicalia.local
└── Medicalia
    ├── Empleados
    │   ├── Almacen
    │   ├── RRHH
    │   ├── Nutricion
    │   ├── Financiero
    │   └── Operaciones
    ├── Presidencia
    └── Equipos
```

Departmental security groups follow the `GG_` naming convention.

Examples:
- GG_Almacen
- GG_RRHH
- GG_Nutricion
- GG_Financiero
- GG_Operaciones

## 4. Network Configuration

The domain controller currently has the following IPv4 configuration:

- IP address: 10.0.2.15
- Subnet mask: 255.255.255.0
- DNS server: 127.0.0.1

The virtual network configuration and Windows client connectivity are pending validation.

## 5. Implementation Status

The domain controller, DNS role, organizational units, departmental security groups and domain user accounts have been configured.

The Windows client, shared resources, Group Policy configuration and connectivity tests remain pending.

## 6. Design Considerations

The infrastructure is designed to centralize identity management and apply security policies according to the company's organizational structure.

Further documentation will be added as the infrastructure evolves.
