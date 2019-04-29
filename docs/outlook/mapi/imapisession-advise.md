---
title: imapisessionadvise
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
  
セッションに影響を与える指定したイベントの通知を受信するように登録します。
  
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
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番通知を生成する必要があるアドレス帳またはメッセージストアオブジェクトのエントリ id へのポインター。または、クライアントがセッションにのみ影響を与えるイベントに関する通知を受信するように登録していることを示します。 
    
 _uleventmask_
  
> 順番クライアントが関心を持っている通知イベントの種類を示す値のマスク。また、登録に含める必要があります。 _lな tryid_が NULL の場合、MAPI は、セッションにのみ影響を与える重大なエラーイベントに対してクライアントを自動的に登録します。 _lare tryid_がエントリ識別子を指す場合、 _uleventmask_パラメーターには次の値が有効です。 
    
fnevCriticalError 
  
> メモリ不足などの重大なエラーに関する通知を登録します。
    
fnevExtended 
  
> 特定のアドレス帳またはメッセージストアプロバイダーに固有のイベントと、セッションがシャットダウンしたことに関する通知を登録します。
    
fnevNewMail 
  
> 新しいメッセージが到着したことに関する通知を登録します。 
    
fnevObjectCreated 
  
> 新しいオブジェクトの作成に関する通知を登録します。
    
fnevObjectCopied
  
> コピーされているオブジェクトに関する通知を登録します。
    
fnevObjectDeleted
  
> 削除されるオブジェクトに関する通知を登録します。
    
fnevObjectModified
  
> 変更されているオブジェクトに関する通知を登録します。
    
fnevObjectMoved
  
> 移動中のオブジェクトに関する通知を登録します。
    
fnevSearchComplete
  
> 検索操作の完了に関する通知を登録します。
    
 _lpAdviseSink_
  
> 順番後続の通知を受け取るアドバイズシンクオブジェクトへのポインター。 このアドバイズシンクオブジェクトは、既に割り当てられている必要があります。
    
 _lアウト接続_
  
> 読み上げ呼び出し元のアドバイズシンクオブジェクトとセッション間の接続を表す0以外の数値へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録に成功しました。
    
MAPI_E_INVALID_ENTRYID 
  
> _lな tryid_が指すエントリ識別子が有効なエントリ識別子を表していません。 
    
MAPI_E_NO_SUPPORT 
  
> _lな tryid_で指定されたエントリ識別子を担当するサービスプロバイダーは、 _uleventmask_パラメーターで指定されたイベントの種類をサポートしていないか、または通知をサポートしていません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lな tryid_で示されるエントリ識別子は、プロファイル内のどのサービスプロバイダーでも処理できません。 
    
## <a name="remarks"></a>注釈

**imapisession:: アドバイズ**メソッドは、呼び出し元のアドバイズシンクオブジェクト、セッション、およびサービスプロバイダーの間の接続を確立します。 この接続は、 _uleventmask_パラメーターで指定された1つ以上のイベントが、 _lな tryid_によって参照されるオブジェクトに対して発生したときに、アドバイズシンクに通知を送信するために使用されます。 _lare tryid_が NULL の場合、ターゲットオブジェクトはセッションで、重大なエラーと拡張イベントに対してのみ通知が送信されます。 
  
_lpentryid_が有効なエントリ識別子を指している場合、MAPI は、責任のあるサービスプロバイダーに属するログオンオブジェクトの**アドバイズ**メソッドを呼び出します。 たとえば、lIABLogon _tryid_が配布リストのエントリ識別子を指す場合、MAPI は適切なアドレス帳プロバイダーの[:: Advise](iablogon-advise.md)メソッドを呼び出します。 
  
通知を送信するために、サービスプロバイダーまたは MAPI は、登録されているアドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 **onnotify**へのパラメーターの1つは通知構造で、特定のイベントを説明する情報が含まれています。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数の実行スレッドをサポートするシステムでは、 **onnotify**への呼び出しは任意のスレッドでいつでも発生する可能性があります。 特定のスレッドの特定の時点でのみ通知が発生することを保証する必要がある場合は、 [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を呼び出して、**アドバイズ**メソッドに渡すアドバイズシンクオブジェクトを生成します。 
  
クライアントがいつログオフしたかを確認するには、 _lcbEntryID tryid_を**** NULL に設定し、 __ を0に設定して、サービスプロバイダーに通知を登録します。 ログオフが発生すると、fnevExtended 通知が表示されます。 
  
**アドバイズ**の呼び出しが成功し、 [imapisession::](imapisession-unadvise.md)登録をキャンセルする前に、アドバイズシンクを呼び出した後、特定の長期間使用しない限り、アドバイズシンクオブジェクトを解放します。 
  
通知プロセスの概要については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。 
  
通知の処理の詳細については、「[通知の処理](handling-notifications.md)」を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|basedialog  <br/> |cbasedialog:: onnotificationson  <br/> |mfcmapi は、 **imapisession:: アドバイズ**メソッドを使用して、セッションに対する通知を登録します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI のイベント通知](event-notification-in-mapi.md)

