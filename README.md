# Kokokbeluk-SOC
kokokbeluk adalah Security Operations Center (SOC) yang efektif. 
Menggunakan Wazuh yang terintegrasi dengan 10 tools open source terbaik untuk meningkatkan: 
1. deteksi ancaman,
2. analisis forensik, dan
3. respons otomatis.

# 🔐 Wazuh Integrations Toolkit

Automated scripts to integrate Wazuh with 10 open-source security tools for enhanced SOC capabilities.

## 🌟 Featured Integrations
| #  | Tool              | Category          | Integration Method           |
|----|-------------------|-------------------|------------------------------|
| 1  | Suricata          | IDS/IPS           | JSON alerts to Wazuh Manager  |
| 2  | Zeek              | Network Analysis  | Filebeat module              |
| 3  | MISP              | Threat Intel      | Python integration           |
| 4  | TheHive           | Incident Response | REST API connector           |
| 5  | Shuffle           | SOAR              | Webhooks                     |
| 6  | Snort             | IDS               | Unified2 format              |
| 7  | GRR               | Forensics         | Remote API                   |
| 8  | Cortex            | IOC Analysis      | TheHive4py library           |
| 9  | OpenSearch        | Log Management    | Replace Elasticsearch        |
| 10 | MITRE ATT&CK      | Framework         | TTP mapping                  |

## 🛠️ Prerequisites
- Wazuh Manager 4.7+
- Ubuntu/Debian/CentOS
- Root/sudo access

## 🚀 Quick Start
```bash
git clone https://github.com/yourrepo/wazuh-integrations.git
cd wazuh-integrations
chmod +x wazuh_integrations.sh
sudo ./wazuh_integrations.sh
```

## 📚 Detailed Documentation
### Suricata Integration
1. Automatically installs Suricata
2. Configures JSON alert output to Wazuh Manager
3. Enables Suricata rules auto-update

```xml
<!-- Example Wazuh config for Suricata -->
<localfile>
  <location>/var/log/suricata/eve.json</location>
  <log_format>json</log_format>
</localfile>
```

### MISP Integration
[![MISP-Wazuh](https://img.shields.io/badge/MISP-v2.4-green)](https://www.misp-project.org/)

```python
# Sample MISP event processor
def process_event(alert):
    ioc = alert['data']['srcip']
    misp.search(value=ioc)
```

## 🧩 Custom Integrations
For advanced users:
```bash
# Manual GRR integration
wget https://raw.githubusercontent.com/google/grr/master/scripts/install_script_ubuntu.sh
```

## 📜 License
GNU v3.0 License - See [LICENSE](LICENSE) for details.

## 🤝 Contributing
Pull requests welcome! For major changes, please open an issue first.
