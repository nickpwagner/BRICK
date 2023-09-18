___
# {{title}}

**Links**: [**Zotero**]({{desktopURI}}) | [**DOI**](https://doi.org/{{DOI}}) | {% for attachment in attachments | filterby("path", "endswith", ".pdf") %}[**PDF**](file:///{{attachment.path | replace(" ", "%20")}}){%- endfor %}
Status: #paper
**Tags**: {% for t in tags %} [[{{t.tag}}]] {% if not loop.last %}, {% endif %}{% endfor %}

> [!abstract]-
> {% if abstractNote %}
> {{abstractNote|replace("\n"," ")|striptags(true)|replace("Objectives", "**Objectives**")|replace("Background", "**Background**")|replace("Methodology", "**Methodology**")|replace("Results","**Results**")|replace("Conclusion","**Conclusion**")}}
> {% endif %}
> [!quote]- Citations
> 
> ```query
> content: "@{{citekey}}" -file:@{{citekey}}
> ```

> [!quote]- Citations
> 
> ```query
> content: "@{{citekey}}" -file:@{{citekey}}
> ```

**Authors**: {% for a in creators %} {% if loop.first %}{{a.firstName}} {{a.lastName}} et al. {% endif %}{% endfor %}
**Revision Date**: {{date | format("YYYY-MM-DD")}}
**Import Date**: {{importDate | format("YYYY-MM-DD")}}
___

{% macro heading(color) -%}
{%- if color == ("#2ea8e5") -%}
📓 Definition
{%- endif -%}
{%- if color == "#ffd400" -%}  
📑 Marking
{%- endif -%}
{%- if color == "#a28ae5" -%}
✨ Hypothesis
{%- endif -%}
{%- if color == "#5fb236" -%}
➕ Strength
{%- endif -%}
{%- if color == "#ff6666" -%}
➖ Weakness
{%- endif -%}
{%- if color == "#aaaaaa" -%}
❔ Question
{%- endif -%}
{%- endmacro -%}
{% macro calloutCharacter(color) -%}
{%- if color == ("#2ea8e5") -%}
📓
{%- endif -%}
{%- if color == "#ffd400" -%}
📑
{%- endif -%}
{%- if color == "#a28ae5" -%}
✨
{%- endif -%}
{%- if color == "#5fb236" -%}
➕
{%- endif -%}
{%- if color == "#ff6666" -%}
➖
{%- endif -%}
{%- if color == "#aaaaaa" -%}
❔
{%- endif -%}
{%- endmacro -%}

{% persist "annotations" %}
{% set annotations = annotations | filterby("date", "dateafter", lastImportDate) -%}
{% if annotations.length > 0 %}
{% for color, annotations in annotations | groupby("color") -%}
# {{heading(color)}} %% fold %%
{% for annotation in annotations -%}
{%- if annotation.imageRelativePath %}

![[{{annotation.imageRelativePath}}]][(p. {{annotation.pageLabel}})](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.pageLabel}}&annotation={{annotation.id}}) {% if annotation.hashTags %}
{{annotation.hashTags}}{% endif %}{%- if (annotation.comment or []).indexOf("todo ") !== -1 %}
- [ ] **{{annotation.comment | replace("todo ", "")}}**{% else %}
{{annotation.comment}}{%- endif -%}

{% elif (annotation.comment or []).indexOf("todo ") !== -1 %}
- [ ] **{{annotation.comment | replace("todo ", "")}}**{% if not annotation.annotatedText %} [(p. {{annotation.pageLabel}})](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.pageLabel}}&annotation={{annotation.id}}){% else %}
	- {{calloutCharacter(annotation.color)}} {{annotation.annotatedText | nl2br}} [(p. {{annotation.pageLabel}})](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.pageLabel}}&annotation={{annotation.id}}) {% if annotation.hashTags %}{{annotation.hashTags}}{% endif -%}{% endif -%}

{% elif annotation.comment %}
- ** {{annotation.comment}}**{% if not annotation.annotatedText %} [(p. {{annotation.pageLabel}})](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.pageLabel}}&annotation={{annotation.id}}){% else %}
	- {{calloutCharacter(annotation.color)}} {{annotation.annotatedText | nl2br}} [(p. {{annotation.pageLabel}})](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.pageLabel}}&annotation={{annotation.id}}) {% if annotation.hashTags %}{{annotation.hashTags}}{% endif -%}{% endif %}

{%- elif annotation.annotatedText %}
- {{calloutCharacter(annotation.color)}} {{annotation.annotatedText | nl2br}} [(p. {{annotation.pageLabel}})](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.pageLabel}}&annotation={{annotation.id}}) {% if annotation.hashTags %}{{annotation.hashTags}}{% endif %}

{%- endif -%}{%- endfor %}
{% endfor -%}
{% endif %}
{% endpersist %}