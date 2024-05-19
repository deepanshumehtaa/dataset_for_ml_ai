
    import pandas
    
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
Follow this Documentation for Keras Dataset: https://jovianlin.io/datasets-within-keras/

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

    url = requests.get('https://doc-0g-78docs.googleusercontent.com/docs/securesc/token')
    csv_raw = StringIO(url.text)
    df = pd.read_csv(csv_raw)


# Download Dataset from Kaggle using kaggle API

"""
!pip install -q kaggle: installing this packageing but quitely with no loading bars


!mkdir -p ~/.kaggle

the command is creating a -p as parent directory if not exist at root(~/) 

!cp kaggle.json ~/.kaggle/

copy the api secrete key to main kaggle folder
Ensure kaggle.json is in the location ~/.kaggle/kaggle.json to use the API.

!ls ~/.kaggle
if present return nothing else error

!chmod 600 /root/.kaggle/kaggle.json 
-- 600 permissions means that only the owner of the file has full read and write access to it. 
   Once a file permission is set to 600, no one else can access the file.

calling kaggle api with kaggle's python package:
!kaggle datasets download -d emmarex/plantdisease
"""
!pip install -q kaggle
!mkdir -p ~/.kaggle
!cp <your_key_file>.json ~/.kaggle/
!ls ~/.kaggle
!mv '/root/.kaggle/<your_key_file>.json' '/root/.kaggle/kaggle.json' 
!chmod 600 /root/.kaggle/kaggle.json  # set permission

# Run the Download API
!kaggle datasets download -d devashish0507/big-mart-sales-prediction

# Unzip that also
!unzip plantdisease.zip
