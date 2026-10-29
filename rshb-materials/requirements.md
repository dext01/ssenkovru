# Соответствие задачам «Своё Жильё»

Основание: формулировки трёх задач, предоставленные участником в переписке. Это самостоятельная проверка соответствия, а не заключение организатора. Допустимость подачи трёх задач одной заявкой не подтверждена.

Версия продукта: `8ec117a`; дата проверки: 29.10.2026.

| Пункт | Требование | Статус | Что показать и границы | Ссылка | Исходники в source.zip |

|---|---|---|---|---|---|

| 1.1 | Досрочный платёж | Есть | Сумма, срок/платёж, экономия, график. | https://ssenkov.ru/task_for_rshb/#/s/early-repayment | src/config/defaultScenarios.ts; src/engine/finance.ts |

| 1.2 | Кредит на ремонт | Есть | Платёж, нагрузка, бюджет, сравнение с накоплением. | https://ssenkov.ru/task_for_rshb/#/s/renovation-loan | src/config/defaultScenarios.ts |

| 1.3 | Сдача квартиры в аренду | Есть | Простой, расходы, НДФЛ/НПД, покрытие ипотеки. | https://ssenkov.ru/task_for_rshb/#/s/rent-out | src/engine/tax.ts; src/config/defaultScenarios.ts |

| 1.4 | Изменение платежа, срока, переплаты и бюджета | Есть | Карточки «было → стало», подробная таблица и графики. | https://ssenkov.ru/task_for_rshb/#/s/refinance | src/ui/sim/Results.tsx |

| 1.5 | Изолированные расчёты | Есть | Чистое ядро без React/DOM/сети. Подтверждение — исходники и тесты. | source.zip | src/engine/scenario.ts; src/engine/expression.ts |

| 1.6 | Добавление сценариев, формул и параметров администратором | Есть | Создание, редактирование, проверка, импорт/экспорт. Публичная админка — локальное демо. | https://ssenkov.ru/task_for_rshb/#/admin | src/ui/admin/ScenarioEditor.tsx; src/config/parse.ts |

| 1.7 | Настройка подсказок | Есть | Условия, текст с подстановками, уровень и главный вывод. | https://ssenkov.ru/task_for_rshb/#/admin/early-repayment | src/ui/admin/ScenarioEditor.tsx |

| 2.1 | Этапы от выбора до сделки и обустройства | Есть | Цель, бюджет, объект, сделка, жизнь после сделки. | https://ssenkov.ru/task_for_rshb/#/path | src/config/defaultJourney.ts |

| 2.2 | Квартира в новостройке | Есть | Маршрут, вопросы о взносе и маткапитале, документы. | https://ssenkov.ru/task_for_rshb/#/path/flat | src/config/defaultJourney.ts |

| 2.3 | Частный дом | Есть | Сценарий покупки дома. | https://ssenkov.ru/task_for_rshb/#/path/house | src/config/defaultJourney.ts |

| 2.4 | Участок | Есть | Покупка участка и дальнейшие планы. | https://ssenkov.ru/task_for_rshb/#/path/land | src/config/defaultJourney.ts |

| 2.5 | Строительство | Есть с допущениями | Шаги меняются для подрядчика и своих сил; расчёт использует равные транши. | https://ssenkov.ru/task_for_rshb/#/path/build | src/config/defaultJourney.ts |

| 2.6 | Ремонт | Есть | Разные виды ремонта и источники средств. | https://ssenkov.ru/task_for_rshb/#/path/repair | src/config/defaultJourney.ts |

| 2.7 | Сельская ипотека | Есть как справочный маршрут | Покупка готового жилья или строительство. Актуальность условий подтверждает банк. | https://ssenkov.ru/task_for_rshb/#/path/rural | src/config/defaultJourney.ts |

| 2.8 | Готовый объект | Есть | Отдельный маршрут покупки готового жилья. | https://ssenkov.ru/task_for_rshb/#/path/ready | src/config/defaultJourney.ts |

| 2.9 | Адаптация шагов и рекомендаций | Есть | Условия над ответами, варианты шагов, сравнение маршрутов. | https://ssenkov.ru/task_for_rshb/#/path/build | src/engine/journey.ts |

| 3.1 | Досрочное погашение и изменение срока/платежа | Есть | Рекомендации открывают калькулятор с данными профиля. | https://ssenkov.ru/task_for_rshb/#/after | src/engine/after.ts |

| 3.2 | Налоговый вычет | Есть с границами модели | Один заявитель, общая шкала с 2025 года, использованная база и бюджетные средства. Не налоговая экспертиза. | https://ssenkov.ru/task_for_rshb/#/s/tax-deduction | src/engine/tax.ts; src/config/defaultScenarios.ts |

| 3.3 | Справки, страхование и другие сервисы | Есть | Карточки действий, документы, страховка, бюджет, аренда и ремонт. | https://ssenkov.ru/task_for_rshb/#/after | src/config/defaultAfter.ts |

| 3.4 | Гость: демо или ручной ввод | Есть | Переключатели источника данных и ручная форма. | https://ssenkov.ru/task_for_rshb/#/after | src/config/afterState.ts |

| 3.5 | Публичный сайт | Есть | Рабочая клиентская версия в браузере. | https://ssenkov.ru/task_for_rshb/ | src/App.tsx |

| 3.6 | Авторизованный клиент: данные банковского контура | Контракт и демонстрация | postMessage, разрешённые origin, проверка структуры, хранение профиля в памяти. Настоящий контур не подключён. | https://ssenkov.ru/task_for_rshb/#/after | src/config/bank.ts; docs/modules.md |

| 3.7 | Работа в личном кабинете | Подготовлено к интеграции | iframe, embed=1, события и изменение высоты. SSO/API требуют участия банка. | https://ssenkov.ru/task_for_rshb/?embed=1#/after | docs/integration.md |

| Д.1 | Единый личный план | Есть | Общие данные, сохранение и закрепление варианта в маршруте. | https://ssenkov.ru/task_for_rshb/#/saved | src/config/decision.ts; src/ui/SelectedDecision.tsx |

| Д.2 | Версии и согласование публикаций | Есть в серверном эталоне | Черновик, различия, другой сотрудник, контрольные примеры. На Pages сервер не запущен. | source.zip | server/app.ts; docs/server.md |

| Д.3 | Качество и доступность | Автоматические проверки | 359 модульных/интеграционных и 49 браузерных проверок; axe, телефон, печать, офлайн. Не сертификат доступности. | https://github.com/dext01/ssenkov/actions/runs/40907568205 | tests/; e2e/ |

## Границы готовности

Публичная версия — клиентское приложение с локальным хранением. Настоящие банковские данные, SSO и публикация через сервер на домене не подключены. Серверный эталон поставляется в исходниках и проверен отдельно.

В модуле после оформления ипотеки есть справочная памятка закрытия, но нет самостоятельного состояния «кредит полностью погашен». Условия программ, сроки и документы перед банковским внедрением утверждаются заказчиком.

Синтетическая проверка описана отдельно в review-report.md. Отзывы реальных людей не представлены.
