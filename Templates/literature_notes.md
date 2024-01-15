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
> **Year**:: {{date | format("YYYY")}}
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
{% macro callout(a) -%}
{%- if a.type == "highlight" -%}
<b class="thickUnd" style="text-decoration-color: {{a.color}}">Quote</b>
> {{a.annotatedText}}

{%- endif -%}

{%- if a.type == "text" -%}
<b class="thickUnd" style="text-decoration-color: {{a.color}}">Note</b>
> {{a.annotatedText}}

{%- endif -%}

{%- if a.type  == "image" -%}
<b class="thickUnd" style="text-decoration-color: {{a.color}}">Rectangle</b>
> ![[{{a.imageRelativePath.replace("base_name/output_path", citekey)}}|65%]]

{%- endif -%}


{%- endmacro -%}

{% persist "annotations" %}
{% set newAnnotations = annotations | filterby("date", "dateafter", lastImportDate) %}
{% if newAnnotations.length > 0 %}

### Imported: {{importDate | format("YYYY-MM-DD hh:mm a")}}

{% for a in newAnnotations %}
{{callout(a)}}
{% endfor %}
{% endif %}
{% endpersist %}
