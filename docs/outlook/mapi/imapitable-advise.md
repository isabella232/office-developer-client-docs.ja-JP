---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329020"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドバイズシンクオブジェクトを登録して、テーブルに影響を与える指定したイベントの通知を受信します。
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>パラメーター

 _uleventmask_
  
> 順番通知を生成するイベントの種類を示す値です。 有効な値は次のとおりです。
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> 順番後続の通知を受け取るアドバイズシンクオブジェクトへのポインター。 このアドバイズシンクオブジェクトは、既に割り当てられている必要があります。
    
 _lアウト接続_
  
> 読み上げ正常な通知登録を表す0以外の値へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知の登録が正常に完了しました。
    
MAPI_E_NO_SUPPORT 
  
> テーブルの実装では、行と列の変更がサポートされていないか、通知をサポートしていません。
    
## <a name="remarks"></a>解説

**IMAPITable:: アドバイズ**メソッドを使用して、通知コールバック用にプロバイダーに実装されている table オブジェクトを登録します。 テーブルオブジェクトが変更されるたびに、プロバイダーは、 _uleventmask_パラメーターにどのイベントマスクビットが設定されているかを確認します。したがって、どのような種類の変更が発生したかを確認します。 ビットが設定されている場合、プロバイダーはイベントを報告するために、 _lpAdviseSink_パラメーターによって示されるアドバイズシンクオブジェクトの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 通知構造で**onnotify**ルーチンに渡されるデータは、イベントについての説明です。 
  
**onnotify**への呼び出しは、オブジェクトを変更する呼び出し中、または次のときに発生することがあります。 複数の実行スレッドをサポートするシステムでは、 **onnotify**への呼び出しは任意のスレッドで発生する可能性があります。 inopportune 時に発生する可能性のある**onnotify**への呼び出しを、より安全に処理できるようにする方法については、プロバイダーが[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用する必要があります。 
  
通知を提供するには、**アドバイズ**を実装するプロバイダーに、 _lpAdviseSink_アドバイズシンクオブジェクトへのポインターのコピーを保持する必要があります。これを行うには、アドバイズシンクに対して**IUnknown:: AddRef**メソッドを呼び出して、 [IMAPITable:: アドバイズ](imapitable-unadvise.md)中止メソッドへの呼び出しで通知登録が取り消されるまでオブジェクトポインターを保持します。 **アドバイズ**実装は、接続番号を通知登録に割り当て、この接続番号で**AddRef**を呼び出してから、lアウト_connection_パラメーターで取得する必要があります。 登録が取り消される前に、サービスプロバイダーはアドバイズシンクオブジェクトを解放できますが、* * アドバイズ中止 * * が呼び出されるまで、接続番号を解放してはなりません。 
  
**アドバイズ**の呼び出しが成功し、* * アドバイズ中止 * * が呼び出された後は、アドバイズシンクオブジェクトを解放するためにクライアントを準備する必要があります。 そのため、特定の長期間使用しない限り、**アドバイズ**が返された後、クライアントはアドバイズシンクオブジェクトを解放する必要があります。 
  
通知の非同期動作のため、テーブル列の設定を変更する実装は、前の列の順序で整理された情報に関する通知を受け取ることができます。 たとえば、コンテナーから削除されたばかりのメッセージに対して、テーブル行が返される場合があります。 このような通知は、列設定の変更が行われ、その情報が送信されたが、通知テーブルのビューがその情報に対してまだ更新されていない場合に送信されます。
  
通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。 テーブル通知に関する特定の情報については、「[テーブル通知につい](about-table-notifications.md)て」を参照してください。 **imapisupport**メソッドを使用して通知をサポートする方法については、「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> |CContestTableListCtrl:: notificationon  <br/> |mfcmapi は、 **IMAPITable:: アドバイズ**メソッドを使用して通知を登録し、テーブルビューが最新の状態を維持できるようにします。  <br/> |
   
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

