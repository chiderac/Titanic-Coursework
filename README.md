# Titanic-Coursework
Predicting survivability of titanic passengers using machine learning techniques



**Add this Code for fscore


from sklearn.metrics import precision_recall_fscore_support
Score_model = {}
clfs = [RandomForestClassifier(), LogisticRegression(), DecisionTreeClassifier()]
models = ['RandomForest', 'LogisticRegression', 'DecisionTreeClassificer']
for i in range(3):
    clf = clfs[i]
    clf.fit(x_train,y_train)
    y_pred = clf.predict(x_test)
    (precision, recall, fscore, none) = precision_recall_fscore_support(y_test, y_pred, average='binary')
    print("\nModel: ", models[i],"[\nprecision:", precision,"],[recall:",recall, "],[fscore:", fscore,"] ") 
