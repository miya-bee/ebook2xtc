# Optional GUI dependency

The desktop interface uses the optional `PySide6` extra. Qt for Python is offered under LGPLv3/GPLv3 and commercial terms; some Qt modules use GPL-only terms. The current app uses the Qt Widgets API. Before distributing packaged builds, review the licenses of the exact PySide6/Qt modules and bundled components with the intended distribution model.

- [Qt for Python licensing](https://doc.qt.io/qtforpython-6/)
- [Qt licensing](https://doc.qt.io/qt-6/licensing.html)

The optional GUI dependency is PySide6-Essentials, which includes QtWidgets; WebEngine and other add-on wheels are not needed by this interface. See [PySide6 Essentials package details](https://pypi.org/project/PySide6-Essentials/).

## LZ4 compression

The `lz4` runtime dependency uses the Python bindings distributed by `python-lz4`. The bindings are covered by the BSD 3-Clause License; the embedded LZ4 implementation uses the BSD 2-Clause License. A packaged build must include both applicable license notices. The dependency is used to produce XTCZ block data.

- [python-lz4 license and project](https://github.com/python-lz4/python-lz4)
- [LZ4 library license](https://github.com/lz4/lz4/blob/dev/LICENSE)
