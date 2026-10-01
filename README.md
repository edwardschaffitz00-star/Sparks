# Sparks admin — finish

The live `/admin` UI is already built. It stays blank until:

1. You run `supabase/004_admin.sql` in the Supabase SQL editor for project `kiaihjyreftwsqycyrpt`.
2. You mark yourself admin:

```sql
update public.profiles
set is_admin = true
where id = '<your auth.users uuid>';
```

3. You log in at `/login?next=/admin`.

That installs `admin_list_users` and `admin_set_ban` (the “chunk 4” the page looks for), plus admin RLS so Users / Messages / Reports actually load.

Also added: `dm-thread.html` (admin “Thread” links were 404).

Redeploy this folder to the same Vercel project if you want the thread page live.
