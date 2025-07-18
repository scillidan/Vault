What is the difference between lsp `pyright`, `pylsp`?

```md
In the context of Neovim and other editors that support the Language Server Protocol (LSP), both `pyright` and `pylsp` serve as language servers for Python, but they are built on different foundations and have different features. Here's a comparison of the two:

### 1. Pyright
- **Purpose**: Pyright is a static type checker and language server for Python developed by Microsoft, focusing on type checking and providing fast, accurate IntelliSense.
- **Features**:
  - **Type Checking**: Pyright performs static type checking using Python's type hints. It can catch type errors before runtime, making it particularly useful for developers using type annotations.
  - **Performance**: It's known for its high performance and low memory usage compared to some other Python language servers.
  - **Code Intelligence**: It provides autocompletion, function signatures, and code navigation (go to definition, find references).
  - **Configuration**: Pyright can be configured through a `pyrightconfig.json` file to specify how type checking should behave.

### 2. Pylsp (Python Language Server)
- **Purpose**: Pylsp, formerly known as `python-language-server`, is an LSP server for Python that implements a variety of features including linting, debugging, and completion.
- **Features**:
  - **Multiple Linting Tools**: Pylsp can be configured to work with various linting tools like Pylint, Flake8, and others, offering flexibility in linting choices.
  - **Extensibility**: Pylsp supports plugins, allowing users to extend its functionality with additional features and tools.
  - **Type Checking and Introspection**: Pylsp includes features for code introspection, autocompletion, and basic type checking (although it may not be as robust as Pyright's type checking).
  - **Integration with other tools**: You can integrate other Python tools directly into Pylsp, giving you the option to unify several development tools into one server.

### Summary of Differences:
- **Focus**:
  - **Pyright**: Primarily focused on type checking and performance.
  - **Pylsp**: A more general-purpose language server that can integrate with multiple linting tools and plugins for different features.

- **Performance**:
  - **Pyright**: Generally faster and optimized for static analysis.
  - **Pylsp**: Performance can vary depending on the plugins and linting tools being used.

- **Type Checking**:
  - **Pyright**: Strong emphasis on type checking with detailed analysis.
  - **Pylsp**: Basic type checking capabilities, but less robust compared to Pyright.

- **Extensibility**:
  - **Pyright**: Limited configuration options, focused on type checking.
  - **Pylsp**: Highly extensible through plugins, allowing for broader features.

### Conclusion
Choosing between `pyright` and `pylsp` largely depends on your development needs. If your focus is on leveraging type hints and having a speedy experience with strong type-checking capabilities, `pyright` is a great choice. On the other hand, if you want flexibility with linting options and extensibility through plugins, then `pylsp` may be more suitable.
```

```md
在 Neovim 和其他支持语言服务器协议 (LSP) 的编辑器中，`pyright` 和 `pylsp` 都作为 Python 的语言服务器，但它们建立在不同的基础上，并具有不同的功能。以下是两者的比较：

### 1. Pyright
- **目的**：Pyright 是由 Microsoft 开发的 Python 静态类型检查器和语言服务器，专注于类型检查和提供快速、准确的 IntelliSense。
- **特点**：
  - **类型检查**：Pyright 使用 Python 的类型提示进行静态类型检查。它可以在运行时之前捕获类型错误，非常适合使用类型注解的开发人员。
  - **性能**：与其他一些 Python 语言服务器相比，Pyright 以其高性能和低内存使用而闻名。
  - **代码智能**：它提供自动补全、函数签名和代码导航（跳转到定义、查找引用）。
  - **配置**：可以通过 `pyrightconfig.json` 文件配置 Pyright，以指定类型检查的行为。

### 2. Pylsp (Python 语言服务器)
- **目的**：Pylsp，前称为 `python-language-server`，是一个为 Python 提供的 LSP 服务器，实施多种功能，包括检验、调试和补全。
- **特点**：
  - **多个检验工具**：Pylsp 可以配置为使用 Pylint、Flake8 等多种检查工具，提供检验选择的灵活性。
  - **可扩展性**：Pylsp 支持插件，允许用户通过额外的功能和工具扩展其功能。
  - **类型检查和代码 introspection**：Pylsp 包含代码 introspection、自动补全和基本类型检查功能（尽管可能不如 Pyright 的类型检查强大）。
  - **与其他工具的集成**：您可以直接将其他 Python 工具集成到 Pylsp 中，使您有机会将多个开发工具统一到一个服务器中。

### 差异总结：
- **关注点**：
  - **Pyright**：主要专注于类型检查和性能。
  - **Pylsp**：更通用的语言服务器，可以与多个检验工具和插件集成，以支持不同的功能。

- **性能**：
  - **Pyright**：通常更快，并针对静态分析进行了优化。
  - **Pylsp**：性能可能因所使用的插件和检查工具而异。

- **类型检查**：
  - **Pyright**：对类型检查有强烈的关注，提供详细的分析。
  - **Pylsp**：基本的类型检查能力，但与 Pyright 的类型检查相比不够强大。

- **可扩展性**：
  - **Pyright**：配置选项有限，专注于类型检查。
  - **Pylsp**：通过插件高度可扩展，允许更广泛的功能。

### 结论
在 `pyright` 和 `pylsp` 之间的选择在很大程度上取决于您的开发需求。如果您的重点是利用类型提示并拥有强大的类型检查能力，同时追求快速的体验，`pyright` 是一个不错的选择。另一方面，如果您希望在检验选项和通过插件的可扩展性方面获得灵活性，那么 `pylsp` 可能更合适。
```