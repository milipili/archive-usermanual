Embedder's Guide
================


Overview
--------

Nany can be easily embbeded in your C or C++ application.

Here is the famous "Hello world" from a simple C++ program:
```cpp
#include <nany/nany.h>
#include <cstdlib>


int main(int argc, char** argv)
{
    // create a nany context
    nycontext_t* ctx = nany_context_create();
    if (ctx == nullptr)
        return EXIT_FAILURE;

    const char* script = u8R" // our nany script to execute
        public func main: i32
        {
            console << "hello world from nany !";
        }";

    // add the script (with its unique identifier)
    nany_context_sources_add(ctx, "my_script", script);

    // compile and execute
    int exitcode = nany_run_main(ctx, argc, argv);
        
    // release the context
    nany_context_release(ctx);
    return exitcode;
}
```



Other simple examples
---------------------

### Compile and run all scripts from the command line

```cpp
#include <nany/nany.h>
#include <cstdlib>


int main(int argc, char** argv)
{
    if (argc <= 1)
        return EXIT_SUCCESS;
        
    // create a nany context
    nycontext_t* ctx = nany_context_create();
    if (ctx == nullptr)
        return EXIT_FAILURE;

    // add all input script filenames
    for (int i = 1; i < argc; ++i)
        nany_context_sources_add_from_file(ctx, argv[i]);

    // compile and execute
    int exitcode = nany_run_main(ctx, argc, argv);
        
    // release the context
    nany_context_release(ctx);
    return exitcode;
}
```