    url = 'https://raw.githubusercontent.com/deepanshumehtaa/csvfiles/master/xyz.csv'
    df = pd.read_csv(url, index_col=0, delimiter=',')
    df = df.reset_index()
    df.head(5)


# csvfiles
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
