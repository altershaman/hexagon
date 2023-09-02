###### View angle :id:: {{va}}

---
{{#error}}
:warning: Объекта **{{va}}** не существует
{{/error}}

{{^error}}
# {{body.title}}
{{body.description}}

---
{{#modes_avail_show}}
###### Доступные моды: {{#modes_avail}}{{^active}}[{{title}}]{{/active}}{{#active}}[=={{title}}==]{{/active}}({{^active}}/entities/hexV/view?id={{va}}.{{id}} " Выбрать hexModes.{{id}}"{{/active}}{{#active}}/entities/hexV/view?id={{va}} "Отключить hexModes.{{id}}"{{/active}}){{^last}} | {{/last}}{{/modes_avail}}

{{/modes_avail_show}}

{{#modes_tree}}
{{#branch}}{{#active}}[=={{title}}==]{{/active}}{{^active}}[{{title}}]{{/active}}(/entities/hexV/view?id={{va}}.{{prefix}}.{{id}}){{^last}} | {{/last}}{{/branch}}

{{/modes_tree}}

{{#branch}}{{#active}}[=={{title}}==]{{/active}}{{^active}}[{{title}}]{{/active}}(/entities/hexV/view?id={{prefix}}.{{id}}){{^last}} | {{/last}}{{/branch}}

![](@entity/hexV/l1?{{patternParams}})

{{/error}}

