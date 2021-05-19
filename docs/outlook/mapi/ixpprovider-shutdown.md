---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409693"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="a81c5-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="a81c5-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="a81c5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a81c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a81c5-105">トランスポート プロバイダーを順番に閉じます。</span><span class="sxs-lookup"><span data-stu-id="a81c5-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a81c5-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a81c5-106">Parameters</span></span>

 <span data-ttu-id="a81c5-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="a81c5-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="a81c5-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="a81c5-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a81c5-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="a81c5-109">Return value</span></span>

<span data-ttu-id="a81c5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a81c5-110">S_OK</span></span> 
  
> <span data-ttu-id="a81c5-111">呼び出しは、トランスポート プロバイダーのシャットダウンに成功しました。</span><span class="sxs-lookup"><span data-stu-id="a81c5-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a81c5-112">注釈</span><span class="sxs-lookup"><span data-stu-id="a81c5-112">Remarks</span></span>

<span data-ttu-id="a81c5-113">MAPI スプーラーは、トランスポート プロバイダー オブジェクトを解放する前に **IXPProvider::Shutdown** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a81c5-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="a81c5-114">Shutdown を **呼び出す** 前に、MAPI はプロバイダーのすべてのログオン オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="a81c5-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a81c5-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="a81c5-115">See also</span></span>



[<span data-ttu-id="a81c5-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="a81c5-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="a81c5-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a81c5-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

