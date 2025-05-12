![image](https://github.com/user-attachments/assets/914ec507-7fc3-4e1a-bff1-a37467163aa9)# Code-AuditingTool
A Python-based code auditing tool that uses Bandit, Flake8, and Semgrep to detect security flaws, code quality issues, and map them to CVEs and CWEs. It generates summary and HTML reports to help developers identify and fix vulnerabilities efficiently during development.
This project is a Python-based static code auditing tool that scans Python source files for security vulnerabilities, syntax errors, and insecure coding practices. It integrates three widely-used scanners — Bandit, Flake8, and Semgrep — and enhances their findings with mapped Common Vulnerabilities and Exposures (CVEs) and mitigation suggestions.

The tool supports parallel scanning, directory and file-based audits, and generates both terminal output and a styled HTML report, making it ideal for secure development, auditing, and DevSecOps pipelines.
Instructions to Run the Project
Clone the Repository: git clone https://github.com/your-username/code-auditing-tool.git cd code-auditing-tool

Install Required Tools: Ensure Python 3 is installed. Then run: pip install bandit flake8 semgrep prettytable

Prepare the Directory: Place your target Python files in a directory (e.g., code_audit_test/). Ensure vuln_to_cve_mapping.json and vuln_mitigations.json files are present in the root of the repo.

Run the Tool: python code_auditor.py

Input Prompt: To scan a full directory: code_audit_test To scan a single file: code_audit_test/filename.py

Output:

Terminal: Color-coded summary of issues. File: audit_report.html with enriched details (CVE, severity, and mitigation).

Tools and Frameworks Used

Tool/Library	Purpose
Bandit	Detects Python-specific security issues
Flake8	Flags syntax and formatting problems
Semgrep	Finds logic-based and pattern-matching security flaws
multiprocessing	Runs scans in parallel to improve performance
subprocess	Executes CLI tools from the Python script
prettytable	Formats terminal output in a readable table
html.escape	Safely renders text in the HTML report
JSON	Used to store CVE mappings and mitigations

Project Files
code-auditing-tool/ │ ├── code_auditing_tool_with_reporting.py # Main script ├── vuln_to_cve_mapping.json # CVE keyword mapping ├── vuln_mitigations.json # Mitigation suggestions ├── code_audit_test/ # Zip folder containing Python files to scan ├── audit_report.html # Generated HTML output └── README.md # This file

Ethical Disclaimer: This tool is intended only for authorized auditing. Scanning proprietary or third-party code without consent is unethical and possibly illegal. Only use this tool on code you are legally permitted to audit

