---
title: ixpprovidershutdown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357198"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="52e61-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="52e61-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="52e61-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52e61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52e61-105">トランスポートプロバイダーを正しい順序で閉じます。</span><span class="sxs-lookup"><span data-stu-id="52e61-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="52e61-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="52e61-106">Parameters</span></span>

 <span data-ttu-id="52e61-107">_lアウトフラグ_</span><span class="sxs-lookup"><span data-stu-id="52e61-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="52e61-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="52e61-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="52e61-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="52e61-109">Return value</span></span>

<span data-ttu-id="52e61-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="52e61-110">S_OK</span></span> 
  
> <span data-ttu-id="52e61-111">呼び出しがトランスポートプロバイダーのシャットダウンに成功しました。</span><span class="sxs-lookup"><span data-stu-id="52e61-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="52e61-112">解説</span><span class="sxs-lookup"><span data-stu-id="52e61-112">Remarks</span></span>

<span data-ttu-id="52e61-113">MAPI スプーラーは、トランスポートプロバイダーオブジェクトを解放する直前に、 **ixpprovider:: Shutdown**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="52e61-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="52e61-114">**シャットダウン**を呼び出す前に、MAPI はプロバイダーのすべてのログオンオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="52e61-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="52e61-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="52e61-115">See also</span></span>



[<span data-ttu-id="52e61-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="52e61-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="52e61-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52e61-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

