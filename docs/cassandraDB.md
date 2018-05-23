# Cassandra Schema #

## Creation Scripts ##

Create the name space:
`create keyspace api_victorsesma with replication = { 'class' : 'SimpleStrategy', 'replication_factor' : 1 };`
Create the table for the curriculum vitae
`create table api_victorsesma.curriculum_vitae(id timeuuid, start_date date, end_date date, name text, summary text, description text, show_order int, PRIMARY KEY(id));`
Insert some data:

```cql
INSERT INTO api_victorsesma.curriculum_vitae
(id, start_date,end_date,name,summary,description,show_order)
VALUES
(
    now(),
    '2016-06-05',
    '2018-05-14',
    'Full Stack Developer in SmarterClick.com',
    'PHP, JavaScript, CSS, HTML',
    'Full Stack Developer in SmarterClick.com. Building all the back-end and front-end internal systems.',
    1
);RIMARY KEY(id));
```