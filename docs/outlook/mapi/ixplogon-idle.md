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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298482"
---
# <a name="ixplogonidle"></a><span data-ttu-id="3f538-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="3f538-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="3f538-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f538-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f538-105">システムがアイドル状態であることを示します。これにより、トランスポートプロバイダーは優先度の低い操作を実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="3f538-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3f538-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3f538-106">Parameters</span></span>

 <span data-ttu-id="3f538-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3f538-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3f538-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="3f538-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3f538-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="3f538-109">Return value</span></span>

<span data-ttu-id="3f538-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f538-110">S_OK</span></span> 
  
> <span data-ttu-id="3f538-111">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="3f538-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f538-112">解説</span><span class="sxs-lookup"><span data-stu-id="3f538-112">Remarks</span></span>

<span data-ttu-id="3f538-113">MAPI スプーラーは、要求された場合、 **IXPLogon:: idle**メソッドを定期的に呼び出します。これは、システムがアイドル状態になっている間に、現在のセッションを開いた[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)メソッドへの呼び出しで XP_LOGON_SP フラグを渡すことによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="3f538-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="3f538-114">システムがアイドル状態になると、トランスポートプロバイダーは、他の通話中に、または定期的に発生する必要があるバックグラウンド操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="3f538-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f538-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="3f538-115">See also</span></span>



[<span data-ttu-id="3f538-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="3f538-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="3f538-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f538-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

