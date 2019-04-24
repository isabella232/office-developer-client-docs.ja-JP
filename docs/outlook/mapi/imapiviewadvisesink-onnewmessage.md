---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6a6f8f9d675bee362b4a9f1c5b7fc544fa66d7b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328792"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="18694-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="18694-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="18694-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18694-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18694-105">フォームビューアーに、新規または既存のメッセージがフォームにロードされたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="18694-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="18694-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="18694-106">Parameters</span></span>

<span data-ttu-id="18694-107">なし</span><span class="sxs-lookup"><span data-stu-id="18694-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="18694-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="18694-108">Return value</span></span>

<span data-ttu-id="18694-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="18694-109">S_OK</span></span> 
  
> <span data-ttu-id="18694-110">通知に成功しました。</span><span class="sxs-lookup"><span data-stu-id="18694-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18694-111">解説</span><span class="sxs-lookup"><span data-stu-id="18694-111">Remarks</span></span>

<span data-ttu-id="18694-112">form オブジェクトは、 [IPersistMessage:: InitNew](ipersistmessage-initnew.md)または[IPersistMessage:: Load](ipersistmessage-load.md)メソッドのいずれかを使用して、フォームにメッセージが読み込まれるたびに**IMAPIViewAdviseSink:: onnewmessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="18694-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="18694-113">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="18694-113">Notes to implementers</span></span>

<span data-ttu-id="18694-114">閲覧者が以前に表示していたメッセージをポイントしていないため、アクティブポインターをフォームオブジェクトに解放します。</span><span class="sxs-lookup"><span data-stu-id="18694-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="18694-115">フォーム通知の詳細については、「[フォーム通知の送信と受信](sending-and-receiving-form-notifications.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18694-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18694-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="18694-116">See also</span></span>



[<span data-ttu-id="18694-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="18694-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="18694-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="18694-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="18694-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="18694-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="18694-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="18694-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

