## Tabs for configs on multiple resources

<Tabs
  defaultValue="models"
  values={[
    { label: 'Models', value: 'models', },
    { label: 'Sources', value:'sources', },
    { label: 'Seeds', value: 'seeds', },
    { label: 'Snapshots', value: 'snapshots', },
  ]
}>

<TabItem value="models">

<File name='models/<modelname>.sql'>

```sql

{{ config(

) }}

select ...


```

</File>

<File name='dbt_project.yml'>

```yml
models:
  [<resource-path>](resource-path):


```

</File>

</TabItem>

<TabItem value="sources">

<File name='dbt_project.yml'>

```yml
sources:
  [<resource-path>](resource-path):


```

</File>

</TabItem>

<TabItem value="seeds">

<File name='dbt_project.yml'>

```yml
seeds:
  [<resource-path>](resource-path):


```

</File>

</TabItem>

<TabItem value="snapshots">

<File name='snapshots/<filename>.sql'>

```sql
{% snapshot [snapshot_name](snapshot_name) %}

{{ config(
  
) }}

select ...

{% endsnapshot %}

```

</File>

<File name='dbt_project.yml'>

```yml
snapshots:
  [<resource-path>](resource-path):
    enabled: true | false

```

</File>

</TabItem>

</Tabs>
