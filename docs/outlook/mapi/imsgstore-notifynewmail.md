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
ms.openlocfilehash: a8ec06fd0401a129e08a06acdb1c18785f90d4a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348756"
---
# <a name="imsgstorenotifynewmail"></a>IMsgStore::NotifyNewMail

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいメッセージが到着したことをメッセージストアに通知します。 このメソッドは、MAPI スプーラーによってのみ呼び出されます。
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a>パラメーター

 _lpnotification_
  
> [in] A pointer to a [NOTIFICATION](notification.md) structure that describes the new message notification. 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ���b�Z�[�W �X�g�A������ɒʒm��󂯎��܂��B
    
## <a name="remarks"></a>解説

**IMsgStore::NotifyNewMail**���\�b�h�́A���b�Z�[�W���z�M�i�ޏ������ł�����A���b�Z�[�W �X�g�A�ɒʒm���� MAPI �X�v�[���[�ɂ���ĂƌĂ΂�܂��B 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

When **NotifyNewMail** is called, send a new mail notification to all registered clients. You can send the notification by calling [IMAPISupport::Notify](imapisupport-notify.md), if you elect to use the support object methods, or by using your own implementation. A registered client is one that has called [IMsgStore::Advise](imsgstore-advise.md) and set the  _lpEntryID_ parameter to NULL and the  _ulEventMask_ parameter to  _fnevNewMail_. 
  
Do not modify or free the memory for the [NOTIFICATION](notification.md) structure that describes the new mail notification. Copy the **NOTIFICATION** structure by calling the utility function [ScCopyNotifications](sccopynotifications.md) to make use of the information in its members. 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
  
[�ʒm](notification.md)
  
[ScCopyNotifications](sccopynotifications.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

