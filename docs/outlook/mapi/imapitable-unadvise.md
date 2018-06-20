---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e9d8565cfaa17764e92bddafb29e744d23872515
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800868"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**適用されます**: Outlook 
  
[IMAPITable::Advise](imapitable-advise.md)メソッドへの呼び出しは、設定済みの通知の送信をキャンセルします。 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in][IMAPITable::Advise](imapitable-advise.md)への呼び出しによって返された登録接続の数です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功しました。
    
## <a name="remarks"></a>備考

**IMAPITable::Advise**通知の登録をキャンセルするために以前の呼び出しで_lpAdviseSink_パラメーターで渡されたアドバイズ シンク オブジェクトへのポインターを解放するのにには、 **IMAPITable::Unadvise**メソッドを使用します。 アドバイズ シンク オブジェクトへのポインターを破棄することの一環として、オブジェクト**が**呼び出されます。 **リリース**が呼び出される一般的には、別のスレッドがいる、アドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出す場合は、 **Unadvise**の呼び出し中に**リリース**の呼び出し、 **OnNotify**まで延期メソッドを返します。 
  
通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。 テーブル通知の詳細については、[テーブルについての通知](about-table-notifications.md)を参照してください。 通知をサポートするために**IMAPISupport**メソッドを使用する方法の詳細については、[イベント通知のサポート](supporting-event-notification.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |MFCMAPI では、 **IMAPITable::Unadvise**メソッドを使用して、テーブルの通知をキャンセルします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

