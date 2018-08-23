---
title: ラップされた PST ストア プロバイダーを使用します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: 4a2ccbbcdd3459af6b69156d80b37695251ba8d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804194"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="93949-103">ラップされた PST ストア プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="93949-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="93949-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93949-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93949-105">ラップされた個人用フォルダー ファイル (PST) のストア プロバイダーを使用することができます、前に初期化し、ラップされた PST ストア プロバイダーを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93949-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="93949-106">ラップされた PST ストア プロバイダーを構成した後、できるように、MAPI スプーラーと MAPI にログオンできます、メッセージ ストア プロバイダーの機能を実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="93949-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="93949-107">初期化し、ラップされた PST ストア プロバイダーへのログインの詳細については、[ラップ PST ストア プロバイダーを初期化](initializing-a-wrapped-pst-store-provider.md)し、[ラップ PST ストア プロバイダーへのログ](logging-on-to-a-wrapped-pst-store-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93949-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="93949-108">**[IMAPISupport::IUnknown](imapisupportiunknown.md)** インターフェイスは、プロバイダーを格納するメッセージでよく実行されるタスクの実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="93949-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="93949-109">サンプル ラップ PST ストア プロバイダーの機能をこのインターフェイスをラップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="93949-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="93949-110">**[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** 関数には、特別な実装が必要です。</span><span class="sxs-lookup"><span data-stu-id="93949-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="93949-111">他のすべての関数は、ラップされたオブジェクトにパラメーターを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="93949-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="93949-112">このトピックでは、 **IMAPISupport::OpenProfileSection**関数はサンプル ラップ PST ストア プロバイダーのコード例を使用して示されます。</span><span class="sxs-lookup"><span data-stu-id="93949-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="93949-113">レプリケーション API と連携して使用するものでは、ラップされた PST プロバイダーを実装します。</span><span class="sxs-lookup"><span data-stu-id="93949-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="93949-114">ダウンロードとサンプル ラップ PST ストア プロバイダーをインストールする方法の詳細については、「[サンプル ラップ PST ストア プロバイダーをインストールする](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93949-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="93949-115">レプリケーション API の詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93949-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="93949-116">ラップされた PST ストア プロバイダーを使用してが完了したらは、ラップされた PST ストア プロバイダーをシャット ダウンする必要があります正しく。</span><span class="sxs-lookup"><span data-stu-id="93949-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="93949-117">詳細については、[シャット ダウン、ラップされた PST ストア プロバイダー](shutting-down-a-wrapped-pst-store-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93949-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="93949-118">プロファイル セクションの開いているルーチン</span><span class="sxs-lookup"><span data-stu-id="93949-118">Open Profile Section routine</span></span>

<span data-ttu-id="93949-119">**[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** 関数は、現在のプロファイルのセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="93949-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="93949-120">関数は、ラップされた PST ストア プロバイダーの実装で特別な処理を必要とします。</span><span class="sxs-lookup"><span data-stu-id="93949-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="93949-121">`pgNSTGlobalProfileSectionGuid`が要求されると、キャッシュされているプロファイルのセクションを返します。</span><span class="sxs-lookup"><span data-stu-id="93949-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="93949-122">CSupport::OpenProfileSection() の使用例</span><span class="sxs-lookup"><span data-stu-id="93949-122">CSupport::OpenProfileSection() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="93949-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="93949-123">See also</span></span>

- [<span data-ttu-id="93949-124">ラップされた PST ストア プロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="93949-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="93949-125">ラップされた PST ストア プロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="93949-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="93949-126">ラップされた PST ストア プロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="93949-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="93949-127">ラップされた PST ストア プロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="93949-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="93949-128">ラップされた PST ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="93949-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

