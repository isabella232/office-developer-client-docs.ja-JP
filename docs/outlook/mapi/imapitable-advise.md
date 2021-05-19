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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418814"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルに影響を与える指定されたイベントの通知を受信するアアドバイス シンク オブジェクトを登録します。
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulEventMask_
  
> [in]通知を生成するイベントの種類を示す値。 有効な値は次のとおりです。
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> [in]後続の通知を受信するアアドバイス シンク オブジェクトへのポインター。 このアアドバイス シンク オブジェクトは、既に割り当てられている必要があります。
    
 _lpulConnection_
  
> [out]正常な通知登録を表す 0 以外の値へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知登録が正常に完了しました。
    
MAPI_E_NO_SUPPORT 
  
> テーブルの実装では、行と列の変更がサポートされていないか、通知がサポートされていません。
    
## <a name="remarks"></a>注釈

**IMAPITable::Advise メソッドを使用して**、通知コールバック用にプロバイダーに実装されたテーブル オブジェクトを登録します。 テーブル オブジェクトに変更が発生するたびに、プロバイダーは  _ulEventMask_ パラメーターで設定されたイベント マスク ビットと、発生した変更の種類を確認します。 ビットが設定されている場合、プロバイダーは _、lpAdviseSink_ パラメーターで示されるアアドバイス シンク オブジェクトの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出して、イベントを報告します。 通知構造で **OnNotify** ルーチンに渡されたデータは、イベントについて説明します。 
  
**OnNotify の呼び出し** は、オブジェクトを変更する呼び出し中、または次の任意の時点で発生する可能性があります。 複数の実行スレッドをサポートするシステムでは **、OnNotify** の呼び出しは任意のスレッドで行われます。 **Inopportune** 時に発生する可能性がある OnNotify への呼び出しを、より安全に処理できる呼び出しに変える方法として、プロバイダーは [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用する必要があります。 
  
通知を提供するには、**アドバイス** を実装するプロバイダーは _、lpAdviseSink_ アアドバイス シンク オブジェクトへのポインターのコピーを保持する必要があります。これを行うには、通知登録が [IMAPITable::Unadvise](imapitable-unadvise.md)メソッドの呼び出しで取り消されるまで、そのオブジェクト ポインターを維持するために、アドバイス シンクの **IUnknown::AddRef** メソッドを呼び出します。 **Advise 実装では**、通知登録に接続番号を割り当て、lpulConnection パラメーターで返す前に、この接続番号で **AddRef** _を呼び出す必要_ があります。 サービス プロバイダーは、登録が取り消される前にアアドバイス シンク オブジェクトを解放できますが、** Unadvise ** が呼び出されるまで接続番号を解放する必要があります。 
  
**Advise** の呼び出しが成功した後、** Unadvise ** が呼び出される前に、クライアントは、アアドバイス シンク オブジェクトが解放される準備が必要です。 そのため、クライアントは、特定の長期的な使用がない限り **、Advise** が返した後にアアドバイス シンク オブジェクトを解放する必要があります。 
  
通知の非同期動作のため、テーブル列の設定を変更する実装は、前の列の順序で整理された情報を含む通知を受信できます。 たとえば、コンテナーから削除されたばかりのメッセージに対してテーブル行が返される場合があります。 このような通知は、列設定の変更が行われたときに送信され、その通知に関する情報が送信されましたが、通知テーブル ビューがまだその情報で更新されていません。
  
通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。 テーブル通知の詳細については、「テーブル通知について [」を参照してください](about-table-notifications.md)。 **IMAPISupport メソッドを使用して通知を** サポートする方法については、「Support Event Notification 」[を参照してください](supporting-event-notification.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI では **、IMAPITable::Advise** メソッドを使用して通知を登録し、テーブル ビューを最新の状態にできます。  <br/> |
   
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

