# Differences Between the FMECA Methodology and the Current Practice

The researchers:

Utilize SUC states or modes of operation and then assigned relevant failure modes and mechanisms to each, e.g., maintenance, degraded, debug, etc. 

Calculate criticality of the component in the system model based on the number of connections it has to other components (graph theory measures of centrality are used).

Cite that the most observed threat model is STRIDE, and that some researchers have also extended the model (adding "link-ability"(a threat to privacy) and confusion (a threat to trustworthiness)).

Assert that STRIDE and the Cyber Kill Chain fail to reflect the "granularity of actions that adversaries take, how they relate to one another, their consequences related to adversarial objectives, their correlation with mitigation methods and data sources, and their targeted platforms and systems."

Estimate impact severity using four dimensions: safety, operational, privacy, and legislative. Later they add Security.

Cite other papers which describe impact in terms of the effect on CIA.

Cite that yet others assess impact in terms of the CVSS impact sub-index and its elements.

Other researchers have performed the risk assessment earlier in the development cycle - at the time the requirements are analyzed or elicited for the first time - to ensure that countermeasures are well integrated into the solution's requirements.

Explain that several existing practitioners use a model-based risk assessment framework and these models are industry and asset specific, e.g., the maritime transport industry uses the Maritime Cyber Risk Assessment (MaCRA).. In MaCRA, the first step is to identify assets in both physical and informational terms.

TODO: We should definitely create a railway specific threat model, inherit from EULYNX?

Take a bottom-up approach, rather than a top-down one, using intimate knowledge of the components in the SUC to determine which failure modes (tactics) and failure mechanisms (techniques) apply to the component.

Combine MITRE classes when an asset has features from more than one, e.g. a wireless radio subsystem on a worker safety control system would use both the ICS and Mobile MITRE categories of threats.

Recognise the importance of being able to clearly articulate and communicate risks, by using the relating the failure modes and failure mechanisms to the MITRE ATT&CK tactics and techniques.

Consequence is analysed in several dimensions, this is recommended in the IEC 62443 training in risk assessment training when developing an organisation's consequence table: safety, operational, financial, informational, and security (S,O, I, F, SE)

TODO: this is something we should do to harmonise how risk is managed in the company and valued and accounted for. It could go further and the risk we measure in engineering or customer projects could also be harmonised.

Determine the application failure mechanisms by aggregating multiple classes of MITRE frameworks, if a complnent has capabilities from more than one class.

The automation method is largely dependent on the component classifications and attributes assigned

Do not necessarily apply all failure modes to all components. They have a specific mapping in the APS use case they present. This is something we should do and it is based on expert judgement about the components.

There is a lengthy process to make a precise evaluation of impact.

Q: Who estimates effectiveness of a mitigation against a technique? Why is it set to 0.5 for every mitigation? If this is the norm, why include efficiency at all?

Q. When we do a risk assessment for a generic application or a specific application, is the difference in the number of assumptions we need to set out to specify the generic context?

