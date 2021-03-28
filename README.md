# cml-dvc-test

dvc commit was done like this expecting to execute repro in the CI

```sh
pip install requirements
python get_data.py

dvc init
dvc remote add -d myremote s3://daviddvctest/dvc-cml-test1
dvc add data
dvc push --run-cache

WARNING: Output 'metrics.json'(stage: 'mystage') is missing version info. Cache for it will not be collected. Use `dvc repro` to get your pipeline up to date.
WARNING: Output 'loss.csv'(stage: 'mystage') is missing version info. Cache for it will not be collected. Use `dvc repro` to get your pipeline up to date.
5 files pushed        
```

