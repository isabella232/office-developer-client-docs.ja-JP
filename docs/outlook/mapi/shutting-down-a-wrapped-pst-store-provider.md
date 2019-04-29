---
title: ラップされた PST ストアプロバイダーのシャットダウン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: '最終更新日: 2012 年7月2日'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409945"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="dc21c-103">ラップされた PST ストアプロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="dc21c-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="dc21c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc21c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc21c-105">ラップされた個人用フォルダーファイル (pst) ストアプロバイダーの使用が終了したら、ラップされた PST ストアプロバイダーを適切にシャットダウンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc21c-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="dc21c-106">ラップされた pst ストアプロバイダーの使用の詳細については、「ラップされ[た pst ストアプロバイダーの使用](using-a-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc21c-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="dc21c-107">ラップされた PST ストアプロバイダーをシャットダウンするには、 **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** 関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc21c-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="dc21c-108">この関数は、ラップされた PST ストアプロバイダーを正しい順序で閉じます。</span><span class="sxs-lookup"><span data-stu-id="dc21c-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="dc21c-109">このトピックでは、サンプルのラップされた PST ストアプロバイダーのコード例を使用して、 **IMSProvider:: Shutdown**関数をデモンストレーションします。</span><span class="sxs-lookup"><span data-stu-id="dc21c-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="dc21c-110">このサンプルでは、レプリケーション API と共に使用することを目的とした、ラップされた PST プロバイダーを実装しています。</span><span class="sxs-lookup"><span data-stu-id="dc21c-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="dc21c-111">サンプルのラップされた pst ストアプロバイダーのダウンロードとインストールの詳細については、「[サンプルのラップされた pst ストアプロバイダーのインストール](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc21c-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="dc21c-112">レプリケーション api の詳細については、「[レプリケーション api につい](about-the-replication-api.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc21c-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="dc21c-113">ルーチンをシャットダウンする</span><span class="sxs-lookup"><span data-stu-id="dc21c-113">Shut Down Routine</span></span>

<span data-ttu-id="dc21c-114">MAPI スプーラーは、ラップされた pst ストアプロバイダーを適切にシャットダウンできるように、ラップされた pst ストアプロバイダーを解放する直前に、 **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dc21c-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="dc21c-115">この関数は、ラップされた PST ストアプロバイダーに関連付けられているすべてのセッションオブジェクトを終了します。</span><span class="sxs-lookup"><span data-stu-id="dc21c-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="dc21c-116">cmsprovider:: ShutDown () の例</span><span class="sxs-lookup"><span data-stu-id="dc21c-116">CMSProvider::ShutDown() Example</span></span>

```cpp
STDMETHODIMP CMSProvider::Shutdown(ULONG * pulFlags) 
{ 
    HRESULT hRes = S_OK; 
    Log(true,"CMSProvider::Shutdown\n"); 
    hRes =m_pPSTMS->Shutdown(pulFlags); 
    Log(true,"CMSProvider::Shutdown returned: 0x%08X\n", hRes); 
    return hRes ;  
}
```

## <a name="see-also"></a><span data-ttu-id="dc21c-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc21c-117">See also</span></span>



[<span data-ttu-id="dc21c-118">ラップされた PST ストアプロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="dc21c-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="dc21c-119">ラップされた PST ストアプロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="dc21c-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="dc21c-120">ラップされた PST ストアプロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="dc21c-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="dc21c-121">ラップされた PST ストアプロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="dc21c-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="dc21c-122">ラップされた PST ストアプロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="dc21c-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

