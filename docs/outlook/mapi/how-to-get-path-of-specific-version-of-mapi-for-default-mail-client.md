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
  
このトピックには、コンピューター上の既定のメール クライアントで使用される MAPI の特定のバージョンのパスを取得する方法を示す C++ のコード サンプルが含まれています。 MAPI メール クライアントには、MAPI スタブ ライブラリが MAPI 呼び出しを読み込み、ディスパッチするカスタム DLL をレジストリに指定するオプションがあります。 既定のメール クライアントのこのカスタム DLL に設定するレジストリ キーは、既定のメール クライアントの **HKLM\Software\Client\Mail** キーの下の **MSIComponentID** です。 MAPI スタブ ライブラリ mapistub.dll によってエクスポートされた [FGetComponentPath](fgetcomponentpath.md) 関数は **、MSIComponentID** レジストリ キーで指定された MAPI のカスタム バージョンへのパスを返します。 
  
このコード サンプルには、次の 2 つの関数  `HrGetRegMultiSZValueA` が含まれています  `GetMAPISVCPath` 。 この  `GetMAPISVCPath` 関数は [、FGetComponentPath](fgetcomponentpath.md) を使用して、MAPI のカスタム バージョンへのパスを取得します。 既定のメール クライアントが Microsoft Office Outlook 2007 であることを前提とし、Outlook 2007 が MSIComponentID レジストリ キーの MAPI のコンポーネント ID として設定する値を **FGetComponentPath** に渡します。 `{FF1D0740-D227-11D1-A4B0-006008AF820E}`  
  
> [!NOTE]
> 実際には、値を想定し、常に MAPI のコンポーネント ID であり、  `{FF1D0740-D227-11D1-A4B0-006008AF820E}` **直接 FGetComponentPath に渡す必要があります**。 コンピューターで使用する MAPI Outlook のバージョンを確実に確認するには、レジストリから **MSIComponentID** の値を読み取り、 **それを FGetComponentPath** に渡す必要があります。 
  
次の手順では、この方法  `GetMAPISVCPath` について説明します。 
  
1. MAPI スタブ ライブラリをシステム mapistub.dllから読み込む。
    
2. **FGetComponentPath** 関数mapistub.dllエクスポートする場合は、この関数のアドレスを取得しようと試みmapistub.dll。 
    
3. サーバーからアドレスを取得mapistub.dll、アドレスを取得しようとしてエラーが発生mapi32.dll。
    
4. **FGetComponentPath** のアドレスを取得すると、レジストリが開き、この関数を使用して `HrGetRegMultiSZValueA` **HKLM\Software\Clients\Mail\Microsoft Outlook** のレジストリ値を読み取ることができます。 
    
5. 値を指定して、Outlook 2007 が使用する MAPI のバージョンへのパスを取得するために **、FGetComponentPath** を  `{FF1D0740-D227-11D1-A4B0-006008AF820E}` 呼び出します。
    
英語および英語以外のロケールの MAPI のローカライズされたコピーをサポートするために、コード サンプルは **MSIApplicationLCID** サブキーと **MSIOfficeLCID** サブキーの値を読み取り **、FGetComponentPath** を呼び出し、最初に **MSIApplicationLCID** を  *szQualifier*  として指定し、次に **MSIOfficeLCID** を  *szQualifier*  として指定します。 英語以外の言語をサポートするメール クライアントのレジストリ キーの詳細については、「MAPI DLL の MSI キーのセットアップ」 [を参照してください](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)。
  
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


