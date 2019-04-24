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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a2da3f6851e45a70dcd4604396a85430c539a830
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322394"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="14982-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="14982-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="14982-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14982-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14982-105">この[imapisecuremessage: IUnknown](imapisecuremessageiunknown.md)がカプセル化されている、基になる[IMessage: imapiprop](imessageimapiprop.md)を取得します。</span><span class="sxs-lookup"><span data-stu-id="14982-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="14982-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14982-106">Parameters</span></span>

 <span data-ttu-id="14982-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="14982-107">_ppmsg_</span></span>
  
> <span data-ttu-id="14982-108">読み上げセキュリティで保護されたメッセージオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="14982-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="14982-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="14982-109">Return value</span></span>

<span data-ttu-id="14982-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="14982-110">S_OK</span></span>
  
> <span data-ttu-id="14982-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="14982-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14982-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="14982-112">See also</span></span>



[<span data-ttu-id="14982-113">IMAPISecureMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14982-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="14982-114">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="14982-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

