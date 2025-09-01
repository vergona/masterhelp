---
{}
---
Подсистемы
- [[Социальный бой]]
- [[Конспект по правилам боя]]
	- [[Правила боевых групп]]
- [[Exalted Solar Road/Бестиарий/Бестиарий]]
- [[Хоумрул - Венчуры из ExEss]]

Банг
[[Exalted Solar Road/Банг Шишигами/Банг Шишигами]]
- [[Exalted Solar Road/Банг Шишигами/🔆Чарник - Рассветный Банг]]
- [[Exalted Solar Road/Банг Шишигами/Действия у Банга]]

Предыстория
[[Exalted Solar Road/Свиток героев/SoS Вся история Лиловой Жемчужины]] - закулисное
[[Exalted Solar Road/Свиток героев/SoS Лиловая Жемчужина Безмятежности]]

История в Калине
[[Exalted Solar Road/01. Once there was a maiden/01. Once there was a maiden]]
[[Exalted Solar Road/Черновики]]

История в Пневме
[[Exalted Solar Road/⚙Autochtony/DpSk once there was a maiden.zip]] - 8 Пневма
[[Exalted Solar Road/мастерская будущего/02. заметки по Пневме]]

Сфинкс Черного Кварца




# ф 
= = 
> [!info] Подсчет свойств в текущей папке
> ```dvjs
> const folderPath = dv.page("").file.path.split('/').slice(0, -1).join('/');
> // автоматически указывает путь папке текущей заметки
> const notes = dv.pages(`"${folderPath}"`).where(p => p.file.name != null);
> 
> dv.header(4, `Количество заметок в папке "${folderPath}": ${notes.length}`);
> 
> // Словарь для хранения свойств и количества их появлений
> const propertiesCount = {};
> 
> // Получение свойств из заметок и подсчет их количеств
> for (const note of notes) {
>     // Используйте Object.keys чтобы получить все ключи (свойства)
>     const properties = Object.keys(note);
>     
>     for (const prop of properties) {
>         // Пропускаем стандартные свойства файла
>         if (prop !== 'file' && prop !== 'file.name' && prop !== 'file.path') {
>             propertiesCount[prop] = (propertiesCount[prop] || 0) + 1;
>         }
>     }
> }
> 
> // Сортировка свойств по количеству заметок
>const sortedProperties = Object.entries(propertiesCount).sort((a, b) => b[1] - a[1]);
> 
> // Вывод списка свойств и количества заметок
> const table = dv.table(["Свойство ", "Количество заметок"], sortedProperties);
> 
> ```
