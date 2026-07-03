# State-Gated Multimodal Digital Human Docent System

**IEEE Access** #Access-2026-23083 (Resubmission)

State-gating mechanism for context-aware multimodal processing in digital human docent systems.

## Core Contributions

- **State-Gating Mechanism**: Context-aware state management ensuring consistency in multimodal processing
- **Multimodal Integration**: Unified processing of text, image, and audio streams
- **Real-world Deployment**: Production deployment case study at King Sejong Museum
- **Performance Analysis**: Comprehensive evaluation of latency, resource utilization, and hallucination metrics

## Repository Structure

```
state-gated-multimodal-docent/
├── README.md                 This file
├── log/
│   ├── README.md           
│   ├── EXP1_total_gating_dataset.json         
│   ├── EXP3_vlmm_batch_log_260702.txt
│   ├── EXP2_proposed_full_001_20260701_182400.jsonl
│   ├── EXP2_proposed_full_002_20260701_183957.jsonl
│   ├── EXP2_proposed_full_003_20260701_184725.jsonl
│   ├── EXP2_baseline_alwayson_001_backradio_user_20260701_190728.jsonl
│   ├── EXP2_baseline_alwayson_002_backmusic_user_20260701_185942.jsonl
│   ├── EXP2_baseline_alwayson_003_radionly_nonuser_20260701_192534.jsonl
│   └── EXP2_baseline_alwayson_004_radiosideface_nonuser_20260702_134838.jsonl
```

## Experimental Data

All experimental data for reproducing the paper's results is available in the `data/` folder:

- **EXP1**: Gating Policy Ablation Study 
  - 97 voice-activity detection events with sensor states (P, F, V)
  - 4 gating policy definitions and ablation results

- **EXP2**: Resource Profiling & Latency Analysis
  - 3 proposed state-gating session logs (full mode, P AND F AND V)
  - 4 always-on baseline session logs for comparison

- **EXP3**: Hallucination Evaluation & Batch Analysis (Section VI.C, VI.E)
  - 200 LLM responses (40 questions × 5 repetitions)
  - vLLM llama-3-8b-instruct-awq model

See `data/README.md` for detailed file descriptions and field schemas.

## Data Availability

All experimental data required to reproduce the results in Section VI of the paper are provided in the `/log` folder:

- Gating policy evaluation on 97 logged voice-activity events
- Pipeline latency measurement on live full-mode sessions (proposed + baseline)
- Large-scale batch analysis of 200 LLM responses
- Complete resource profiling metrics (CPU, RAM, GPU utilization)

## Author

(이준형 / Junhyeong Lee)

