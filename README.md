# Elixir Immutable List Modification
This example demonstrates a common mistake in Elixir: attempting to modify an immutable list in place using `List.delete` within an `Enum.each` loop.  Because lists in Elixir are immutable, the `List.delete` function creates a *new* list without modifying the original. The `IO.inspect` function at the end will show that the original list has not been changed.

The solution shows the proper way to handle this, using `Enum.filter` to create a new list excluding the element you want to remove.