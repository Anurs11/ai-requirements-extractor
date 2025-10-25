# AI Requirements Extractor - Sample Comparison Guide

## Quick Comparison Table

| Aspect | E-Commerce | Healthcare | Fleet Mgmt | Banking | SaaS | IoT |
|--------|-----------|-----------|-----------|---------|------|-----|
| **Complexity** | Medium | High | High | Very High | Very High | Very High |
| **Domain** | Retail | Medical | Transport | FinTech | Software | Facilities |
| **Requirements** | 8-10 | 10-12 | 10-12 | 12-14 | 12-14 | 12-14 |
| **Compliance** | PCI-DSS | HIPAA | DOT/HOS | PCI-DSS/SOX | SOC2/GDPR | Custom |
| **Integration** | 3-4 | 3-4 | 2-3 | 4-5 | 8-10 | 6-7 |

## Sample-by-Sample Comparison

### Functional vs Non-Functional Requirements

**E-Commerce Platform:**
- Functional Heavy: 60% functional, 40% non-functional
- Focus: Shopping experience, payment flow
- Users: Customers, admins, support staff

**Healthcare Patient Portal:**
- Balanced: 50% functional, 50% non-functional
- Focus: Patient access, provider workflows
- Users: Patients, doctors, healthcare admin

**Fleet Management System:**
- Mixed: 40% functional, 60% non-functional
- Focus: Real-time tracking, analytics
- Users: Drivers, dispatchers, management

**Mobile Banking App:**
- Balanced: 50% functional, 50% non-functional
- Focus: Security, transactions, features
- Users: Individual users, enterprises, regulators

**Project Management SaaS:**
- Feature Heavy: 60% functional, 40% non-functional
- Focus: Collaboration, customization
- Users: Individual contributors, PMs, executives

**Smart Building (IoT):**
- Complex: 50% functional, 50% non-functional
- Focus: Monitoring, predictive maintenance
- Users: Facility managers, engineers, executives

---

### Compliance & Regulatory Requirements

**Healthcare:**
- HIPAA (Health Insurance Portability & Accountability Act)
- WCAG 2.1 (Web Content Accessibility Guidelines)
- HITRUST (Healthcare Information Trust)
- State-specific privacy laws

**Banking/FinTech:**
- PCI DSS (Payment Card Industry Data Security Standard)
- SOX (Sarbanes-Oxley Act)
- AML/KYC (Anti-Money Laundering / Know Your Customer)
- GLBA (Gramm-Leach-Bliley Act)
- GDPR (if international)

**SaaS (General):**
- SOC 2 Type II (Service Organization Control)
- GDPR (General Data Protection Regulation)
- CCPA (California Consumer Privacy Act)
- HIPAA (if healthcare-related)

**Fleet Management:**
- DOT (Department of Transportation)
- HOS (Hours of Service Regulations)
- FMCSA (Federal Motor Carrier Safety Administration)
- State vehicle regulations

**E-Commerce:**
- PCI DSS (payment processing)
- State consumer protection laws
- ADA (accessibility)
- Data protection regulations (varies by region)

**IoT/Smart Building:**
- Building codes and safety standards
- Energy efficiency regulations
- Occupancy and environmental standards
- Cybersecurity frameworks

---

### Integration Complexity

**Minimal Integration (2-3):**
- Fleet Management: Vehicle hardware, dispatch system, mapping service

**Moderate Integration (3-4):**
- E-Commerce: Payment gateway, shipping provider, inventory system
- Healthcare: EHR system, lab system, appointment system

**Advanced Integration (4-5):**
- Banking: Payment networks, identity verification, compliance systems

**Complex Integration (8-10):**
- SaaS: Slack, GitHub, Jira, Google Workspace, Salesforce, HubSpot, etc.

**Multi-System Integration (6-7):**
- IoT: Building automation, HVAC, lighting, security, energy management, utilities

---

### Performance Requirements

**E-Commerce:**
- Page Load: < 3 seconds
- Concurrent Users: 10,000+
- API Response: < 500ms
- Peak Traffic: 100x normal during sales

**Healthcare:**
- System Uptime: 99.9%
- Query Response: < 2 seconds
- Image Load (radiology): < 5 seconds
- Concurrent Sessions: 1,000+

**Fleet Management:**
- GPS Update: Every 30 seconds
- Route Optimization: < 10 seconds for 1,000 stops
- Real-time Alerts: < 2 seconds
- Concurrent Vehicles: 5,000+

**Banking:**
- Login: < 2 seconds
- Transaction Processing: < 500ms
- Biometric Auth: < 1 second
- Concurrent Users: 100,000+

**SaaS:**
- Dashboard Load: < 2 seconds
- Search Results: < 1 second for 1M records
- Concurrent Users: 10,000+
- API Rate Limit: 10,000 req/min

**IoT:**
- Sensor Data Ingestion: 1,000/second
- Dashboard Refresh: Real-time
- Alert Latency: < 1 second
- Historical Data Query: < 5 seconds

---

### Security Requirements Emphasis

| Aspect | E-Comm | Health | Fleet | Bank | SaaS | IoT |
|--------|--------|--------|-------|------|------|-----|
| **Encryption** | ★★☆ | ★★★ | ★★☆ | ★★★ | ★★★ | ★★☆ |
| **Authentication** | ★★☆ | ★★★ | ★★☆ | ★★★ | ★★★ | ★☆☆ |
| **Authorization** | ★★☆ | ★★★ | ★★★ | ★★★ | ★★★ | ★★☆ |
| **Audit Trail** | ★★☆ | ★★★ | ★★☆ | ★★★ | ★★☆ | ★★☆ |
| **Disaster Recovery** | ★★☆ | ★★★ | ★★☆ | ★★★ | ★★★ | ★★★ |

---

### Scalability Approach

**E-Commerce:**
- Challenge: Flash sales, holiday traffic spikes
- Solution: CDN, load balancing, caching, database replication

**Healthcare:**
- Challenge: Predictable growth, strict availability
- Solution: Redundancy, failover systems, regional backup

**Fleet Management:**
- Challenge: Real-time data from thousands of devices
- Solution: Stream processing, edge computing, time-series DB

**Banking:**
- Challenge: Regulatory requirements, transaction throughput
- Solution: High-availability clusters, transaction queuing

**SaaS:**
- Challenge: Multi-tenant architecture, varied usage patterns
- Solution: Microservices, Kubernetes, auto-scaling

**IoT:**
- Challenge: Massive data volume, real-time processing
- Solution: Apache Kafka, Spark, distributed databases

---

## When to Use Each Sample

### Choose E-Commerce if...
- Building a retail platform
- Need mid-level complexity example
- Showing typical web app requirements
- Interviewing for mid-level BA roles

### Choose Healthcare if...
- Working in healthcare/medical domain
- Need compliance-focused example
- Showing accessibility requirements
- Interviewing for regulated industry roles

### Choose Fleet Management if...
- Building logistics/transportation system
- Need real-time system example
- Showing hardware integration
- Interviewing for IoT/embedded roles

### Choose Banking if...
- Building fintech product
- Need high-security example
- Showing compliance complexity
- Interviewing for financial services

### Choose SaaS if...
- Building software as a service
- Need integration-heavy example
- Showing multi-tenant architecture
- Interviewing for SaaS companies

### Choose IoT if...
- Building IoT/smart systems
- Need data-heavy example
- Showing edge computing
- Interviewing for hardware/IoT roles

---

## Key Takeaways

1. **Complexity Increases** from E-Commerce (8-10 reqs) → IoT (12-14 reqs)

2. **Compliance Varies** by industry - shows domain expertise

3. **Integration Patterns** range from simple APIs to complex ecosystems

4. **Performance Needs** differ dramatically by use case

5. **Security Focus** highest in Healthcare, Banking, SaaS

6. **Scalability Challenge** grows with data volume and user count

---

## Using Samples in Your Portfolio

1. **Show Range:** Use different samples for different audiences
2. **Tell Story:** Explain why you chose each sample
3. **Highlight Insights:** Point out interesting requirement patterns
4. **Discuss Trade-offs:** Explain complexity vs. business value
5. **Demonstrate Expertise:** Show understanding of domain-specific needs

Perfect for portfolio projects, client meetings, and technical interviews!
