# python-portfolio
My Python programs
[data.csv](https://github.com/user-attachments/files/25138124/data.csv)
Hours_Studied,Hours_Slept,Test_Score
1,5,60
3,6,70
5,7,80
7,8,88
9,9,95
[model.py](https://github.com/user-attachments/files/25138137/model.py)
import pandas as pd
from sklearn.linear_model import LinearRegression

data = pd.read_csv("data.csv")

X = data[["Hours_Studied", "Hours_Slept"]]
y = data["Test_Score"]

model = LinearRegression()
model.fit(X, y)

prediction = model.predict([[5, 5]])

print("The AI predicted a test score of " + str(prediction[0]) +
      " for a student who studied 6 hours and slept 8 hours.")
