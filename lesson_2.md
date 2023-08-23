# GitHub-Flavored Markdown

## Краткое руководство

Абзацы создаются при помощи пустой строки. Если вокруг текста сверху и снизу есть пустые строки, то текст превращается в абзац.

Чтобы сделать перенос строки вместо абзаца,  
нужно поставить два пробела в конце предыдущей строки.

### Списки

Для разметки неупорядоченных списков можно использовать или `*`, или `-`, или `+`:

- элемент 1
- элемент 2
- элемент ...

Вложенные пункты создаются четырьмя пробелами перед маркером пункта:

- элемент 1
- элемент 2
  - вложенный элемент 2.1
  - вложенный элемент 2.2
- элемент ...

Упорядоченный список:

1. элемент 1
2. элемент 2
   1. вложенный
   2. вложенный
3. элемент 3
4. Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse id sem consectetuer libero luctus adipiscing.

На самом деле не важно как в коде пронумерованы пункты, главное, чтобы перед элементом списка стояла цифра (любая) с точкой. Можно сделать и так:

0. элемент 1
1. элемент 2
2. элемент 3
3. элемент 4

Список с абзацами:

- Раз абзац. Lorem ipsum dolor sit amet, consectetur adipisicing elit.

- Два абзац. Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse id sem consectetuer libero luctus adipiscing.

- Три абзац. Ea, quis, alias nobis porro quos laborum minus sed fuga odio dolore natus quas cum enim necessitatibus magni provident non saepe sequi?

  Четыре абзац (Четыре пробела в начале или один tab).

### Исходный код

В чистом Маркдауне блоки кода отбиваются 4 пробелами в начале каждой строки.

Но в GitHub-Flavored Markdown (сокращенно GFM) есть более удобный способ: ставим по три апострофа (на букве Ё) до и после кода. Также можно указать язык исходного кода.

```python
def changing_direction(nums):
    direction_changes = 0
    current_direction = 0

    for i in range(1, len(nums)):
        if nums[i] > nums[i - 1]:
            new_direction = 1
        elif nums[i] < nums[i - 1]:
            new_direction = -1
        else:
            new_direction = 0

        if new_direction != 0 and new_direction != current_direction:
            direction_changes += 1
            current_direction = new_direction

    return direction_changes
```

### Инлайн код

Описание:
Для вставки кода внутри предложений нужно заключать этот код в апострофы (на букве Ё). Пример: `<html class="ie no-js">`.

Если внутри кода есть апостроф, то код надо обрамить двойными апострофами: `` There is a literal backtick (`) here. ``

### Ссылки

Это встроенная [ссылка с title элементом](http://example.com/link "Я ссылка"). Это — [без title](http://example.com/link).

А вот [пример][1] [нескольких][2] [ссылок][id] с разметкой как у сносок. Прокатит и [короткая запись][] без указания id.

[1]: http://example.com/ "Optional Title Here"
[2]: http://example.com/some
[id]: http://example.com/links "Optional Title Here"
[короткая запись]: http://example.com/short

Вынос длинных урлов из предложения способствует сохранению читабельности исходника. Сноски можно располагать в любом месте документа.

### Картинки
