# XingnCode-Dump
Dump of XingnCode's Client module 20/11/2020


String Decryption:

you will see a bunch of strings that look like this: https://imgur.com/ZbjF7Wk

```
const wchar_t* decrypt_chinkstring(const char* encrypted_string)
{
    signed __int64 v2; // rax
    unsigned __int64 v1; // r8
    __int16 ClassName[124]; // [rsp+40h] [rbp-A8h]
    const char* v0; // rax
    v1 = 0i64;
    v0 = encrypted_string;
    v2 = v0 - (const char*)ClassName;
    do
    {
        ClassName[v1] = *(__int16*)((char*)&ClassName[v1] + v2) ^ 0x5017;
        ++v1;
    } while (v1 < 0x26);

    return (LPCWSTR)ClassName;
}
```
