# WASI Filesystem API

## `open`
```wai
resource open {
    /// Read bytes from this open handle.
    read: function(fd: handle open, buffer: pull-buffer) -> expected<size, error>

    /// Write bytes to this open handle.
    write: function(fd: handle open, buffer: push-buffer) -> expected<size, error>

    /// Open a new file.
    open: function(fd: handle open, path: string, flags: open-flags, mode: open-mode) -> expected<handle open, error>
}
```
