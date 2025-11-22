# 🛡️ NIS2 Compliance Mapper

A comprehensive web-based tool for managing NIS2 Directive (EU Directive 2022/2555) compliance across multiple entities. Built for Information Security Officers, Compliance Teams, and Risk Managers.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## 📋 Overview

The NIS2 Directive establishes cybersecurity requirements for essential and important entities across the EU. This tool helps organizations:

- Track compliance across all 13 core NIS2 requirements
- Manage multiple entities in a portfolio view
- Map to industry standards (ISO 27001, NIST CSF, CIS Controls)
- Identify critical gaps with personal management liability
- Generate compliance reports and visualizations

## ✨ Key Features

### 🎯 **Multi-Entity Management**
- Track compliance for unlimited entities/business units
- Portfolio-wide overview and statistics
- Entity comparison and benchmarking

### 📊 **Visual Dashboards**
- Real-time compliance scoring
- Interactive heatmaps showing status across all requirements
- Color-coded progress tracking
- Chart.js powered visualizations

### 📋 **Comprehensive Requirements Tracking**
All 13 core NIS2 articles including:
- Art. 20: Governance
- Art. 21(2): Technical & Operational Measures (a-j)
- Art. 23: Incident Reporting
- Art. 24: European Cybersecurity Schemes

### 🔗 **Standards Mapping**
Cross-reference NIS2 requirements with:
- **ISO 27001:2022** controls
- **NIST Cybersecurity Framework 2.0**
- **CIS Controls v8**

### 🚨 **Risk Management**
- Critical gap identification (requirements with personal management liability)
- Common gaps analysis across entities
- Penalty information for each requirement
- Prioritized remediation recommendations

### 📎 **Evidence Management**
- Document compliance evidence per requirement
- Track evidence count and coverage
- Notes and commentary support

### 📤 **Export Capabilities**
- JSON data export
- CSV compliance reports
- Portfolio-wide summary reports
- Ready for SharePoint integration

## 🚀 Getting Started

### Quick Start (No Installation Required)

1. **Download the tool:**
   ```bash
   git clone https://github.com/YOUR-USERNAME/nis2-compliance-mapper.git
   ```

2. **Open in browser:**
   - Simply open `nis2-compliance-mapper-enhanced.html` in any modern browser
   - No server, no dependencies, no setup required!

3. **Create your first entity:**
   - Enter an entity name (e.g., "IT Infrastructure")
   - Click "Save"
   - Start tracking compliance

### Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

## 📖 Usage Guide

### Single Entity Mode

1. **Create Entity:** Enter name and click "New Entity"
2. **Track Requirements:** Update status for each NIS2 article
   - ✓ Compliant
   - ⚠ Partial
   - ✗ Non-Compliant
   - N/A Not Applicable
3. **Add Evidence:** Document your compliance proof
4. **Add Notes:** Track implementation details

### Portfolio View

1. **Switch View:** Select "Portfolio Overview" from view mode dropdown
2. **Review Heatmap:** Visual matrix of all entities vs requirements
3. **Check Critical Gaps:** Requirements with personal liability highlighted
4. **Analyze Common Gaps:** Identify patterns across entities
5. **Export Report:** Generate CSV for stakeholders

### Standards Mapping

Navigate to the "Standards Mapping" tab to see how NIS2 requirements align with:
- ISO 27001 controls
- NIST CSF functions
- CIS Controls

## 💾 Data Storage

### Current Implementation
- Uses browser **localStorage** (5-10MB typical limit)
- Data persists across sessions
- Client-side only (no server required)

### Important Notes
- ⚠️ Clear browser data = lose compliance data
- ⚠️ One browser/device only
- ⚠️ No multi-user collaboration

### Recommended for Production

For enterprise deployment, consider:

1. **SharePoint Integration**
   ```javascript
   // Connect to SharePoint REST API
   // Store data in SharePoint lists
   // Enable multi-user collaboration
   ```

2. **Backend Database**
   - SQL Server, PostgreSQL, MySQL
   - Enable multi-user access
   - Centralized data management

3. **Regular Backups**
   - Use Export feature regularly
   - Store exported JSON files securely
   - Version control compliance data

## 🏗️ Architecture

```
┌─────────────────────────────────────────┐
│         NIS2 Compliance Mapper          │
├─────────────────────────────────────────┤
│  Presentation Layer (HTML/CSS)          │
│  ├─ Dashboard Views                     │
│  ├─ Portfolio Views                     │
│  └─ Export Interfaces                   │
├─────────────────────────────────────────┤
│  Business Logic (JavaScript)            │
│  ├─ Compliance Calculations             │
│  ├─ Risk Analysis                       │
│  ├─ Data Validation                     │
│  └─ Report Generation                   │
├─────────────────────────────────────────┤
│  Data Layer                              │
│  ├─ LocalStorage (current)              │
│  └─ SharePoint/DB (recommended)         │
└─────────────────────────────────────────┘
```

## 📊 NIS2 Requirements Coverage

| Article | Requirement | Category | Max Penalty |
|---------|------------|----------|-------------|
| Art. 20 | Governance | Governance | €10M or 2% + Personal Liability |
| Art. 21(2)(a) | Risk Analysis & Policies | Governance | €7M or 1.4% |
| Art. 21(2)(b) | Incident Handling | Operational | €10M or 2% + Personal Liability |
| Art. 21(2)(c) | Business Continuity | Operational | €7M or 1.4% |
| Art. 21(2)(d) | Supply Chain Security | Governance | €7M or 1.4% |
| Art. 21(2)(e) | Security in Development | Technical | €7M or 1.4% |
| Art. 21(2)(f) | Vulnerability Assessment | Technical | €7M or 1.4% |
| Art. 21(2)(g) | Cryptography | Technical | €7M or 1.4% |
| Art. 21(2)(h) | Human Resources Security | Governance | €7M or 1.4% |
| Art. 21(2)(i) | MFA & Secure Comms | Technical | €10M or 2% + Personal Liability |
| Art. 21(2)(j) | Emergency Communications | Operational | €7M or 1.4% |
| Art. 23 | Incident Reporting | Operational | €10M or 2% + Personal Liability |
| Art. 24 | EU Cyber Schemes | Governance | €7M or 1.4% |

## 🔐 Security Considerations

### Current Implementation
- ⚠️ No authentication layer
- ⚠️ No access control
- ⚠️ Data visible to anyone with browser access

### Recommendations for Production
1. **Add Authentication:** Azure AD, OAuth, or similar
2. **Implement RBAC:** Role-based access control
3. **Encrypt Sensitive Data:** At rest and in transit
4. **Audit Logging:** Track all changes
5. **HTTPS Only:** Enforce secure connections

## 🛠️ Customization

### Adding Custom Requirements

Edit the `nis2Requirements` array in the JavaScript:

```javascript
{
    article: "Custom-01",
    title: "Your Custom Requirement",
    description: "Description here",
    category: "technical",
    penalty: "Define penalty",
    iso27001: ["A.5.1"],
    nistCSF: ["ID.AM-01"],
    cisControls: ["1.1"]
}
```

### Changing Color Schemes

Modify CSS variables:

```css
.stat-box.custom {
    background: linear-gradient(135deg, #YOUR_COLOR_1 0%, #YOUR_COLOR_2 100%);
}
```

### Adding Export Formats

Extend the `exportData()` function:

```javascript
function exportData(format) {
    if(format === 'pdf') {
        // Add PDF generation logic
    }
}
```

## 📈 Roadmap

### Version 1.1 (Planned)
- [ ] Task assignment and tracking
- [ ] Historical trend analysis
- [ ] Risk matrix visualization
- [ ] PDF report generation

### Version 1.2 (Future)
- [ ] SharePoint REST API integration
- [ ] Multi-user collaboration
- [ ] Real-time notifications
- [ ] Mobile responsive design

### Version 2.0 (Vision)
- [ ] AI-powered gap analysis
- [ ] Automated evidence suggestions
- [ ] Integration with SIEM tools
- [ ] Compliance prediction models

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Areas for Contribution
- 🐛 Bug fixes
- ✨ New features
- 📝 Documentation improvements
- 🌍 Internationalization (i18n)
- ♿ Accessibility enhancements
- 🎨 UI/UX improvements

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚖️ Legal Disclaimer

This tool is provided for compliance tracking purposes only. It does not constitute legal advice. Organizations should:

- Consult with legal counsel regarding NIS2 compliance obligations
- Work with cybersecurity professionals for implementation
- Verify all compliance requirements with relevant authorities
- Conduct professional audits for certification

The creators assume no liability for compliance gaps or regulatory violations.

## 🙏 Acknowledgments

- NIS2 Directive (EU 2022/2555)
- ISO 27001:2022 Standards
- NIST Cybersecurity Framework
- CIS Controls
- Chart.js visualization library

## 📞 Support

- 📫 Open an issue for bug reports
- 💡 Submit feature requests via issues
- 📖 Check the Wiki for detailed documentation
- ⭐ Star this repo if you find it useful!

## 📚 Resources

- [Official NIS2 Directive Text](https://eur-lex.europa.eu/eli/dir/2022/2555/oj)
- [ENISA NIS2 Resources](https://www.enisa.europa.eu/)
- [ISO 27001:2022](https://www.iso.org/standard/27001)
- [NIST CSF 2.0](https://www.nist.gov/cyberframework)
- [CIS Controls v8](https://www.cisecurity.org/controls/)

---

**Built with ❤️ for the InfoSec community**

*Last updated: 2025-11-22*
