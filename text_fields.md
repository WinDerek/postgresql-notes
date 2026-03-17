# Text Fields in PostgreSQL

## Use `text` for Text Fields

In PostgreSQL, there are mainly three data types for characters:
- `varchar(n)`: variable length string with max length limit.
- `char(n)`: blank-padded fixed length string.
- `text`: string with no length limit. Max length takes place about 1GB storage.

While `character(n)` has performance advantages in some other database systems, there is no such advantage in PostgreSQL; in fact `character(n)` is usually the slowest of the three because of its additional storage costs. In most situations `text` or `character varying` should be used instead.

Reference: https://www.postgresql.org/docs/14/datatype-character.html

## Character Encoding

Character encoding defines a mapping between bytes and text. A modern and widely used character encoding is `UTF-8`. For `UTF-8`, a Chinese character occupies three bytes. It supports both simplified Chinese and traditional Chinese.

The length unit in PostgreSQL is character, not byte. The default encoding is `UTF-8`. You can check the encoding by `\l` in psql.
