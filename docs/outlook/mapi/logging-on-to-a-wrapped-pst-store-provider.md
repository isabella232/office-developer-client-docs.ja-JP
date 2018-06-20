---
title: ラップされた PST ストア プロバイダーにログオンしています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: 2dfa3820d8d2ab57f278e90bef5d5a40164da6fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801270"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="40412-103">ラップされた PST ストア プロバイダーにログオンしています。</span><span class="sxs-lookup"><span data-stu-id="40412-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="40412-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40412-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40412-105">MAPI は、ラップされた PST ストア プロバイダーにログオンすることができます、前に初期化し、ラップされた個人用フォルダー ファイル (PST) のストア プロバイダーを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40412-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="40412-106">詳細については、[ラップの PST ストア プロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40412-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="40412-107">初期化し、ラップされた PST ストア プロバイダーを構成した後、2 つのログオン ルーチンを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40412-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="40412-108">**[IMSProvider::Logon](imsprovider-logon.md)** 関数は、MAPI、ラップされた PST ストア プロバイダーにログオンします。</span><span class="sxs-lookup"><span data-stu-id="40412-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="40412-109">**[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** 関数は、ラップされた PST ストア プロバイダーに MAPI スプーラーによってログオンします。</span><span class="sxs-lookup"><span data-stu-id="40412-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="40412-110">このトピックでは、 **IMSProvider::Logon**関数および**IMSProvider::SpoolerLogon**関数はサンプル ラップ PST ストア プロバイダーのコード例を使用して説明します。</span><span class="sxs-lookup"><span data-stu-id="40412-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="40412-111">レプリケーション API と連携して使用するものでは、ラップされた PST プロバイダーを実装します。</span><span class="sxs-lookup"><span data-stu-id="40412-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="40412-112">ダウンロードとサンプル ラップ PST ストア プロバイダーをインストールする方法の詳細については、「[サンプル ラップ PST ストア プロバイダーをインストールする](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40412-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="40412-113">レプリケーション API の詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40412-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="40412-114">MAPI および MAPI スプーラーがログに記録した後にラップされた pst ファイルには、プロバイダーを格納、使用する準備ができてです。</span><span class="sxs-lookup"><span data-stu-id="40412-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="40412-115">詳細については、「[ラップの PST ストア プロバイダー](using-a-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40412-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="40412-116">MAPI ログオン ルーチン</span><span class="sxs-lookup"><span data-stu-id="40412-116">MAPI Logon routine</span></span>

<span data-ttu-id="40412-117">ラップされた PST ストア プロバイダーが初期化された後は、ラップされた PST ストアに、MAPI ログオンを**[IMSProvider::Logon](imsprovider-logon.md)** 関数を実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="40412-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="40412-118">この関数は、ユーザーの資格情報を検証し、プロバイダーの構成のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="40412-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="40412-119">実装する必要があります、 `SetOLFIInOST` 、オフライン ファイルの情報 (**[OLFI](olfi.md)** ) を設定します。</span><span class="sxs-lookup"><span data-stu-id="40412-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="40412-120">**OLFI**は、新しいメッセージまたはオフライン モードでのフォルダーのエントリ ID を割り当てるには、ラップされた PST ストア プロバイダーによって使用される ID の長期的な構造体のキューです。</span><span class="sxs-lookup"><span data-stu-id="40412-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="40412-121">最後に、 **IMSProvider::Logon**関数オブジェクトを返します、メッセージ ストア内に MAPI スプーラーとクライアント アプリケーションがログオンできること、`ppMDB`のパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="40412-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="40412-122">CMSProvider::Logon() の使用例</span><span class="sxs-lookup"><span data-stu-id="40412-122">CMSProvider::Logon() example</span></span>

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

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="40412-123">MAPI スプーラー ログオン ルーチン</span><span class="sxs-lookup"><span data-stu-id="40412-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="40412-124">**IMSProvider::Logon**と同様に、ラップされた PST ストアに、MAPI スプーラーをログに記録する**[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** 関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40412-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="40412-125">MAPI スプーラーとクライアント アプリケーションがログオンすることができるメッセージ ストア オブジェクトが返され、`ppMDB`のパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="40412-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="40412-126">CMSProvider::SpoolerLogon() の使用例</span><span class="sxs-lookup"><span data-stu-id="40412-126">CMSProvider::SpoolerLogon() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="40412-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="40412-127">See also</span></span>

- [<span data-ttu-id="40412-128">サンプルの PST ストア プロバイダーをラップ</span><span class="sxs-lookup"><span data-stu-id="40412-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="40412-129">PST ストア プロバイダーをラップして、サンプルをインストールします。</span><span class="sxs-lookup"><span data-stu-id="40412-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="40412-130">ラップされた PST ストア プロバイダーを初期化しています。</span><span class="sxs-lookup"><span data-stu-id="40412-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="40412-131">ラップされた PST ストア プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="40412-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="40412-132">ラップされた PST ストア プロバイダーをシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="40412-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

