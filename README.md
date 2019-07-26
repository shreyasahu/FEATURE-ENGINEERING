# FEATURE-ENGINEERING
CONTAINS CODE FOR MAPPING VALUES IN THE COLUMNS AND CONVERTING CATEGORICAL COLUMNS TO INTEGERS


    dict_cat = {"No Garage": 0, "Po": 1, "Fa": 2, "TA": 3, "Gd": 4, "Ex": 5,"No Basement":0}
    cat_cols = np.array(['ExterQual','ExterCond','BsmtCond','HeatingQC','KitchenQual','FireplaceQu', 'GarageQual','GarageCond','BsmtQual'])
    for i in cat_cols:
         df[i] = df[i].map(dict_cat).astype(int)

     
     
     df['BsmtExposure'] = df['BsmtExposure'].map({'No Basement': 0, 'No': 1, 'Mn': 2, 'Av': 3, 'Gd': 4}).astype(int)
 
 
 
 
     dict_bsmt={'No Basement': 0, "Unf": 1, "LwQ": 2, "Rec": 3, "BLQ": 4, "ALQ": 5, "GLQ": 6}
     df['BsmtFinType1'] = df['BsmtFinType1'].map(dict_bsmt).astype(int)
     
  CODE WHICH IS WRITTEN BELOW IN THAT (DF["LANDCONTOUR"]=="LVL")*1
RETURNS TRUE OR FALSE     

           df["Is_Land_Level"] = (df["LandContour"] == "Lvl") * 1
