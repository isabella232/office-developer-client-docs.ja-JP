---
title: ラップされた PST ストア プロバイダーのシャットダウン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: 5c8ad7443b0c1aa05f48284e4b09859ab53dd2c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803910"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="81aa6-103">ラップされた PST ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="81aa6-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="81aa6-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="81aa6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="81aa6-105">ラップされた個人用フォルダー ファイル (PST) のストア プロバイダーの使用が終了したら後、は、ラップされた PST ストア プロバイダーをシャット ダウンする必要があります正しく。</span><span class="sxs-lookup"><span data-stu-id="81aa6-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="81aa6-106">ラップされた PST ストア プロバイダーの使用に関する詳細については、「[ラップされた PST ストア プロバイダー](using-a-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81aa6-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="81aa6-107">ラップされた PST ストア プロバイダーを停止するには、 **[IMSProvider::Shutdown](imsprovider-shutdown.md)** 関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="81aa6-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="81aa6-108">この関数は、正しい順序でラップされた PST ストア プロバイダーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="81aa6-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="81aa6-109">このトピックでは、 **IMSProvider::Shutdown**関数はサンプル ラップ PST ストア プロバイダーのコード例を使用して示されます。</span><span class="sxs-lookup"><span data-stu-id="81aa6-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="81aa6-110">レプリケーション API と連携して使用するものでは、ラップされた PST プロバイダーを実装します。</span><span class="sxs-lookup"><span data-stu-id="81aa6-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="81aa6-111">ダウンロードとサンプル ラップ PST ストア プロバイダーをインストールする方法の詳細については、「[サンプル ラップ PST ストア プロバイダーをインストールする](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81aa6-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="81aa6-112">レプリケーション API の詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81aa6-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="81aa6-113">シャット ダウン ルーチン</span><span class="sxs-lookup"><span data-stu-id="81aa6-113">Shut Down Routine</span></span>

<span data-ttu-id="81aa6-114">MAPI スプーラーは、ラップされた PST ストア プロバイダーが正常にシャット ダウンするようにラップされた PST ストア プロバイダーを解放する前に、 **[IMSProvider::Shutdown](imsprovider-shutdown.md)** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="81aa6-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="81aa6-115">関数は、ラップされた PST ストア プロバイダーに関連付けられているすべてのセッション オブジェクトを終了します。</span><span class="sxs-lookup"><span data-stu-id="81aa6-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="81aa6-116">CMSProvider::ShutDown() の使用例</span><span class="sxs-lookup"><span data-stu-id="81aa6-116">CMSProvider::ShutDown() Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="81aa6-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="81aa6-117">See also</span></span>



[<span data-ttu-id="81aa6-118">ラップされた PST ストア プロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="81aa6-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="81aa6-119">ラップされた PST ストア プロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="81aa6-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="81aa6-120">ラップされた PST ストア プロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="81aa6-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="81aa6-121">ラップされた PST ストア プロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="81aa6-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="81aa6-122">ラップされた PST ストア プロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="81aa6-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

