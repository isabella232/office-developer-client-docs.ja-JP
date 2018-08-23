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
# <a name="imsgstorenotifynewmail"></a>IMsgStore::NotifyNewMail

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
�V�������b�Z�[�W�������������b�Z�[�W �X�g�A�ɒʒm���܂��B���̕��@�́AMAPI �X�v�[���[�ɂ���Ă̂݌Ăяo����܂��B
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a>�p�����[�^�[

 _lpNotification_
  
> [in]新着メッセージの通知を説明する[通知](notification.md)の構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ���b�Z�[�W �X�g�A������ɒʒm��󂯎��܂��B
    
## <a name="remarks"></a>����

**IMsgStore::NotifyNewMail**���\�b�h�́A���b�Z�[�W���z�M�i�ޏ������ł�����A���b�Z�[�W �X�g�A�ɒʒm���� MAPI �X�v�[���[�ɂ���ĂƌĂ΂�܂��B 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**NotifyNewMail**が呼び出されると、すべての登録済みクライアントに新着メールの通知を送信します。 サポート オブジェクトのメソッドを使用するよう選択した場合は、 [IMAPISupport::Notify](imapisupport-notify.md)を呼び出すことによって、または独自の実装を使用して通知を送信できます。 登録されているクライアントは、 [IMsgStore::Advise](imsgstore-advise.md)と呼ばれるがあり、NULL と、 _ulEventMask_パラメーターを_fnevNewMail_に、 _lpEntryID_パラメーターを設定する 1 つです。 
  
変更したり、新着メールの通知を説明する[通知](notification.md)の構造体のメモリを解放しないでください。 ユーティリティ関数を作成するのには[ScCopyNotifications](sccopynotifications.md)を呼び出すことによって、**通知**の構造体をコピーのメンバーの情報を使用します。 
  
## <a name="see-also"></a>�֘A����



[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
  
[�ʒm](notification.md)
  
[ScCopyNotifications](sccopynotifications.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

