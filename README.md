DictViews.jl
============

# Introduction

DictView.jl provides the types `KeysView` and `ValuesView` for dynamic and low-overhead views into the entries (either the keys or the values) of a dictionary. The types implement the `start`, `done`, and `next` methods for iterating over the entries. They further implement the `show`, `eltype`, and `length` methods.

# Example

```jlcon
julia> using DictViews

julia> d = ["grass" => "green", "sky" => "blue"]
["sky"=>"blue","grass"=>"green"]

julia> colors() = ValuesView(d)
# method added to generic function colors

julia> for color in colors(); println(color); end
blue
green
        
julia> d["sky"] = "black"
"black"

julia> colors()
ValuesView{ASCIIString}("black","green")
```
