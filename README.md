# 日本語
## 呼び出し方
``` C++
DLL<返り値, 引数1, 引数2, ...> 関数名(HMODULE変数, DLL内での関数名);
```
※引数は0個以上であればいくらあっても問題ありません

## 使用例
``` C++
HMODULE dll = LoadLibrary("example.dll");
DLL<uint32_t, const std::string&> calculateCRC32(dll, "calculateCRC32");

std::cout << "CRC32: " << calculateCRC32("example.txt") << "\n";

cleanDLL(dll);
```



# English

## How to call.
``` C++
DLL<return value, argument 1, argument 2, ... > function name (HMODULE variable, function name in DLL);.
```
*It does not matter how many arguments there are, as long as they are zero or more!

## Example usage
``` C++
HMODULE dll = LoadLibrary("example.dll");
DLL<uint32_t, const std::string&> calculateCRC32(dll, "calculateCRC32");

std::cout << "CRC32: " << calculateCRC32("example.txt") << "\n";

cleanDLL(dll);
```
