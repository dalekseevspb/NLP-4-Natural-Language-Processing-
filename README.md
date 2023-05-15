# NLP-4 (Natural Language Processing, Обработка естественного языка)
# (#3) Классификация по тональности. Thematic_modeling, Тематическое моделирование
# 1) Классификация по тональности.
В этом домашнем задании вам предстоит классифицировать по тональности отзывы на банки с сайта banki.ru.
Данные содержат непосредственно тексты отзывов, некоторую дополнительную информацию, а также оценку по шкале от 1 до 5.
Тексты хранятся в json-ах в массиве responses.

# Часть 1. Анализ текстов.
а) Посчитайте количество отзывов в разных городах и на разные банки.

б) Постройте гистограммы длин слов в символах и в словах.

в) Найдите 10 самых частых:
- слов.
- слов без стоп-слов.
- лемм.
- существительных.

г) Постройте кривые Ципфа и Хипса.

д) Ответьте на следующие вопросы:
- какое слово встречается чаще, "сотрудник" или "клиент"?
- сколько раз встречаются слова "мошенничество" и "доверие"?

е) В поле "rating_grade" записана оценка отзыва по шкале от 1 до 5. Используйте меру tf-idf для того, чтобы найти ключевые слова и биграммы для положительных отзывов (с оценкой 5) и отрицательных отзывов (с оценкой 1).

# Часть 2. Тематическое моделирование.
а) Постройте несколько тематических моделей коллекции документов с разным числом тем. Приведите примеры понятных (интерпретируемых) тем.

б) Найдите темы, в которых упомянуты конкретные банки (Сбербанк, ВТБ, другой банк). Можете ли вы их прокомментировать / объяснить?
Эта часть задания может быть сделана с использованием gensim.

# Часть 3. Классификация текстов.
а) Сформулируем для простоты задачу бинарной классификации: будем классифицировать на два класса, то есть, различать резко отрицательные отзывы (с оценкой 1) и положительные отзывы (с оценкой 5).

б) Составьте обучающее и тестовое множество: выберите из всего набора данных N1 отзывов с оценкой 1 и N2 отзывов с оценкой 5 (значение N1 и N2 – на ваше усмотрение). Используйте sklearn.model_selection.train_test_split для разделения множества отобранных документов на обучающее и тестовое. Используйте любой известный вам алгоритм классификации текстов для решения задачи и получите baseline. Сравните разные варианты векторизации текста: использование только униграм, пар или троек слов или с использованием символьных n-грам.

в) Сравните, как изменяется качество решения задачи при использовании скрытых тем в качестве признаков:
- 1-ый вариант: tf-idf преобразование (sklearn.feature_extraction.text.TfidfTransformer) и сингулярное разложение (оно же – латентый семантический анализ) (sklearn.decomposition.TruncatedSVD),
- 2-ой вариант: тематические модели LDA (sklearn.decomposition.LatentDirichletAllocation). Используйте accuracy и F-measure для оценки качества классификации.

# HW(7), ДЗ к лекции №7 "Классификация в NLP".

# HW(11), ДЗ к лекции №11 "Синтаксический анализ".
