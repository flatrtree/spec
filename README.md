# Flatrtree

Flatrtree is a serialization format and set of libraries for reading and writing R-trees. It's directly inspired by [Flatbush](https://github.com/mourner/flatbush) and [FlatGeobuf](https://github.com/flatgeobuf/flatgeobuf), and aims to make tiny, portable R-trees accessible in new contexts.

- Store R-trees to disk and transport them over a network.
- Build R-trees in one language and query them in another.
- Query R-trees before reading the data they index.

## Status

This is not a proper specification yet. It's just a proto file shared by a couple of repos. I'd like to have something more formal in the future but don't have a timeline. The protocol buffer format and the current implementations should provide enough detail if you want to implement it yourself in code.

## Contributing

This project is new as of January 2023 and subject to change as (hopefully) more people use it. Please open an issue and explain your use case if you want to use Flatrtree in a language that isn't offered yet. Ports to other languages are encouraged and appreciated.

## Ideas

A collection of half-baked ideas:

- Target this format from non-static R-tree implementations.
- Create serializable prepared geometries that include the underlying R-tree.
- Exclude item rects. Searches return "fuzzy" results based on parent node intersection. Caller tests items for intersection.
- Support 3-D.
