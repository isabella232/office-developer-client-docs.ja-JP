---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4dc842416200ae6a65011e994689e2792642750c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564107"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストアに影響を与える指定されたイベントの通知を受信するために登録します。
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]生成する通知に関するフォルダーまたはメッセージのエントリ識別子へのポインター、または **null** です。 _lpEntryID が_ NULL に設定されている場合は、**メッセージ** ストア全体で通知を登録します。 
    
 _ulEventMask_
  
> [in]呼び出し元が関心を持ち、登録に含める必要がある通知イベントの種類を示す値のマスク。 イベントに関する [情報を](notification.md) 保持する各種類のイベントに関連付けられた対応する NOTIFICATION 構造があります。 ulEventMask パラメーターの有効な値  _を次に示_ します。 
    
 _fnevCriticalError_
  
> メモリ不足などの重大なエラーに関する通知を登録します。
    
 _fnevExtended_
  
> 特定のメッセージ ストア プロバイダーに固有のイベントに関する通知を登録します。
    
 _fnevNewMail_
  
> 新しいメッセージの到着に関する通知を登録します。 
    
 _fnevObjectCreated_
  
> 新しいフォルダーまたはメッセージの作成に関する通知を登録します。
    
 _fnevObjectCopied_
  
> コピーするフォルダーまたはメッセージに関する通知を登録します。
    
 _fnevObjectDeleted_
  
> 削除するフォルダーまたはメッセージに関する通知を登録します。
    
 _fnevObjectModified_
  
> 変更するフォルダーまたはメッセージに関する通知を登録します。
    
 _fnevObjectMoved_
  
> 移動するフォルダーまたはメッセージに関する通知を登録します。
    
 _fnevSearchComplete_
  
> 検索操作の完了に関する通知を登録します。
    
 _lpAdviseSink_
  
> [in]後続の通知を受信するアアドバイス シンク オブジェクトへのポインター。 このアアドバイス シンク オブジェクトは既に割り当てられている必要があります。
    
 _lpulConnection_
  
> [out]呼び出し元の通知シンク オブジェクトとセッションの間の接続を表す 0 以外の数値へのポインター。 
    
 _lpAdviseSink_
  
> [in]後続の通知を受信するアアドバイス シンク オブジェクトへのポインター。 このアアドバイス シンク オブジェクトは既に割り当てられている必要があります。 
    
 _lpulConnection_
  
> [out]呼び出し元のアアドバイス シンク オブジェクトとメッセージ ストア間の接続を表す 0 以外の接続番号へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録が成功しました。
    
MAPI_E_NO_SUPPORT 
  
> メッセージ ストア プロバイダーは、メッセージ ストアを通じた通知の登録をサポートしていない。
    
## <a name="remarks"></a>注釈

**IMsgStore::Advise** メソッドは、呼び出し元のアドバイス シンク オブジェクトと、メッセージ ストアまたはメッセージ ストア内のオブジェクトとの間の接続を確立します。 この接続は  _、ulEventMask_ パラメーターで指定されている 1 つ以上のイベントがアアドバイス ソース オブジェクトに発生した場合に、通知シンクに通知を送信するために使用されます。 _lpEntryID_ パラメーターが有効なエントリ識別子をポイントする場合、アドバイス ソースは、このエントリ識別子で識別されるオブジェクトです。 _lpEntryID が_ NULL の場合、アドバイス ソースはメッセージ ストアです。 
  
通知を送信するには、メッセージ ストア プロバイダーまたは MAPI が登録されているアアドバイス シンクの [IMAPIAdviseSink::OnNotify メソッドを呼び出](imapiadvisesink-onnotify.md) します。 通知構造である **OnNotify** のパラメーターの 1 つには、特定のイベントを記述する情報が含まれています。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

MAPI からの通知のサポートとサポートなし。 MAPI には、サービス プロバイダーが通知を実装するための 3 つのサポート オブジェクト メソッドがあります[。IMAPISupport::Subscribe](imapisupport-subscribe.md) [、IMAPISupport::Unsubscribe、](imapisupport-unsubscribe.md)[および IMAPISupport::Notify](imapisupport-notify.md)です。 MAPI サポート メソッドを使用する場合は **、Advise** メソッドが呼び出されたときに Subscribe を呼び出し _、lpAdviseSink ポインターを解放_ します。  
  
通知を自分でサポートする場合は _、lpAdviseSink_ パラメーターで表されるアアドバイス シンクの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出して、このポインターのコピーを保持します。 登録を取り消す [IMsgStore::Unadvise](imsgstore-unadvise.md) メソッドが呼び出されるまで、このコピーを維持します。 
  
通知のサポート方法に関係なく、0 以外の接続番号を通知登録に割り当て  _、lpulConnection パラメーターで返_ します。 **Unadvise** が呼び出され、完了するまで、この接続番号を解放しない。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数の実行スレッドをサポートするシステムでは **、OnNotify** の呼び出しは、任意のスレッドでもいつでも実行できます。 通知が特定のスレッドの特定の時刻にのみ発生すると確信する必要がある場合は [、HrThisThreadAdviseSink](hrthisthreadadvisesink.md) 関数を呼び出して **、Advise** に渡すアアドバイス シンク オブジェクトを生成します。 
  
Advise の呼 **び出** しが成功し、登録を取り消す **Unadvise** が呼び出される前に、アアドバイス シンク オブジェクトが解放される準備をしてください。 特定の長期的な使用がない限り **、Advise** が返された後にアアドバイス シンク オブジェクトを解放する必要があります。 
  
通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。 
  
通知の処理の詳細については、「通知の処理」 [を参照してください](handling-notifications.md)。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI は **、IMsgStore::Advise** メソッドを使用して、メッセージ ストア全体の通知に登録します。  <br/> |
   
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[�ʒm](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

