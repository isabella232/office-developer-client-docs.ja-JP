---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ceca6a2dbe5f80f8a3499e509db8d5e6c35d72d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436049"
---
# <a name="ixplogonidle"></a><span data-ttu-id="58351-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="58351-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="58351-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58351-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58351-105">システムがアイドル状態であることを示します。これにより、トランスポートプロバイダーは優先度の低い操作を実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="58351-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="58351-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="58351-106">Parameters</span></span>

 <span data-ttu-id="58351-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="58351-107">_ulFlags_</span></span>
  
> <span data-ttu-id="58351-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="58351-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="58351-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="58351-109">Return value</span></span>

<span data-ttu-id="58351-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="58351-110">S_OK</span></span> 
  
> <span data-ttu-id="58351-111">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="58351-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58351-112">注釈</span><span class="sxs-lookup"><span data-stu-id="58351-112">Remarks</span></span>

<span data-ttu-id="58351-113">MAPI スプーラーは、要求された場合、 **IXPLogon:: idle**メソッドを定期的に呼び出します。これは、システムがアイドル状態になっている間に、現在のセッションを開いた[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)メソッドへの呼び出しで XP_LOGON_SP フラグを渡すことによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="58351-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="58351-114">システムがアイドル状態になると、トランスポートプロバイダーは、他の通話中に、または定期的に発生する必要があるバックグラウンド操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="58351-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58351-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="58351-115">See also</span></span>



[<span data-ttu-id="58351-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="58351-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="58351-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="58351-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

