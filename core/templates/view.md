{{#error}}
###### View

---
:warning: {{.}}
{{/error}}

{{^error}}
###### View :id: {{vId}}

---
# {{body.title}}
{{body.description}}

{{#modes}}
###### {{#row}}{{#.}}{{#selected}}=={{title}}== | {{/selected}}{{^selected}}[{{title}}](/entities/hexV/view?id={{vId}}&mode={{chain}}) | {{/selected}}{{/.}}{{/row}}

{{/modes}}


![](@entity/hexV/pattern_graph?data={{resView.pattern}})

---

![](@entity/hexV/landscape_graph?data={{resView.landscape}})



    ###### View angle :id:: {{va}}

    ---

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

