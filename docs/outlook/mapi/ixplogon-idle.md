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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 12aa8b79e38320d9767a6c333cb0197ea5669862
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578014"
---
# <a name="ixplogonidle"></a><span data-ttu-id="6dc6b-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="6dc6b-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="6dc6b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dc6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dc6b-105">システムがアイドル状態、優先度の低い操作を実行するトランスポート プロバイダーを有効にすることを示します。</span><span class="sxs-lookup"><span data-stu-id="6dc6b-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6dc6b-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="6dc6b-106">Parameters</span></span>

 <span data-ttu-id="6dc6b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6dc6b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6dc6b-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="6dc6b-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6dc6b-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6dc6b-109">Return value</span></span>

<span data-ttu-id="6dc6b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="6dc6b-110">S_OK</span></span> 
  
> <span data-ttu-id="6dc6b-111">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6dc6b-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6dc6b-112">注釈</span><span class="sxs-lookup"><span data-stu-id="6dc6b-112">Remarks</span></span>

<span data-ttu-id="6dc6b-113">MAPI スプーラーは、時間の場合、システムがアイドル状態、現在のセッションを開いている[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)メソッドの呼び出しで、XP_LOGON_SP フラグを渡すことによって、要求された場合定期的に、 **IXPLogon::Idle**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6dc6b-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="6dc6b-114">システムがアイドル状態のときに、トランスポート プロバイダーは、適切な他の呼び出し時にまたは定期的に発生する必要があるバック グラウンドの操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6dc6b-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6dc6b-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="6dc6b-115">See also</span></span>



[<span data-ttu-id="6dc6b-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="6dc6b-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="6dc6b-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6dc6b-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

