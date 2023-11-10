# lldb-vscode

lldb-vscode is not available anymore and got repalced with `lldb-dap`. The
reason is from the `llvm-project` built that we did in
`./B01_building_against_custom_lldb.md`.

1. I have changed the lldb adapter for debugging the `C/C++` codes in my nvim.
2. I removed the old built of the `llvm-project` called
   `~/.cpp_debug_adapter/` and repalced with the one by `2023-11-11 00:22`
   called `~/buildspace/` based on the steps that we created for building the
   `llvm-project` on our macOS machine.

# Reference

- [read more here](https://www.reddit.com/r/LLVM/comments/17s5ywl/lldbvscode_renamed_to_lldbdap_in_llvmproject/)
- [here](https://discourse.llvm.org/t/rfc-rename-lldb-vscode-to-lldb-dap/74075)
