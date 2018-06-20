---
title: ラップされた PST ストア プロバイダーを初期化しています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: '最終更新日: 2012 年 10 月 05 日'
ms.openlocfilehash: a332c63814163579d5fe8ab365145e9583fa6c97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801080"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーを初期化しています。

**適用されます**: Outlook 
  
ラップされた個人用フォルダー ファイル (PST) のストア プロバイダーを実装するためのエントリ ポイントとして、 **[MSProviderInit](msproviderinit.md)** 関数を使用して、ラップされた PST ストア プロバイダーを初期化する必要があります。 プロバイダーの DLL が初期化された後、 **[MSGSERVICEENTRY](msgserviceentry.md)** 関数は、ラップされた PST ストア プロバイダーを構成します。 
  
このトピックでは、 **MSProviderInit**関数および**MSGSERVICEENTRY**関数はサンプル ラップ PST ストア プロバイダーのコード例を使用して説明します。 レプリケーション API と連携して使用するものでは、ラップされた PST プロバイダーを実装します。 ダウンロードとサンプル ラップ PST ストア プロバイダーをインストールする方法の詳細については、「[サンプル ラップ PST ストア プロバイダーをインストールする](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。 レプリケーション API の詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。
  
ラップされた PST ストア プロバイダーを初期化すると、MAPI および MAPI スプーラーは、メッセージ ストア プロバイダーにログオンできるように関数を実装する必要があります。 詳細については、[ラップされた PST ストア プロバイダーにログを](logging-on-to-a-wrapped-pst-store-provider.md)参照してください。
  
## <a name="initialization-routine"></a>初期化ルーチン

ラップされたすべての PST ストア プロバイダーは、プロバイダーの DLL を初期化するためにエントリ ポイントとして、 **[MSProviderInit](msproviderinit.md)** 関数を実装する必要があります。 **MSProviderInit**をチェックするかどうか、サービス プロバイダーのインターフェイスのバージョン番号`ulMAPIVer`、現在のバージョン番号と互換性のある`CURRENT_SPI_VERSION`。 保存 MAPI メモリに管理ルーチンの関数、 `g_lpAllocateBuffer`、 `g_lpAllocateMore`、および`g_lpFreeBuffer`のパラメーターです。 メモリの割り当てと割り当て解除には、ラップされた PST ストアの実装でこれらのメモリ管理ルーチンを使用してください。 
  
### <a name="msproviderinit-example"></a>MSProviderInit() の使用例

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

### <a name="wrapped-pst-and-unicode-paths"></a>ラップされた pst ファイルと Unicode のパス

NST への Unicode のパスを使用して、Unicode 対応の Microsoft Outlook 2010、Outlook 2013 で使用する Microsoft Visual Studio 2008 の準備をして、元のサンプルを改造するには、エントリの識別子を作成するには、 **CreateStoreEntryID**ルーチンを使用する必要があります。ASCII パス、および Unicode のパスの別の 1 つの形式です。 これらは、次の例では、構造体として表されます。 
  
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
> これらの構造の違いは、Unicode のパスの前に 2 つの NULL バイトです。 「サービス エントリ ルーチン」の後のエントリ id を解釈する必要があります、か、そうではあるかどうかを決定する方法の 1 つのように EIDMS し、先ず、szPath [0] が NULL であるかどうかをキャストするでしょう。 場合は、代わりに EIDMSW としてキャストします。 
  
## <a name="service-entry-routine"></a>サービス エントリ ルーチン

**[MSGSERVICEENTRY](msgserviceentry.md)** 関数は、ラップされた PST ストア プロバイダーが構成されているメッセージ サービスのエントリ ポイントです。 関数呼び出し`GetMemAllocRoutines()`MAPI のメモリ管理ルーチンを取得します。 関数を使用して、`lpProviderAdmin`プロファイルにプロパティを設定、プロバイダーのプロファイル セクションを検索するパラメーターです。 
  
### <a name="serviceentry-example"></a>ServiceEntry() の使用例

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

- [サンプルの PST ストア プロバイダーをラップ](about-the-sample-wrapped-pst-store-provider.md)
- [PST ストア プロバイダーをラップして、サンプルをインストールします。](installing-the-sample-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーを使用します。](using-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーをシャット ダウン](shutting-down-a-wrapped-pst-store-provider.md)

