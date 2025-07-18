What is the difference between firewalld, iptables, nftables, ufw?

```md
`firewalld`, `iptables`, `nftables`, and `ufw` are all tools for managing firewall rules on Linux systems, but they have different designs, features, and use cases. Here's a breakdown of each:

### 1. iptables
- **Description**: A user-space utility program that allows the configuration of the Linux kernel firewall implemented as different Netfilter modules.
- **Functionality**: Uses a rule-based approach to allow or block traffic to and from network interfaces. Has multiple "tables" and "chains" for different types of rules.
- **Complexity**: Can be complex to manage as the rules can become intricate and require detailed knowledge of its syntax and behavior.
- **Status**: Considered a legacy tool as it has been largely replaced by `nftables` in many distributions.

### 2. nftables
- **Description**: A newer packet filtering framework, which is intended to replace `iptables`, `ip6tables`, `arptables`, and `ebtables`.
- **Functionality**: Provides a unified way to configure firewall rules for IPv4, IPv6, ARP, and Ethernet frames. It uses a single syntax and can manage large rule sets more efficiently.
- **Complexity**: Simplifies the rule-set management process with a more consistent syntax and better performance.
- **Status**: Recommended for new configurations and is actively developed and maintained.

### 3. firewalld
- **Description**: A dynamic firewall management tool that uses `nftables` or `iptables` as a backend. It abstracts the underlying complexity of these tools.
- **Functionality**: Provides zones (which define trust levels for network connections) and services (which represent predefined sets of rules). This makes it easier to manage, especially in dynamic environments.
- **Complexity**: User-friendly compared to `iptables`, especially with a graphical management tool available (`firewall-config`).
- **Status**: Used in many Linux distributions (like CentOS, Fedora, and RHEL) as the default firewall management tool.

### 4. UFW (Uncomplicated Firewall)
- **Description**: A user-friendly interface for managing firewall rules based on `iptables`.
- **Functionality**: Aimed primarily at ease of use; provides a simpler command-line interface to handle firewall settings and is often used for personal and small-scale server setups.
- **Complexity**: Extremely simple to use with straightforward commands, making it suitable for users who do not need intricate configurations.
- **Status**: Popular among users of Ubuntu and other Debian-based distributions.

### Summary
- **iptables**: Powerful but complex; mainly used historically.
- **nftables**: Modern replacement for `iptables`, offering unified rule management.
- **firewalld**: User-friendly abstraction over `nftables` or `iptables`, emphasizing dynamic management with zones and services.
- **UFW**: Simplifies firewall management using `iptables`; great for beginners and smaller installations.

When choosing among these options, consider your level of expertise, the complexity of your networking needs, and whether you prefer a command-line or GU-based management approach. For new setups, `nftables` or `firewalld` is generally recommended.
```

```md
`firewalld`、`iptables`、`nftables` 和 `ufw` 都是用于管理 Linux 系统防火墙规则的工具，但它们在设计、功能和使用场景上有所不同。以下是每个工具的详细介绍：

### 1. iptables
- **描述**：一个用户空间实用程序，允许配置作为不同 Netfilter 模块实现的 Linux 内核防火墙。
- **功能**：采用基于规则的方法来允许或阻止进出网络接口的流量。具有多个“表”和“链”以处理不同类型的规则。
- **复杂性**：管理起来可能比较复杂，因为规则可能变得复杂并且需要对其语法和行为有详细的了解。
- **状态**：被视为遗留工具，因为在许多发行版中，它已被 `nftables` 大部分取代。

### 2. nftables
- **描述**：一个较新的数据包过滤框架，旨在替代 `iptables`、`ip6tables`、`arptables` 和 `ebtables`。
- **功能**：提供统一的方式来配置 IPv4、IPv6、ARP 和以太网帧的防火墙规则。它使用统一的语法，并能更高效地管理大量规则集。
- **复杂性**：通过更统一的语法和更好的性能简化了规则集管理过程。
- **状态**：推荐用于新的配置，并且正在积极开发和维护中。

### 3. firewalld
- **描述**：一个动态防火墙管理工具，使用 `nftables` 或 `iptables` 作为后端。它抽象了这些工具的底层复杂性。
- **功能**：提供区域（定义网络连接的信任级别）和服务（表示预定义的规则集合）。这使得在动态环境中更容易管理。
- **复杂性**：相比 `iptables` 更加用户友好，尤其是提供了图形管理工具 (`firewall-config`)。
- **状态**：在许多 Linux 发行版中（如 CentOS、Fedora 和 RHEL）被作为默认的防火墙管理工具使用。

### 4. UFW (简单防火墙)
- **描述**：一个基于 `iptables` 的用户友好接口，用于管理防火墙规则。
- **功能**：主要以易用性为主，提供简单的命令行接口来处理防火墙设置，通常用于个人和小规模服务器设置。
- **复杂性**：使用起来极其简单，命令直观，非常适合不需要复杂配置的用户。
- **状态**：在 Ubuntu 和其他基于 Debian 的发行版中受到广泛欢迎。

### 总结
- **iptables**：功能强大但复杂；主要用于历史情况。
- **nftables**：`iptables` 的现代替代品，提供统一的规则管理。
- **firewalld**：在 `nftables` 或 `iptables` 之上提供用户友好的抽象，强调基于区域和服务的动态管理。
- **UFW**：使用 `iptables` 简化防火墙管理；非常适合初学者和较小的安装场景。

在这些选项中进行选择时，请考虑您的专业水平、网络需求的复杂性以及您是偏好命令行还是图形用户界面的管理方式。对于新配置，通常推荐使用 `nftables` 或 `firewalld`。
```