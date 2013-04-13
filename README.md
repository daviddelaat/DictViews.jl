DictViews.jl
============

Provides the immutable types `KeysView{K,V}` and `ValuesView{K,V}` for dynamic, low-overhead views into the entries (either the keys or the values) of a dictionary. The types implement the `start`, `done`, and `next` methods for iterating over the entries. They respectively inherit the `View{K}` and `View{V}` abstract type which implements the `eltype`, and `length` methods.
