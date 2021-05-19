---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419836"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッションに影響を与える指定されたイベントの通知を受信するために登録します。
  
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
  
> [in]生成する必要がある通知に関するアドレス帳またはメッセージ ストア オブジェクトのエントリ識別子へのポインター、または NULL 。これは、クライアントがセッションにのみ影響を与えるイベントに関する通知を受信するために登録中です。 
    
 _ulEventMask_
  
> [in]クライアントが関心を持ち、登録に含める必要がある通知イベントの種類を示す値のマスク。 _lpEntryID が_ NULL の場合、MAPI はセッションにのみ影響する重大なエラー イベントのためにクライアントを自動的に登録します。 _lpEntryID が_ エントリ識別子をポイントすると _、ulEventMask_ パラメーターに対して次の値が有効になります。 
    
fnevCriticalError 
  
> メモリ不足などの重大なエラーに関する通知を登録します。
    
fnevExtended 
  
> 特定のアドレス帳またはメッセージ ストア プロバイダーに固有のイベントとセッションのシャットダウンに関する通知を登録します。
    
fnevNewMail 
  
> 新しいメッセージの到着に関する通知を登録します。 
    
fnevObjectCreated 
  
> 新しいオブジェクトの作成に関する通知を登録します。
    
fnevObjectCopied
  
> コピーするオブジェクトに関する通知を登録します。
    
fnevObjectDeleted
  
> 削除するオブジェクトに関する通知を登録します。
    
fnevObjectModified
  
> 変更するオブジェクトに関する通知を登録します。
    
fnevObjectMoved
  
> 移動するオブジェクトに関する通知を登録します。
    
fnevSearchComplete
  
> 検索操作の完了に関する通知を登録します。
    
 _lpAdviseSink_
  
> [in]後続の通知を受信するアアドバイス シンク オブジェクトへのポインター。 このアアドバイス シンク オブジェクトは既に割り当てられている必要があります。
    
 _lpulConnection_
  
> [out]呼び出し元の通知シンク オブジェクトとセッションの間の接続を表す 0 以外の数値へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録が成功しました。
    
MAPI_E_INVALID_ENTRYID 
  
> _lpEntryID_ が指すエントリ識別子は、有効なエントリ識別子を表すではありません。 
    
MAPI_E_NO_SUPPORT 
  
> _lpEntryID_ が指すエントリ識別子を担当するサービス プロバイダーは _、ulEventMask_ パラメーターで指定されたイベントの種類をサポートしていないか、通知をサポートしていません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lpEntryID_ が指すエントリ識別子は、プロファイル内のサービス プロバイダーでは処理できません。 
    
## <a name="remarks"></a>注釈

**IMAPISession::Advise** メソッドは、呼び出し元のアアドバイス シンク オブジェクト、セッション、およびオプションでサービス プロバイダー間の接続を確立します。 この接続は  _、ulEventMask_ パラメーターで指定された 1 つ以上のイベントが  _lpEntryID_ によって指されるオブジェクトに発生した場合に、アアドバイス シンクに通知を送信するために使用されます。 _lpEntryID が_ NULL の場合、ターゲット オブジェクトはセッションであり、重大なエラーと拡張イベントに対してだけ通知が送信されます。 
  
_lpEntryID が有効_ なエントリ識別子をポイントすると、MAPI は責任あるサービス プロバイダーに属するログオン オブジェクトの **Advise** メソッドを呼び出します。 たとえば  _、lpEntryID_ が配布リストのエントリ識別子をポイントする場合、MAPI は適切なアドレス帳プロバイダーの [IABLogon::Advise メソッドを呼び出](iablogon-advise.md) します。 
  
通知を送信するには、サービス プロバイダーまたは MAPI が登録されているアアドバイス シンクの [IMAPIAdviseSink::OnNotify メソッドを呼び出](imapiadvisesink-onnotify.md) します。 通知構造である **OnNotify** のパラメーターの 1 つには、特定のイベントを記述する情報が含まれています。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数の実行スレッドをサポートするシステムでは **、OnNotify** の呼び出しは、任意のスレッドでもいつでも実行できます。 通知が特定のスレッド上の特定の時間にのみ発生する保証が必要な場合は [、HrThisThreadAdviseSink](hrthisthreadadvisesink.md) 関数を呼び出して **、Advise** メソッドに渡すアアドバイス シンク オブジェクトを生成します。 
  
クライアントがログオフした時間を確認するには、lpEntryID を NULLに設定し _、cbEntryID_ を 0 に設定して、サービス プロバイダーに通知を登録します。 ログオフが発生すると、fnevExtended 通知が表示されます。 
  
**Advise** の呼び出しが成功した後 [、IMAPISession::Unadvise](imapisession-unadvise.md)が呼び出され、登録を取り消す前に、特定の長期的な使用がない限り、アアドバイス シンク オブジェクトを解放します。 
  
通知プロセスの概要については、「MAPI の [イベント通知」を参照してください](event-notification-in-mapi.md)。 
  
通知の処理の詳細については、「通知の処理」 [を参照してください](handling-notifications.md)。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI は **IMAPISession::Advise** メソッドを使用して、セッションに対する通知を登録します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI のイベント通知](event-notification-in-mapi.md)

