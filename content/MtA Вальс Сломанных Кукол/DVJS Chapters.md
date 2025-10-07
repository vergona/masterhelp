---
aliases:
tags:
vaultpart: кампейн магов
topics:
  - "!Шаблон"
---
## Вводная
```dvjs
const currentNoteName = dv.current().file.name;

const pages = dv.pages("#1-Сторителл/хроника/глава").where(page => page.file.name != null)
  .sort(page => page.file.name);
dv.header(4, `Количество заметок в : ${pages.length}`);

for (let page of pages) {

  const file = app.vault.getAbstractFileByPath(page.file.path);
  const headings = app.metadataCache.getFileCache(file).headings;
  var index = headings.findIndex(h => h.heading === 'Вводная');

  if (index !== -1) {
    const noteContent = await dv.io.load(page.file.path);
    var start = headings[index].position.end.offset;
    var end = headings[index + 1]?.position.start.offset;
    const headingContent = noteContent.substring(start, end);
    if (headingContent.replace(/[\s\-]/g,'').length) {
     dv.header(2, page.file.link);
     dv.paragraph(headingContent);
    }
  }
}
```
### Итоги
```dvjs
const currentNoteName = dv.current().file.name;

const pages = dv.pages("#1-Сторителл/хроника/глава").where(page => page.file.name != null)
  .sort(page => page.file.name);
dv.header(4, `Количество заметок в : ${pages.length}`);

for (let page of pages) {

  const file = app.vault.getAbstractFileByPath(page.file.path);
  const headings = app.metadataCache.getFileCache(file).headings;
  var index = headings.findIndex(h => h.heading === 'Итоги');

  if (index !== -1) {
    const noteContent = await dv.io.load(page.file.path);
    var start = headings[index].position.end.offset;
    var end = headings[index + 1]?.position.start.offset;
    const headingContent = noteContent.substring(start, end);
    if (headingContent.replace(/[\s\-]/g,'').length) {
     dv.header(2, page.file.link);
     dv.paragraph(headingContent);
    }
  }
}
```
### Занятные личности
```dvjs
const currentNoteName = dv.current().file.name;

const pages = dv.pages("#1-Сторителл/хроника/глава").where(page => page.file.name != null)
  .sort(page => page.file.name);
dv.header(4, `Количество заметок в : ${pages.length}`);

for (let page of pages) {

  const file = app.vault.getAbstractFileByPath(page.file.path);
  const headings = app.metadataCache.getFileCache(file).headings;
  var index = headings.findIndex(h => h.heading === 'Занятные личности');

  if (index !== -1) {
    const noteContent = await dv.io.load(page.file.path);
    var start = headings[index].position.end.offset;
    var end = headings[index + 1]?.position.start.offset;
    const headingContent = noteContent.substring(start, end);
    if (headingContent.replace(/[\s\-]/g,'').length) {
     dv.header(2, page.file.link);
     dv.paragraph(headingContent);
    }
  }
}
```
