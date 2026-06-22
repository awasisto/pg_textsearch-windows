# [pg_textsearch](https://github.com/timescale/pg_textsearch) binary compile, Microsoft Windows x64, PostgreSQL

<b>***** Unofficial release *****</b>

---

See [releases](https://github.com/awasisto/pg_textsearch-windows/releases) for available version

**Installation**

1. Stop PostgreSQL using `services.msc`

2. Extract the zip file to your PostgreSQL installation folder.
   On the overwrite dialog option, choose "Yes to all"

3. Edit `postgresql.conf` in your PostgreSQL data folder:

   ```
   shared_preload_libraries = 'pg_textsearch'
   ```

4. Start PostgreSQL service

5. Run this query to load the extension: 

   ```
   CREATE EXTENSION pg_textsearch;
   ```

6. Run this query to check if the extension is enabled:

   ```
   SELECT extname, extrelocatable, extversion FROM pg_extension where extname='pg_textsearch';
   ```
