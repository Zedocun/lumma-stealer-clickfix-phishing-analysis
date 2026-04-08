flowchart TD
    A[Phishing Email Delivered<br/>update@windows-update.site<br/>Subject: Upgrade your system to Windows 11 Pro for FREE] --> B[SIEM Alert Triggered<br/>SOC338 - Lumma Stealer - DLL Side-Loading via Click Fix Phishing]

    A --> C[User Click / Interaction]
    C --> D[Fake Windows 11 Upgrade Landing Page<br/>windows-update.site]

    D --> E[HTTPS Connection to 132.232.40.201]
    A --> F[SMTP Delivery from 132.232.40.201]

    E --> G[chrome.exe Spawned by explorer.exe<br/>PID 5188]
    G --> H[Chrome Utility Activity<br/>unzip.mojom.Unzipper]
    G --> I[Chrome Utility Activity<br/>quarantine.mojom.Quarantine]

    H --> J[Archive Download / Extraction Suspected]
    I --> J

    F --> K[Infrastructure Reuse Confirmed]
    E --> K

    K --> L[External Reputation Check<br/>IP flagged by security vendors]

    J --> M[No Confirmed Payload Execution]
    M --> N[No Verified Child Process Chain<br/>No Conclusive Evidence of Compromise]

    style A fill:#1f4b99,stroke:#0b1f44,color:#fff
    style B fill:#7a1f1f,stroke:#3b0c0c,color:#fff
    style D fill:#1565c0,stroke:#0b3a6d,color:#fff
    style E fill:#2e7d32,stroke:#1b4d1d,color:#fff
    style G fill:#6a1b9a,stroke:#3b0d57,color:#fff
    style J fill:#ef6c00,stroke:#8a3d00,color:#fff
    style M fill:#616161,stroke:#2f2f2f,color:#fff
    style N fill:#424242,stroke:#1f1f1f,color:#fff
