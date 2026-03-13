
- Why Postgres?
  1. Opensource and free
  2. Sticks with SQL Query standards
  3. Extenseble, offers lot of feature
  4. Reliable and scalable
  5. better JSON support indexing and query capabilities

### Data types
```SQL
  CREATE TABLE data_types_demo(
    id SERIAL PRIMARY KEY,
    some_smallint SMALLINT,
    some_integer INTEGER,
    some_bigint BIGINT,
    some_decimal DECIMAL(10, 2), -- 10 -> Number of digits including right side of the decimal point, 2 -> number of digits after decimal point
    some_numeric NUMERIC(10, 2),
    some_real REAL,

    some_char CHAR(10), -- "ab" = "_______ab"
    some_varchar VARCHAR(255), -- recommended by VARCHAR(255)
    some_text TEXT, -- Recommended by postgres, misconcept: 

    some_boolean BOOLEAN,
    some_date DATE,
    some_time TIME,
    some_timestamp TIMESTAMP,
    some_timestampz TIMESTAMPZ,
    some_interval INTERVAL,
    some_uuid UUID,
    some_json JSON,
    some_json JSONB, -- PERFORMANT postgres 
    some_array INTEGER[],
    some_inet INET,
    some_macaddr MACADDR,
    some_point POINT,
    some_xml XML
  )
```
```SQL
INSERT INTO (

)

VALUES (

)

```
### Project management platform

  