# LLM Journal Uploader

1. Run `parse.ipynb` notebook to output parsed bibliography into the following text files:
```
test-output/doi_links.txt
test-output/other_links.txt
test-output/pdf_names_w_doi_link.txt
test-output/pdf_names_w_link.txt
test-output/pdf_names_wo_link.txt
```

Already generated `parse.ipynb` output can be found in `parsing-output`.

2. Install `PyPaperBot` binary

```
pip3 install ./PyPaperBot
```

To update `PyPaperBot`, also run the command above  


3. Run the following script to download the papers using their doi links:

```
PyPaperBot --mix-file="./parsing-output/pdf_names_w_doi_link.txt" --dwn-dir="test-papers" --scihub-mirror="https://sci-hub.se/"
```

```
PyPaperBot --query="A review of methods for spike sorting: the detection and classification of neural action potentials."  --dwn-dir="test-papers" --scihub-mirror="https://sci-hub.se/" --scholar-pages=1
```

```
pip3 install ./myPyPaperBot
```