# Data Collection Scripts

The folder contains two python notebooks
1. terrorist_org_list.ipynb - a scraper used to gather the names of terrorist organisations from a wikipedia url - 'https://en.wikipedia.org/wiki/List_of_designated_terrorist_groups' and save it to a csv file.
2. wiki_info_scraper.ipynb - inputs a csv file and scrapes the wiki infoboxes accordingly for each entry in the csv file. please not - the path to the input csv must be defined before executing the notebook.
3. year_wise_scraper.ipynb - scrapes 12 urls from january to december 2018 (wiki) and writes the dataframe to a csv file.