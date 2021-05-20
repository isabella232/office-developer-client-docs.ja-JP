---
title: CreateMAPIInitializationMonitor
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: MAPI 初期化モニター
Last modified: April 26, 2021
ms.openlocfilehash: da7c48a6b026ccd4cbe4cbac192a1a0760202835
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062054"
---
# <a name="createmapiinitializationmonitor"></a><span data-ttu-id="8531a-103">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="8531a-103">CreateMAPIInitializationMonitor</span></span>

<span data-ttu-id="8531a-104">**適用対象 :** Outlook 2016 |Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="8531a-104">**Applies to**: Outlook 2016 | Outlook 2019</span></span>
  
## <a name="mapi-initialization-monitor"></a><span data-ttu-id="8531a-105">MAPI 初期化モニター</span><span class="sxs-lookup"><span data-stu-id="8531a-105">MAPI Initialization Monitor</span></span>

<span data-ttu-id="8531a-106">MAPI を使用するアプリケーションが、初期化が完了した時間を知りたい場合があります。</span><span class="sxs-lookup"><span data-stu-id="8531a-106">There are times when an application which consumes MAPI might want to know when the initialization is completed.</span></span> <span data-ttu-id="8531a-107">たとえば、MAPI を初期化できる複数のスレッドがある場合や、アプリケーションの初期化中に MAPI が初期化された場合は、何らかの処理を実行する必要がありますが、MAPI スタックを常にスピンアップする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8531a-107">For example, it have multiple threads which could initialize MAPI, or in response to MAPI being initialize the application would like perform some work, but does not want to always spin up the MAPI stack.</span></span> <span data-ttu-id="8531a-108">初期化モニターは、関数 (OLMAPI32.DLL からエクスポート) と、以下に示すいくつかの簡単なインターフェイスを使用して、この機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="8531a-108">The initialization monitor provides this functionality through a function (exported from OLMAPI32.DLL) and a couple of simple interfaces described below.</span></span>

<span data-ttu-id="8531a-109">これは、OLMAPI32.DLL からエクスポートされたエントリ ポイントです。これにより、呼び出し元はインターフェイスを取得して現在の初期化状態を照会したり、初期化完了用のコールバックをセットアップしたり、完了するまで現在のスレッドをブロックすることができます。</span><span class="sxs-lookup"><span data-stu-id="8531a-109">This is entry point exported from OLMAPI32.DLL this allows the caller to retrieve an interface to query the current initialization state, setup a callback for initialization completion or block the current thread until has completed.</span></span> <span data-ttu-id="8531a-110">この API から返されるオブジェクトは再利用可能でスレッド セーフであり、それを取得したスレッドではなく、任意のスレッドから呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8531a-110">The object returned from this API is reusable and thread safe and can be invoked from any thread, not just thread which retrieved it.</span></span> <span data-ttu-id="8531a-111">また、MAPI から公開される他のオブジェクトとは異なり、このオブジェクトは、DLL が読み込まれている限り有効であり、初期化セッション間で再使用できます。MAPIInitialize が呼び出される前または後に使用できます。</span><span class="sxs-lookup"><span data-stu-id="8531a-111">Also, unlike other objects exposed from MAPI, this object is valid as long as the DLL is loaded, it can be re-used across initialization sessions and can be consumed before or after MAPIInitialize has been called.</span></span> <span data-ttu-id="8531a-112">COM 標準 HRESULT を使用して成功または失敗を返し、IMAPIInitMonitor のインスタンスに out パラメーターを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="8531a-112">Returns success or failure through an COM standard HRESULT, and assigns an out parameter to an instance of IMAPIInitMonitor.</span></span>

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```
#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a><span data-ttu-id="8531a-113">HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)</span><span class="sxs-lookup"><span data-stu-id="8531a-113">HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)</span></span>

<span data-ttu-id="8531a-114">OLMAPI32.DLL からエクスポートされたこのエントリ ポイントを使用すると、呼び出し元はインターフェイスを取得して、現在の初期化状態を照会したり、初期化完了用のコールバックをセットアップしたり、完了するまで現在のスレッドをブロックすることができます。</span><span class="sxs-lookup"><span data-stu-id="8531a-114">This entry point exported from OLMAPI32.DLL allows the caller to retrieve an interface to query the current initialization state, setup a callback for initialization completion or block the current thread until has completed.</span></span> <span data-ttu-id="8531a-115">この API から返されるオブジェクトは再利用可能でスレッド セーフであり、それを取得したスレッドではなく、任意のスレッドから呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8531a-115">The object returned from this API is reusable and thread safe and can be invoked from any thread, not just thread which retrieved it.</span></span> <span data-ttu-id="8531a-116">また、MAPI から公開される他のオブジェクトとは異なり、このオブジェクトは、DLL が読み込まれている限り有効であり、初期化セッション間で再使用できます。MAPIInitialize が呼び出される前または後に使用できます。</span><span class="sxs-lookup"><span data-stu-id="8531a-116">Also, unlike other objects exposed from MAPI, this object is valid as long as the DLL is loaded, it can be re-used across initialization sessions and can be consumed before or after MAPIInitialize has been called.</span></span> <span data-ttu-id="8531a-117">COM 標準 HRESULT を使用して成功または失敗を返し、IMAPIInitMonitor のインスタンスに out パラメーターを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="8531a-117">Returns success or failure through an COM standard HRESULT, and assigns an out parameter to an instance of IMAPIInitMonitor.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8531a-118">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="8531a-118">Quick info</span></span>

| <span data-ttu-id="8531a-119">識別子</span><span class="sxs-lookup"><span data-stu-id="8531a-119">identifier</span></span> | <span data-ttu-id="8531a-120">result</span><span class="sxs-lookup"><span data-stu-id="8531a-120">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="8531a-121">次の方法でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="8531a-121">Exported by:</span></span>  <br/> |<span data-ttu-id="8531a-122">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="8531a-122">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="8531a-123">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="8531a-123">Called by:</span></span>  <br/> |<span data-ttu-id="8531a-124">クライアント</span><span class="sxs-lookup"><span data-stu-id="8531a-124">Client</span></span>  <br/> |
|<span data-ttu-id="8531a-125">実装元:</span><span class="sxs-lookup"><span data-stu-id="8531a-125">Implemented by:</span></span>  <br/> |<span data-ttu-id="8531a-126">Outlook</span><span class="sxs-lookup"><span data-stu-id="8531a-126">Outlook</span></span>  <br/> |

## <a name="parameters"></a><span data-ttu-id="8531a-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8531a-127">Parameters</span></span>
  
 <span data-ttu-id="8531a-128">_ppInitMonitor_</span><span class="sxs-lookup"><span data-stu-id="8531a-128">_ppInitMonitor_</span></span>
> <span data-ttu-id="8531a-129">[out]MAPI 初期化モニターの新しく作成されたインスタンスを受信するポインター。</span><span class="sxs-lookup"><span data-stu-id="8531a-129">[out] A pointer to receive the newly created instance of the MAPI initialization monitor.</span></span>
  
## <a name="return-values"></a><span data-ttu-id="8531a-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="8531a-130">Return values</span></span>

<span data-ttu-id="8531a-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="8531a-131">S_OK</span></span>
> <span data-ttu-id="8531a-132">初期化モニターの新しいインスタンスが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="8531a-132">A new instance of the initialization monitor was created successfully.</span></span>

<span data-ttu-id="8531a-133">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="8531a-133">E_OUTOFMEMORY</span></span>
> <span data-ttu-id="8531a-134">新しいオブジェクトをクレートするのに十分なメモリがなかった。</span><span class="sxs-lookup"><span data-stu-id="8531a-134">There was not enough memory to crate a new object.</span></span>

## <a name="see-also"></a><span data-ttu-id="8531a-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="8531a-135">See also</span></span>
[<span data-ttu-id="8531a-136">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="8531a-136">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="8531a-137">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="8531a-137">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
