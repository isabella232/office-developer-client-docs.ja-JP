---
title: ラップされた PST ストア プロバイダーの初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: '最終更新日: 2012 年 10 月 5 日'
ms.openlocfilehash: 31114e4082fbc5e4c57da95eb6b32339822b1645
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427823"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーの初期化

**適用対象**: Outlook 2013 | Outlook 2016 
  
ラップされた個人用フォルダー ファイル (PST) ストア プロバイダーを実装するには **[、MSProviderInit](msproviderinit.md)** 関数をエントリ ポイントとして使用して、ラップされた PST ストア プロバイダーを初期化する必要があります。 プロバイダーの DLL が初期化されると **[、MSGSERVICEENTRY](msgserviceentry.md)** 関数はラップされた PST ストア プロバイダーを構成します。 
  
このトピックでは、サンプル ラップされた PST ストア プロバイダーのコード例を使用して **、MSProviderInit** 関数と **MSGSERVICEENTRY** 関数を示します。 このサンプルでは、レプリケーション API と組み合わせて使用することを目的としたラップされた PST プロバイダーを実装しています。 サンプル ラップ PST ストア プロバイダーのダウンロードとインストールの詳細については、「サンプル ラップされた PST ストア プロバイダーのインストール [」を参照してください](installing-the-sample-wrapped-pst-store-provider.md)。 レプリケーション API の詳細については、「レプリケーション [API について」を参照してください](about-the-replication-api.md)。
  
ラップされた PST ストア プロバイダーを初期化した後、MAPI と MAPI スプーラーがメッセージ ストア プロバイダーにログオンできるよう、関数を実装する必要があります。 詳細については、「ラップされた PST ストア プロバイダー [へのログオン」を参照してください](logging-on-to-a-wrapped-pst-store-provider.md)。
  
## <a name="initialization-routine"></a>初期化ルーチン

ラップされた PST ストア プロバイダーはすべて、プロバイダーの DLL を初期化するためのエントリ ポイントとして **[MSProviderInit](msproviderinit.md)** 関数を実装する必要があります。 **MSProviderInit** は、サービス プロバイダー インターフェイスのバージョン番号が、現在のバージョン番号と互換性  `ulMAPIVer` が確認されます  `CURRENT_SPI_VERSION` 。 この関数は、MAPI メモリ管理ルーチンを  `g_lpAllocateBuffer` 、 、および  `g_lpAllocateMore` パラメーターに保存  `g_lpFreeBuffer` します。 これらのメモリ管理ルーチンは、メモリの割り当てと割り当て解除のためにラップされた PST ストアの実装全体で使用する必要があります。 
  
### <a name="msproviderinit-example"></a>MSProviderInit() の例

```cpp
STDINITMETHODIMP MSProviderInit ( 
    HINSTANCE /*hInstance*/, 
    LPMALLOC lpMalloc, 
    LPALLOCATEBUFFER lpAllocateBuffer, 
    LPALLOCATEMORE lpAllocateMore, 
    LPFREEBUFFER lpFreeBuffer, 
    ULONG ulFlags, 
    ULONG ulMAPIVer, 
    ULONG FAR * lpulProviderVer, 
    LPMSPROVIDER FAR * lppMSProvider) 
{ 
    Log(true,"MSProviderInit function called\n"); 
    if (!lppMSProvider || !lpulProviderVer) return MAPI_E_INVALID_PARAMETER; 
    HRESULT hRes = S_OK; 
 
    *lppMSProvider = NULL; 
    *lpulProviderVer = CURRENT_SPI_VERSION; 
    if (ulMAPIVer < CURRENT_SPI_VERSION) 
    { 
        Log(true,"MSProviderInit: The version of the subsystem cannot handle this" 
            + "version of the provider\n"); 
        return MAPI_E_VERSION; 
    } 
 
    Log(true,"MSProviderInit: saving off memory management routines\n"); 
    g_lpAllocateBuffer = lpAllocateBuffer; 
    g_lpAllocateMore = lpAllocateMore; 
    g_lpFreeBuffer = lpFreeBuffer; 
    HMODULE hm = LoadLibrary("C:\\Program Files\\Common Files\\System" + 
        "\\MSMAPI\\1033\\MSPST32.dll" ); 
    if (!hm) hm = LoadLibrary("C:\\Program Files\\Microsoft Office\\Office12" + 
        "\\MSPST32.dll" ); 
    Log(true,"LoadLibrary returned 0x%08X\n", hm); 
 
    LPMSPROVIDERINIT pMsProviderInit = NULL; 
    if (hm) 
    { 
        pMsProviderInit = (LPMSPROVIDERINIT)GetProcAddress(hm, "MSProviderInit"); 
        Log(true,"GetProcAddress returned 0x%08X\n", pMsProviderInit); 
    } 
    else hRes = E_OUTOFMEMORY; 
    if (pMsProviderInit) 
    { 
        Log(true,"Calling pMsProviderInit\n"); 
        CMSProvider* pWrappedProvider = NULL; 
        LPMSPROVIDER pSyncProviderObj = NULL; 
        hRes = pMsProviderInit( 
            hm,// not hInstance: first param is handle of module in which the function lives 
            lpMalloc, 
            lpAllocateBuffer, 
            lpAllocateMore, 
            lpFreeBuffer, 
            ulFlags, 
            ulMAPIVer, 
            lpulProviderVer, 
            &pSyncProviderObj                         
            ); 
        Log(true,"pMsProviderInit returned 0x%08X\n", hRes); 
        if (SUCCEEDED(hRes)) 
        { 
            pWrappedProvider = new CMSProvider (pSyncProviderObj); 
            if (NULL == pWrappedProvider) 
            { 
                Log(true,"MSProviderInit: Failed to allocate new CMSProvider object\n"); 
                hRes = E_OUTOFMEMORY; 
            } 
            // Copy pointer to the allocated object back into the  
            //return IMSProvider object pointer 
            *lppMSProvider = pWrappedProvider; 
        } 
    } 
    else hRes = E_OUTOFMEMORY; 
    return hRes; 
}
```

### <a name="wrapped-pst-and-unicode-paths"></a>ラップされた PST パスと Unicode パス

Microsoft Visual Studio 2008 で準備された元のサンプルを、Unicode 対応の Microsoft Outlook 2010 および Outlook 2013 で使用するために NST への Unicode パスを使用するために後付けするには、エントリ識別子を生成する **CreateStoreEntryID** ルーチンで ASCII パスに 1 つの形式を使用し、もう 1 つの形式を Unicode パスに使用する必要があります。 これらは、次の例では構造体として表されます。 
  
```cpp
typedef struct                              // short format
{
         BYTE             rgbFlags[4];     // MAPI-defined flags
         MAPIUID          uid;             // PST provider MUID
         BYTE             bReserved;       // Reserved (must be zero)
         CHAR             szPath[1];       // Full path to store (ASCII)
 } EIDMS;
// Unicode version of EIDMSW is an extension of EIDMS
// and szPath is always NULL
typedef struct                              // Long format to support Unicode path and name
{
         BYTE             rgbFlags[4];     // MAPI-defined flags
         MAPIUID          uid;             // PST provider MUID
         BYTE             bReserved;       // Reserved (must be zero)
         CHAR             szPath[1];       // ASCII path to store is always NULL
         WCHAR            wzPath[1];       // Full path to store (Unicode)
} EIDMSW;
```

> [!IMPORTANT]
> これらの構造の違いは、Unicode パスより前の 2 つの NULL バイトです。 次に示す "サービス エントリ ルーチン" のエントリ識別子を解釈する必要がある場合は、最初に EIDMS としてキャストするかどうかを判断する 1 つの方法として、szPath[0] が NULL であるかどうかを確認します。 その場合は、代わりに EIDMSW としてキャストします。 
  
## <a name="service-entry-routine"></a>サービス エントリ ルーチン

**[MSGSERVICEENTRY 関数](msgserviceentry.md)** は、ラップされた PST ストア プロバイダーが構成されているメッセージ サービス エントリ ポイントです。 この関数は  `GetMemAllocRoutines()` 、MAPI メモリ管理ルーチンを取得するために呼び出されます。 この関数は、パラメーター  `lpProviderAdmin` を使用してプロバイダーのプロファイル セクションを検索し、プロファイルのプロパティを設定します。 
  
### <a name="serviceentry-example"></a>ServiceEntry() の例

```cpp
HRESULT STDAPICALLTYPE ServiceEntry ( 
    HINSTANCE /*hInstance*/, 
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR *lppMapiError) 
{ 
    if (!lpMAPISup || !lpProviderAdmin) return MAPI_E_INVALID_PARAMETER; 
    HRESULT         hRes = S_OK; 
    Log(true,"ServiceEntry function called\n"); 
    Log(true,"About to call NSTServiceEntry\n"); 
 
    if (MSG_SERVICE_INSTALL         == ulContext || 
        MSG_SERVICE_DELETE            == ulContext || 
        MSG_SERVICE_UNINSTALL        == ulContext || 
        MSG_SERVICE_PROVIDER_CREATE == ulContext || 
        MSG_SERVICE_PROVIDER_DELETE == ulContext) 
    { 
        // These contexts are not supported 
        return MAPI_E_NO_SUPPORT; 
    } 
 
    // Get memory routines 
    hRes = lpMAPISup-> 
        GetMemAllocRoutines(&g_lpAllocateBuffer,&g_lpAllocateMore,&g_lpFreeBuffer); 
    HMODULE hm = LoadLibrary("C:\\Program Files\\Common Files\\System" + 
        "\\MSMAPI\\1033\\MSPST32.dll" ); 
    if (!hm) hm = LoadLibrary("C:\\Program Files\\Microsoft Office\\Office12" + 
        "\\MSPST32.dll" ); 
    Log(true, "Got module 0x%08X\n", hm); 
    if (!hm) return E_OUTOFMEMORY; 
    LPMSGSERVICEENTRY pNSTServiceEntry =  
        (LPMSGSERVICEENTRY)GetProcAddress(hm, "NSTServiceEntry"); 
    Log(true, "Got procaddress  0x%08X\n", pNSTServiceEntry); 
    if (!pNSTServiceEntry) return E_OUTOFMEMORY; 
 
    // Get profile section 
    LPPROFSECT lpProfSect = NULL; 
    hRes = lpProviderAdmin-> 
        OpenProfileSection((LPMAPIUID) NULL, NULL, MAPI_MODIFY, &lpProfSect); 
    // Set passed in props into the profile 
    if (lpProps && cValues) 
    { 
        hRes = lpProfSect->SetProps(cValues,lpProps,NULL); 
    } 
    // Make sure there is a store path set 
    if (SUCCEEDED(hRes)) hRes = SetOfflineStoreProps(lpProfSect,ulUIParam); 
    ULONG            ulProfProps = 0; 
    LPSPropValue    lpProfProps = NULL; 
 
    // Evaluate props 
    hRes = lpProfSect->GetProps((LPSPropTagArray)&sptClientProps, 
                                fMapiUnicode, 
                                &ulProfProps, 
                                &lpProfProps); 
    if (SUCCEEDED(hRes)) 
    { 
        CSupport * pMySup = NULL; 
        pMySup = new CSupport(lpMAPISup, lpProfSect); 
        if (!pMySup) 
        { 
            Log(true,"MSProviderInit: Failed to allocate new CSupport object\n"); 
            hRes = E_OUTOFMEMORY; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            hRes = pNSTServiceEntry( 
                hm,  
                lpMalloc, 
                pMySup, 
                ulUIParam, 
                ulFlags, 
                ulContext, 
                ulProfProps, 
                lpProfProps, 
                NULL,//pAdminProvObj, //Don't pass this when creating an NST 
                lppMapiError); 
            if (SUCCEEDED(hRes)) 
            { 
                // Finish setting up the profile 
                hRes = InitStoreProps( 
                    lpMAPISup,  
                    lpProfSect,  
                    lpProviderAdmin); 
                hRes = lpProfSect->SaveChanges(KEEP_OPEN_READWRITE); 
            } 
        } 
    } 
    Log(true, "Ran pNSTServiceEntry 0x%08X\n", hRes); 
    MyFreeBuffer(lpProfProps); 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="see-also"></a>関連項目

- [ラップされた PST ストア プロバイダーのサンプルについて](about-the-sample-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーのサンプルのインストール](installing-the-sample-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーの使用](using-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)

