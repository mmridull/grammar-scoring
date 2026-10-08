# grammar-scoring

# Grammar Scoring Engine for Spoken Audio (SHL Hiring Assessment 2026)

Predicts a 0-5 grammar score from 45-60 s speech clips.

**Approach:** frozen Whisper encoders (small and medium) used as feature extractors; hidden states mean-pooled over time; best layers chosen by 5-fold CV; ridge regression; weighted blend of the two models.

**Results:** Training RMSE 0.3130 | 5-fold CV RMSE 0.5421 | Baseline (predict mean) 1.2382 | Best public leaderboard RMSE 0.4310

**Files:**
- `shl_grammar_scoring_executed.ipynb` - full notebook with report, code, plots and outputs
- `submission_v4.csv` - best submission file (public score 0.4310)
