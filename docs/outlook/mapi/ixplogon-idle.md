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
ms.openlocfilehash: 75607550f1d6085a670ad997238994400e08f7bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801253"
---
# <a name="ixplogonidle"></a><span data-ttu-id="5e086-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="5e086-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="5e086-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e086-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e086-105">システムがアイドル状態、優先度の低い操作を実行するトランスポート プロバイダーを有効にすることを示します。</span><span class="sxs-lookup"><span data-stu-id="5e086-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5e086-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="5e086-106">Parameters</span></span>

 <span data-ttu-id="5e086-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e086-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5e086-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="5e086-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e086-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5e086-109">Return value</span></span>

<span data-ttu-id="5e086-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e086-110">S_OK</span></span> 
  
> <span data-ttu-id="5e086-111">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5e086-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e086-112">備考</span><span class="sxs-lookup"><span data-stu-id="5e086-112">Remarks</span></span>

<span data-ttu-id="5e086-113">MAPI スプーラーは、時間の場合、システムがアイドル状態、現在のセッションを開いている[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)メソッドの呼び出しで、XP_LOGON_SP フラグを渡すことによって、要求された場合定期的に、 **IXPLogon::Idle**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5e086-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="5e086-114">システムがアイドル状態のときに、トランスポート プロバイダーは、適切な他の呼び出し時にまたは定期的に発生する必要があるバック グラウンドの操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5e086-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e086-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e086-115">See also</span></span>



[<span data-ttu-id="5e086-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="5e086-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="5e086-117">IXPLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e086-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

