## Development

Prerequisites:

```
$ ruby -v
ruby 2.7.3p183 (2021-04-05 revision 6847ee089d) [x86_64-linux]
$ gem install jekyll jekyll-paginate
```

Or if you use VSCode you can open in a container and get Ruby and Jekyll automatically.

Then:

```
$ jekyll serve --watch --future
```

Where `--watch` watches the file system for chamges and re-renders (you have to refresh the browser), and `--future` includes future-dated blog entries, so you can test them before you publish.

.
