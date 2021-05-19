---
title: ラップされた PST ストア プロバイダーの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420823"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="5052c-103">ラップされた PST ストア プロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="5052c-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="5052c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5052c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5052c-105">ラップされた個人用フォルダー ファイル (PST) ストア プロバイダーを使用する前に、ラップされた PST ストア プロバイダーを初期化して構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5052c-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="5052c-106">ラップされた PST ストア プロバイダーを構成した後、MAPI と MAPI スプーラーがメッセージ ストア プロバイダーにログオンできるよう、関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5052c-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="5052c-107">ラップされた PST ストア プロバイダーへの初期化とログオンの詳細については、「ラップされた PST ストア プロバイダーの初期化とラップ [された PST](initializing-a-wrapped-pst-store-provider.md) ストア プロバイダーへのログオン」を [参照してください](logging-on-to-a-wrapped-pst-store-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="5052c-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="5052c-108">**[IMAPISupport::IUnknown](imapisupportiunknown.md)** インターフェイスは、メッセージ ストア プロバイダーによって一般的に実行されるタスクの実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="5052c-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="5052c-109">このインターフェイスは、サンプル ラップされた PST ストア プロバイダーが動作するためにラップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5052c-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="5052c-110">**[IMAPISupport::OpenProfileSection 関数には](imapisupport-openprofilesection.md)** 特別な実装が必要です。</span><span class="sxs-lookup"><span data-stu-id="5052c-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="5052c-111">他のすべての関数は、基になるラップされたオブジェクトにパラメーターを渡す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5052c-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="5052c-112">このトピックでは **、IMAPISupport::OpenProfileSection** 関数について、サンプル ラップ PST ストア プロバイダーのコード例を使用して説明します。</span><span class="sxs-lookup"><span data-stu-id="5052c-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="5052c-113">このサンプルでは、レプリケーション API と組み合わせて使用することを目的としたラップされた PST プロバイダーを実装しています。</span><span class="sxs-lookup"><span data-stu-id="5052c-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="5052c-114">サンプル ラップ PST ストア プロバイダーのダウンロードとインストールの詳細については、「サンプル ラップされた PST ストア プロバイダーのインストール [」を参照してください](installing-the-sample-wrapped-pst-store-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="5052c-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="5052c-115">レプリケーション API の詳細については、「レプリケーション [API について」を参照してください](about-the-replication-api.md)。</span><span class="sxs-lookup"><span data-stu-id="5052c-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="5052c-116">ラップされた PST ストア プロバイダーの使用が完了したら、ラップされた PST ストア プロバイダーを適切にシャットダウンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5052c-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="5052c-117">詳細については、「ラップされた PST ストア プロバイダー [をシャットダウンする」を参照してください](shutting-down-a-wrapped-pst-store-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="5052c-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="5052c-118">Open Profile Section ルーチン</span><span class="sxs-lookup"><span data-stu-id="5052c-118">Open Profile Section routine</span></span>

<span data-ttu-id="5052c-119">**[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** 関数は、現在のプロファイルのセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="5052c-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="5052c-120">この関数では、ラップされた PST ストア プロバイダーの実装で特別な処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="5052c-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="5052c-121">要求された  `pgNSTGlobalProfileSectionGuid` 場合、関数はキャッシュされるプロファイル セクションを返します。</span><span class="sxs-lookup"><span data-stu-id="5052c-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="5052c-122">CSupport::OpenProfileSection() の例</span><span class="sxs-lookup"><span data-stu-id="5052c-122">CSupport::OpenProfileSection() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="5052c-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="5052c-123">See also</span></span>

- [<span data-ttu-id="5052c-124">ラップされた PST ストア プロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="5052c-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5052c-125">ラップされた PST ストア プロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="5052c-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5052c-126">ラップされた PST ストア プロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="5052c-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5052c-127">ラップされた PST ストア プロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="5052c-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5052c-128">ラップされた PST ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="5052c-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

