# Alternative-Data-Alpha-News-Sentiment-Signal-Backtest-
Build an end-to-end quantitative trading system that ingests financial news via a live API, converts unstructured text into sentiment signals, and backtests a cost-aware long–short equity strategy with strict timestamp controls.

altdata-sentiment-alpha/
  README.md
  pyproject.toml
  .env.example
  data/
    raw/news/         # json/csv dumps (gitignored)
    raw/prices/
    processed/
  notebooks/
    01_collect_news.ipynb
    02_sentiment_model.ipynb
    03_signal_backtest.ipynb
  src/
    altalpha/
      config.py
      data/
        collect_news.py
        fetch_prices.py
        align_calendar.py
      nlp/
        preprocess.py
        finbert_infer.py
        embed.py
      signal/
        aggregate.py
        decay.py
        validation.py
      portfolio/
        construct.py
        costs.py
      backtest/
        run.py
      analysis/
        plots.py
        report.py
  reports/
    figures/
    writeup.md
  tests/
  scripts/
    run_pipeline.py
