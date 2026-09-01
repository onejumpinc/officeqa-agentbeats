# OfficeQA AgentBeats — purple agent manifest

Amber deployment manifest for the **One Jump OfficeQA Agent**, a purple
(subject) agent for the OfficeQA benchmark on AgentBeats.

This repository exists solely to serve `amber-manifest.json5` from a stable
`raw.githubusercontent.com` URL, which AgentBeats requires.

The published container is a thin A2A adapter: it speaks the A2A protocol and
forwards each question to a private endpoint supplied at run time as a secret.
It contains no retrieval logic, prompts, corpus or reference data.

    ghcr.io/onejumpinc/officeqa-proxy-agent

Both `officeqa_api_url` and `officeqa_api_token` are declared as secrets in the
manifest and are injected by the assessment runner; neither is stored here.
