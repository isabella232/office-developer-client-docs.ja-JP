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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407607"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="6a08a-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="6a08a-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="6a08a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a08a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a08a-105">フォームの現在のメッセージが保存されたとフォーム ビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="6a08a-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="6a08a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6a08a-106">Parameters</span></span>

<span data-ttu-id="6a08a-107">なし</span><span class="sxs-lookup"><span data-stu-id="6a08a-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6a08a-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="6a08a-108">Return value</span></span>

<span data-ttu-id="6a08a-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a08a-109">S_OK</span></span> 
  
> <span data-ttu-id="6a08a-110">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="6a08a-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a08a-111">注釈</span><span class="sxs-lookup"><span data-stu-id="6a08a-111">Remarks</span></span>

<span data-ttu-id="6a08a-112">フォーム オブジェクトは、フォーム内の現在のメッセージが正常に保存された後 **、IMAPIViewAdviseSink::OnSaved** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6a08a-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="6a08a-113">これにより、閲覧者はメッセージの変更を反映するようにウィンドウを更新できます。</span><span class="sxs-lookup"><span data-stu-id="6a08a-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="6a08a-114">フォーム通知の詳細については、「フォーム通知の送受信 [」を参照してください](sending-and-receiving-form-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="6a08a-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6a08a-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="6a08a-115">See also</span></span>



[<span data-ttu-id="6a08a-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a08a-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

