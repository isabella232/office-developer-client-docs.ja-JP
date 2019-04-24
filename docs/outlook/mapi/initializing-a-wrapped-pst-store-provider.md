---
title: ラップされた PST ストア プロバイダーの初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 最終更新日:05 年10月2012日
ms.openlocfilehash: 31114e4082fbc5e4c57da95eb6b32339822b1645
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317242"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーの初期化

**適用対象**: Outlook 2013 | Outlook 2016 
  
ラップされた個人用フォルダーファイル (PST) ストアプロバイダーを実装するには、エントリポイントとして**[msproviderinit](msproviderinit.md)** 関数を使用して、ラップされた PST ストアプロバイダーを初期化する必要があります。 プロバイダーの DLL が初期化された後、 **[msgserviceentry](msgserviceentry.md)** 関数は、ラップされた PST ストアプロバイダーを構成します。 
  
このトピックでは、サンプルのラップされた PST ストアプロバイダーからのコード例を使用して、 **msproviderinit**関数と**msgserviceentry**関数をデモンストレーションします。 このサンプルでは、レプリケーション API と共に使用することを目的とした、ラップされた PST プロバイダーを実装しています。 サンプルのラップされた pst ストアプロバイダーのダウンロードとインストールの詳細については、「[サンプルのラップされた pst ストアプロバイダーのインストール](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。 レプリケーション api の詳細については、「[レプリケーション api につい](about-the-replication-api.md)て」を参照してください。
  
ラップされた PST ストアプロバイダーを初期化した後、mapi および mapi スプーラーがメッセージストアプロバイダーにログオンできるように、関数を実装する必要があります。 詳細については、「ラップされ[た PST ストアプロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)」を参照してください。
  
## <a name="initialization-routine"></a>初期化ルーチン

ラップされたすべての PST ストアプロバイダーは、プロバイダーの DLL を初期化するためのエントリポイントとして**[msproviderinit](msproviderinit.md)** 関数を実装する必要があります。 **msproviderinit**は、サービスプロバイダーインターフェイス`ulMAPIVer`のバージョン番号が現在のバージョン番号と互換性があるかどうかを確認`CURRENT_SPI_VERSION`します。 この関数は、MAPI メモリ管理ルーチンを、 `g_lpAllocateBuffer`、 `g_lpAllocateMore`および`g_lpFreeBuffer`パラメーターに保存します。 これらのメモリ管理ルーチンは、メモリの割り当てと解放のために、ラップされた PST ストアの実装全体で使用する必要があります。 
  
### <a name="msproviderinit-example"></a>msproviderinit () の例

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

### <a name="wrapped-pst-and-unicode-paths"></a>ラップされた PST および Unicode パス

unicode 対応の microsoft outlook 2010 および outlook 2013 で使用するために、NST への unicode パスを使用するために、microsoft Visual Studio 2008 で準備された元のサンプルを retrofit するには、エントリ識別子を生成する**createstoreentryid**ルーチンを使用する必要があります。1つは ASCII パスで、もう1つは Unicode パスです。 次の例では、これらは構造体として表されています。 
  
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
> これらの構造体の違いは、Unicode パスの前の2つの NULL バイトです。 次の「サービスエントリルーチン」のエントリ識別子を解釈する必要がある場合は、最初に eidms としてキャストするかどうかを確認してから、szpath [0] が NULL かどうかを確認する方法の1つです。 その場合は、代わりに EIDMSW としてキャストします。 
  
## <a name="service-entry-routine"></a>サービスエントリルーチン

**[msgserviceentry](msgserviceentry.md)** 関数は、ラップされた PST ストアプロバイダーが構成されているメッセージサービスエントリポイントです。 MAPI メモリ管理`GetMemAllocRoutines()`ルーチンを取得する関数呼び出し。 この関数は、 `lpProviderAdmin`パラメーターを使用してプロバイダーのプロファイルセクションを見つけ、プロファイルのプロパティを設定します。 
  
### <a name="serviceentry-example"></a>serviceentry () の例

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

- [ラップされた PST ストアプロバイダーのサンプルについて](about-the-sample-wrapped-pst-store-provider.md)
- [ラップされた PST ストアプロバイダーのサンプルのインストール](installing-the-sample-wrapped-pst-store-provider.md)
- [ラップされた PST ストアプロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストアプロバイダーの使用](using-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストアプロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)

