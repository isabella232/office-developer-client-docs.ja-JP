---
title: IMAPISecureMessageGetBaseMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISecureMessage.GetBaseMessage
api_type:
- COM
ms.assetid: 573f40c5-e0d2-4281-8c22-10a1ae1f0dee
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 70c8bd36142d18b541ad6a2e0ded3bebcfb6dbb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800666"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="957f2-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="957f2-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="957f2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="957f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="957f2-105">基になるを取得[IMessage: IMAPIProp](imessageimapiprop.md)この[IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md)カプセル化することです。</span><span class="sxs-lookup"><span data-stu-id="957f2-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="957f2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="957f2-106">Parameters</span></span>

 <span data-ttu-id="957f2-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="957f2-107">_ppmsg_</span></span>
  
> <span data-ttu-id="957f2-108">[out]セキュリティで保護されたメッセージのオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="957f2-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="957f2-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="957f2-109">Return value</span></span>

<span data-ttu-id="957f2-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="957f2-110">S_OK</span></span>
  
> <span data-ttu-id="957f2-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="957f2-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="957f2-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="957f2-112">See also</span></span>



[<span data-ttu-id="957f2-113">IMAPISecureMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="957f2-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="957f2-114">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="957f2-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

