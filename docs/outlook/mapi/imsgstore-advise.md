---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6a315cef8263f7e241a815a0f054dc3174d88fa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800989"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**適用対象**: Outlook 
  
メッセージ ・ ストアに影響を与える特定のイベントの通知を受け取ることを登録します。
  
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
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]フォルダーまたはメッセージに関する通知を生成するか、または**null**のエントリの識別子へのポインター。 _LpEntryID_を NULL に設定すると、**アドバイス**は全体のメッセージ ・ ストアに通知を登録します。 
    
 _ulEventMask_
  
> [in]呼び出し元に興味を持って登録に含めることが通知イベントの種類を示す値のマスク。 各イベントに関する情報を保持するイベントの種類に関連付けられている対応する[通知](notification.md)の構造があります。 _UlEventMask_パラメーターに有効な値は、次のように。 
    
 _fnevCriticalError_
  
> メモリ不足などの重大なエラーに関する通知を登録します。
    
 _fnevExtended_
  
> プロバイダーを格納する特定のメッセージに特定のイベントに関する通知を登録します。
    
 _fnevNewMail_
  
> 新しいメッセージの到着の通知を登録します。 
    
 _fnevObjectCreated_
  
> 新しいフォルダーまたはメッセージの作成についての通知を登録します。
    
 _fnevObjectCopied_
  
> フォルダーまたはコピーするメッセージに関する通知を登録します。
    
 _fnevObjectDeleted_
  
> フォルダーまたはメッセージの削除についての通知を登録します。
    
 _fnevObjectModified_
  
> フォルダーまたはメッセージの変更に関する通知を登録します。
    
 _fnevObjectMoved_
  
> フォルダーまたは移動するメッセージに関する通知を登録します。
    
 _fnevSearchComplete_
  
> 検索操作の完了に関する通知を登録します。
    
 _lpAdviseSink_
  
> [in]後続の通知を受信するアドバイズ シンク オブジェクトへのポインター。 このアドバイズ シンク オブジェクトは既に割り当てられている必要があります。
    
 _lpulConnection_
  
> [out]呼び出し元の間の接続を表す数値を 0 以外の値へのポインターでは、シンク オブジェクトとのセッションを案内します。 
    
 _lpAdviseSink_
  
> [in]後続の通知を受信するアドバイズ シンク オブジェクトへのポインター。 このアドバイズ シンク オブジェクトは既に割り当てられている必要があります。 
    
 _lpulConnection_
  
> [out]呼び出し元の間の接続を表す、0 以外の接続番号へのポインターでは、シンク オブジェクトとメッセージ ストアを案内します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 登録が正常に完了しました。
    
MAPI_E_NO_SUPPORT 
  
> メッセージ ストア プロバイダーは、メッセージ ・ ストアを使用して通知の登録をサポートしていません。
    
## <a name="remarks"></a>注釈

**IMsgStore::Advise**メソッドでは、シンク オブジェクトと、メッセージ ストアまたはメッセージ ・ ストア内のオブジェクトにアドバイスの呼び出し元の間の接続を確立します。 この接続を使用していずれかのアドバイズ シンクに通知を送信するか、アドバイズ ソース オブジェクトに、 _ulEventMask_パラメーターで指定されているより多くのイベントが発生します。 _LpEntryID_パラメーターが有効なエントリの識別子にポイントして、アドバイズ ソースは、このエントリの識別子によって識別されるオブジェクト。 _LpEntryID_が NULL の場合は、アドバイスのソースは、メッセージ ストアです。 
  
通知を送信するには、メッセージ ストア プロバイダーまたは MAPI のいずれかが登録されているアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 **OnNotify**通知の構造体をパラメーターの 1 つには、特定のイベントを説明する情報が含まれています。
  
## <a name="notes-to-implementers"></a>実装者へのメモ

MAPI の支援の有無にかかわらず、通知をサポートすることができます。 MAPI サービス プロバイダーの通知を実装するために役立つ 3 つのサポート オブジェクトのメソッドを持つ: [IMAPISupport::Subscribe](imapisupport-subscribe.md)、 [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)、および[IMAPISupport::Notify](imapisupport-notify.md)。 MAPI サポートされている方法を使用する場合、 **Subscribe**を呼び出して **、メソッド**が呼び出されたときと、 _lpAdviseSink_ポインターを解放します。 
  
自分で通知をサポートするように選択する場合は、このポインターのコピーを保持するのには、 _lpAdviseSink_パラメーターで表されるアドバイズ シンクの[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。 登録をキャンセルするのには、 [IMsgStore::Unadvise](imsgstore-unadvise.md)メソッドが呼び出されるまでは、このコピーを維持します。 
  
通知をサポートする方法に関係なく、通知の登録には 0 以外の接続番号を割り当てるし、 _lpulConnection_パラメーターに返すことです。 **Unadvise**が呼び出され、完了するまでは、この接続の数を解放しません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

システムでは複数の実行スレッドをサポートする、 **OnNotify**への呼び出しも発生することが任意のスレッドで任意の時点。 必要がありますが確実に特定のスレッドで特定の時刻にのみ通知が発生する場合、は、**アドバイス**に渡すアドバイズ シンク オブジェクトを生成する[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を呼び出します。 
  
**Advise**への呼び出しの後が成功し、 **Unadvise**は、登録をキャンセルするのには呼び出されると、前に、リリースするアドバイズ シンク オブジェクトを準備します。 特定の長期的な使用がない限り、**アドバイス**が返された後は、アドバイズ シンク オブジェクトを解放する必要があります。 
  
通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。 
  
通知の処理の詳細については、[通知の処理](handling-notifications.md)を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI では、 **IMsgStore::Advise**メソッドを使用して、全体のメッセージ ・ ストアに通知を登録します。  <br/> |
   
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[�ʒm](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

