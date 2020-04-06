    url = 'https://raw.githubusercontent.com/deepanshumehtaa/csvfiles/master/xyz.csv'
    df = pd.read_csv(url, index_col=0, delimiter=',')
    df = df.reset_index()
    df.head(5)


use this to access csv file
for inbuilt datasets lik iris to load them use

For Seaborn Dataset

    iris = sns.load_dataset('iris')
    
    -OR-
    
    from sklearn.datasets import load_iris
    iris = load_iris()
    data = iris.data
    column_names = iris.feature_names
 
 For Pandas
 
    import pandas as pd
    df = pd.DataFrame(iris.data, iris.feature_names)
    
For Sklearn

befor you start with sea born database https://medium.com/@haydar_ai/learning-data-science-day-9-linear-regression-on-boston-housing-dataset-cd62a80775ef

    from sklearn.datasets import load_iris
    sk_data = load_iris()
    print(sk_data)

    df = pd.DataFrame(sk_data.data, columns=sk_data.feature_names)
    df.head()

Iris is decleared in Sklearn so to convert it into df  

For all the Datasets present for ML

    import seaborn as sb
    df = sns.load_dataset('iris')
    print( sns.get_dataset_names() )
    
    
 To split the data without train_test_split
 
    # splitting the data BUT, not randomly
    X =df.drop(['car'], axis=1)
    y =df.car

    train_index = int(0.8 * len(X))
    X_train, X_test = X[:train_index], X[train_index:]
    y_train, y_test = y[:train_index], y[train_index:]
    
 .
Follow this Documentation for Keras Dataset: https://jovianlin.io/datasets-within-keras

# From G-Drive

    import pandas as pd
    import requests
    from io import StringIO

    url = requests.get('https://doc-0g-78docs.googleusercontent.com/docs/securesc/ha0ro937gcuc7l7deffksulhg5h7mbp1/5otus4mg51j69f99n47jgs0t374r46u3/1560607200000/09837260612050622056/*/0B6GhBwm5vaB2ekdlZW5WZnppb28?e=download')
    csv_raw = StringIO(url.text)
    df = pd.read_csv(csv_raw)

