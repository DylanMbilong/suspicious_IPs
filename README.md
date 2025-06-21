# 🚨 Suspicious IPs Tracker 🚨

![GitHub Repo stars](https://img.shields.io/github/stars/DylanMbilong/suspicious_IPs?style=social) ![GitHub Repo forks](https://img.shields.io/github/forks/DylanMbilong/suspicious_IPs?style=social) ![GitHub Release](https://img.shields.io/github/release/DylanMbilong/suspicious_IPs.svg)

Welcome to the **Suspicious IPs** repository. This project collects suspicious IP addresses from my SSH honeypot running on a cloud VPS. The honeypot accepts a small percentage of authentication requests, providing a controlled environment to monitor and log potentially malicious activity.

## 📥 Get Started

To explore the collected data, you can visit the [Releases section](https://github.com/DylanMbilong/suspicious_IPs/releases). Here, you will find the latest updates. If you need to download any specific file, make sure to execute it as per the instructions provided.

## 📊 Project Overview

### What is a Honeypot?

A honeypot is a security resource whose value lies in being probed, attacked, or compromised. In this case, the SSH honeypot serves to attract potential attackers, allowing us to gather data on their methods and the IP addresses they use.

### How It Works

1. **Random Acceptance**: The honeypot randomly accepts 1% of all authentication requests. This randomness helps create a realistic environment for attackers.
  
2. **Fake Shell**: Once accepted, the honeypot sends a fake Linux shell to the client. This shell simulates a real environment but does not grant any actual access to the server.

3. **Data Collection**: All interactions are logged, including the IP addresses of the clients attempting to connect. This data helps in identifying patterns and potential threats.

4. **Regular Updates**: The repository updates every 15 minutes, provided there is new activity. This ensures that the data remains current and relevant.

## 🔍 Topics Covered

- **Firewall**: Understanding how to configure firewalls to block suspicious IPs.
- **Hacking**: Insights into common hacking techniques used against SSH.
- **Honeypot**: The design and implementation of honeypots for security.
- **IPv4**: Working with IPv4 addresses and their significance in networking.
- **Linux**: Using Linux as the operating system for the honeypot.
- **Networking**: Fundamentals of networking that apply to security.
- **Security**: Best practices for maintaining secure systems.
- **Security Audit**: Conducting audits to find vulnerabilities.
- **Security Tools**: Tools and software that aid in security.
- **SSH**: Understanding SSH and its role in secure communications.

## 📈 Data Visualization

### Sample Data

To help you understand the data better, here’s a brief overview of what the logs might look like:

| Timestamp           | Source IP       | Action Taken     | Notes                  |
|---------------------|-----------------|-------------------|------------------------|
| 2023-10-01 12:00:00 | 192.168.1.1     | Accepted          | Attempted SSH login    |
| 2023-10-01 12:01:00 | 192.168.1.2     | Blocked           | Invalid credentials     |
| 2023-10-01 12:02:00 | 192.168.1.3     | Accepted          | Attempted SSH login    |

### Visualization Tools

You can use various tools to visualize the data:

- **Grafana**: For real-time monitoring and visualization.
- **Kibana**: For searching and analyzing log data.
- **Matplotlib**: A Python library for creating static, animated, and interactive visualizations.

## 🔒 Security Practices

### Configuring Your Firewall

1. **Block Known Bad IPs**: Use the collected data to block known malicious IPs.
2. **Whitelist Trusted IPs**: Allow only trusted IP addresses to connect.
3. **Rate Limiting**: Implement rate limiting to prevent brute-force attacks.

### Regular Audits

Conduct regular security audits to identify vulnerabilities in your system. Use the data collected from the honeypot to inform your audit process.

### Security Tools

Here are some essential security tools you might consider:

- **Fail2Ban**: Monitors log files and bans IPs that show malicious signs.
- **Snort**: An intrusion detection system that analyzes network traffic.
- **Wireshark**: A network protocol analyzer for troubleshooting and analysis.

## 🛠️ Installation

To set up your own SSH honeypot, follow these steps:

1. **Choose a VPS Provider**: Select a cloud VPS provider that meets your needs.
  
2. **Install Necessary Packages**:
   ```bash
   sudo apt update
   sudo apt install python3 python3-pip
   ```

3. **Clone the Repository**:
   ```bash
   git clone https://github.com/DylanMbilong/suspicious_IPs.git
   cd suspicious_IPs
   ```

4. **Run the Honeypot**:
   ```bash
   python3 honeypot.py
   ```

5. **Monitor Logs**: Check the logs to see incoming connections and their IP addresses.

## 📚 Resources

- [OWASP](https://owasp.org) - Open Web Application Security Project
- [NIST](https://www.nist.gov) - National Institute of Standards and Technology
- [CIS](https://www.cisecurity.org) - Center for Internet Security

## 🤝 Contributing

We welcome contributions to improve the project. If you have ideas or suggestions, please fork the repository and submit a pull request. Ensure that your code adheres to the existing style and passes all tests.

### Reporting Issues

If you encounter any issues, please open an issue in the repository. Provide as much detail as possible to help us address the problem quickly.

## 📅 Roadmap

- **Feature Enhancements**: Implement additional features for better data analysis.
- **Integration with Other Tools**: Explore integrations with other security tools.
- **User Documentation**: Improve documentation for better user experience.

## 📧 Contact

For any inquiries, feel free to reach out via GitHub issues or directly through my profile.

## 🌐 Visit Us

To stay updated with the latest releases, check out the [Releases section](https://github.com/DylanMbilong/suspicious_IPs/releases). Download any relevant files and execute them as needed.

---

This repository serves as a valuable resource for anyone interested in network security, honeypots, and monitoring suspicious activity. Your contributions and feedback are highly appreciated as we strive to make the internet a safer place.