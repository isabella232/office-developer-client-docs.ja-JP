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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2ec78331fd013777f001d39bd7e978a67abb5342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351199"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="926ae-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="926ae-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="926ae-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="926ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="926ae-105">フォームの現在のメッセージが保存されたことをフォームビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="926ae-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="926ae-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="926ae-106">Parameters</span></span>

<span data-ttu-id="926ae-107">なし</span><span class="sxs-lookup"><span data-stu-id="926ae-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="926ae-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="926ae-108">Return value</span></span>

<span data-ttu-id="926ae-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="926ae-109">S_OK</span></span> 
  
> <span data-ttu-id="926ae-110">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="926ae-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="926ae-111">解説</span><span class="sxs-lookup"><span data-stu-id="926ae-111">Remarks</span></span>

<span data-ttu-id="926ae-112">form オブジェクトは、フォーム内の現在のメッセージが正常に保存された後に、 **IMAPIViewAdviseSink:: onsaved**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="926ae-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="926ae-113">これにより、閲覧者は、メッセージの変更を反映するように windows を更新することができます。</span><span class="sxs-lookup"><span data-stu-id="926ae-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="926ae-114">フォーム通知の詳細については、「[フォーム通知の送信と受信](sending-and-receiving-form-notifications.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="926ae-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="926ae-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="926ae-115">See also</span></span>



[<span data-ttu-id="926ae-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="926ae-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

