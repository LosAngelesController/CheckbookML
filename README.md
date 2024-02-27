# CheckbookML




# Documentation: 
The first two lines is to set up the OpenAI API key and specify the GPT-3 model engine to be used for summarization.

The **generate_summaries()** function defines how to generate summaries using GPT-3. The function takes in batches of text data and generates a summary for each batch. The summary prompt is defined as a string with a fixed length limit of 250 words. The function uses the OpenAI API to generate a response for each batch and appends the summaries to a list. Finally, it returns the list of summaries.

The for loop reads a CSV file containing text data, groups the data by certain columns, generates summaries using the generate_summaries() function for each group of data, and writes the summaries to a new CSV file.

In detail, the loop reads a CSV file named vendor1.csv. The data is then converted to string format. The data is then grouped by specific columns, namely Account, Fund, Description, Item, and Department.

The **grouped_data** variable holds the grouped data for each unique combination of the grouped columns. The generate_summaries() function is then called for each group, where each group's 'Item' column values are combined into a single batch of text data and passed to the function. The generated summaries are then appended to the summaries list.

After generating summaries for all groups of data, the loop adds the summaries to a new column in the original data frame called summary. The new data frame with the added summary column is then written to a new CSV file, with a name that ends with "summarize.csv".

Overall, this code uses the OpenAI API to summarize text data in a CSV file and outputs a new CSV file with the summaries added as a new column.


Developed by Vartan A. 
 
