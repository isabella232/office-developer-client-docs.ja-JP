---
title: ラップされた PST ストア プロバイダーへのログオン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408987"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="d16c4-103">ラップされた PST ストア プロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="d16c4-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="d16c4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d16c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d16c4-105">ラップされた PST ストア プロバイダーに MAPI をログオンする前に、ラップされた個人用フォルダー ファイル (PST) ストア プロバイダーを初期化して構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d16c4-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="d16c4-106">詳細については、「ラップされた PST ストア [プロバイダーの初期化」を参照してください](initializing-a-wrapped-pst-store-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="d16c4-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="d16c4-107">ラップされた PST ストア プロバイダーを初期化して構成した後、2 つのログオン ルーチンを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d16c4-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="d16c4-108">**[IMSProvider::Logon 関数は](imsprovider-logon.md)**、MAPI でラップされた PST ストア プロバイダーにログを記録します。</span><span class="sxs-lookup"><span data-stu-id="d16c4-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="d16c4-109">**[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** 関数は、MAPI スプーラーにラップされた PST ストア プロバイダーにログを記録します。</span><span class="sxs-lookup"><span data-stu-id="d16c4-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="d16c4-110">このトピックでは、サンプル ラップ PST ストア プロバイダーのコード例を使用して **、IMSProvider::Logon** 関数と **IMSProvider::SpoolerLogon** 関数を示します。</span><span class="sxs-lookup"><span data-stu-id="d16c4-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="d16c4-111">このサンプルでは、レプリケーション API と組み合わせて使用することを目的としたラップされた PST プロバイダーを実装しています。</span><span class="sxs-lookup"><span data-stu-id="d16c4-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="d16c4-112">サンプル ラップ PST ストア プロバイダーのダウンロードとインストールの詳細については、「サンプル ラップされた PST ストア プロバイダーのインストール [」を参照してください](installing-the-sample-wrapped-pst-store-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="d16c4-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="d16c4-113">レプリケーション API の詳細については、「レプリケーション [API について」を参照してください](about-the-replication-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d16c4-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="d16c4-114">MAPI と MAPI スプーラーがラップされた PST ストア プロバイダーにログオンした後、使用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="d16c4-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="d16c4-115">詳細については、「Wrapped [PST ストア プロバイダーの使用」を参照してください](using-a-wrapped-pst-store-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="d16c4-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="d16c4-116">MAPI ログオン ルーチン</span><span class="sxs-lookup"><span data-stu-id="d16c4-116">MAPI Logon routine</span></span>

<span data-ttu-id="d16c4-117">ラップされた PST ストア プロバイダーが初期化された後、ラップされた PST ストアに MAPI にログオンするには **[、IMSProvider::Logon](imsprovider-logon.md)** 関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d16c4-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="d16c4-118">この関数は、ユーザー資格情報を検証し、プロバイダーの構成プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="d16c4-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="d16c4-119">オフライン ファイル情報  `SetOLFIInOST` **[(OLFI)](olfi.md)** を設定する関数も実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d16c4-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="d16c4-120">**OLFI** は、ラップされた PST ストア プロバイダーがオフライン モードで新しいメッセージまたはフォルダーのエントリ ID を割り当てるのに使用する長期 ID 構造のキューです。</span><span class="sxs-lookup"><span data-stu-id="d16c4-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="d16c4-121">最後に **、IMSProvider::Logon** 関数は、MAPI スプーラーとクライアント アプリケーションがパラメーターにログオンできるメッセージ ストア オブジェクトを返  `ppMDB` します。</span><span class="sxs-lookup"><span data-stu-id="d16c4-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="d16c4-122">CMSProvider::Logon() の例</span><span class="sxs-lookup"><span data-stu-id="d16c4-122">CMSProvider::Logon() example</span></span>

```cpp
STDMETHODIMP CMSProvider::Logon( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG * pcbSpoolSecurity, 
    LPBYTE * ppbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMDB lpPSTMDB = NULL; 
    CMsgStore* pWrappedMDB = NULL; 
 
    Log(true,"CMSProvider::Logon Pst logon Called\n"); 
 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        ulFlags = (ulFlags & ~MDB_OST_LOGON_ANSI) | MDB_OST_LOGON_UNICODE; 
        hRes = m_pPSTMS->Logon( 
            pMySup, 
            ulUIParam,  
            pszProfileName,  
            cbEntryID, 
            pEntryID,  
            ulFlags,  
            pInterface,  
            pcbSpoolSecurity, 
            ppbSpoolSecurity,  
            ppMAPIError,  
            ppMSLogon,  
            &lpPSTMDB); 
    } 
    Log(true,"CMSProvider::Logon returned 0x%08X\n", hRes); 
 
    // Set up the MDB to allow synchronization 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = SetOLFIInOST(lpPSTMDB); 
        Log(true,"SetOLFIInOST returned 0x%08X\n", hRes); 
    } 
    // Wrap the outgoing MDB 
    pWrappedMDB = new CMsgStore (lpPSTMDB); 
    if (NULL == pWrappedMDB) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CMsgStore object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    // Copy pointer to the allocated object back into the return LPMDB object pointer 
    *ppMDB = pWrappedMDB; 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="d16c4-123">MAPI スプーラー ログオン ルーチン</span><span class="sxs-lookup"><span data-stu-id="d16c4-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="d16c4-124">**IMSProvider::Logon** と同様に、MAPI スプーラーをラップされた PST ストアに記録するには **[、IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** 関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d16c4-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="d16c4-125">MAPI スプーラーとクライアント アプリケーションがログオンできるメッセージ ストア オブジェクトがパラメーターに返  `ppMDB` されます。</span><span class="sxs-lookup"><span data-stu-id="d16c4-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="d16c4-126">CMSProvider::SpoolerLogon() の例</span><span class="sxs-lookup"><span data-stu-id="d16c4-126">CMSProvider::SpoolerLogon() example</span></span>

```cpp
STDMETHODIMP CMSProvider::SpoolerLogon ( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG cbSpoolSecurity, 
    LPBYTE pbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
     
    Log(true,"CMSProvider::SpoolerLogon\n"); 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::SpoolerLogon: " + 
            "Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = m_pPSTMS->SpoolerLogon(  
            pMySup,//pSupObj, 
            ulUIParam, 
            pszProfileName, 
            cbEntryID, 
            pEntryID, 
            ulFlags, 
            pInterface, 
            cbSpoolSecurity, 
            pbSpoolSecurity, 
            ppMAPIError, 
            ppMSLogon, 
            ppMDB); 
    } 
    Log(true,"CMSProvider::SpoolerLogon returned 0x%08X\n", hRes); 
 
    return hRes; 
}
```

## <a name="see-also"></a><span data-ttu-id="d16c4-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="d16c4-127">See also</span></span>

- [<span data-ttu-id="d16c4-128">ラップされた PST ストア プロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="d16c4-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="d16c4-129">ラップされた PST ストア プロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="d16c4-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="d16c4-130">ラップされた PST ストア プロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="d16c4-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="d16c4-131">ラップされた PST ストア プロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="d16c4-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="d16c4-132">ラップされた PST ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="d16c4-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

