---
title: IMAPIViewAdviseSinkOnShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnShutdown
api_type:
- COM
ms.assetid: c9c3aecf-5e4b-407a-8ea1-6211b4c6e0a5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2a09731dbd0ba2c5d6c1055a7c5ed11097c5ef27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800862"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="30604-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="30604-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="30604-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30604-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30604-105">フォーム ビューアーに、フォームが閉じられることを通知します。</span><span class="sxs-lookup"><span data-stu-id="30604-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="30604-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="30604-106">Parameters</span></span>

<span data-ttu-id="30604-107">なし</span><span class="sxs-lookup"><span data-stu-id="30604-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="30604-108">�߂�l</span><span class="sxs-lookup"><span data-stu-id="30604-108">Return value</span></span>

<span data-ttu-id="30604-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="30604-109">S_OK</span></span> 
  
> <span data-ttu-id="30604-110">通知が成功しました。</span><span class="sxs-lookup"><span data-stu-id="30604-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30604-111">備考</span><span class="sxs-lookup"><span data-stu-id="30604-111">Remarks</span></span>

<span data-ttu-id="30604-112">フォームの通知の詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="30604-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30604-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="30604-113">See also</span></span>



[<span data-ttu-id="30604-114">IMAPIViewAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="30604-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

