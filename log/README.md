\# Experimental Data



\## File Overview



\### EXP1\_total\_gating\_dataset.json

\*\*Experiment\*\*: Section VI.A - Gating Policy Ablation Study

\*\*Content\*\*: 97 voice-activity detection (VAD) events with sensor states and 4 gating policy definitions

\*\*Structure\*\*: 

\- `records`: 97 VAD events, each containing P (person detection), F (frontal-face), V (voice-activity) states

\- `gating\_definitions`: 4 policies - voice\_only, person\_voice, face\_voice, full (proposed)

\- `ablation\_results`: Performance metrics for each policy

\*\*Use\*\*: Reproduces gating policy comparison (Section VI.A, Table III-V)



\### EXP2\_proposed\_full\_\*.jsonl \& EXP2\_baseline\_alwayson\_\*.jsonl

\*\*Experiment\*\*: Section VI.B - Resource Profiling, Section VI.D - Latency Analysis

\*\*Proposed (state-gating ON)\*\*:

\- `EXP2\_proposed\_full\_001\_20260701\_182400.jsonl`: Live session 1

\- `EXP2\_proposed\_full\_002\_20260701\_183957.jsonl`: Live session 2

\- `EXP2\_proposed\_full\_003\_20260701\_184725.jsonl`: Live session 3



\*\*Baseline (always-on mode, state-gating OFF)\*\*:

\- `EXP2\_baseline\_alwayson\_001\_backradio\_user\_\*.jsonl`: Baseline session 1

\- `EXP2\_baseline\_alwayson\_002\_backmusic\_user\_\*.jsonl`: Baseline session 2

\- `EXP2\_baseline\_alwayson\_003\_radionly\_nonuser\_\*.jsonl`: Baseline session 3

\- `EXP2\_baseline\_alwayson\_004\_radiosideface\_nonuser\_\*.jsonl`: Baseline session 4



\*\*Content\*\*: JSONL format (one JSON object per line)

\- `ev`: event type (meta, res, mic, vad, resp, summary)

\- `cpu`, `ram`, `gpu`, `gpu\_mem\_mb`: resource metrics

\- `t`: Unix timestamp

\*\*Use\*\*: Resource profiling, latency measurement, deployment evidence



\### EXP3\_vlmm\_batch\_log\_260702.txt

\*\*Experiment\*\*: Section VI.C - Hallucination Evaluation, Section VI.E - Batch Evaluation

\*\*Content\*\*: vLLM API server log with 200 LLM responses (40 questions × 5 repetitions)

\*\*Model\*\*: llama-3-8b-instruct-awq

\*\*Metrics\*\*: Token throughput, GPU utilization, KV cache hit rate, latency per request

\*\*Use\*\*: Hallucination rate, batch evaluation protocol, LLM consistency analysis

