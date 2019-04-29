---
title: ラップされた PST ストア プロバイダーの初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 最終更新日:05 年10月2012日
ms.openlocfilehash: 31114e4082fbc5e4c57da95eb6b32339822b1645
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427823"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a><span data-ttu-id="08699-103">ラップされた PST ストア プロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="08699-103">Initializing a wrapped PST store provider</span></span>

<span data-ttu-id="08699-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08699-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08699-105">ラップされた個人用フォルダーファイル (PST) ストアプロバイダーを実装するには、エントリポイントとして**[msproviderinit](msproviderinit.md)** 関数を使用して、ラップされた PST ストアプロバイダーを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08699-105">To implement a wrapped Personal Folders file (PST) store provider, you must initialize the wrapped PST store provider by using the **[MSProviderInit](msproviderinit.md)** function as an entry point.</span></span> <span data-ttu-id="08699-106">プロバイダーの DLL が初期化された後、 **[msgserviceentry](msgserviceentry.md)** 関数は、ラップされた PST ストアプロバイダーを構成します。</span><span class="sxs-lookup"><span data-stu-id="08699-106">After the provider's DLL is initialized, the **[MSGSERVICEENTRY](msgserviceentry.md)** function configures the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="08699-107">このトピックでは、サンプルのラップされた PST ストアプロバイダーからのコード例を使用して、 **msproviderinit**関数と**msgserviceentry**関数をデモンストレーションします。</span><span class="sxs-lookup"><span data-stu-id="08699-107">In this topic, the **MSProviderInit** function and the **MSGSERVICEENTRY** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="08699-108">このサンプルでは、レプリケーション API と共に使用することを目的とした、ラップされた PST プロバイダーを実装しています。</span><span class="sxs-lookup"><span data-stu-id="08699-108">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="08699-109">サンプルのラップされた pst ストアプロバイダーのダウンロードとインストールの詳細については、「[サンプルのラップされた pst ストアプロバイダーのインストール](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08699-109">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="08699-110">レプリケーション api の詳細については、「[レプリケーション api につい](about-the-replication-api.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08699-110">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="08699-111">ラップされた PST ストアプロバイダーを初期化した後、mapi および mapi スプーラーがメッセージストアプロバイダーにログオンできるように、関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08699-111">After you have initialized a wrapped PST store provider, you must implement functions so that MAPI and the MAPI spooler can log onto the message store provider.</span></span> <span data-ttu-id="08699-112">詳細については、「ラップされ[た PST ストアプロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08699-112">For more information, see [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="initialization-routine"></a><span data-ttu-id="08699-113">初期化ルーチン</span><span class="sxs-lookup"><span data-stu-id="08699-113">Initialization routine</span></span>

<span data-ttu-id="08699-114">ラップされたすべての PST ストアプロバイダーは、プロバイダーの DLL を初期化するためのエントリポイントとして**[msproviderinit](msproviderinit.md)** 関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08699-114">All wrapped PST store providers must implement the **[MSProviderInit](msproviderinit.md)** function as an entry point to initialize the provider's DLL.</span></span> <span data-ttu-id="08699-115">**msproviderinit**は、サービスプロバイダーインターフェイス`ulMAPIVer`のバージョン番号が現在のバージョン番号と互換性があるかどうかを確認`CURRENT_SPI_VERSION`します。</span><span class="sxs-lookup"><span data-stu-id="08699-115">**MSProviderInit** checks to see if the version number of the service provider interface,  `ulMAPIVer`, is compatible with the current version number,  `CURRENT_SPI_VERSION`.</span></span> <span data-ttu-id="08699-116">この関数は、MAPI メモリ管理ルーチンを、 `g_lpAllocateBuffer`、 `g_lpAllocateMore`および`g_lpFreeBuffer`パラメーターに保存します。</span><span class="sxs-lookup"><span data-stu-id="08699-116">The function saves the MAPI memory management routines into the  `g_lpAllocateBuffer`,  `g_lpAllocateMore`, and  `g_lpFreeBuffer` parameters.</span></span> <span data-ttu-id="08699-117">これらのメモリ管理ルーチンは、メモリの割り当てと解放のために、ラップされた PST ストアの実装全体で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08699-117">These memory management routines should be used throughout the wrapped PST store implementation for memory allocation and deallocation.</span></span> 
  
### <a name="msproviderinit-example"></a><span data-ttu-id="08699-118">msproviderinit () の例</span><span class="sxs-lookup"><span data-stu-id="08699-118">MSProviderInit() example</span></span>

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

### <a name="wrapped-pst-and-unicode-paths"></a><span data-ttu-id="08699-119">ラップされた PST および Unicode パス</span><span class="sxs-lookup"><span data-stu-id="08699-119">Wrapped PST and Unicode paths</span></span>

<span data-ttu-id="08699-120">unicode 対応の microsoft outlook 2010 および outlook 2013 で使用するために、NST への unicode パスを使用するために、microsoft Visual Studio 2008 で準備された元のサンプルを retrofit するには、エントリ識別子を生成する**createstoreentryid**ルーチンを使用する必要があります。1つは ASCII パスで、もう1つは Unicode パスです。</span><span class="sxs-lookup"><span data-stu-id="08699-120">To retrofit the original sample prepared in Microsoft Visual Studio 2008 to use Unicode paths to the NST for use in Unicode-enabled Microsoft Outlook 2010 and Outlook 2013, the **CreateStoreEntryID** routine, which produces the entry identifier, should use one format for ASCII paths, and another for Unicode paths.</span></span> <span data-ttu-id="08699-121">次の例では、これらは構造体として表されています。</span><span class="sxs-lookup"><span data-stu-id="08699-121">These are represented as structures in the following example.</span></span> 
  
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
> <span data-ttu-id="08699-122">これらの構造体の違いは、Unicode パスの前の2つの NULL バイトです。</span><span class="sxs-lookup"><span data-stu-id="08699-122">The differences in these structures are two NULL bytes prior to a Unicode path.</span></span> <span data-ttu-id="08699-123">次の「サービスエントリルーチン」のエントリ識別子を解釈する必要がある場合は、最初に eidms としてキャストするかどうかを確認してから、szpath [0] が NULL かどうかを確認する方法の1つです。</span><span class="sxs-lookup"><span data-stu-id="08699-123">If you need to interpret the entry identifier in the "Service Entry Routine" that follows, one way to determine whether that is the case or not would be to cast as EIDMS first, then check whether the szPath[0] is NULL.</span></span> <span data-ttu-id="08699-124">その場合は、代わりに EIDMSW としてキャストします。</span><span class="sxs-lookup"><span data-stu-id="08699-124">If it is, cast it as EIDMSW instead.</span></span> 
  
## <a name="service-entry-routine"></a><span data-ttu-id="08699-125">サービスエントリルーチン</span><span class="sxs-lookup"><span data-stu-id="08699-125">Service Entry routine</span></span>

<span data-ttu-id="08699-126">**[msgserviceentry](msgserviceentry.md)** 関数は、ラップされた PST ストアプロバイダーが構成されているメッセージサービスエントリポイントです。</span><span class="sxs-lookup"><span data-stu-id="08699-126">The **[MSGSERVICEENTRY](msgserviceentry.md)** function is the message service entry point where the wrapped PST store provider is configured.</span></span> <span data-ttu-id="08699-127">MAPI メモリ管理`GetMemAllocRoutines()`ルーチンを取得する関数呼び出し。</span><span class="sxs-lookup"><span data-stu-id="08699-127">The function calls  `GetMemAllocRoutines()` to get the MAPI memory management routines.</span></span> <span data-ttu-id="08699-128">この関数は、 `lpProviderAdmin`パラメーターを使用してプロバイダーのプロファイルセクションを見つけ、プロファイルのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="08699-128">The function uses the  `lpProviderAdmin` parameter to locate the profile section for the provider and sets the properties in the profile.</span></span> 
  
### <a name="serviceentry-example"></a><span data-ttu-id="08699-129">serviceentry () の例</span><span class="sxs-lookup"><span data-stu-id="08699-129">ServiceEntry() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="08699-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="08699-130">See also</span></span>

- [<span data-ttu-id="08699-131">ラップされた PST ストアプロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="08699-131">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="08699-132">ラップされた PST ストアプロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="08699-132">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="08699-133">ラップされた PST ストアプロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="08699-133">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="08699-134">ラップされた PST ストアプロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="08699-134">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="08699-135">ラップされた PST ストアプロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="08699-135">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

