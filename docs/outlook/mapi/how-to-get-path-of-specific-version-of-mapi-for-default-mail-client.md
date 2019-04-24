---
title: 既定のメール クライアント用の MAPI の特定のバージョンのパスを取得する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ee7fb05-cfb3-6b68-5a9a-1d6375f2e879
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1992e34a684a6b5894963eae0c299b21c064578c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346460"
---
# <a name="get-the-path-of-a-specific-version-of-mapi-for-the-default-mail-client"></a>既定のメール クライアント用の MAPI の特定のバージョンのパスを取得する

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックには、コンピューター上の既定のメールクライアントで使用されている特定のバージョンの MAPI のパスを取得する方法を示す、C++ のコードサンプルが含まれています。 mapi メールクライアントには、mapi スタブライブラリが mapi 呼び出しを読み込んでディスパッチするカスタム DLL をレジストリで指定するオプションがあります。 既定のメールクライアントに対してこのカスタム DLL に設定するレジストリキーは、既定のメールクライアントの**HKLM\Software\Clients\Mail**キーの下にある**MSIComponentID**です。 mapi スタブライブラリ mapistub によってエクスポートされた[FGetComponentPath](fgetcomponentpath.md)関数は、 **MSIComponentID**レジストリキーで指定された mapi のカスタムバージョンへのパスを返すことができます。 
  
このコードサンプルには`HrGetRegMultiSZValueA` 、との`GetMAPISVCPath`2 つの関数が含まれています。 この`GetMAPISVCPath`関数は、 [FGetComponentPath](fgetcomponentpath.md)を使用して、MAPI のカスタムバージョンへのパスを取得します。 この例では、既定のメールクライアントが Microsoft Office Outlook 2007 である**** ことを想定し`{FF1D0740-D227-11D1-A4B0-006008AF820E}`、FGetComponentPath に渡します。この場合、Outlook 2007 は**MSIComponentID**レジストリキーの MAPI のコンポーネント ID として設定されます。 
  
> [!NOTE]
> 実際には、値`{FF1D0740-D227-11D1-A4B0-006008AF820E}`を想定しないでください。は常に MAPI のコンポーネント ID であり、 **FGetComponentPath**に直接渡されます。 コンピューターでどのバージョンの MAPI Outlook が使用されているかを確実に確認するには、レジストリから**MSIComponentID**の値を読み取り、それを**FGetComponentPath**に渡します。 
  
次の手順では`GetMAPISVCPath` 、これを行う方法について説明します。 
  
1. システムディレクトリから MAPI スタブライブラリ mapistub を読み込みます。
    
2. mapistub が**FGetComponentPath**関数をエクスポートし、mapistub からこの関数のアドレスを取得しようとしていることを前提としています。 
    
3. mapistub からアドレスを取得しようとすると、mapi32 からアドレスを取得しようと試みます。
    
4. **FGetComponentPath**のアドレスの取得に成功すると、レジストリが開き、 `HrGetRegMultiSZValueA`関数を使用して**HKLM\Software\Clients\Mail\Microsoft Outlook**の下にあるレジストリ値を読み取ります。 
    
5. 値**** `{FF1D0740-D227-11D1-A4B0-006008AF820E}`を指定して FGetComponentPath を呼び出し、Outlook 2007 で使用される MAPI のバージョンへのパスを取得します。
    
英語および英語以外のロケールで MAPI のローカライズされたコピーをサポートするために、コードサンプルでは**msiapplicationlcid**および**msiofficeelcid**サブキーの値を読み取り、 **FGetComponentPath**を呼び出しています。最初の指定**msiapplicationlcid**を*szqualifier*として再度指定して、 **msiofficeelcid**を*szqualifier*として指定します。 英語以外の言語をサポートするメールクライアントのレジストリキーの詳細については、「 [Setting Up the MSI keys for the MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)」を参照してください。
  
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


