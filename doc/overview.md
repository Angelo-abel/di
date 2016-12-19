###Quick Start

* Get [boost/di.hpp](https://raw.githubusercontent.com/boost-experimental/di/cpp14/include/boost/di.hpp) header
```sh
wget https://raw.githubusercontent.com/boost-experimental/di/cpp14/include/boost/di.hpp
```

* Include the header and define `di` namespace alias
```cpp
#include "boost/di.hpp"
namespace di = boost::di;
```

* Compile with C++14 support
```sh
$CXX -std=c++14 ...
```

* To run tests
```sh
git clone https://github.com/boost-experimental/di && cd di && make
```

###Dependencies

* No external dependencies are required (neither STL nor Boost)

###Supported/Tested compilers

* [Clang-3.4+](https://travis-ci.org/boost-experimental/di)
* [GCC-5.2+](https://travis-ci.org/boost-experimental/di)
* [MSVC-2015+](https://ci.appveyor.com/project/krzysztof-jusiak/di)

###Configuration
| Macro                             | Description |
| --------------------------------- | ----------- |
| `BOOST_DI_VERSION`                | Current version of [Boost].DI (ex. 1'0'0) |
| `BOOST_DI_CFG`                    | Global configuration allows to customize provider and policies (See [Config](user_guide.md#di_config)) |
| `BOOST_DI_CFG_CTOR_LIMIT_SIZE`    | Limits number of allowed constructor parameters [0-10, default=10] (See [Injections](user_guide.md#injections)) |
| `BOOST_DI_CFG_DIAGNOSTICS_LEVEL`  | Gives more information with error messages (See [Error messages](#error-messages)) |
| `BOOST_DI_NAMESPACE_BEGIN`        | `namespace boost { namespace di { inline namespace v_1_0_0 {` |
| `BOOST_DI_NAMESPACE_END`          | `}}}` |

###Exception Safety

* [Boost].DI is not using exceptions internally and therefore might be compiled with `-fno-exceptions`.
* Check [User Guide](user_guide.md) to verify which API's are marked `noexcept`.

###Thread Safety

* [Boost].DI is thread safe.

###Error Messages

* [Boost].DI is designed to give great diagnostic errors. The examples below will show you the actual error messages for different scenarios. Check [`Concepts`](user_guide.md#concepts) to check it out.

###Performance

* [Boost].DI has none run-time overhead and compiles faster than Java's DI frameworks. Check [`Benchmarks`](benchmark.md) to see more.

---

[Bindings]: user_guide.md#bindings
[Scopes]: user_guide.md#scopes
[Providers]: user_guide.md#providers
[Policies]: user_guide.md#policies
[Config]: user_guide.md#di_config
[di::inject]: #di_inject
[di::ctor_traits]: #di_ctor_traits
[BOOST_DI_INJECT]: #BOOST_DI_INJECT
[BOOST_DI_INJECT_TRAITS]: #BOOST_DI_INJECT_TRAITS