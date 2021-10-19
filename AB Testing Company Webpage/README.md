# AB Testing on Company Website
For this project, I performed an A/B test on a company e-commerce website with the goal of helping the company understand if they should implement a new page, keep the old page, or perhaps run the experiment a little longer to aid better decision. 

Below is the description of the data, there are a total of 5 columns:

<center>

|Data columns|Purpose|Valid values|
| ------------- |:-------------| -----:|
|user_id|Unique ID|Int64 values|
|timestamp|Time stamp when the user visited the webpage|-|
|group|In the current A/B experiment, the users are categorized into two broad groups. <br>The `control` group users are expected to be served with `old_page`; and `treatment` group users are matched with the `new_page`. <br>However, **some inaccurate rows** are present in the initial data, such as a `control` group user is matched with a `new_page`. |`['control', 'treatment']`|
|landing_page|It denotes whether the user visited the old or new webpage.|`['old_page', 'new_page']`|
|converted|It denotes whether the user decided to pay for the company's product. Here, `1` means yes, the user bought the product.|`[0, 1]`|
</center>

Please view [the notebook file](https://github.com/mathias-mike/Analyzing-Data/blob/master/AB%20Testing%20Company%20Webpage/Analyze_ab_test_results_notebook.ipynb) for the full scope of the project. 