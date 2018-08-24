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
ms.openlocfilehash: 1ae94b40d984adee0f3c888f69dfdbffb1e352e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584437"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="3c490-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="3c490-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="3c490-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c490-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c490-105">フォームの現在のメッセージが保存されているフォーム ビューアーを通知します。</span><span class="sxs-lookup"><span data-stu-id="3c490-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="3c490-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3c490-106">Parameters</span></span>

<span data-ttu-id="3c490-107">なし</span><span class="sxs-lookup"><span data-stu-id="3c490-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3c490-108">�߂�l</span><span class="sxs-lookup"><span data-stu-id="3c490-108">Return value</span></span>

<span data-ttu-id="3c490-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c490-109">S_OK</span></span> 
  
> <span data-ttu-id="3c490-110">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="3c490-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3c490-111">����</span><span class="sxs-lookup"><span data-stu-id="3c490-111">Remarks</span></span>

<span data-ttu-id="3c490-112">フォーム オブジェクトは、フォームの現在のメッセージが正常に保存された後に、 **IMAPIViewAdviseSink::OnSaved**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3c490-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="3c490-113">これを行うメッセージへの変更を反映するように、windows を更新するためのビューアーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3c490-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="3c490-114">フォームの通知の詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c490-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3c490-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c490-115">See also</span></span>



[<span data-ttu-id="3c490-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3c490-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

