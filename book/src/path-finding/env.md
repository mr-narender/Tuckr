# Path from environment variable

Certain programs depend on environment variables to know where to put things in.
Sometimes you might also just want to script the deployment of your dotfiles. For both cases you can expand your path through an enviroment variables.

You can tell Tuckr to expand an environment variable by using `%`. 

For example if you set an environment variable `PROGRAM_PATH` to `/home/user/Documents/program` and you have a dotfile with this file structure:
```
program
└── %PROGRAM_PATH
    └── config.txt
```
Tuckr will expand it to `/home/user/Documents/program/config.txt`.

## Default paths
Tuckr sets a few default environment variables when it runs that are useful to prevent duplicated config file for each 
conditional target.

- [`TUCKR_USER_CONFIG`](https://docs.rs/dirs/latest/dirs/fn.config_dir.html)
- [`TUCKR_USER_DOWNLOADS`](https://docs.rs/dirs/latest/dirs/fn.download_dir.html)
- [`TUCKR_USER_DOCUMENTS`](https://docs.rs/dirs/latest/dirs/fn.document_dir.html)
- [`TUCKR_USER_DESKTOP`](https://docs.rs/dirs/latest/dirs/fn.desktop_dir.html) 
- [`TUCKR_USER_DATA`](https://docs.rs/dirs/latest/dirs/fn.data_dir.html)
- [`TUCKR_USER_PICTURES`](https://docs.rs/dirs/latest/dirs/fn.picture_dir.html)
