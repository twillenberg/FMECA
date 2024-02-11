# Summary

## Abstract

The paper titled "Assessing Cyber Risks in Cyber-Physical Systems Using the ATT&CK Framework" focuses on the safety and security implications of Autonomous Passenger Ships (APSs) in urban waterways. The study utilizes a Failure Modes Effects and Criticality Analysis (FMECA) enhanced with the MITRE ATT&CK framework and graph theory-based metrics to assess cyber risks in these systems. The primary objective is to analyze threats endangering passengers and the operational environment of APSs, identifying potential risks and proposing mitigation methods.

The introduction highlights the increasing attention towards automated and autonomous ships and the potential cybersecurity risks due to enhanced connectivity and reduced human supervision. This section underscores the necessity of risk management in APS communication architecture to ensure the safety and security of both passengers and the operational environment.

The paper employs FMECA for risk assessment, integrating the MITRE ATT&CK framework to identify and describe attacks' techniques and tactics. This combination aims to overcome limitations in existing risk assessment methods, providing a comprehensive analysis of the risks. Additionally, graph theory concepts are used to estimate the impact of identified risks.

Section 2 of the paper provides background information on APSs, their communication architecture, and the relevance of the MITRE ATT&CK framework and graph theory in this context. It describes the communication architecture of an APS prototype, highlighting its autonomous and remote navigation and control capabilities.

The proposed risk assessment approach detailed in the paper involves specifying components and their functions, identifying relevant failure modes, detecting methods, existing controls, and estimating the impact of consequences of each failure mode. This approach is systematic and comprehensive, considering multiple aspects such as safety, financial, operational, and information criticality. Special emphasis is placed on the integration of the ATT&CK framework in identifying failure mechanisms, considering it a comprehensive source for attack identification.

In summary, the paper offers a detailed methodology for assessing cyber risks in Cyber-Physical Systems like APSs, leveraging the ATT&CK framework and graph theory. This approach enhances the understanding of safety and security implications in such systems and contributes to developing robust risk management strategies.

## Abbreviations

I   Input
O   Output

## References

[REF-01] Amro, A., Gkioulos, V., & Katsikas, S. (2023). Assessing Cyber Risk in Cyber-Physical Systems Using the ATT&CK Framework. ACM Transactions on Privacy and Security, 26(2), 1-33. [https://doi.org/10.1145/3571733](online source).

[REF-02] Oruc, A., Amro, A., & Gkioulos, V. (2022). Assessing Cyber Risks of an INS Using the MITRE ATT&CK Framework. Sensors (Basel), 22(22). [https://doi.org/10.3390/s22228745](online source).

[REF-03] Amro, A., & Gkioulos, V. (2023). Evaluation of a Cyber Risk Assessment Approach for Cyber–Physical Systems: Maritime- and Energy-Use Cases. Journal of Marine Science and Engineering, 11(4). [https://doi.org/10.3390/jmse11040744](online source).

## Issues

[1] Table 3 lists 'failure modes', but refers to 'failure mechanisms' in section 4.3.1. Section 4.4.4 defines "failure modes" as MITRE tactics and "failure mechanisms" as MITRE techniques. In table 4, the MITRE matrix name is linked to a MITRE "technique". Table 4, although an example, lists techniques against the MITRE matrix equivalent to the component classes of table 3 which are listed in terms of the component class name not the MITRE matrix name.

[2] Failure modes are used as headers when the column values include both failure modes and failure mechanisms. The researcher said that the relationship was expertly determined. Table 6 lists ICS failure modes, but includes both failure modes (e.g., Collection, Command and Control, Defense Evaluation) and failure mechanisms (e.g., Damage to Property, Denial of Control, Loss of Availability).

[3] Figure 3 depicts the one to one mapping between Enterprise and IT, Mobile and Wireless, and ICS and OT but the names are used interchangeably when referring to component class. Table 4, 6, and 8 use the MITRE matrix names.

[4] Which MITRE matrix is used among the Enterprise matrices?

[5] Tables 3, 4, and 6 list different rows

[6] How can "efficiency" be estimated? Why is it always set to 0.5?

[7] Sample tables are insufficiently illustrative of the concept they are meant to exemplify.

## Assumptions

[1] Assume table 4 lists techniques applicable to a component class based on the link between tactic or technique to the component class made earlier in table 3.

[2] Assume the Enterprise matrices are selected based on the closest match to the technology used and the ability to combine the matrices should a component use more than one technology: e.g., Linux and Network might be combined in the case of a host

## The Process Description

### 1. Specify Components, Functions, and Performance Standard

(Source: section 4.1 in [REF-01])

First, the methodology expects a system architecture to be used to identify components, their functions, and interconnections. Reviewing an architecture diagram, among other documents, helps to identify *functional* components (components that do something to change the state of the SUC) and shall include hardware and software. It is a reasonable assumption that the definition of a component, as set out in IEC 62443-4-2, can apply without complication: embedded, host, network, and software application.

The study suggests that "operational modes" of the SUC must be identified and considered to improve the analysis, particularly if they cause a change in the system state - 'state' being the combination of functional components and their interconnections.

Then, the identified components are classified into one or more of the MITRE ATT&CK matrices: Enterprise, ICS, or Mobile. The set of matrices needed to represent the SUC's components is then tabulated.

I: System architecture
O: List of component classes that contain the SUC's components, as determined by expert
Component Class

### 2. Identify Failure Modes

(Source: section 4.2 in [REF-01])

Next, for each component class in the SUC, the applicable "failure modes" are identified. The link is made based on expert judgement, and the expectation is that the expert has deep knowledge of the component to which tactics are linked.

"Failure modes", in the context of the study, are MITRE ATT&CK tactics (e.g. Initial Access, Collection, Evasion, Discovery, etc.) In addition to failure mode (tactic), a component's failure effect is also defined.

I: System architecture
O: List of failure modes (tactics) applicable to a component class, as determined by expert
O: List of failure effects which represents the performance threshold of the component class' failure mode.

### 3. Identify Detection Methods and Risk Reduction Measures

In this step we utilise three sub-steps to ultimately identify and evaluate the existing detection and risk reduction measures (i.e., controls and countermeasures). The aim is to calculate "detectability" of attacks by the existing measures available in the SUC.

#### 3.1 Create a Failure-Mitigation Table (FMT)

A link is made between failure mechanisms (techniques) and the corresponding mitigation methods and their efficiency. However, step 4.1 of the method results in a table associating 'component classes' with expertly selected 'failure modes' (tactics). It is unclear how we get to this step, which begins by associating failure mechanisms (techniques) to their mitigations and then rates "efficiency". It appears an association (tactics to techniques) has not been documented in the study.

Let's assume we make that association: for each given component class, the expertly selected tactics and their corresponding techniques (also expertly selected) are associated. Then for each component class we list the tactics and techniques and mitigations, and estimate their "efficiency". "Effectiveness" is a more accurate term.

O. List of mitigations for each failure mechanism, for each failure mode, and their estimated "efficiency".

#### 3.2 Create the Component-Mitigation Table (CMT)

Next, the practitioner must create a table that represents the particular component which is covered by each of the mitigations. "A component is said to be influenced by a mitigation method if the component in the proposed architecture is subject to an architectural decision that enforces the mitigation method." The columns of the CMT include: operational mode, mitigation, then compoent A, B, C, etc.

O. List of operational modes (e.g., debug and operative), the mitigations that apply (from the FMT) and a binary indication of whether a component in the SUC is "covered" by the mitigation.

#### 3.3 Calculate Detectability

The aim of this sub-step is to determine the detectability of each failure mechanism (technique). It is calculated by evaluating, for each combination of mitigation covering a component, coverage x efficiency.

### 4. Estimate the Impact of the Consequences of Failure Modes

### 5. Identify Failure Mechanisms

### 6. Estimate the Likelihood of Failure Mechanisms

### 7. Evaluate the Risks

### 8. Propose Risk Reduction Measures

Once the failure modes and mechanisms are identified for a particular
