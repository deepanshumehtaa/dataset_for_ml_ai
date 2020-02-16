# csvfiles
use this to access csv file

for inbuilt datasets lik iris to load them use
      
    from sklearn.datasets import load_iris
    sk_data = load_iris()
    print(sk_data)

    df = pd.DataFrame(sk_data.data, columns=sk_data.feature_names)
    df.head()

Iris is decleared in Sklearn so to convert it into df  
