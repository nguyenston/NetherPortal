---
category: literaturenote
tags: {% if allTags %}{{allTags}}{% endif %}
citekey: "{{citekey}}"
status: unread
dateread:
---
> [!Cite]
> {{bibliography}}

>[!Synth]
>**Contribution**:: {% persist "contr" %} {% endpersist %}
>
>**Related**:: {% for relation in relations | selectattr("citekey") %} [[@{{relation.citekey}}]]{% if not loop.last %}, {% endif %} {% endfor %}

>[!md]
{% for type, creators in creators | groupby("creatorType") -%}
{%- for creator in creators -%}
> **{{"First" if loop.first}}{{type | capitalize}}**::
{%- if creator.name %} {{creator.name}}
{%- else %} {{creator.lastName}}, {{creator.firstName}}
{%- endif %}
{% endfor %}~
{%- endfor %}
> **Title**:: {{title}}
> **Year**:: {% if date -%}{{date | format("YYYY")}}{%- else -%}N/A{%- endif %}
> **Citekey**:: {{citekey}} {%- if itemType %}
> **itemType**:: {{itemType}}{%- endif %}{%- if itemType == "journalArticle" %}
> **Journal**:: *{{publicationTitle}}* {%- endif %}{%- if volume %}
> **Volume**:: {{volume}} {%- endif %}{%- if issue %}
> **Issue**:: {{issue}} {%- endif %}{%- if itemType == "bookSection" %}
> **Book**:: {{publicationTitle}} {%- endif %}{%- if publisher %}
> **Publisher**:: {{publisher}} {%- endif %}{%- if pages %}
> **Pages**:: {{pages}} {%- endif %}{%- if DOI %}
> **DOI**:: {{DOI}} {%- endif %}{%- if ISBN %}
> **ISBN**:: {{ISBN}} {%- endif %}

> [!LINK]
> {%- for attachment in attachments | filterby("path", "endswith", ".pdf") %}
> [{{attachment.title}}](file://{{attachment.path | replace(" ", "%20")}}) {%- endfor %}

> [!Abstract]
> {%- if abstractNote %}
> {{abstractNote}}
> {%- endif %}

# Notes
> {%- if markdownNotes %}
>{{markdownNotes}}{%- endif %}

# Annotations
{% macro callout(a, label) -%}
{%- if a.type == "highlight" -%}
<b class="thickUnd" style="text-decoration-color: {{a.color}}">{{label}}</b>
> {{a.annotatedText}}

{%- endif -%}

{%- if a.type == "note" -%}
<b class="thickUnd" style="text-decoration-color: {{a.color}}">Note</b>
> {{a.comment}}

{%- endif -%}

{%- if a.type  == "image" -%}
<b class="thickUnd" style="text-decoration-color: {{a.color}}">{{label}}</b>
> ![[{{a.imageRelativePath.replace("base_name/output_path", citekey)}}|65%]]

{%- endif -%}


{%- endmacro -%}

{% for a in annotations -%}

{%- if a.colorCategory == "Yellow" -%}
{{callout(a, "Quote")}}

{% endif -%}
{%- if a.colorCategory == "Orange" -%}
{{callout(a, "Procedure")}}

{% endif -%}
{%- if a.colorCategory == "Blue" -%}
{{callout(a, "Thesis")}}

{% endif %}
{%- if a.colorCategory == "Red" -%}
{{callout(a, "Definitions")}}

{% endif %}
{%- if a.colorCategory == "Green" -%}
{{callout(a, "Follow up read")}}

{% endif -%}
{%- endfor -%}
