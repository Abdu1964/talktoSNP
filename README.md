# SNPedia Data Fetching and Report Generation

This project fetches SNP (Single Nucleotide Polymorphisms) data from SNPedia (files are cached via git lfs) and generates a report using a user-provided SNP list. The project uses an OpenAI model to create a report with lisfestyle recommendations based on the found snps.

## Scripts and Their Execution Sequence

1. `fetch_snpedia_variant_list.py`: This script retrieves a list of all available SNPs from SNPedia without fetching the associated data.

2. `fetch_snpedia.py`: This script uses the list generated by the previous script to fetch all the data summaries from SNPedia.

You have the option of running these scripts manually in sequence, or instead directly pulling the necessary files from the cache using Git Large File Storage (LFS).

## Obtaining Cached Files via Git LFS

If you would like to use the cached files, you first need to install Git LFS. Afterwards, you can pull the necessary files using the following command:

```git lfs pull```

This operation provides a convenient and faster method than running the first two scripts.

## Generating the Report

`generate_report.py`: This script generates a report based on the user-provided SNP list. You can run the script like so:

```export OPENAI_API_KEY='your_key';python generate_report.py user_snps.txt```

Make sure to replace `path_to_your_snp_list.txt` with the actual path to your SNP list file and put your OPENAI_API_KEY.