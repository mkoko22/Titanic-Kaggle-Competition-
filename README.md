# 🚢 Titanic - Machine Learning from Disaster

## 📌 კონკურსის და პროექტის მიმოხილვა

Kaggle-ის **Titanic** კონკურსის მიზანია მგზავრების გადარჩენის (Survived: 1 ან 0) პროგნოზირება მათი დემოგრაფიული და ბილეთის მონაცემების საფუძველზე. 

## 🎯 შეფასების კრიტერიუმები / სასწავლო მიზნები
სტუდენტებისთვის ამ პროექტის შესრულებისას მთავარი ფოკუსი კეთდება შემდეგ უნარებზე:
* **EDA & Data Cleaning:** ლოგიკური მიდგომა დაკარგული მონაცემების (Age, Cabin, Embarked) შესავსებად.
* **Feature Engineering:** ახალი, აზრიანი სვეტების შექმნა (მაგ. FamilySize, Title).
* **Model Selection:** საბაზისო (Baseline) და რთული მოდელების (Trees, Ensembles) შედარება.
* **MLOps Foundations:** ექსპერიმენტების (ჰიპერპარამეტრები, მეტრიკები) აღრიცხვა და მოდელების რეგისტრაცია **MLflow**-სა და **DagsHub**-ის გამოყენებით.

---

## 📁 რეპოზიტორიის სტრუქტურა

```text
Titanic-Tutoring/
│
├── notebooks/                  ← Jupyter რვეულები ექსპერიმენტებისთვის
│   ├── 01_titanic-experiment-pipeline.ipynb
│   ├── 02_titanic-inference.ipynb
│
├── README.md

Gemini said
აი ზუსტად ისეთი სტილის (Blueprint/შაბლონი) README, როგორიც House Prices-ის შემთხვევაში გქონდა, თუმცა მორგებული Titanic-ის კლასიფიკაციის ამოცანაზე და სასწავლო/Tutoring მიზნებზე. აქ დამატებულია შეფასების კრიტერიუმების ბლოკიც, როგორც ითხოვე.

შეგიძლია პირდაპირ დააკოპირო შენს README.md ფაილში და [...] ადგილები შენი კონკრეტული ლინკებითა და მონაცემებით შეავსო.

Markdown
# 🚢 Titanic - Machine Learning from Disaster (სასწავლო პროექტი)

## 📌 კონკურსის და პროექტის მიმოხილვა

Kaggle-ის **Titanic** კონკურსის მიზანია მგზავრების გადარჩენის (Survived: 1 ან 0) პროგნოზირება მათი დემოგრაფიული და ბილეთის მონაცემების საფუძველზე. 
**სასწავლო მიზანი:** ეს რეპოზიტორია შექმნილია მენტორინგისთვის/სწავლებისთვის. ის გვიჩვენებს Machine Learning-ის სრულ ციკლს (End-to-End Pipeline) — საწყისი მონაცემების ანალიზიდან (EDA), Feature Engineering-ისა და სხვადასხვა მოდელის აგების გავლით, **MLflow**-ში ექსპერიმენტების ტრექინგამდე.

## 🎯 შეფასების კრიტერიუმები / სასწავლო მიზნები
სტუდენტებისთვის ამ პროექტის შესრულებისას მთავარი ფოკუსი კეთდება შემდეგ უნარებზე:
* **EDA & Data Cleaning:** ლოგიკური მიდგომა დაკარგული მონაცემების (Age, Cabin, Embarked) შესავსებად.
* **Feature Engineering:** ახალი, აზრიანი სვეტების შექმნა (მაგ. FamilySize, Title).
* **Model Selection:** საბაზისო (Baseline) და რთული მოდელების (Trees, Ensembles) შედარება.
* **MLOps Foundations:** ექსპერიმენტების (ჰიპერპარამეტრები, მეტრიკები) აღრიცხვა და მოდელების რეგისტრაცია **MLflow**-სა და **DagsHub**-ის გამოყენებით.

---

## 📁 რეპოზიტორიის სტრუქტურა

```text
Titanic-Tutoring/
│
├── notebooks/                  ← Jupyter რვეულები ექსპერიმენტებისთვის
│   ├── 01_Model_Training_Experiments.ipynb
│   ├── 02_Inference_and_Submission.ipynb
│
├── src/                        ← Custom Python სკრიპტები
│   ├── data_cleaner.py         ← კლასები Null-ების შესავსებად
│   ├── feature_engineering.py  ← Custom Sklearn კომპონენტები
│
├── README.md


ფაილი	აღწერა
01_Model_Training_Experiments.ipynb	ძირითადი notebook მოდელების კვლევისთვის
02_Inference_and_Submission.ipynb	MLflow-დან საუკეთესო მოდელის ჩამოტვირთვა და submission.csv-ის გენერაცია

🧼 Cleaning & 🧬 Feature Engineering
➤ Missing Values (NA-ების შევსება)

Age: [მოკლედ დაწერე შენი მიდგომა, მაგ: შეივსო title-ების მიხედვით მედიანით ან უბრალოდ მედიანით]

Embarked: [მაგ: შეივსო mode-ით]

Cabin: [მაგ: დიდი რაოდენობით NA-ების გამო დაიდროფა, ან შეიქმნა ახალი ბინარული სვეტი Has_Cabin]

➤ ახალი Feature-ების შექმნა

FamilySize: SibSp + Parch + 1 ფორმულით.

➤ Categorical Encoding

Sex → ბინარული კოდირება (0/1).

Embarked და Pclass → OneHotEncoder (ან სხვა ენკოდერი, რასაც იყენებ).

🧪 Training & ექსპერიმენტები
ტიტანიკის ამოცანისთვის მთავარი მეტრიკაა Accuracy. ყველა მოდელი დარეგისტრირდა MLflow-ში და გადაირჩა K-Fold Cross Validation-ის საშუალებით.

🔹 Model 1: Logistic Regression (Baseline)
მიდგომა: უმარტივესი მოდელი მხოლოდ ძირითადი რიცხვითი და One-Hot ენკოდირებული სვეტებით.

შედეგი: Accuracy: [შენი ციფრი]

ექსპერიმენტის ბმული: [ჩასვი MLflow ლინკი]

🔹 Model 2: Decision Tree & Random Forest
მიდგომა: ვცადეთ GridSearch-ით max_depth და n_estimators პარამეტრების ოპტიმიზაცია.

შედეგი (Random Forest): Accuracy: [შენი ციფრი]

ექსპერიმენტის ბმული: [ჩასვი MLflow ლინკი]

Gemini said
აი ზუსტად ისეთი სტილის (Blueprint/შაბლონი) README, როგორიც House Prices-ის შემთხვევაში გქონდა, თუმცა მორგებული Titanic-ის კლასიფიკაციის ამოცანაზე და სასწავლო/Tutoring მიზნებზე. აქ დამატებულია შეფასების კრიტერიუმების ბლოკიც, როგორც ითხოვე.

შეგიძლია პირდაპირ დააკოპირო შენს README.md ფაილში და [...] ადგილები შენი კონკრეტული ლინკებითა და მონაცემებით შეავსო.

Markdown
# 🚢 Titanic - Machine Learning from Disaster (სასწავლო პროექტი)

## 📌 კონკურსის და პროექტის მიმოხილვა

Kaggle-ის **Titanic** კონკურსის მიზანია მგზავრების გადარჩენის (Survived: 1 ან 0) პროგნოზირება მათი დემოგრაფიული და ბილეთის მონაცემების საფუძველზე. 
**სასწავლო მიზანი:** ეს რეპოზიტორია შექმნილია მენტორინგისთვის/სწავლებისთვის. ის გვიჩვენებს Machine Learning-ის სრულ ციკლს (End-to-End Pipeline) — საწყისი მონაცემების ანალიზიდან (EDA), Feature Engineering-ისა და სხვადასხვა მოდელის აგების გავლით, **MLflow**-ში ექსპერიმენტების ტრექინგამდე.

## 🎯 შეფასების კრიტერიუმები / სასწავლო მიზნები
სტუდენტებისთვის ამ პროექტის შესრულებისას მთავარი ფოკუსი კეთდება შემდეგ უნარებზე:
* **EDA & Data Cleaning:** ლოგიკური მიდგომა დაკარგული მონაცემების (Age, Cabin, Embarked) შესავსებად.
* **Feature Engineering:** ახალი, აზრიანი სვეტების შექმნა (მაგ. FamilySize, Title).
* **Model Selection:** საბაზისო (Baseline) და რთული მოდელების (Trees, Ensembles) შედარება.
* **MLOps Foundations:** ექსპერიმენტების (ჰიპერპარამეტრები, მეტრიკები) აღრიცხვა და მოდელების რეგისტრაცია **MLflow**-სა და **DagsHub**-ის გამოყენებით.

---

## 📁 რეპოზიტორიის სტრუქტურა

```text
Titanic-Tutoring/
│
├── notebooks/                  ← Jupyter რვეულები ექსპერიმენტებისთვის
│   ├── 01_EDA_and_Baseline.ipynb
│   ├── 02_Model_Training_Experiments.ipynb
│   ├── 03_Inference_and_Submission.ipynb
│
├── src/                        ← Custom Python სკრიპტები
│   ├── data_cleaner.py         ← კლასები Null-ების შესავსებად
│   ├── feature_engineering.py  ← Custom Sklearn კომპონენტები
│
├── README.md
📄 ფაილების აღწერა
ფაილი	აღწერა
01_EDA_and_Baseline.ipynb	მონაცემების ვიზუალიზაცია და მარტივი ლოჯისტიკური რეგრესიის (Baseline) აგება
02_Model_Training...ipynb	ძირითადი notebook ხისებრი და Boosting მოდელების კვლევისთვის
03_Inference...ipynb	MLflow-დან საუკეთესო მოდელის ჩამოტვირთვა და submission.csv-ის გენერაცია
data_cleaner.py	მონაცემთა გაწმენდის რეუსაბელური კოდი (Pipeline-ისთვის)
🧼 Cleaning & 🧬 Feature Engineering
➤ Missing Values (NA-ების შევსება)

Age: [მოკლედ დაწერე შენი მიდგომა, მაგ: შეივსო title-ების მიხედვით მედიანით ან უბრალოდ მედიანით]

Embarked: [მაგ: შეივსო mode-ით]

Cabin: [მაგ: დიდი რაოდენობით NA-ების გამო დაიდროფა, ან შეიქმნა ახალი ბინარული სვეტი Has_Cabin]

➤ ახალი Feature-ების შექმნა

FamilySize: SibSp + Parch + 1 ფორმულით.

Title: მგზავრის სახელიდან სტატუსის (Mr, Mrs, Miss და ა.შ.) ამოღება, რაც Age-ის ლოგიკურად შესავსებად გამოგვადგა.

➤ Categorical Encoding

Sex → ბინარული კოდირება (0/1).

Embarked და Pclass → OneHotEncoder (ან სხვა ენკოდერი, რასაც იყენებ).

🧪 Training & ექსპერიმენტები
ტიტანიკის ამოცანისთვის მთავარი მეტრიკაა Accuracy. ყველა მოდელი დარეგისტრირდა MLflow-ში და გადაირჩა K-Fold Cross Validation-ის საშუალებით.

🔹 Model 1: Logistic Regression (Baseline)
მიდგომა: უმარტივესი მოდელი მხოლოდ ძირითადი რიცხვითი და One-Hot ენკოდირებული სვეტებით.

შედეგი: Accuracy: [შენი ციფრი]

ექსპერიმენტის ბმული: [ჩასვი MLflow ლინკი]

🔹 Model 2: Decision Tree & Random Forest
მიდგომა: ვცადეთ GridSearch-ით max_depth და n_estimators პარამეტრების ოპტიმიზაცია.

შედეგი (Random Forest): Accuracy: [შენი ციფრი]

ექსპერიმენტის ბმული: [ჩასვი MLflow ლინკი]

🔹 Model 3: XGBoost / GradientBoosting
მიდგომა: საუკეთესო შედეგისთვის გამოვიყენეთ Boosting. შეირჩა პარამეტრები: learning_rate=[...], max_depth=[...].

შედეგი: Accuracy: [შენი ციფრი]

ექსპერიმენტის ბმული: [ჩასვი MLflow ლინკი]

📊 MLflow – შემაჯამებელი მიმოხილვა
ყველა მოდელის ექსპერიმენტი რეგისტრირებულია DagsHub / MLflow-ში.

▪️ ჩაწერილი მეტრიკები:

Accuracy – კეგლის მთავარი მეტრიკა.

F1-Score – კლასების დისბალანსის (გადარჩა/არ გადარჩა) უკეთ შესაფასებლად.

⭐️ საუკეთესო მოდელი:
საბოლოოდ კეგლზე დასასაბმითებლად შეირჩა [ჩაწერე საუკეთესო მოდელი, მაგ: XGBoost Version 1], რადგან ტესტ სეტზე აჩვენა საუკეთესო გენერალიზაციის უნარი.

Kaggle Leaderboard Score: [კეგლის ქულა]

🛠 გამოცდილება (Lessons Learned)
Feature Engineering: მხოლოდ FamilySize სვეტის დამატებამ საბაზისო მოდელის სიზუსტე [X]%-ით გაზარდა.

Overfitting-ის კონტროლი: ხისებრი მოდელები ძალიან სწრაფად იმახსოვრებდნენ თრეინინგ სეტს (100% accuracy), ამიტომ აუცილებელი გახდა max_depth და min_samples_split პარამეტრების შეზღუდვა.

MLflow-ის პრაქტიკულობა: ცალკეულ ნოუთბუქში (Inference) უკვე დატრენინგებული მოდელის Cloud-დან models:/[ModelName]/[Version] სახით წამოღებამ კოდი ბევრად სუფთა და პროფესიონალური გახადა.
