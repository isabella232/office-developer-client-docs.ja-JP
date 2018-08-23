---
title: ラップされた PST ストア プロバイダーを初期化しています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: '最終更新日: 2012 年 10 月 05 日'
ms.openlocfilehash: c39f66917ecc080785b3a3e91506d3994427ca62
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569079"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a><span data-ttu-id="77813-103">ラップされた PST ストア プロバイダーを初期化しています。</span><span class="sxs-lookup"><span data-stu-id="77813-103">Initializing a wrapped PST store provider</span></span>

<span data-ttu-id="77813-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77813-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77813-105">ラップされた個人用フォルダー ファイル (PST) のストア プロバイダーを実装するためのエントリ ポイントとして、 **[MSProviderInit](msproviderinit.md)** 関数を使用して、ラップされた PST ストア プロバイダーを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77813-105">To implement a wrapped Personal Folders file (PST) store provider, you must initialize the wrapped PST store provider by using the **[MSProviderInit](msproviderinit.md)** function as an entry point.</span></span> <span data-ttu-id="77813-106">プロバイダーの DLL が初期化された後、 **[MSGSERVICEENTRY](msgserviceentry.md)** 関数は、ラップされた PST ストア プロバイダーを構成します。</span><span class="sxs-lookup"><span data-stu-id="77813-106">After the provider's DLL is initialized, the **[MSGSERVICEENTRY](msgserviceentry.md)** function configures the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="77813-107">このトピックでは、 **MSProviderInit**関数および**MSGSERVICEENTRY**関数はサンプル ラップ PST ストア プロバイダーのコード例を使用して説明します。</span><span class="sxs-lookup"><span data-stu-id="77813-107">In this topic, the **MSProviderInit** function and the **MSGSERVICEENTRY** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="77813-108">レプリケーション API と連携して使用するものでは、ラップされた PST プロバイダーを実装します。</span><span class="sxs-lookup"><span data-stu-id="77813-108">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="77813-109">ダウンロードとサンプル ラップ PST ストア プロバイダーをインストールする方法の詳細については、「[サンプル ラップ PST ストア プロバイダーをインストールする](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77813-109">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="77813-110">レプリケーション API の詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77813-110">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="77813-111">ラップされた PST ストア プロバイダーを初期化すると、MAPI および MAPI スプーラーは、メッセージ ストア プロバイダーにログオンできるように関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77813-111">After you have initialized a wrapped PST store provider, you must implement functions so that MAPI and the MAPI spooler can log onto the message store provider.</span></span> <span data-ttu-id="77813-112">詳細については、[ラップされた PST ストア プロバイダーにログを](logging-on-to-a-wrapped-pst-store-provider.md)参照してください。</span><span class="sxs-lookup"><span data-stu-id="77813-112">For more information, see [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="initialization-routine"></a><span data-ttu-id="77813-113">初期化ルーチン</span><span class="sxs-lookup"><span data-stu-id="77813-113">Initialization routine</span></span>

<span data-ttu-id="77813-114">ラップされたすべての PST ストア プロバイダーは、プロバイダーの DLL を初期化するためにエントリ ポイントとして、 **[MSProviderInit](msproviderinit.md)** 関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77813-114">All wrapped PST store providers must implement the **[MSProviderInit](msproviderinit.md)** function as an entry point to initialize the provider's DLL.</span></span> <span data-ttu-id="77813-115">**MSProviderInit**をチェックするかどうか、サービス プロバイダーのインターフェイスのバージョン番号`ulMAPIVer`、現在のバージョン番号と互換性のある`CURRENT_SPI_VERSION`。</span><span class="sxs-lookup"><span data-stu-id="77813-115">**MSProviderInit** checks to see if the version number of the service provider interface,  `ulMAPIVer`, is compatible with the current version number,  `CURRENT_SPI_VERSION`.</span></span> <span data-ttu-id="77813-116">保存 MAPI メモリに管理ルーチンの関数、 `g_lpAllocateBuffer`、 `g_lpAllocateMore`、および`g_lpFreeBuffer`のパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="77813-116">The function saves the MAPI memory management routines into the  `g_lpAllocateBuffer`,  `g_lpAllocateMore`, and  `g_lpFreeBuffer` parameters.</span></span> <span data-ttu-id="77813-117">メモリの割り当てと割り当て解除には、ラップされた PST ストアの実装でこれらのメモリ管理ルーチンを使用してください。</span><span class="sxs-lookup"><span data-stu-id="77813-117">These memory management routines should be used throughout the wrapped PST store implementation for memory allocation and deallocation.</span></span> 
  
### <a name="msproviderinit-example"></a><span data-ttu-id="77813-118">MSProviderInit() の使用例</span><span class="sxs-lookup"><span data-stu-id="77813-118">MSProviderInit() example</span></span>

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

### <a name="wrapped-pst-and-unicode-paths"></a><span data-ttu-id="77813-119">ラップされた pst ファイルと Unicode のパス</span><span class="sxs-lookup"><span data-stu-id="77813-119">Wrapped PST and Unicode paths</span></span>

<span data-ttu-id="77813-120">NST への Unicode のパスを使用して、Unicode 対応の Microsoft Outlook 2010、Outlook 2013 で使用する Microsoft Visual Studio 2008 の準備をして、元のサンプルを改造するには、エントリの識別子を作成するには、 **CreateStoreEntryID**ルーチンを使用する必要があります。ASCII パス、および Unicode のパスの別の 1 つの形式です。</span><span class="sxs-lookup"><span data-stu-id="77813-120">To retrofit the original sample prepared in Microsoft Visual Studio 2008 to use Unicode paths to the NST for use in Unicode-enabled Microsoft Outlook 2010 and Outlook 2013, the **CreateStoreEntryID** routine, which produces the entry identifier, should use one format for ASCII paths, and another for Unicode paths.</span></span> <span data-ttu-id="77813-121">これらは、次の例では、構造体として表されます。</span><span class="sxs-lookup"><span data-stu-id="77813-121">These are represented as structures in the following example.</span></span> 
  
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
> <span data-ttu-id="77813-122">これらの構造の違いは、Unicode のパスの前に 2 つの NULL バイトです。</span><span class="sxs-lookup"><span data-stu-id="77813-122">The differences in these structures are two NULL bytes prior to a Unicode path.</span></span> <span data-ttu-id="77813-123">「サービス エントリ ルーチン」の後のエントリ id を解釈する必要があります、か、そうではあるかどうかを決定する方法の 1 つのように EIDMS し、先ず、szPath [0] が NULL であるかどうかをキャストするでしょう。</span><span class="sxs-lookup"><span data-stu-id="77813-123">If you need to interpret the entry identifier in the "Service Entry Routine" that follows, one way to determine whether that is the case or not would be to cast as EIDMS first, then check whether the szPath[0] is NULL.</span></span> <span data-ttu-id="77813-124">場合は、代わりに EIDMSW としてキャストします。</span><span class="sxs-lookup"><span data-stu-id="77813-124">If it is, cast it as EIDMSW instead.</span></span> 
  
## <a name="service-entry-routine"></a><span data-ttu-id="77813-125">サービス エントリ ルーチン</span><span class="sxs-lookup"><span data-stu-id="77813-125">Service Entry routine</span></span>

<span data-ttu-id="77813-126">**[MSGSERVICEENTRY](msgserviceentry.md)** 関数は、ラップされた PST ストア プロバイダーが構成されているメッセージ サービスのエントリ ポイントです。</span><span class="sxs-lookup"><span data-stu-id="77813-126">The **[MSGSERVICEENTRY](msgserviceentry.md)** function is the message service entry point where the wrapped PST store provider is configured.</span></span> <span data-ttu-id="77813-127">関数呼び出し`GetMemAllocRoutines()`MAPI のメモリ管理ルーチンを取得します。</span><span class="sxs-lookup"><span data-stu-id="77813-127">The function calls  `GetMemAllocRoutines()` to get the MAPI memory management routines.</span></span> <span data-ttu-id="77813-128">関数を使用して、`lpProviderAdmin`プロファイルにプロパティを設定、プロバイダーのプロファイル セクションを検索するパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="77813-128">The function uses the  `lpProviderAdmin` parameter to locate the profile section for the provider and sets the properties in the profile.</span></span> 
  
### <a name="serviceentry-example"></a><span data-ttu-id="77813-129">ServiceEntry() の使用例</span><span class="sxs-lookup"><span data-stu-id="77813-129">ServiceEntry() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="77813-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="77813-130">See also</span></span>

- [<span data-ttu-id="77813-131">ラップされた PST ストア プロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="77813-131">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="77813-132">ラップされた PST ストア プロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="77813-132">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="77813-133">ラップされた PST ストア プロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="77813-133">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="77813-134">ラップされた PST ストア プロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="77813-134">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="77813-135">ラップされた PST ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="77813-135">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

