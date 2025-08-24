# 🕶️ Compliance tracker

The compliance tracker is a central location for examining the _EU AI Act_ compliance metrics of a given project.

The _Act_ involves a considerable number of rules and regulations that AI providers need to follow to ensure the ethical use of their AI applications.

### Compliance tracker structure

Compliance Tracker organizes these obligations into separate **sections**. Each section contains one or more **controls**. These controls are then divided into individual, actionable **subcontrols**.

There is a simple numbering system for denoting individual subcontrols: `X.Y.Z` refers to Section `X` , Control `Y` , Subcontrol `Z`.

For instance:

```
Section 3: Human oversight
Control 3.2: Oversight Documentation
Subcontrol 3.2.1: We document system limitations and human oversight options.

```

<figure><img src=".gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

At the top of the screen, you will see a table of metrics:

* **Compliance status:** Percentage of implemented subcontrols, calculated by `100 * (Implemented subcontrols / Total subcontrols)`
* **Total number of subcontrols**
* **Implemented subcontrols**
* **Auditor completed:** Number of subcontrols that have been successfully audited

### Sections

<figure><img src="https://github.com/bluewave-labs/verifywise-documentation/raw/master/.gitbook/assets/image%20(11).png" alt=""><figcaption></figcaption></figure>

Click a section to expand it.

Once expanded, each control under the selected section will show the following fields:

* **Status icon**
* **Control name**
* **Owner:** The person responsible for overseeing this control
* **Number of subcontrols:** All subcontrols bound to this control
* **Completion:** Percentage of fully implemented subcontrols

### Controls

Click on a given control to open up its control window.

<figure><img src="https://github.com/bluewave-labs/verifywise-documentation/raw/master/.gitbook/assets/image%20(12).png" alt=""><figcaption></figcaption></figure>

Each compliance control has some general settings and different tabs for its subcontrols. The general settings are:

* **Status (Waiting/ In Progress/ Done):** Current implementation status of this control
* **Approver:** Organization member who has approved the current status of this control
* **Risk review (Acceptable risk/ Residual risk/ Unacceptable risk):** Current risk status of this control
* **Owner:** The person responsible for the implementation of this control
* **Reviewer:** The person who has reviewed the control
* **Due date:** Due date for the full implementation of the control
* **Implementation details**

**NOTE:** Do not forget to press `Save` when you finish updating your control or subcontrol.

### **Subcontrols**

Subcontrols are the most granular _EU AI Act_ measures you can examine in the compliance tracker. Each subcontrol is specific and actionable.

<figure><img src="https://github.com/bluewave-labs/verifywise-documentation/raw/master/.gitbook/assets/image%20(13).png" alt=""><figcaption></figcaption></figure>

The "Overview" tab operates identically to the general control settings:

* **Status (Waiting/ In Progress/ Done):** Current implementation status of this control
* **Approver:** Organization member who has approved the current status of this control
* **Risk review (Acceptable risk/ Residual risk/ Unacceptable risk):** Current risk status of this control
* **Owner:** Person responsible for the implementation of this control
* **Reviewer:** Person who has reviewed the control
* **Due date:** Due date for the full implementation of the control
* **Implementation details**

**Evidence**

Here, users can type an explanation of any evidence they have for their compliance with this subcontrol. Alternatively, users can upload a PDF containing evidence.

**Auditor feedback**

<figure><img src="https://github.com/bluewave-labs/verifywise-documentation/raw/master/.gitbook/assets/image%20(14).png" alt=""><figcaption></figcaption></figure>

Auditors can provide feedback to project members via direct text input or by uploading a PDF containing feedback.\
\
