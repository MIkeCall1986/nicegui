<a href="https://nicegui.io/#about">
  <img src="https://raw.githubusercontent.com/zauberzeug/nicegui/main/screenshot.png"
    width="200" align="right" alt="Try online!" />
</a>

# NiceGUI

NiceGUI is an easy-to-use, Python-based UI framework, which shows up in your web browser.
You can create buttons, dialogs, Markdown, 3D scenes, plots and much more.

It is great for micro web apps, dashboards, robotics projects, smart home solutions and similar use cases.
You can also use it in development, for example when tweaking/configuring a machine learning algorithm or tuning motor controllers.

NiceGUI is available as [PyPI package](https://pypi.org/project/nicegui/), [Docker image](https://hub.docker.com/r/zauberzeug/nicegui) and on [conda-forge](https://anaconda.org/conda-forge/nicegui) as well as [GitHub](https://github.com/zauberzeug/nicegui).

[![PyPI](https://img.shields.io/pypi/v/nicegui?color=dark-green)](https://pypi.org/project/nicegui/)
[![PyPI downloads](https://img.shields.io/pypi/dm/nicegui?color=dark-green)](https://pypi.org/project/nicegui/)
[![Conda version](https://img.shields.io/conda/v/conda-forge/nicegui?color=green&label=conda-forge)](https://anaconda.org/conda-forge/nicegui)
[![Conda downloads](https://img.shields.io/conda/dn/conda-forge/nicegui?color=green&label=downloads)](https://anaconda.org/conda-forge/nicegui)
[![Docker pulls](https://img.shields.io/docker/pulls/zauberzeug/nicegui)](https://hub.docker.com/r/zauberzeug/nicegui)<br />
[![GitHub license](https://img.shields.io/github/license/zauberzeug/nicegui?color=orange)](https://github.com/zauberzeug/nicegui/blob/main/LICENSE)
[![GitHub commit activity](https://img.shields.io/github/commit-activity/m/zauberzeug/nicegui)](https://github.com/zauberzeug/nicegui/graphs/commit-activity)
[![GitHub issues](https://img.shields.io/github/issues/zauberzeug/nicegui?color=blue)](https://github.com/zauberzeug/nicegui/issues)
[![GitHub forks](https://img.shields.io/github/forks/zauberzeug/nicegui)](https://github.com/zauberzeug/nicegui/network)
[![GitHub stars](https://img.shields.io/github/stars/zauberzeug/nicegui)](https://github.com/zauberzeug/nicegui/stargazers)

## Features

- browser-based graphical user interface
- implicit reload on code change
- acts as webserver (accessed by the browser) or in native mode (eg. desktop window)
- standard GUI elements like label, button, checkbox, switch, slider, input, file upload, ...
- simple grouping with rows, columns, cards and dialogs
- general-purpose HTML and Markdown elements
- powerful high-level elements to
  - plot graphs and charts,
  - render 3D scenes,
  - get steering events via virtual joysticks
  - annotate and overlay images
  - interact with tables
  - navigate foldable tree structures
  - embed video and audio files
- built-in timer to refresh data in intervals (even every 10 ms)
- straight-forward data binding and refreshable functions to write even less code
- notifications, dialogs and menus to provide state of the art user interaction
- shared and individual web pages
- easy-to-use per-user and general persistence
- ability to add custom routes and data responses
- capture keyboard input for global shortcuts etc.
- customize look by defining primary, secondary and accent colors
- live-cycle events and session data
- runs in Jupyter Notebooks and allows Python's interactive mode
- auto-complete support for Tailwind CSS
- SVG, Base64 and emoji favicon support
- testing framework based on pytest

## Installation

```bash
python3 -m pip install nicegui
```

## Usage

Write your nice GUI in a file `main.py`:

```python
from nicegui import ui

ui.label('Hello NiceGUI!')
ui.button('BUTTON', on_click=lambda: ui.notify('button was pressed'))

ui.run()
```

Launch it with:

```bash
python3 main.py
```

The GUI is now available through http://localhost:8080/ in your browser.
Note: NiceGUI will automatically reload the page when you modify the code.

## Documentation and Examples

The documentation is hosted at [https://nicegui.io/documentation](https://nicegui.io/documentation) and provides plenty of live demos.
The whole content of [https://nicegui.io](https://nicegui.io) is [implemented with NiceGUI itself](https://github.com/zauberzeug/nicegui/blob/main/main.py)
and can be started locally with `docker run -p 8080:8080 zauberzeug/nicegui` or by executing `main.py` from this repository.

You may also have a look at our [in-depth examples](https://github.com/zauberzeug/nicegui/tree/main/examples) of what you can do with NiceGUI.
In our wiki we have a list of great [NiceGUI projects from the community](https://github.com/zauberzeug/nicegui/wiki#community-projects), a section with [Tutorials](https://github.com/zauberzeug/nicegui/wiki#tutorials), a growing list of [FAQs](https://github.com/zauberzeug/nicegui/wiki/FAQs) and [some strategies for using ChatGPT / LLMs to get help about NiceGUI](https://github.com/zauberzeug/nicegui/wiki#chatgpt).

## Why?

We at [Zauberzeug](https://zauberzeug.com) like [Streamlit](https://streamlit.io/)
but find it does [too much magic](https://github.com/zauberzeug/nicegui/issues/1#issuecomment-847413651) when it comes to state handling.
In search for an alternative nice library to write simple graphical user interfaces in Python we discovered [JustPy](https://justpy.io/).
Although we liked the approach, it is too "low-level HTML" for our daily usage.
But it inspired us to use [Vue](https://vuejs.org/) and [Quasar](https://quasar.dev/) for the frontend.

We have built on top of [FastAPI](https://fastapi.tiangolo.com/),
which itself is based on the ASGI framework [Starlette](https://www.starlette.io/)
and the ASGI webserver [Uvicorn](https://www.uvicorn.org/)
because of their great performance and ease of use.

## Sponsors

Maintenance of this project is made possible by all the [contributors](https://github.com/zauberzeug/nicegui/graphs/contributors) and [sponsors](https://github.com/sponsors/zauberzeug).
If you would like to support this project and have your avatar or company logo appear below, please [sponsor us](https://github.com/sponsors/zauberzeug). 💖

<!-- SPONSORS -->
<p align="center">
  <a href="https://github.com/lechler-gmbh"><img src="https://github.com/lechler-gmbh.png" width="50px" alt="Lechler GmbH" /></a>
  <a href="https://github.com/Zhifeng2019"><img src="https://github.com/Zhifeng2019.png" width="50px" alt="Zhifeng" /></a>
  <a href="https://github.com/sereneturtlefox"><img src="https://github.com/sereneturtlefox.png" width="50px" alt="None" /></a>
  <a href="https://github.com/daviborges666"><img src="https://github.com/daviborges666.png" width="50px" alt="Davi Borges" /></a>
  <a href="https://github.com/whoulden"><img src="https://github.com/whoulden.png" width="50px" alt="Wayne Houlden" /></a>
  <a href="https://github.com/digiquip"><img src="https://github.com/digiquip.png" width="50px" alt="DigiQuip AS" /></a>
</p>
<!-- SPONSORS -->

Consider this low-barrier form of contribution yourself.
Your [support](https://github.com/sponsors/zauberzeug) is much appreciated.

## Contributing

Thank you for your interest in contributing to NiceGUI! We are thrilled to have you on board and appreciate your efforts to make this project even better.

As a growing open-source project, we understand that it takes a community effort to achieve our goals. That's why we welcome all kinds of contributions, no matter how small or big they are. Whether it's adding new features, fixing bugs, improving documentation, or suggesting new ideas, we believe that every contribution counts and adds value to our project.

We have provided a detailed guide on how to contribute to NiceGUI in our [CONTRIBUTING.md](https://github.com/zauberzeug/nicegui/blob/main/CONTRIBUTING.md) file. We encourage you to read it carefully before making any contributions to ensure that your work aligns with the project's goals and standards.

If you have any questions or need help with anything, please don't hesitate to reach out to us. We are always here to support and guide you through the contribution process.

## Included Web Dependencies

See [DEPENDENCIES.md](https://github.com/zauberzeug/nicegui/blob/main/DEPENDENCIES.md) for a list of web frameworks NiceGUI depends on.

18.02.26
Ось результати аналізу та стратегія трансформації для проекту **NiceGUI**, підготовлені у форматі для копіювання в Notion.

---

# 📑 Звіт AI-консультанта: Проект "NiceGUI"

**NiceGUI** — це високорівневий Python-фреймворк для створення веб-інтерфейсів, який дозволяє розробникам будувати кнопки, діалоги, 3D-сцени та графіки, використовуючи лише мову Python,.

## 🧬 Частина 1: "ДНК" Проекту

Логіку коду **NiceGUI** можна розбити на такі **атомарні функції**:

*   **Рендеринг та UI-компоненти:** Використання Vue та Quasar на фронтенді для відображення стандартних (кнопки, слайдери) та складних (3D-сцени, графіки) елементів інтерфейсу,.
*   **Серверна логіка (Backend):** Побудова на базі FastAPI, Starlette та Uvicorn, що забезпечує високу продуктивність та обробку запитів.
*   **Обробка подій (Event Handling):** Захоплення дій користувача (натискання клавіш, кліки, рух джойстика) та зв'язок їх із Python-функціями,.
*   **Управління станом та даними:** Пряме зв'язування даних (data binding) та функції оновлення, що дозволяють писати менше коду для синхронізації інтерфейсу.
*   **Персистентність:** Вбудована підтримка зберігання даних на рівні користувача або загального стану.
*   **Автоматизація розробки:** Функція неявного перезавантаження сторінки при зміні коду (implicit reload),.

### 💎 Головна технічна цінність
Головна цінність полягає у **спрощенні веброзробки для Python-розробників**. NiceGUI пропонує ідеальний баланс: він не робить занадто багато "магії" зі станом, як Streamlit, але при цьому є високорівневим, на відміну від JustPy. Це робить його ідеальним для мікро-сервісів, дашбордів та проектів у робототехніці.

---

## 🚀 Частина 2: "Трансформація" (Інтеграція з Gemini LLM)

Інтеграція з **Gemini** (наприклад, через **GitHub Models**) перетворює NiceGUI з бібліотеки компонентів на **адаптивний інтелектуальний інтерфейс**.

### Як зміниться функціонал?
1.  **Генеративний UI:** Користувач описує задачу текстом, а Gemini через NiceGUI миттєво генерує потрібні віджети, графіки або форми введення даних.
2.  **Інтелектуальні дашборди:** Gemini може аналізувати дані, що відображаються у таблицях NiceGUI, і автоматично підсвічувати аномалії або пропонувати оптимальні типи графіків для візуалізації.
3.  **Природно-мовне керування:** Можливість замінити складні меню одним полем введення, де Gemini інтерпретує команди користувача та викликає відповідні Python-функції NiceGUI.

### Сценарій сервісу "Smart Python Assistant" (NiceGUI + Gemini + ID_{$})

Створення інтелектуального сервісу на вашому сайті:
1.  **Інтерфейс (NiceGUI):** На вашому сайті розгорнуто лаконічний інтерфейс із вікном чату та зоною відображення результатів.
2.  **Запит:** Користувач просить виконати складну обробку даних.
3.  **Інтерпретація (Gemini):** LLM аналізує запит і вирішує, які саме функції з ваших базових Python-скриптів `ID_{$}` потрібно викликати.
4.  **Виконання (ID_{$}):** Ваші скрипти проводять розрахунки або обробку файлів.
5.  **Візуалізація (NiceGUI):** Результати обробки автоматично рендеряться у NiceGUI у вигляді інтерактивних діаграм або 3D-моделей.
6.  **Деплой:** Використовуючи **GitHub Spark**, ви можете миттєво розгорнути цей додаток як готовий сервіс для кінцевих користувачів.

---

## 📋 План дій для Notion
| Крок | Дія | Результат |
| :--- | :--- | :--- |
| **1** | Встановлення: `pip install nicegui` | Готове середовище розробки |
| **2** | Підключення Gemini API | Додавання ШІ-логіки до `main.py` |
| **3** | Інтеграція скриптів `ID_{$}` | Зв'язок інтерфейсу з вашими алгоритмами |
| **4** | Налаштування Tailwind CSS | Кастомізація дизайну під ваш бренд |

---

### 💡 Резюме

**Суть:** **Створення веб-інтерфейсів виключно на Python**.

**AI-Роль:** **Побудова та розгортання інтелектуальних застосунків** (за допомогою GitHub Spark та Gemini для автоматизації взаємодії).
