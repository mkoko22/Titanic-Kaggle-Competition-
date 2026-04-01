# Titanic - Machine Learning from Disaster - Tutoring

## კონკურსის და პროექტის მიმოხილვა

Kaggle-ის **Titanic** კონკურსის მიზანია მგზავრების გადარჩენის (Survived: 1 ან 0) პროგნოზირება მათი დემოგრაფიული და ბილეთის მონაცემების საფუძველზე. 

## შეფასების კრიტერიუმები / სასწავლო მიზნები
სტუდენტებისთვის ამ პროექტის შესრულებისას მთავარი ფოკუსი კეთდება შემდეგ უნარებზე:
* **EDA & Data Cleaning:** ლოგიკური მიდგომა დაკარგული მონაცემების (Age, Cabin, Embarked) შესავსებად.
* **Feature Engineering:** ახალი, აზრიანი სვეტების შექმნა (მაგ. FamilySize, Title).
* **Model Selection:** საბაზისო (Baseline) და რთული მოდელების (Trees, Ensembles) შედარება.
* **MLOps Foundations:** ექსპერიმენტების (ჰიპერპარამეტრები, მეტრიკები) აღრიცხვა და მოდელების რეგისტრაცია **MLflow**-სა და **DagsHub**-ის გამოყენებით.

## 📁 რეპოზიტორიის სტრუქტურა

```text
Titanic-Tutoring/
│
├── notebooks/
│   ├── 01...
│   ├── 02...
│   ├── 03...
│
├── src/ 
│   ├── 
│   ├── 
│
└── README.md
└── README.md
```

## ფაილების აღწერა

Cleaning &  Feature Engineering

➤ Missing Values (NA-ების შევსება)

➤ ახალი Feature-ების შექმნა

FamilySize: SibSp + Parch + 1 ფორმულით.

➤ Categorical Encoding

Sex → ბინარული კოდირება (0/1).

Embarked და Pclass → OneHotEncoder.

## Training & ექსპერიმენტები

ტიტანიკის ამოცანისთვის მთავარი მეტრიკაა Accuracy. ყველა მოდელი დარეგისტრირდა MLflow-ში და გადაირჩა K-Fold Cross Validation-ის საშუალებით.

## 🔹 Model 1: Logistic Regression (Baseline)


## 🔹 Model 2: Decision Tree & Random Forest


## MLflow – შემაჯამებელი მიმოხილვა

ყველა მოდელის ექსპერიმენტი რეგისტრირებულია DagsHub / MLflow-ში.

## საუკეთესო მოდელი:

საბოლოოდ კეგლზე დასასაბმითებლად შეირჩა Decision Tree, რადგან ტესტ სეტზე აჩვენა საუკეთესო გენერალიზაციის უნარი.

Kaggle Leaderboard Score: 0.78
