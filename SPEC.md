# Fire Sprinkler System Specification

## Part I: Overview and Scope

### 1. Purpose
This document defines the foundational requirements for the Fire Sprinkler System. Part I establishes the system context, scope, and high-level requirements that guide detailed design, implementation, and verification in later parts of the specification.

### 2. System Context
The Fire Sprinkler System (FSS) is a life-safety subsystem intended to detect fire events and deliver water suppression to affected zones while integrating with building automation and life-safety infrastructure. The FSS coordinates with:
- **Fire Detection and Alarm System (FDAS):** Provides fire detection signals and alarm status.
- **Building Management System (BMS):** Receives operational status and fault reporting.
- **Water Supply Infrastructure:** Provides adequate pressure and flow to deliver suppression.
- **Emergency Power Systems:** Ensures operation during power loss.

### 3. Scope
In-scope capabilities for Part I include:
- System objectives and boundaries.
- Primary operational states and high-level behaviors.
- Minimum safety and compliance requirements.
- Assumptions, dependencies, and constraints.

Out of scope for Part I:
- Detailed hydraulic calculations, nozzle sizing, and pipe routing.
- Electrical schematics, firmware design, and detailed control logic.
- Commissioning procedures and maintenance schedules.

### 4. Goals and Non-Goals
**Goals**
1. Provide automatic water suppression for designated zones upon fire detection.
2. Maintain fail-safe behavior during component failure or loss of power.
3. Provide reliable status reporting and fault indication to building systems.
4. Support manual activation and emergency override.

**Non-Goals**
1. Fire detection algorithm design (owned by FDAS).
2. Building evacuation procedures.
3. Architectural fire compartmentation design.

### 5. Stakeholders
- **Facilities Management:** Ensures compliance, maintenance, and readiness.
- **Safety and Compliance Officers:** Verify regulatory adherence.
- **Building Owners and Occupants:** Depend on system reliability and minimal disruption.
- **Authorities Having Jurisdiction (AHJ):** Enforce codes and acceptance criteria.

### 6. Assumptions and Dependencies
- The FDAS provides reliable fire detection signals and zone identifiers.
- Water supply pressure and flow meet local code requirements.
- The system is installed in an environment within specified temperature and humidity ranges.
- Emergency power is available and tested regularly.

### 7. Constraints
- Must comply with applicable codes and standards (e.g., NFPA 13, NFPA 72, local fire codes).
- Must meet building-specific hazard classifications and occupancy requirements.
- Must maintain operational readiness with routine inspection and testing.

### 8. Operational States (High Level)
1. **Normal:** Monitoring and ready state; valves closed, system pressurized.
2. **Alarm:** Activation signal received; suppression sequence initiated.
3. **Suppressing:** Water delivered to designated zone(s); status reported.
4. **Fault:** A system malfunction detected; fault reported and logged.
5. **Manual Override:** Authorized manual activation or shutdown in progress.

### 9. High-Level Functional Requirements
- **FR-1:** The system shall initiate suppression within the required activation time after a valid alarm signal is received.
- **FR-2:** The system shall deliver water to the correct zone(s) based on the alarm identifier.
- **FR-3:** The system shall report status (normal, alarm, suppressing, fault) to the BMS.
- **FR-4:** The system shall support manual activation by authorized personnel.
- **FR-5:** The system shall fail safe and report faults upon loss of critical components or power.

### 10. High-Level Non-Functional Requirements
- **NFR-1:** Availability shall meet or exceed code-defined readiness requirements.
- **NFR-2:** Fault detection shall occur within the maximum reporting interval defined by local code.
- **NFR-3:** Components shall be rated for the environmental conditions of installation.

---

**End of Part I**
