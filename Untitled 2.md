**Requirements Engineering - Detailed Bullet Notes with Explanations**

---

**Introduction to Requirements Engineering**

- Process of establishing services and constraints for a system.
    
    - This defines what the system must do and under which conditions it must operate.
        
- System requirements are descriptions generated during the process.
    
    - These are detailed and guide the development.
        

**What is a Requirement?**

- High-level abstract or detailed functional specification.
    
    - Abstract statements describe broad objectives; detailed specs explain exact operations.
        
- Serves dual purposes: basis for contract bids and system definition.
    
    - Abstract for proposals; detailed for legal contracts.
        

**Types of Requirements**

- User Requirements: Natural language, diagrams; for customers.
    
    - Simplified explanations meant for non-technical stakeholders.
        
- System Requirements: Detailed descriptions; for developers.
    
    - Precise and technical for actual development work.
        

**System Stakeholders**

- End Users, System Managers, System Owners, External Stakeholders.
    
    - Anyone affected directly or indirectly by the system.
        
- Example: Mentcare System stakeholders include patients, doctors, nurses, IT staff.
    
    - Real-world users help define practical requirements.
        

**Agile Methods and Requirements**

- Agile methods use incremental engineering and user stories.
    
    - Focus on evolving needs over time.
        
- Detailed documentation often avoided as requirements change quickly.
    
    - Reduces waste and speeds up response to changes.
        

**Functional vs Non-Functional Requirements**

- Functional: Services, reactions to inputs, specific behaviors.
    
    - Describe actions and operations the system must perform.
        
- Non-Functional: Constraints like timing, standards, reliability.
    
    - Specify quality attributes and system conditions.
        
- Domain Requirements: Constraints from the domain of operation.
    
    - Industry-specific rules and conditions.
        

**Examples of Functional Requirements (Mentcare)**

- Search appointment lists.
    
- Generate daily patient lists.
    
- Unique staff identification with 8-digit number.
    
    - Practical examples showing expected system functionalities.
        

**Requirements Imprecision**

- Ambiguous language can cause different interpretations.
    
    - Leads to confusion between developers and users.
        
- Example: "Search" interpreted differently by users and developers.
    
    - Misunderstandings can delay projects and cause errors.
        

**Requirements Completeness and Consistency**

- Complete: Includes all needed facilities.
    
    - No missing features.
        
- Consistent: No contradictions.
    
    - Requirements should not conflict with each other.
        
- Practically difficult to achieve completely.
    
    - Some inconsistencies are inevitable.
        

**Non-Functional Requirements**

- Define system properties: reliability, response time, storage needs.
    
    - Describe how the system performs, not what it does.
        
- Often more critical than functional requirements.
    
    - Poor performance can render systems unusable.
        

**Types of Non-Functional Requirements**

- Product Requirements: Behavior like speed, reliability.
    
- Organizational Requirements: Internal policies, standards.
    
- External Requirements: Legislative or external system constraints.
    
    - Different focus areas needing separate management.
        

**Non-Functional Requirement Example (Mentcare)**

- Product: Available Mon-Fri, 8:30-17:30 with minimal downtime.
    
- Organizational: Authentication using identity cards.
    
- External: Compliance with privacy standards.
    
    - Specific real-world non-functional examples.
        

**Goals and Requirements**

- Goal: General user intentions (e.g., ease of use).
    
- Verifiable Requirement: Objectively testable metrics.
    
    - Clear measurable standards help validation.
        

**Usability Requirements Example**

- Training limited to four hours.
    
- Error rate less than two errors per hour.
    
    - Quantifiable usability targets.
        

**Metrics for Non-Functional Requirements**

- Speed: Transactions/second.
    
- Size: MB.
    
- Ease of Use: Training time.
    
- Reliability: Mean time to failure.
    
    - Provides measurable benchmarks.
        

**Requirements Engineering Process**

- Common activities: Elicitation, Analysis, Validation, Management.
    
    - Standard process steps.
        
- Iterative and interleaved.
    
    - Often revisited multiple times.
        

**Requirements Elicitation and Analysis**

- Discover system services and operational constraints.
    
- Stakeholders: End-users, managers, domain experts.
    
    - Wide variety of inputs needed.
        

**Elicitation Activities**

- Discovery, Classification, Prioritization, Specification.
    
    - Step-by-step process to gather and organize requirements.
        

**Problems of Requirements Elicitation**

- Stakeholders may not know what they want.
    
- Conflicting requirements.
    
- Organizational and political factors.
    
    - Makes gathering requirements complex and difficult.
        

**Techniques for Elicitation**

- Interviews: Open and closed questions.
    
- Ethnography: Observing real work environments.
    
- Scenarios and User Stories: Practical examples.
    
    - Different techniques help understand requirements from different angles.
        

**Stories and Scenarios**

- Real-life usage examples.
    
- Help stakeholders relate and validate needs.
    
    - Easier for non-technical users to understand.
        

**Requirements Specification**

- Writing user and system requirements.
    
- Should be understandable and detailed.
    
    - Bridges gap between users and developers.
        

**Ways to Write Specification**

- Natural Language.
    
- Structured Natural Language.
    
- Graphical Notations (UML diagrams).
    
- Mathematical Specifications (rarely used).
    
    - Choice depends on audience and project needs.
        

**Requirements and Design**

- Requirements state "what", design states "how".
    
- Sometimes inseparable.
    
    - Practical boundaries often blur.
        

**Natural Language Specification Guidelines**

- Standard format.
    
- Consistent language.
    
- Highlight key parts.
    
- Avoid jargon.
    
    - Makes documents easier to read and less ambiguous.
        

**Problems with Natural Language Specifications**

- Lack of clarity.
    
- Mixing functional and non-functional requirements.
    
- Amalgamating multiple requirements together.
    
    - Leads to confusion and misinterpretation.
        

**Structured Specifications**

- Limit freedom of writing.
    
- Suitable for embedded control systems.
    
    - Ensures clarity but may feel rigid.
        

**Form-Based Specifications**

- Describe inputs, outputs, actions, and side effects.
    
    - Clear and consistent documentation.
        

**Tabular Specifications**

- Useful for scenarios with multiple outcomes.
    
- Example: Insulin pump dosage decisions.
    
    - Simplifies complex decision making.
        

**Use Cases**

- Scenario-based descriptions.
    
- Identify actors and interactions.
    
    - Useful for mapping out system operations.
        

**Software Requirements Document**

- Official record of system needs.
    
- Not a design document.
    
    - Focuses on "what" not "how".
        

**Requirements Document Structure**

- Preface.
    
- Introduction.
    
- Glossary.
    
- User Requirements.
    
- System Architecture.
    
- System Requirements.
    
- System Models.
    
- Evolution Plans.
    
- Appendices.
    
- Index.
    
    - Comprehensive organization for clarity.
        

**Requirements Validation**

- Ensure requirements meet customer needs.
    
- Costs of fixing errors are very high post-delivery.
    
    - Early validation saves money and effort.
        

**Validation Techniques**

- Requirements Reviews.
    
- Prototyping.
    
- Test Case Generation.
    
    - Multiple approaches improve accuracy.
        

**Review Checks**

- Verifiability.
    
- Comprehensibility.
    
- Traceability.
    
- Adaptability.
    
    - Ensures robustness of the requirements.
        

**Requirements Change**

- Requirements change post-installation due to evolving needs.
    
- Diverse user communities lead to conflicting priorities.
    
    - Change management is necessary.
        

**Requirements Management**

- Manage changes to requirements.
    
- Maintain traceability links.
    
- Establish formal change management processes.
    
    - Helps control project scope and risks.
        

**Requirements Management Planning**

- Unique identification of requirements.
    
- Change management process.
    
- Traceability policies.
    
- Tool support.
    
    - Planning upfront reduces chaos later.
        

**Requirements Change Management Process**

- Problem analysis.
    
- Change analysis and costing.
    
- Change implementation.
    
    - Structured process to handle evolving needs.
        

**Key Points Summary**

- Requirements define what the system should do.
    
- Functional and non-functional requirements are crucial.
    
- Elicitation, specification, validation are iterative processes.
    
- Requirements management is essential due to inevitable changes.