# Installation Guide

## 1. Virtualization Environment

The infrastructure is deployed using Oracle VirtualBox.

A virtual machine was created to host the Windows Server 2022 operating system.

## 2. Operating System

- Operating system: Windows Server 2022
- Installation type: Desktop Experience (GUI)

## 3. Active Directory Domain Services

The Active Directory Domain Services role was installed through Server Manager.

The server was then promoted to a domain controller by creating a new forest.

Configuration:

- Domain: `medicalia.local`
- NetBIOS name: `MEDICALIA`
- DNS Server: Installed
- Global Catalog: Enabled

## 4. DNS Configuration

DNS was installed during the domain controller promotion process.

The server uses its local DNS service (`127.0.0.1`) for domain name resolution.

## 5. Current Status

The domain controller has been successfully deployed and the initial Active Directory structure has been created.

Client integration and additional infrastructure configuration are pending.
