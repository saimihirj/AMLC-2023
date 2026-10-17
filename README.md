# Amazon ML Challenge 2023: Product Length Prediction

Notes for the Amazon ML Challenge 2023, run on HackerEarth. The task was to predict a product's length from its catalogue listing (title, description, bullet points and product type), so that packaging and warehouse storage can be planned without measuring every item by hand.

This repository records the problem and the data. It does not contain a solution.

## Data

| File | Size | Columns |
|---|---|---|
| `train.csv` | 2,249,698 rows | `PRODUCT_ID`, `TITLE`, `DESCRIPTION`, `BULLET_POINTS`, `PRODUCT_TYPE_ID`, `PRODUCT_LENGTH` |
| `test.csv` | 734,736 rows | the same, without `PRODUCT_LENGTH` |
| `sample_submission.csv` | 734,736 rows | `PRODUCT_ID`, `PRODUCT_LENGTH` |

The dataset was published by HackerEarth at https://s3-ap-southeast-1.amazonaws.com/he-public-data/datasetb2d9982.zip and is not stored here.

## Evaluation

Submissions were scored on mean absolute percentage error (MAPE):

```python
score = max(0, 100 * (1 - metrics.mean_absolute_percentage_error(actual, predicted)))
```

## License

MIT. See [LICENSE](LICENSE).
