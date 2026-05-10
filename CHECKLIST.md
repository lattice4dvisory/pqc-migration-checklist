# PQC Migration Checklist — 200 Items

## Category 1: Cryptographic Asset Inventory (40 items)

### 1.1 Discovery
- [ ] 1. All asymmetric cryptographic algorithms in production have been identified
- [ ] 2. RSA key sizes and usage locations are documented
- [ ] 3. ECC curve types (P-256, P-384, secp256k1 etc.) are catalogued
- [ ] 4. Diffie-Hellman parameter sizes are recorded
- [ ] 5. DSA instances have been located and documented
- [ ] 6. All TLS/SSL certificate authorities are identified
- [ ] 7. Internal PKI structures are fully mapped
- [ ] 8. Code signing certificates are inventoried
- [ ] 9. SSH key types and locations are documented
- [ ] 10. PGP/GPG key usage has been catalogued

### 1.2 Classification
- [ ] 11. Each cryptographic asset is classified by data sensitivity level
- [ ] 12. Assets protecting long-lived data (10+ years) are flagged
- [ ] 13. Assets used in regulatory-mandated processes are identified
- [ ] 14. Customer-facing encryption endpoints are separated from internal
- [ ] 15. Hardware-bound keys (HSM, TPM) are separately tracked
- [ ] 16. Third-party managed cryptographic services are listed
- [ ] 17. Open-source cryptographic libraries in use are documented
- [ ] 18. Proprietary cryptographic implementations are identified
- [ ] 19. Cryptographic assets in cloud environments are catalogued
- [ ] 20. On-premises cryptographic assets are catalogued

### 1.3 Dependency Mapping
- [ ] 21. Application dependencies on specific cryptographic libraries are mapped
- [ ] 22. Certificate expiry dates are tracked in a central register
- [ ] 23. Key rotation schedules are documented
- [ ] 24. Cryptographic assets shared across multiple systems are identified
- [ ] 25. External partners sharing cryptographic infrastructure are listed
- [ ] 26. API endpoints using asymmetric cryptography are documented
- [ ] 27. Database encryption keys and their management systems are mapped
- [ ] 28. Backup encryption mechanisms are identified
- [ ] 29. Archive encryption (long-term stored data) is catalogued
- [ ] 30. Mobile application cryptographic usage is documented

### 1.4 Harvest Now Decrypt Later (HNDL) Exposure
- [ ] 31. Data transmitted today that must remain confidential beyond 2030 is identified
- [ ] 32. Recorded/archived encrypted communications are assessed for HNDL risk
- [ ] 33. Long-lived secrets (master keys, root CA keys) are prioritised
- [ ] 34. Regulatory data with retention periods beyond 10 years is flagged
- [ ] 35. Customer PII encrypted with asymmetric keys is assessed
- [ ] 36. Financial transaction records with long confidentiality requirements are reviewed
- [ ] 37. Board-level communication encryption is assessed
- [ ] 38. M&A related communications encryption is assessed
- [ ] 39. IP and trade secret protection mechanisms are reviewed
- [ ] 40. Nation-state threat model has been applied to inventory prioritisation

---

## Category 2: Risk Assessment (40 items)

### 2.1 Threat Modelling
- [ ] 41. Quantum threat timeline has been assessed against data sensitivity requirements
- [ ] 42. HNDL attack surface has been quantified
- [ ] 43. Adversary capability assumptions are documented
- [ ] 44. Regulatory penalty exposure for non-compliance is calculated
- [ ] 45. Reputational risk from cryptographic breach is assessed
- [ ] 46. Third-party supply chain cryptographic risks are evaluated
- [ ] 47. Insider threat model includes cryptographic key access
- [ ] 48. Physical security of cryptographic hardware is assessed
- [ ] 49. Side-channel attack exposure of existing implementations is reviewed
- [ ] 50. Hybrid attack scenarios (classical + quantum) are considered

### 2.2 Regulatory Compliance Gap
- [ ] 51. NIST FIPS 203 (ML-KEM) applicability to current systems is assessed
- [ ] 52. NIST FIPS 204 (ML-DSA) applicability is assessed
- [ ] 53. NIST FIPS 205 (SLH-DSA) applicability is assessed
- [ ] 54. EU DORA Article 27 cryptographic requirements are mapped to current state
- [ ] 55. NSA CNSA 2.0 timeline compliance gap is calculated
- [ ] 56. Local regulatory requirements (FSA, MAS, APRA, BaFin etc.) are mapped
- [ ] 57. Customer contractual obligations regarding encryption are reviewed
- [ ] 58. Cross-border data transfer cryptographic requirements are assessed
- [ ] 59. Audit and reporting obligations for cryptographic practices are identified
- [ ] 60. Insurance policy coverage for cryptographic incidents is reviewed

### 2.3 Technical Risk
- [ ] 61. Cryptographic agility of each system is rated (easy/hard to update)
- [ ] 62. Legacy systems with hard-coded cryptographic algorithms are identified
- [ ] 63. Systems requiring vendor support for cryptographic updates are flagged
- [ ] 64. Performance impact of PQC algorithms on critical systems is estimated
- [ ] 65. Network bandwidth impact of larger PQC key/signature sizes is assessed
- [ ] 66. HSM vendor PQC roadmap compatibility is verified
- [ ] 67. PKI infrastructure upgrade complexity is assessed
- [ ] 68. Certificate management system PQC readiness is evaluated
- [ ] 69. Authentication system PQC migration complexity is rated
- [ ] 70. Interoperability requirements with external parties are documented

### 2.4 Operational Risk
- [ ] 71. Staff cryptographic expertise for PQC migration is assessed
- [ ] 72. Budget requirements for PQC migration are estimated
- [ ] 73. Timeline feasibility against regulatory deadlines is confirmed
- [ ] 74. Business continuity risk during migration is assessed
- [ ] 75. Rollback procedures for failed cryptographic migrations are defined
- [ ] 76. Testing environment availability for PQC validation is confirmed
- [ ] 77. Change management capacity for cryptographic updates is assessed
- [ ] 78. Vendor dependency risks for PQC tooling are evaluated
- [ ] 79. Training requirements for operations staff are estimated
- [ ] 80. Communication plan for customer-facing cryptographic changes exists

---

## Category 3: Migration Planning (40 items)

### 3.1 Prioritisation
- [ ] 81. Migration priority tiers are defined (Critical/High/Medium/Low)
- [ ] 82. HNDL-exposed systems are in Tier 1 (immediate action)
- [ ] 83. Regulatory deadline-driven systems are prioritised
- [ ] 84. Customer-facing systems are prioritised over internal
- [ ] 85. Systems with long procurement/upgrade cycles are fast-tracked
- [ ] 86. Quick wins (easy-to-migrate, high-impact) are identified
- [ ] 87. Dependencies between systems are factored into sequencing
- [ ] 88. Budget allocation reflects priority tiers
- [ ] 89. Executive sign-off on priority framework is obtained
- [ ] 90. Priority framework is reviewed quarterly

### 3.2 Algorithm Selection
- [ ] 91. ML-KEM (FIPS 203) is selected for key encapsulation use cases
- [ ] 92. ML-DSA (FIPS 204) is selected for digital signature use cases
- [ ] 93. SLH-DSA (FIPS 205) is evaluated for stateless signature use cases
- [ ] 94. Hybrid classical+PQC approach is adopted for transition period
- [ ] 95. X25519 + ML-KEM hybrid is specified for TLS key exchange
- [ ] 96. Algorithm selection rationale is documented for audit purposes
- [ ] 97. Fallback algorithms for interoperability are specified
- [ ] 98. Parameter size selections are documented (ML-KEM-768 vs 1024 etc.)
- [ ] 99. Algorithm selections are reviewed against latest NIST guidance
- [ ] 100. External cryptographic review of algorithm selections is completed

### 3.3 Roadmap Development
- [ ] 101. Phase 1 (inventory + assessment) completion date is set
- [ ] 102. Phase 2 (pilot migration) scope and timeline is defined
- [ ] 103. Phase 3 (production migration) schedule is created
- [ ] 104. Phase 4 (verification + decommission legacy) timeline is set
- [ ] 105. Milestones are mapped to regulatory deadlines
- [ ] 106. Resource requirements per phase are defined
- [ ] 107. External vendor dependencies per phase are identified
- [ ] 108. Board-level reporting schedule for migration progress is established
- [ ] 109. Risk register for migration project is maintained
- [ ] 110. Change freeze periods (year-end, regulatory reporting) are avoided

### 3.4 Vendor and Tooling
- [ ] 111. HSM vendors with ML-KEM/ML-DSA support are evaluated
- [ ] 112. TLS library PQC support (OpenSSL 3.x, BoringSSL, etc.) is confirmed
- [ ] 113. PKI software vendor PQC roadmap is obtained
- [ ] 114. Certificate management platform PQC support timeline is confirmed
- [ ] 115. Cloud provider (AWS/Azure/GCP) PQC service availability is assessed
- [ ] 116. SIEM/monitoring tool updates for PQC event logging are planned
- [ ] 117. Cryptographic testing tools for PQC validation are procured
- [ ] 118. Vendor contracts include PQC migration support obligations
- [ ] 119. Open-source library update cadence for PQC patches is established
- [ ] 120. Fallback vendors are identified in case primary vendor delays PQC support

---

## Category 4: Implementation Verification (40 items)

### 4.1 Testing Framework
- [ ] 121. PQC algorithm implementation test vectors are sourced from NIST
- [ ] 122. Unit tests for ML-KEM key generation, encapsulation, decapsulation exist
- [ ] 123. Unit tests for ML-DSA key generation, signing, verification exist
- [ ] 124. Integration tests for hybrid TLS handshakes are implemented
- [ ] 125. Performance benchmarks for PQC operations are established
- [ ] 126. Load testing under PQC key sizes is completed
- [ ] 127. Interoperability testing with external counterparties is planned
- [ ] 128. Regression testing suite covers cryptographic changes
- [ ] 129. Fuzzing of PQC implementations is conducted
- [ ] 130. Third-party cryptographic code review is commissioned

### 4.2 TLS/Network Layer
- [ ] 131. TLS 1.3 with ML-KEM hybrid key exchange is tested in staging
- [ ] 132. Certificate sizes with ML-DSA are verified against network constraints
- [ ] 133. MTU/fragmentation issues with larger PQC messages are addressed
- [ ] 134. Load balancer and proxy PQC passthrough is verified
- [ ] 135. CDN provider PQC TLS support is confirmed
- [ ] 136. VPN gateway PQC cipher suite support is verified
- [ ] 137. API gateway PQC certificate handling is tested
- [ ] 138. Monitoring alerts for classical-only TLS connections are configured
- [ ] 139. Certificate transparency log support for PQC certificates is confirmed
- [ ] 140. OCSP/CRL infrastructure handles PQC certificate sizes

### 4.3 Application Layer
- [ ] 141. Code signing with ML-DSA is tested in CI/CD pipeline
- [ ] 142. JWT/token signing migration to ML-DSA is validated
- [ ] 143. Document signing workflows with PQC are tested
- [ ] 144. Email encryption (S/MIME) PQC migration is tested
- [ ] 145. Database encryption key migration procedures are tested
- [ ] 146. Backup decryption with migrated keys is validated
- [ ] 147. Key derivation functions are updated to post-quantum secure versions
- [ ] 148. Random number generation quality for PQC key generation is verified
- [ ] 149. Key storage security for larger PQC key sizes is confirmed
- [ ] 150. Audit logging captures all PQC key operations

### 4.4 Decommissioning Legacy
- [ ] 151. Deprecation timeline for RSA-2048 is published internally
- [ ] 152. Deprecation timeline for ECC P-256 is published internally
- [ ] 153. Legacy algorithm usage monitoring dashboards are operational
- [ ] 154. Automated alerts for new legacy algorithm deployments are configured
- [ ] 155. Exception process for legacy algorithm retention is defined
- [ ] 156. External party notification plan for legacy algorithm deprecation exists
- [ ] 157. Customer communication plan for encryption changes is prepared
- [ ] 158. Regulatory notification requirements for cryptographic changes are met
- [ ] 159. Legacy key material destruction procedures are defined
- [ ] 160. Post-migration audit confirms no legacy algorithm usage in scope systems

---

## Category 5: Governance & Compliance (40 items)

### 5.1 Policy and Standards
- [ ] 161. Cryptographic policy is updated to reference NIST PQC standards
- [ ] 162. Algorithm approval process includes PQC algorithm governance
- [ ] 163. Key management policy covers ML-KEM and ML-DSA key lifecycle
- [ ] 164. Data classification policy references quantum threat model
- [ ] 165. Vendor security requirements include PQC migration obligations
- [ ] 166. Software development standards mandate PQC-ready cryptographic libraries
- [ ] 167. Incident response plan covers cryptographic compromise scenarios
- [ ] 168. Change management policy covers cryptographic algorithm changes
- [ ] 169. Risk acceptance process for PQC migration delays is defined
- [ ] 170. Cryptographic standards review cycle is set to annual minimum

### 5.2 Roles and Responsibilities
- [ ] 171. CISO owns PQC migration programme
- [ ] 172. Cryptography owner/champion role is assigned
- [ ] 173. Application owners are accountable for their system migrations
- [ ] 174. Procurement team is briefed on PQC vendor requirements
- [ ] 175. Legal/compliance team is engaged on regulatory obligations
- [ ] 176. Board receives quarterly PQC migration progress reports
- [ ] 177. Risk committee reviews PQC risk register quarterly
- [ ] 178. External auditor is briefed on PQC migration scope
- [ ] 179. Regulator engagement plan for PQC readiness is established
- [ ] 180. Customer advisory process for encryption changes is defined

### 5.3 Training and Awareness
- [ ] 181. Security team has completed PQC fundamentals training
- [ ] 182. Development teams understand PQC library usage requirements
- [ ] 183. Operations teams can manage PQC certificates and keys
- [ ] 184. Architecture team can design PQC-ready systems
- [ ] 185. Executive team understands business risk of PQC non-compliance
- [ ] 186. Procurement team can evaluate vendor PQC claims
- [ ] 187. Audit team can assess PQC control effectiveness
- [ ] 188. Tabletop exercise simulating cryptographic breach has been conducted
- [ ] 189. PQC knowledge base is maintained and accessible to staff
- [ ] 190. External PQC expertise (advisory, consultancy) is engaged

### 5.4 Monitoring and Reporting
- [ ] 191. PQC migration KPIs are defined and tracked
- [ ] 192. Percentage of systems migrated is reported monthly
- [ ] 193. Legacy algorithm usage metrics are tracked
- [ ] 194. Regulatory deadline compliance status is monitored
- [ ] 195. Budget vs actual for PQC migration is tracked
- [ ] 196. Vendor milestone delivery is monitored
- [ ] 197. Third-party PQC readiness assessments are scheduled
- [ ] 198. PQC incident/near-miss reporting process is operational
- [ ] 199. Annual independent PQC readiness assessment is planned
- [ ] 200. PQC migration completion is formally signed off by CISO and Board

---

*Maintained by Lattice Advisory | lattice4dvisory@gmail.com*  
*Aligned with: NIST FIPS 203/204/205, EU DORA, NSA CNSA 2.0, MAS TRM*
