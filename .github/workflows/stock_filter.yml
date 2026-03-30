name: 每日选股
on:
    schedule:
         - cron: ‘30 2 * * 1-5’
         - cron: ‘0 6 * * 1-5’
         - cron: ‘0 8 * * 1-5’
    workflow_dispatch:

jobs:
     filter:
         runs-on: ubuntu-latest
         steps:
            - uses: actions/checkout@v5

            - uses: actions/setup-python@v6
    with:
          python-version: ‘3.11’

             - name: 安装依赖
              run: pip install akshare pandas

              - name: 运行选股
    env:
 EMAIL_SENDER: ${{ secrets.EMAIL_SENDER }}
 EMAIL_PASSWORD: ${{ secrets.EMAIL_PASSWORD }}
 EMAIL_RECEIVERS: ${{ secrets.EMAIL_RECEIVERS }}
 run: python stock_filter.py
