# crawl

A fast web crawler based on libcurl and libxml2 that can spawn hundreds of concurrent connections.

Features:

- Find broken links given a starting url
- Build a graph of the network topology and output to the GraphViz dot format

## Developing

```bash
mkdir build && cd build
cmake ..
make
```
