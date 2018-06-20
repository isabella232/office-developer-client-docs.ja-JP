---
title: 既定のメール クライアントの MAPI の特定のバージョンのパスを取得します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ee7fb05-cfb3-6b68-5a9a-1d6375f2e879
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 277505beb11dbc2b32b7e970c2bcf2a34dbdf00b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800217"
---
# <a name="get-the-path-of-a-specific-version-of-mapi-for-the-default-mail-client"></a>既定のメール クライアントの MAPI の特定のバージョンのパスを取得します。

**適用されます**: Outlook 
  
このトピックには、コンピューター上の既定のメール クライアントで使用されている MAPI の特定のバージョンのパスを取得する方法について説明する C++ のコード サンプルが含まれています。 MAPI メール クライアントには、レジストリに MAPI スタブ ライブラリが読み込まれ、MAPI をディスパッチするカスタム DLL の呼び出しで指定するオプションがあります。 既定のメール クライアントでこのカスタム DLL を設定するレジストリ キーでは、 **MSIComponentID**既定のメール クライアントの**HKLM\Software\Clients\Mail**キーの下。 MAPI スタブ ライブラリによってエクスポートされた[FGetComponentPath](fgetcomponentpath.md)関数は、mapistub.dll、 **MSIComponentID**レジストリ キーに指定されている MAPI のカスタム バージョンのパスを返すことができます。 
  
このコード サンプルには、2 つの関数が含まれています:`HrGetRegMultiSZValueA`と`GetMAPISVCPath`。 `GetMAPISVCPath`関数では、 [FGetComponentPath](fgetcomponentpath.md)を使用して、カスタム MAPI のバージョンへのパスを取得します。 既定のメール クライアントは、Microsoft Office Outlook 2007 と**FGetComponentPath**に値を渡すことが前提としています`{FF1D0740-D227-11D1-A4B0-006008AF820E}`、 **MSIComponentID**レジストリ キーのコンポーネント ID の MAPI Outlook 2007 を設定します。 
  
> [!NOTE]
> 実習でないと考えてください、値は、 `{FF1D0740-D227-11D1-A4B0-006008AF820E}`、常にコンポーネント ID の MAPI および**FGetComponentPath**に直接渡すことです。 MAPI Outlook のバージョンがコンピューターで使用することを確実に検索するには**MSIComponentID**の値をレジストリから読み取るし、 **FGetComponentPath**に渡すことです。 
  
次の手順を説明する方法`GetMAPISVCPath`は、このです。 
  
1. システム ディレクトリから mapistub.dll、MAPI スタブ ライブラリを読み込みます。
    
2. Mapistub.dll **FGetComponentPath**関数をエクスポートすることは、mapistub.dll からこの関数のアドレスを取得しようとすることを想定しています。 
    
3. Mapistub.dll が失敗した場合のアドレスの取得、mapi32.dll からアドレスを取得しようとします。
    
4. レジストリを開き、使用して、 **FGetComponentPath**のアドレスの取得が成功した場合、 `HrGetRegMultiSZValueA` **HKLM\Software\Clients\Mail\Microsoft Outlook**の下のレジストリ値を読み取る関数。 
    
5. **FGetComponentPath**の値を指定するには`{FF1D0740-D227-11D1-A4B0-006008AF820E}`、Outlook 2007 を使用する MAPI のバージョンへのパスを取得します。
    
英語と英語以外のロケールのローカライズされたコピー MAPI をサポートするためにサンプル コード**MSIApplicationLCID**と**MSIOfficeLCID**のサブキーの値を読み取り、 **FGetComponentPath**、最初に指定する**を呼び出して注意してください。MSIApplicationLCID** *szQualifier* 、 *szQualifier*と**MSIOfficeLCID**もう一度指定するとします。 英語以外の言語をサポートするメール クライアントのレジストリ キーの詳細については、[設定の [MSI のキーの MAPI DLL](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx)を参照してください。
  
```cpp
// HrGetRegMultiSZValueA 
// Get a REG_MULTI_SZ registry value - allocating memory using new to hold it. 
void HrGetRegMultiSZValueA( 
    IN HKEY hKey, // the key. 
    IN LPCSTR lpszValue, // value name in key. 
    OUT LPVOID* lppData) // where to put the data. 
{ 
    *lppData = NULL; 
    DWORD dwKeyType = NULL;       
    DWORD cb = NULL; 
    LONG lRet = 0; 
    
    // Get its size 
    lRet = RegQueryValueExA( 
        hKey, 
        lpszValue, 
        NULL, 
        &amp;dwKeyType, 
        NULL, 
        &amp;cb); 
 
    if (ERROR_SUCCESS == lRet &amp;&amp; cb &amp;&amp; REG_MULTI_SZ == dwKeyType) 
    { 
        *lppData = new BYTE[cb]; 
       
        if (*lppData) 
        { 
            // Get the current value 
            lRet = RegQueryValueExA( 
                hKey,  
                lpszValue,  
                NULL,  
                &amp;dwKeyType,  
                (unsigned char*)*lppData,  
                &amp;cb); 
          
            if (ERROR_SUCCESS != lRet) 
            { 
                delete[] *lppData; 
                *lppData = NULL; 
            } 
        } 
    } 
} 
 
typedef BOOL (STDAPICALLTYPE FGETCOMPONENTPATH) ( 
    LPSTR szComponent, 
    LPSTR szQualifier, 
    LPSTR szDllPath, 
    DWORD cchBufferSize, 
    BOOL fInstall); 
typedef FGETCOMPONENTPATH FAR * LPFGETCOMPONENTPATH;  
 
/////////////////////////////////////////////////////////////////////////////// 
// Function name   : GetMAPISVCPath 
// Description       : This will get the correct path to the MAPISVC.INF file. 
// Return type      : void  
// Argument         : LPSTR szMAPIDir - Buffer to hold the path to the MAPISVC file. 
//                    ULONG cchMAPIDir - size of the buffer 
void GetMAPISVCPath(LPSTR szMAPIDir, ULONG cchMAPIDir) 
{ 
    HRESULT hRes = S_OK; 
    UINT uiRet = 0; 
    LONG lRet = 0; 
    BOOL bRet = true; 
    
    szMAPIDir[0] = &apos;\0&apos;; // Terminate string at position 0, safer if fail below 
    
    CHAR szSystemDir[MAX_PATH+1] = {0}; 
    
    // Get the system directory path 
    // (mapistub.dll and mapi32.dll reside here) 
    uiRet = GetSystemDirectoryA(szSystemDir, MAX_PATH); 
    if (uiRet &gt; 0) 
    { 
        CHAR szDLLPath[MAX_PATH+1] = {0}; 
       
        hRes = StringCchPrintfA(szDLLPath, MAX_PATH+1, &quot;%s\\%s&quot;,  
            szSystemDir, &quot;mapistub.dll&quot;); 
        if (SUCCEEDED(hRes)) 
        { 
            LPFGETCOMPONENTPATH pfnFGetComponentPath = NULL; 
          
            HMODULE hmodStub = 0; 
            HMODULE hmodMapi32 = 0; 
          
            // Load mapistub.dll 
            hmodStub = LoadLibraryA(szDLLPath); 
            if (hmodStub) 
            {    
                // Get the address of FGetComponentPath from the mapistub 
                pfnFGetComponentPath = (LPFGETCOMPONENTPATH)GetProcAddress( 
                    hmodStub, &quot;FGetComponentPath&quot;); 
            } 
          
            // If failed to get the address of FGetComponentPath, 
            // try mapi32.dll 
            if (!pfnFGetComponentPath) 
            { 
                hRes = StringCchPrintfA(szDLLPath, MAX_PATH+1, &quot;%s\\%s&quot;, 
                    szSystemDir, &quot;mapi32.dll&quot;); 
                if (SUCCEEDED(hRes)) 
                { 
                    // Load mapi32.dll 
                    hmodMapi32 = LoadLibraryA(szDLLPath); 
                    if (hmodMapi32) 
                    { 
                        // Get the address of FGetComponentPath from mapi32 
                        pfnFGetComponentPath = (LPFGETCOMPONENTPATH)GetProcAddress( 
                            hmodMapi32, &quot;FGetComponentPath&quot;); 
                    } 
                 } 
            } 
            if (pfnFGetComponentPath) 
            { 
                LPSTR szAppLCID = NULL; 
                LPSTR szOfficeLCID = NULL; 
                HKEY hMicrosoftOutlook = NULL; 
             
                lRet = RegOpenKeyEx( 
                    HKEY_LOCAL_MACHINE, 
                    _T(&quot;Software\\Clients\\Mail\\Microsoft Outlook&quot;), 
                    NULL, 
                    KEY_READ, 
                    &amp;hMicrosoftOutlook); 
             
                if (ERROR_SUCCESS == lRet &amp;&amp; hMicrosoftOutlook) 
                { 
                    HrGetRegMultiSZValueA(hMicrosoftOutlook, &quot;MSIApplicationLCID&quot;, (LPVOID*) &amp;szAppLCID); 
                    HrGetRegMultiSZValueA(hMicrosoftOutlook, &quot;MSIOfficeLCID&quot;, (LPVOID*) &amp;szOfficeLCID); 
                } 
             
                // Only passing a fixed value as the component ID for MAPI in this example 
                // In practice, must read from the registry the value of MSIComponentID 
                if (szAppLCID) 
                { 
                    bRet = pfnFGetComponentPath( 
                        &quot;{FF1D0740-D227-11D1-A4B0-006008AF820E}&quot;, szAppLCID, szMAPIDir, cchMAPIDir, true); 
                } 
                if ((!bRet || szMAPIDir[0] == _T(&apos;\0&apos;)) &amp;&amp; szOfficeLCID) 
                { 
                    bRet = pfnFGetComponentPath( 
                    &quot;{FF1D0740-D227-11D1-A4B0-006008AF820E}&quot;, szOfficeLCID, szMAPIDir, cchMAPIDir, true); 
                } 
                if (!bRet || szMAPIDir[0] == _T(&apos;\0&apos;)) 
                { 
                    bRet = pfnFGetComponentPath( 
                        &quot;{FF1D0740-D227-11D1-A4B0-006008AF820E}&quot;, NULL, szMAPIDir, cchMAPIDir, true); 
                } 
             
                // Got the path to msmapi32.dll - need to strip it 
                if (bRet &amp;&amp; szMAPIDir[0] != _T(&apos;\0&apos;)) 
                { 
                    LPSTR lpszSlash = NULL; 
                    LPSTR lpszCur = szMAPIDir; 
                
                    for (lpszSlash = lpszCur; *lpszCur; lpszCur = lpszCur++) 
                    { 
                        if (*lpszCur == _T(&apos;\\&apos;)) lpszSlash = lpszCur; 
                    } 
                   *lpszSlash = _T(&apos;\0&apos;); 
                } 
 
                delete[] szOfficeLCID; 
                delete[] szAppLCID; 
                if (hMicrosoftOutlook) RegCloseKey(hMicrosoftOutlook);       
            } 
             
            // If FGetComponentPath returns FALSE or if 
            // it returned nothing, or if failed to find an 
            // address of FGetComponentPath, then 
            // just default to the system directory 
            if (!bRet || szMAPIDir[0] == &apos;\0&apos;) 
            { 
                hRes = StringCchPrintfA( 
                    szMAPIDir, cchMAPIDir,&quot;%s&quot;, szSystemDir); 
            } 
          
            if (szMAPIDir[0] != _T(&apos;\0&apos;)) 
            { 
                hRes = StringCchPrintfA( 
                    szMAPIDir, cchMAPIDir, &quot;%s\\%s&quot;, szMAPIDir, &quot;MAPISVC.INF&quot;); 
            } 
          
            if (hmodMapi32) FreeLibrary(hmodMapi32); 
            if (hmodStub) FreeLibrary(hmodStub); 
        } 
    }    
}

```


