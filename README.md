# NeuralPhish-Detector

<h2>Objective</h2>
<p>
Developed a high-throughput, local AI tool to identify phishing patterns in email content. By utilizing <strong>Python</strong> and <strong>Ollama</strong>, the system analyzes social engineering tactics locally to maintain data privacy.
</p>

<hr>

<h2>Skills Developed</h2>
<ul>
<li>Implemented <strong>Asynchronous Concurrency</strong> (<code>asyncio</code>) for parallel email processing.</li>
<li>Engineered <strong>Structured AI Prompts</strong> to ensure consistent JSON threat reports.</li>
<li>Applied <strong>Local LLM Inference</strong> to detect urgency, impersonation, and fraud.</li>
<li>Managed <strong>Concurrency Semaphores</strong> to optimize local hardware performance.</li>
<li>Developed <strong>Automated Scoring</strong> to classify threats by risk level.</li>
</ul>

<hr>

<h2>Tools</h2>
<ul>
<li><strong>Python</strong> (asyncio, ollama)</li>
<li><strong>Ollama</strong> (Local AI Runtime)</li>
<li><strong>Llama 3</strong> (LLM)</li>
<li><strong>JSON</strong> (Data Formatting)</li>
</ul>

<hr>

<h2>Implementation Steps</h2>

<h3>Ref 1 – NeuralPhish-Detector</h3>

<p>

This project utilizes asynchronous Python to interface with local AI models for rapid security auditing.

Asynchronous Processing: By using the asyncio library and async def function, the script can process multiple emails simultaneously without waiting for one analysis to finish before starting the next.

Localized AI Analysis: The tool leverages the ollama library to run Large Language Models (LLMs) locally, ensuring that sensitive email data remains on the local machine rather than being sent to external cloud APIs.

Structured Intelligence: The system instruction forces the AI to act as a Cybersecurity Analyst. It is programmed to bypass conversational text and return a strictly formatted JSON object including a numerical score, a verdict, a threat level, and a list of specific reasons for the detection.

Data Validation: Using the json and re libraries, the script ensures that the AI’s unstructured insights are converted into valid, structured data that can be easily integrated into other security reporting tools.

 <img width="680" height="235" alt="Screenshot 2026-02-12 134939" src="https://github.com/user-attachments/assets/c7b2cadd-da71-4de3-9a7f-fd2dcbe4f8d4" />


</p>


<h3>Ref 2 – NeuralPhish-Detector</h3>

<p>

The project utilizes a testing suite designed to validate the AI's ability to distinguish between harmless internal messages and sophisticated social engineering attempts:

Malicious & Urgent Lures: Created samples that mimic "Account Urgency" to test the model's sensitivity to high-pressure language meant to bypass critical thinking.

Business Operations (Clean): Included legitimate scenarios, such as team lunch invites, to ensure the system maintains a low false-positive rate for standard corporate communication.

IT Impersonation: Developed technical lures regarding "Password Expiration" and fake internal portals (internal-it-helper.net) to verify if the AI detects unauthorized domain mismatches and administrative impersonation.

Financial & Payroll Scams: Crafted "Payroll Update" scenarios using shortened URLs (bit.ly) to test the model’s ability to flag high-risk requests for sensitive banking information.


<img width="1068" height="195" alt="Screenshot 2026-02-12 001857" src="https://github.com/user-attachments/assets/b82436ee-ce58-48e2-a6dc-1ad470ddfbd2" />


</p>

<h3>Ref 3 - NeuralPhish-Detector</h3>

<p>

The output confirms the script successfully executed the parallel analysis of the four sample categories:

Accurate Threat Identification: The engine correctly identified the "Malicious", "IT Impersonation", and "Payroll Scam" samples as Phish.

Behavioral Detection: Even with deceptive URLs (like internal-it-helper.net or bit.ly links), the AI identified the malicious intent behind the text.

Safety Sensitivity: Interestingly, the "Clean" team lunch sample was flagged as Suspicious. This indicates the model’s current tuning is highly sensitive likely due to the "Cybersecurity Analyst" persona prioritizing caution—which provides a great starting point for further prompt refinement to reduce false positives.

<img width="278" height="71" alt="Screenshot 2026-02-12 002324" src="https://github.com/user-attachments/assets/a722cafd-0bcb-4452-83d6-e2bcde5720d8" />

  
</p>
