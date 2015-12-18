# vim-gtest

**Vim plugin to run *GoogleTest* using https://github.com/benmills/vimux**

<img src="http://files.pezzato.net/github/vim-gtest.gif" />

## Features

### Select gtest command

```
:GTestCmd path/to/test/executable
```

### Select tests by name

You can select test cases and test name, with autocompletion.

```
:GTestCase MyTestCase
:GTestName MyTestName
```

### Run selected tests

```
:GTestRun
```

### Find tests

Go to the prev/next test in the current buffer.

```
:GTestPrev
:GTestNext
```

### Run test under cursor

```
:GTestRunUnderCursor
```

## Shortcuts

You can map these commands to your favorite shortcuts:

```
nnoremap <leader>tt :GTestRun<CR>
nnoremap <leader>tu :GTestRunUnderCursor<CR>
nnoremap <leader>tc :GTestCase<space>
nnoremap <leader>tn :GTestName<space>
```

## Development

### Contributing

If you'd like to help, check out the
[issues](https://github.com/alepez/vim-gtest/issues). I'd greatly appreciate
any contribution you make.

### Testing

To test this plugin you need to test it with a testable project. `googletest`
can test itself. Yeah, like a ship-shipping ship shipping shipping ships.

This will download and compile google test and its unit tests:

```
./test/make_test
```

Now from `vim`, just call from command line `:GTestCmd ./test/launch`.

After editing this plugin, just `:source %` and try something. Samples unit
tests can be found in `test/googletest/googletest/samples` directory.
