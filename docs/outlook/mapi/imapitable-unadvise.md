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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328806"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPITable:: Advise](imapitable-advise.md)メソッドへの呼び出しを使用して、以前に設定した通知の送信をキャンセルします。 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulconnection_
  
> 順番[IMAPITable:: Advise](imapitable-advise.md)への呼び出しによって返される登録接続の番号。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功しました。
    
## <a name="remarks"></a>解説

**imapitable:: アドバイズ**中止メソッドを使用して、前述の**IMAPITable:: advise**の呼び出しで_lpAdviseSink_パラメーターで渡されたアドバイズシンクオブジェクトへのポインターを解放し、通知登録を取り消します。 アドバイズシンクオブジェクトへのポインターを破棄する一環として、オブジェクトの**IUnknown:: Release**メソッドが呼び出されます。 通常、**リリース**は、**アドバイズ**中止の呼び出し中に呼び出されますが、別のスレッドがアドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出している場合は、 **onnotify**になるまで**release**呼び出しが遅延します。メソッドはを返します。 
  
通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。 テーブル通知に関する特定の情報については、「[テーブル通知につい](about-table-notifications.md)て」を参照してください。 **imapisupport**メソッドを使用して通知をサポートする方法については、「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> |CContentsTableListCtrl:: notificationoff  <br/> |mfcmapi は、 **IMAPITable:: アドバイズ**中止メソッドを使用して、テーブルの通知を取り消します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

