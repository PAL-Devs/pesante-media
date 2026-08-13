# pesante-media

Images and video published on the social channels of **Pesante Analytics LLC**.

## Why this repository is public

It is public on purpose. Instagram does not accept file uploads through its
publishing API: it requires a **public URL** that Meta's servers fetch
anonymously. A private repository would return 404.

Everything stored here has already been published on Facebook or Instagram, so
nothing is disclosed that was not already public.

## Rules

**1. Only publish-ready media.** Images and video intended for social channels.
Never code, configuration, credentials, customer data, or screenshots containing
real figures. Git history is public and cannot be truly erased.

**2. File names follow `YYYY-MM-DD-slug.ext`**, lowercase, no accents or spaces.
The leading date keeps the folder in chronological order and makes each file
traceable to the post that uses it.

**3. Append only.** Never delete or rename a file that has been published. A
Facebook post may still reference that URL, and removing it breaks the image. If
something is wrong, upload a new file under a new name.

**4. Instagram accepts JPEG only.** PNG works for Facebook but fails on
Instagram.

## Layout

```
img/    one file per published post
```

## Uploading

Files are uploaded by an automated pipeline, not by hand. The pipeline validates
these rules before the upload, refuses to overwrite an existing file, and
verifies that the resulting URL is reachable anonymously before it is used.

---

Pesante Analytics LLC — https://www.pesanteanalytics.com
