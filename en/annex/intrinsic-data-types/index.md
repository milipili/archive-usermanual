Intrinsic data types
====================



Native intrinsic data types
---------------------------

 * signed integer type with width of exactly 8, 16, 32 and 64 bits:
   - `__i8`: -127 to 127
   - `__i16`: -32,768 to 32,767
   - `__i32`: -2,147,483,648 to 2,147,483,647
   - `__i64`: -(2<sup>63</sup>-1) to 2<sup>63</sup>-1

 * unsigned integer type with width of exactly 8, 16, 32 and 64 bits:  
   - `__u8`: 0 to 255
   - `__u16`: 0 to 65,535
   - `__u32`: 0 to 4,294,967,295
   - `__u64`: 0 to 2<sup>64</sup>

 * floating point data types:
   - `__f32`: +/- 3.4e +/- 38 (~7 digits)
   - `__f64`: +/- 1.7e +/- 308 (~15 digits)
 
 * Pointer:
   - `__pointer`: equivalent to `void*`