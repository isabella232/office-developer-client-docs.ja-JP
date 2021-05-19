---
title: ラップされた PST ストア プロバイダーのシャットダウン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409945"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="d221b-103">ラップされた PST ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="d221b-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="d221b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d221b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d221b-105">ラップされた個人用フォルダー ファイル (PST) ストア プロバイダーの使用が完了したら、ラップされた PST ストア プロバイダーを適切にシャットダウンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d221b-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="d221b-106">ラップされた PST ストア プロバイダーの使用の詳細については、「Wrapped PST ストア プロバイダーの使用 [」を参照してください](using-a-wrapped-pst-store-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="d221b-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="d221b-107">ラップされた PST ストア プロバイダーをシャットダウンするには **[、IMSProvider::Shutdown 関数を呼び出す必要](imsprovider-shutdown.md)** があります。</span><span class="sxs-lookup"><span data-stu-id="d221b-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="d221b-108">この関数は、ラップされた PST ストア プロバイダーを順番に閉じます。</span><span class="sxs-lookup"><span data-stu-id="d221b-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="d221b-109">このトピックでは、サンプル ラップされた PST ストア プロバイダーのコード例を使用して **、IMSProvider::Shutdown** 関数を示します。</span><span class="sxs-lookup"><span data-stu-id="d221b-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="d221b-110">このサンプルでは、レプリケーション API と組み合わせて使用することを目的としたラップされた PST プロバイダーを実装しています。</span><span class="sxs-lookup"><span data-stu-id="d221b-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="d221b-111">サンプル ラップ PST ストア プロバイダーのダウンロードとインストールの詳細については、「サンプル ラップされた PST ストア プロバイダーのインストール [」を参照してください](installing-the-sample-wrapped-pst-store-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="d221b-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="d221b-112">レプリケーション API の詳細については、「レプリケーション [API について」を参照してください](about-the-replication-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d221b-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="d221b-113">シャットダウン ルーチン</span><span class="sxs-lookup"><span data-stu-id="d221b-113">Shut Down Routine</span></span>

<span data-ttu-id="d221b-114">MAPI スプーラーは、ラップされた PST ストア プロバイダーが適切にシャットダウンできるよう、ラップされた PST ストア プロバイダーを解放する直前に **[IMSProvider::Shutdown](imsprovider-shutdown.md)** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d221b-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="d221b-115">この関数は、ラップされた PST ストア プロバイダーに関連付けられているすべてのセッション オブジェクトを終了します。</span><span class="sxs-lookup"><span data-stu-id="d221b-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="d221b-116">CMSProvider::ShutDown() の例</span><span class="sxs-lookup"><span data-stu-id="d221b-116">CMSProvider::ShutDown() Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="d221b-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="d221b-117">See also</span></span>



[<span data-ttu-id="d221b-118">ラップされた PST ストア プロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="d221b-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="d221b-119">ラップされた PST ストア プロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="d221b-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="d221b-120">ラップされた PST ストア プロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="d221b-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="d221b-121">ラップされた PST ストア プロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="d221b-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="d221b-122">ラップされた PST ストア プロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="d221b-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

