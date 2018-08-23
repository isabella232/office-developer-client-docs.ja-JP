---
title: IMsgStoreNotifyNewMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.NotifyNewMail
api_type:
- COM
ms.assetid: d0d003b0-f12f-4422-b71f-26886169461f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 73a4c07c69fb10044cba6e9368cd4bc86c11ad54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575071"
---
# <a name="imsgstorenotifynewmail"></a><span data-ttu-id="8b58f-103">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="8b58f-103">IMsgStore::NotifyNewMail</span></span>

  
  
<span data-ttu-id="8b58f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b58f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b58f-p101">�V�������b�Z�[�W�������������b�Z�[�W �X�g�A�ɒʒm���܂��B���̕��@�́AMAPI �X�v�[���[�ɂ���Ă̂݌Ăяo����܂��B</span><span class="sxs-lookup"><span data-stu-id="8b58f-p101">Informs the message store that a new message has arrived. This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a><span data-ttu-id="8b58f-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="8b58f-107">Parameters</span></span>

 <span data-ttu-id="8b58f-108">_lpNotification_</span><span class="sxs-lookup"><span data-stu-id="8b58f-108">_lpNotification_</span></span>
  
> <span data-ttu-id="8b58f-109">[in]新着メッセージの通知を説明する[通知](notification.md)の構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8b58f-109">[in] A pointer to a [NOTIFICATION](notification.md) structure that describes the new message notification.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8b58f-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="8b58f-110">Return value</span></span>

<span data-ttu-id="8b58f-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b58f-111">S_OK</span></span> 
  
> <span data-ttu-id="8b58f-112">���b�Z�[�W �X�g�A������ɒʒm��󂯎��܂��B</span><span class="sxs-lookup"><span data-stu-id="8b58f-112">The message store was successfully notified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b58f-113">����</span><span class="sxs-lookup"><span data-stu-id="8b58f-113">Remarks</span></span>

<span data-ttu-id="8b58f-114">**IMsgStore::NotifyNewMail**���\�b�h�́A���b�Z�[�W���z�M�i�ޏ������ł�����A���b�Z�[�W �X�g�A�ɒʒm���� MAPI �X�v�[���[�ɂ���ĂƌĂ΂�܂��B</span><span class="sxs-lookup"><span data-stu-id="8b58f-114">The **IMsgStore::NotifyNewMail** method is called by the MAPI spooler to inform the message store that a message is ready for delivery.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8b58f-115">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="8b58f-115">Notes to implementers</span></span>

<span data-ttu-id="8b58f-116">**NotifyNewMail**が呼び出されると、すべての登録済みクライアントに新着メールの通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="8b58f-116">When **NotifyNewMail** is called, send a new mail notification to all registered clients.</span></span> <span data-ttu-id="8b58f-117">サポート オブジェクトのメソッドを使用するよう選択した場合は、 [IMAPISupport::Notify](imapisupport-notify.md)を呼び出すことによって、または独自の実装を使用して通知を送信できます。</span><span class="sxs-lookup"><span data-stu-id="8b58f-117">You can send the notification by calling [IMAPISupport::Notify](imapisupport-notify.md), if you elect to use the support object methods, or by using your own implementation.</span></span> <span data-ttu-id="8b58f-118">登録されているクライアントは、 [IMsgStore::Advise](imsgstore-advise.md)と呼ばれるがあり、NULL と、 _ulEventMask_パラメーターを_fnevNewMail_に、 _lpEntryID_パラメーターを設定する 1 つです。</span><span class="sxs-lookup"><span data-stu-id="8b58f-118">A registered client is one that has called [IMsgStore::Advise](imsgstore-advise.md) and set the  _lpEntryID_ parameter to NULL and the  _ulEventMask_ parameter to  _fnevNewMail_.</span></span> 
  
<span data-ttu-id="8b58f-119">変更したり、新着メールの通知を説明する[通知](notification.md)の構造体のメモリを解放しないでください。</span><span class="sxs-lookup"><span data-stu-id="8b58f-119">Do not modify or free the memory for the [NOTIFICATION](notification.md) structure that describes the new mail notification.</span></span> <span data-ttu-id="8b58f-120">ユーティリティ関数を作成するのには[ScCopyNotifications](sccopynotifications.md)を呼び出すことによって、**通知**の構造体をコピーのメンバーの情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="8b58f-120">Copy the **NOTIFICATION** structure by calling the utility function [ScCopyNotifications](sccopynotifications.md) to make use of the information in its members.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b58f-121">�֘A����</span><span class="sxs-lookup"><span data-stu-id="8b58f-121">See also</span></span>



[<span data-ttu-id="8b58f-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="8b58f-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="8b58f-123">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="8b58f-123">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
  
[<span data-ttu-id="8b58f-124">�ʒm</span><span class="sxs-lookup"><span data-stu-id="8b58f-124">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="8b58f-125">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="8b58f-125">ScCopyNotifications</span></span>](sccopynotifications.md)
  
[<span data-ttu-id="8b58f-126">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8b58f-126">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

