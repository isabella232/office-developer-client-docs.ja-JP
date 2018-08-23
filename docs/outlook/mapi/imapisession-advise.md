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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 45033ab924dcf443e9d231b3a7b4348119758935
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800692"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**適用対象**: Outlook 
  
セッションに影響を与える特定のイベントの通知を受け取ることを登録します。
  
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
  
> [in]アドレス帳またはメッセージ ストアのオブジェクトについては、通知を生成するか、またはセッションにのみ影響するイベントに関する通知を受信するクライアントを登録することを示す、NULL のエントリの識別子へのポインター。 
    
 _ulEventMask_
  
> [in]クライアントに興味を持って登録に含めることが通知イベントの種類を示す値のマスク。 _LpEntryID_が NULL の場合は、MAPI セッションのみに影響する重大なエラー イベントのためにクライアントを自動的に登録します。 _LpEntryID_は、エントリ id をポイントしているときに次の値は、 _ulEventMask_パラメーターに有効です。 
    
fnevCriticalError 
  
> メモリ不足などの重大なエラーに関する通知を登録します。
    
fnevExtended 
  
> レジスタの特定のアドレス帳またはメッセージに特定のイベントに関する通知では、プロバイダーを格納し、セッションのシャット ダウンします。
    
fnevNewMail 
  
> 新しいメッセージの到着の通知を登録します。 
    
fnevObjectCreated 
  
> 新しいオブジェクトの作成についての通知を登録します。
    
fnevObjectCopied
  
> コピーされているオブジェクトについての通知を登録します。
    
fnevObjectDeleted
  
> 削除されているオブジェクトについての通知を登録します。
    
fnevObjectModified
  
> 変更されているオブジェクトについての通知を登録します。
    
fnevObjectMoved
  
> 移動されるオブジェクトについての通知を登録します。
    
fnevSearchComplete
  
> 検索操作の完了に関する通知を登録します。
    
 _lpAdviseSink_
  
> [in]後続の通知を受信するアドバイズ シンク オブジェクトへのポインター。 このアドバイズ シンク オブジェクトは既に割り当てられている必要があります。
    
 _lpulConnection_
  
> [out]呼び出し元の間の接続を表す数値を 0 以外の値へのポインターでは、シンク オブジェクトとのセッションを案内します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 登録が正常に完了しました。
    
MAPI_E_INVALID_ENTRYID 
  
> _LpEntryID_で指定されたエントリの識別子は有効なエントリの識別子ではありません。 
    
MAPI_E_NO_SUPPORT 
  
> _LpEntryID_で指定されたエントリの識別子を担当するサービス プロバイダーは、 _ulEventMask_パラメーターで指定したイベントの種類をサポートしていないか、または通知をサポートしていません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _LpEntryID_で指定されたエントリの識別子は、プロファイル内のサービス プロバイダーのいずれかが処理できません。 
    
## <a name="remarks"></a>注釈

**IMAPISession::Advise**メソッドでは、シンク オブジェクト、セッション、および必要に応じて、サービス プロバイダーにアドバイスの呼び出し元の間の接続を確立します。 この接続を使用していずれかのアドバイズ シンクに通知を送信するか、 _lpEntryID_が指すオブジェクトに、 _ulEventMask_パラメーターで指定されたその他のイベントが発生します。 _LpEntryID_が NULL の場合は、ターゲット オブジェクトは、セッションとのみ、重大なエラー、および拡張イベントの通知を送信します。 
  
_LpEntryID_は、有効なエントリの識別子をポイントしている場合、MAPI は、**担当のサービス プロバイダーに属しているログオン オブジェクトのメソッド**を呼び出します。 などの_lpEntryID_は、配布リストのエントリ id をポイントしている場合、MAPI は、適切なアドレス帳プロバイダーの[IABLogon::Advise](iablogon-advise.md)メソッドを呼び出します。 
  
通知を送信するには、サービス プロバイダーまたは MAPI のいずれかが登録されているアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 **OnNotify**通知の構造体をパラメーターの 1 つには、特定のイベントを説明する情報が含まれています。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

システムでは複数の実行スレッドをサポートする、 **OnNotify**への呼び出しも発生することが任意のスレッドで任意の時点。 特定のスレッドで特定の時刻にのみ通知が発生する保証が必要な場合は、**メソッド**に渡すアドバイズ シンク オブジェクトを生成する[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を呼び出します。 
  
調べるには、クライアントからログオフしたとき、 _lpEntryID_を NULL に設定され_cbEntryID_を 0 に設定の**アドバイス**を呼び出すことによって、サービス ・ プロバイダーに通知を登録します。 ログオフが発生すると、fnevExtended 通知を受け取ります。 
  
**Advise**への呼び出しが成功した後、登録をキャンセルするのには[IMAPISession::Unadvise](imapisession-unadvise.md)前に、特定の長期的な使用がない限り、アドバイズ シンク オブジェクトを放します。 
  
通知の処理の概要については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。 
  
通知の処理の詳細については、[通知の処理](handling-notifications.md)を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI では、 **IMAPISession::Advise**メソッドを使用して、セッションに対して通知を登録します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI のイベント通知](event-notification-in-mapi.md)

