## Материалы по глубокому обучению для Института биоинформатики

### Содержание

| Тема              | Материалы | Задания |
| :---------------- | :------ | :---- |
| 1. Введение в глубокое обучение | [Слайды](slides/dl-intro.pdf) <br><br> |  |
| 2. Введение в Pytorch (часть 1) <br><br> | [Тензоры](notebooks/tensors.ipynb) <br><br><br>| [Операции над тензорами](assignments/tensor_ops.ipynb) <br> [Градиентный спуск на NumPy](assignments/gradient_descent.ipynb) <br> Дедлайн: 19.04 23:59|
| 3. Введение в Pytorch (часть 2) <br><br><br><br><br><br><br><br> | [Autograd в PyTorch](notebooks/autograd.ipynb) <br> [Пример: логистическая регрессия](notebooks/backprop.ipynb) <br> [Оптимизаторы, параметры и модули](notebooks/parameters_and_modules.ipynb) <br> [Работа с данными](notebooks/dataloader.ipynb) <br> [Пример: MLP на датасете MNIST](notebooks/mnist.ipynb) <br> [Инициализация параметров](notebooks/initialization.ipynb) <br> (самостоятельное изучение)| [Стабилизация обучения и регуляризация](assignments/training_tricks.ipynb) <br> Дедлайн: 26.04 23:59 <br><br><br><br><br><br><br> |
| 4. Архитектуры нейронных сетей | [Слайды](slides/dl-architectures.pdf) <br><br> |  |
| 5. Адаптация моделей | [Слайды](https://norsage.github.io/dl-bioinf/slides/dl-model-adaptation.html) <br><br> |  |
| 6. Структура проекта, инструменты и управление экспериментами | [Слайды](https://norsage.github.io/dl-bioinf/slides/dl-experiment-management.html) <br><br> |  |


### Создание окружения
Версии пакетов в списке зависимостей зафиксированы под python 3.13 и pytorch 2.8.0. Можно использовать другие версии, но в этом случае будьте готовы самостоятельно решать проблемы с зависимостями (впрочем, это полезный опыт).

Создаём и активируем виртуальное окружение:
```
python3.13 -m venv .venv
source .venv/bin/activate
```

Далее устанавливаем зависимости, они немного отличаются в зависимости от операционной системы, архитектуры процессора и модели видеокарты.

Для linux без использования CUDA (легковесная версия, подойдёт для большей части заданий)
```
pip install -r requirements-linux-cpu.txt
```
Для linux с использованием CUDA (у вас должна быть видеокарта NVIDIA и до 15 Гб места на диске):
```
pip install -r requirements-linux-cuda.txt
```
Для MacOS с процессором серии M:
```
pip install -r requirements-macos.txt
```
Для более ранних Macbook pytorch новых версий (2.2.0+) больше не поставляется. Если вы хотите использовать такой Macbook, придётся использовать более старые версии python и pytorch.
