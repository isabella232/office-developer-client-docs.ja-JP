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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: adf9b28e941e9ead9b83660f58701f13f35cabc7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800874"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="b5bb2-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="b5bb2-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="b5bb2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b5bb2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b5bb2-105">新規または既存のメッセージがフォームで読み込まれているフォーム ビューアーを通知します。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="b5bb2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b5bb2-106">Parameters</span></span>

<span data-ttu-id="b5bb2-107">なし</span><span class="sxs-lookup"><span data-stu-id="b5bb2-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="b5bb2-108">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b5bb2-108">Return value</span></span>

<span data-ttu-id="b5bb2-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="b5bb2-109">S_OK</span></span> 
  
> <span data-ttu-id="b5bb2-110">通知が成功しました。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b5bb2-111">注釈</span><span class="sxs-lookup"><span data-stu-id="b5bb2-111">Remarks</span></span>

<span data-ttu-id="b5bb2-112">フォーム オブジェクトは、 [IPersistMessage::InitNew](ipersistmessage-initnew.md)または[IPersistMessage::Load](ipersistmessage-load.md)のいずれかのメソッドを使用してフォームのメッセージが読み込まれるたびに、 **IMAPIViewAdviseSink::OnNewMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b5bb2-113">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="b5bb2-113">Notes to implementers</span></span>

<span data-ttu-id="b5bb2-114">ビューアーが以前に表示するメッセージを示していないために、フォーム オブジェクトをアクティブにマウス ポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="b5bb2-115">フォームの通知の詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5bb2-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b5bb2-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="b5bb2-116">See also</span></span>



[<span data-ttu-id="b5bb2-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b5bb2-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="b5bb2-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="b5bb2-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="b5bb2-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="b5bb2-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="b5bb2-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b5bb2-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

