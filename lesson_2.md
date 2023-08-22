# GitHub-Flavored Markdown

## Краткое руководство

Абзацы создаются при помощи пустой строки. Если вокруг текста сверху и снизу есть пустые строки, то текст превращается в абзац.

Чтобы сделать перенос строки вместо абзаца,  
нужно поставить два пробела в конце предыдущей строки.

### Списки

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

### Ссылки

### Картинки
