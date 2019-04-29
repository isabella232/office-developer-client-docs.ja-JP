---
title: ラップされた PST ストア プロバイダーの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: '最終更新日: 2012 年7月3日'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420823"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="5a273-103">ラップされた PST ストア プロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="5a273-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="5a273-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a273-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a273-105">ラップされた個人用フォルダーファイル (PST) ストアプロバイダーを使用する前に、ラップされた PST ストアプロバイダーを初期化して構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a273-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="5a273-106">ラップされた PST ストアプロバイダーを構成した後、mapi および mapi スプーラーがメッセージストアプロバイダーにログオンできるように、関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a273-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="5a273-107">ラップされた pst ストアプロバイダーの初期化とログオンの詳細については、「ラップされた pst ストア[プロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)と、ラップされた[pst ストアプロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a273-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="5a273-108">**[imapisupport:: IUnknown](imapisupportiunknown.md)** インターフェイスは、メッセージストアプロバイダーが一般的に実行するタスクの実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a273-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="5a273-109">このインターフェイスは、サンプルのラップされた PST ストアプロバイダーが機能するようにラップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a273-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="5a273-110">**[imapisupport:: openプロファイル](imapisupport-openprofilesection.md)** の各関数には、特別な実装が必要です。</span><span class="sxs-lookup"><span data-stu-id="5a273-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="5a273-111">他のすべての関数は、パラメーターを基になるラップされたオブジェクトに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="5a273-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="5a273-112">このトピックでは、サンプルのラップされた PST ストアプロバイダーのコード例を使用して、 **imapisupport:: openプロファイル**の使い方を示します。</span><span class="sxs-lookup"><span data-stu-id="5a273-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="5a273-113">このサンプルでは、レプリケーション API と共に使用することを目的とした、ラップされた PST プロバイダーを実装しています。</span><span class="sxs-lookup"><span data-stu-id="5a273-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="5a273-114">サンプルのラップされた pst ストアプロバイダーのダウンロードとインストールの詳細については、「[サンプルのラップされた pst ストアプロバイダーのインストール](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a273-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="5a273-115">レプリケーション api の詳細については、「[レプリケーション api につい](about-the-replication-api.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a273-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="5a273-116">ラップされた pst ストアプロバイダーの使用が終了したら、ラップされた pst ストアプロバイダーを適切にシャットダウンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a273-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="5a273-117">詳細については、「ラップされ[た PST ストアプロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a273-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="5a273-118">プロファイルセクションルーチンを開く</span><span class="sxs-lookup"><span data-stu-id="5a273-118">Open Profile Section routine</span></span>

<span data-ttu-id="5a273-119">**[imapisupport:: openプロファイル](imapisupport-openprofilesection.md)** のセクションは、現在のプロファイルのセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="5a273-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="5a273-120">この関数では、ラップされた PST ストアプロバイダーの実装で、特別な処理を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a273-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="5a273-121">`pgNSTGlobalProfileSectionGuid`が要求されると、関数はキャッシュされたプロファイルセクションを返します。</span><span class="sxs-lookup"><span data-stu-id="5a273-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="5a273-122">csupport:: openプロファイルの例 () の例</span><span class="sxs-lookup"><span data-stu-id="5a273-122">CSupport::OpenProfileSection() example</span></span>

```cpp
STDMETHODIMP CSupport::OpenProfileSection( 
    LPMAPIUID lpUid,     
    ULONG ulFlags, 
    LPPROFSECT * lppProfileObj) 
{ 
    Log(true,"CSupport::OpenProfileSection\n"); 
    if (lpUid &&  
        IsEqualMAPIUID(lpUid, (void *)&pbNSTGlobalProfileSectionGuid) &&  
        m_lpProfSect) 
    {      
        // Allow the opening of the Global Section 
        if (m_lpProfSect) 
        { 
            *lppProfileObj = m_lpProfSect; 
            (*lppProfileObj)->AddRef(); 
            return S_OK; 
        } 
    } 
    return m_pMAPISup->OpenProfileSection(lpUid, ulFlags, lppProfileObj); 
}
```

## <a name="see-also"></a><span data-ttu-id="5a273-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a273-123">See also</span></span>

- [<span data-ttu-id="5a273-124">ラップされた PST ストアプロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="5a273-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5a273-125">ラップされた PST ストアプロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="5a273-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5a273-126">ラップされた PST ストアプロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="5a273-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5a273-127">ラップされた PST ストアプロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="5a273-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5a273-128">ラップされた PST ストアプロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="5a273-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

