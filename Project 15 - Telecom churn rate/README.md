# Проект 15: Прогнозирование оттока телеком компании

### *Направление:*
Машинное обучение

### *Задача:*
Прогнозирование оттока телеком компании

### *Описание:*
Оператор связи «Ниединогоразрыва.ком» хочет научиться прогнозировать отток клиентов. Если выяснится, что пользователь планирует уйти, ему будут предложены промокоды и специальные условия. Команда оператора собрала персональные данные о некоторых клиентах, информацию об их тарифах и договорах.

### *Инструменты:*
Python, Pandas, Re, Phi_K, Seaborn, NumPy, Time, Category_encoders, Scikitplot, SHAP, Statsmodels, Matplotlib, Sklearn, Imblearn, LightGBM, CatBoost, Pipeline, SMOTE, SVM

### *Вывод:*
Во время анализа, мы столкнулись с несколькими трудносятми. Мы обнаружили аномалию, которая повлияла на предвзятость нашей модели. Мы создали несколько синтетических признаков, чтобы невилировать влияние аномалии, но всеравно модель остается предвзятой.
Во время формирования признаков, мы выделили для каждого клитента год начала обслуживания в отдельный признак, но потом отказались от этого из-за возможности утечки целевого признака. Мы разработали модель, показавшую ROC-AUC метрику: 0.955, что удовлетворяет поставленной цели.
Мы определили, что за последний месяц с компанией разорвало договор в 2 раза больше клиентов, чем заключило новых. В денежном эквиваленте, это 33384,7 денежных средств, которые компания не получит в следующем месяце. Основываясь на матрице ошибок, мы можем утверждать, что модель верно предсказала бы уход 73% этих клиентов, что эквивалентно 24447,6 денежных средств, не считая затрат на удержание этих клиентов (скидки и акции). 

### *Рекомендации компании:*
 * Предоставить более полный набор данных, для улучшения работы модели.
 * Срочно начать компанию по удержанию клиентов.
 * Обратить внимание на признаки, оказавшиеся ключевыми для модели: общие и месячные траты клиентов, длительность заключенного договора с клиентом, тип договора и услуги интернет сервиса. (эти же признаки фигурировали в исследовании категориальных признаков с подробными выводами).
