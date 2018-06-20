---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0f9aa5d508afeaf5933c50763e1e42832ae4e3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800872"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="f8200-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="f8200-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="f8200-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f8200-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f8200-105">フォームの現在のメッセージが保存されているフォーム ビューアーを通知します。</span><span class="sxs-lookup"><span data-stu-id="f8200-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="f8200-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f8200-106">Parameters</span></span>

<span data-ttu-id="f8200-107">なし</span><span class="sxs-lookup"><span data-stu-id="f8200-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="f8200-108">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f8200-108">Return value</span></span>

<span data-ttu-id="f8200-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8200-109">S_OK</span></span> 
  
> <span data-ttu-id="f8200-110">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="f8200-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8200-111">����</span><span class="sxs-lookup"><span data-stu-id="f8200-111">Remarks</span></span>

<span data-ttu-id="f8200-112">フォーム オブジェクトは、フォームの現在のメッセージが正常に保存された後に、 **IMAPIViewAdviseSink::OnSaved**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f8200-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="f8200-113">これを行うメッセージへの変更を反映するように、windows を更新するためのビューアーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8200-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="f8200-114">フォームの通知の詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8200-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f8200-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8200-115">See also</span></span>



[<span data-ttu-id="f8200-116">IMAPIViewAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8200-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

