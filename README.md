# Active Directory All The Things

Welcome to the **Active Directory All The Things** repository! This repository is designed to be a comprehensive resource for learning and working with Active Directory (AD) in various scenarios, including penetration testing, administration, and security.

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Tools and Utilities](#tools-and-utilities)
- [Setup and Configuration](#setup-and-configuration)
- [Enumeration and Reconnaissance](#enumeration-and-reconnaissance)
- [Exploitation Techniques](#exploitation-techniques)
- [Post-Exploitation](#post-exploitation)
- [Defensive Measures](#defensive-measures)
- [Resources](#resources)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Active Directory (AD) is a directory service developed by Microsoft for Windows domain networks. It is a crucial component in many IT environments, providing authentication and authorization services as well as management and configuration capabilities.

This repository aims to provide detailed guides, scripts, and resources for working with AD, whether you're an IT administrator, security professional, or penetration tester.

## Prerequisites

Before diving into the content of this repository, it's recommended to have a basic understanding of the following concepts:

- Windows Server and Client Operating Systems
- Networking Fundamentals
- Basic Security Principles
- Scripting (PowerShell, Bash)

## Tools and Utilities

This repository includes various tools and utilities that can be used for different AD tasks. Some of the key tools covered are:

- PowerView
- BloodHound
- Mimikatz
- LDAPSearch
- Impacket

## Setup and Configuration

### Installing Active Directory

1. **Install AD DS Role**: 
    ```bash
    Install-WindowsFeature -Name AD-Domain-Services -IncludeManagementTools
    ```

2. **Promote to Domain Controller**:
    ```bash
    Install-ADDSForest -DomainName "example.com"
    ```

### Configuring DNS

- Ensure that the DNS server is configured correctly to support AD DS.

## Enumeration and Reconnaissance

### LDAP Enumeration

```bash
ldapsearch -H ldap://support.htb -x -s base namingcontexts
