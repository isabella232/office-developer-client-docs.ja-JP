---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 00d70472e5d93eb6a9caab60f444afda3a75b03d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575723"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPITable::Advise](imapitable-advise.md)メソッドへの呼び出しで以前に設定された通知の送信をキャンセルします。 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulConnection_
  
> [in] [IMAPITable::Advise](imapitable-advise.md)への呼び出しによって返される登録接続の数。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功しました。
    
## <a name="remarks"></a>注釈

**IMAPITable::Unadvise** メソッドを使用して **、IMAPITable::Advise** の前の呼び出しで _lpAdviseSink_ パラメーターで渡されたアアドバイス シンク オブジェクトへのポインターを解放し、通知登録を取り消します。 アアドバイス シンク オブジェクトへのポインターを破棄する一環として、オブジェクトの **IUnknown::Release** メソッドが呼び出されます。 一般に **、Unadvise** 呼び出し中に Release が呼び出されますが、別のスレッドがアドバイス シンクの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出している場合 **、OnNotify** メソッドが返されるまで、Release 呼び出しは遅延されます。  
  
通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。 テーブル通知の詳細については、「テーブル通知について [」を参照してください](about-table-notifications.md)。 **IMAPISupport メソッドを使用して通知を** サポートする方法については、「Support Event Notification 」[を参照してください](supporting-event-notification.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |MFCMAPI は **IMAPITable::Unadvise** メソッドを使用して、テーブルの通知をキャンセルします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

