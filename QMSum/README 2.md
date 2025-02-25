# QMSum Dataset
- **Original data**
  - Link: https://github.com/Yale-LILY/QMSum
  - _**QMSum** is a new human-annotated benchmark for query-based multi-domain meeting summarization task, which consists of 1,808 query-summary pairs over 232 meetings in multiple domains._
- **Extracted data**
  - Following preprocessing code in another paper: https://github.com/salesforce/query-focused-sum/tree/master/preprocessing, QMSum dataset is formatted into the _./data_ folder.
  - This folder includes three files for each of the _train_, _val_, and _test_ splits:
    - _split_name_.jsonl : contains one data point per line. Each data point consists of an individual query, query and meeting ids, a reference summary, and the general/specific query type label.
    - _split_name_-meetings.jsonl: contains the meeting transcripts along with the associated meeting_id used to join the data with _split_name_.jsonl.
    - _split_name_.target: contains one data point per line in the format used for ROUGE evaluation. The order of the data points aligns with _split_name_.jsonl.
- The details of each split is described in _data_exploring.ipynb_