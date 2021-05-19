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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419605"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="e9f4a-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="e9f4a-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="e9f4a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9f4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9f4a-105">新しいメッセージまたは既存のメッセージがフォームに読み込まれたとフォーム ビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="e9f4a-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="e9f4a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9f4a-106">Parameters</span></span>

<span data-ttu-id="e9f4a-107">なし</span><span class="sxs-lookup"><span data-stu-id="e9f4a-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="e9f4a-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9f4a-108">Return value</span></span>

<span data-ttu-id="e9f4a-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9f4a-109">S_OK</span></span> 
  
> <span data-ttu-id="e9f4a-110">通知が成功しました。</span><span class="sxs-lookup"><span data-stu-id="e9f4a-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9f4a-111">注釈</span><span class="sxs-lookup"><span data-stu-id="e9f4a-111">Remarks</span></span>

<span data-ttu-id="e9f4a-112">フォーム オブジェクトは [、IPersistMessage::InitNew](ipersistmessage-initnew.md)メソッドまたは [IPersistMessage::Load](ipersistmessage-load.md)メソッドを使用してフォームにメッセージが読み込まれるたびに **IMAPIViewAdviseSink::OnNewMessage** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9f4a-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e9f4a-113">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="e9f4a-113">Notes to implementers</span></span>

<span data-ttu-id="e9f4a-114">アクティブなポインターをフォーム オブジェクトに離すのは、ビューアーが以前表示したメッセージを指し示しなくなったためです。</span><span class="sxs-lookup"><span data-stu-id="e9f4a-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="e9f4a-115">フォーム通知の詳細については、「フォーム通知の送受信 [」を参照してください](sending-and-receiving-form-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="e9f4a-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e9f4a-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9f4a-116">See also</span></span>



[<span data-ttu-id="e9f4a-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9f4a-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="e9f4a-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="e9f4a-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="e9f4a-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="e9f4a-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="e9f4a-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9f4a-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

