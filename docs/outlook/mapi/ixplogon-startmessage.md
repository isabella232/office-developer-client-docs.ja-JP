---
title: IXPLogonStartMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 00273d5572fa0c12a9501a1620db11ea087fd5d1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427606"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーから MAPI スプーラーへの受信メッセージの転送を開始します。
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpMessage_
  
> [in]読み取り/書き込みアクセス許可を持つメッセージ オブジェクト (受信メッセージを表す) へのポインター 。このポインターは、トランスポート プロバイダーがメッセージにアクセスして操作するために使用します。 このオブジェクトは、トランスポート プロバイダーが **IXPLogon::StartMessage** への呼び出しから戻るまで有効です。
    
 _lpulMsgRef_
  
> [out]メッセージに割り当てられた参照値へのポインター。 MAPI スプーラーは、トランスポート プロバイダーへのポインターを返す前に、この値を 1 に初期化します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

MAPI スプーラーは **、IXPLogon::StartMessage** メソッドを呼び出して、トランスポート プロバイダーから MAPI スプーラーへの受信メッセージの転送を開始します。 トランスポート プロバイダーは _、lpMessage_ が示すメッセージの使用を開始する前に [、IXPLogon::TransportNotify](ixplogon-transportnotify.md)メソッドの呼び出しで使用される可能性があるメッセージ参照を _lpulMsgRef_ パラメーターに格納する必要があります。 
  
**StartMessage 呼び出し** 中に、MAPI スプーラーはメッセージの転送中に開いたオブジェクトのメソッドを処理し、添付ファイルも処理します。 この処理には長い時間がかかる場合があります。 トランスポート プロバイダーは、この処理中に MAPI スプーラーの [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) コールバック関数を頻繁に呼び出して、他のシステム タスクの CPU 時間を解放できます。 
  
トランスポート プロバイダーがメッセージ用に作成する受信者テーブル内のすべての受信者には、必要なすべてのアドレス指定プロパティが含まれている必要があります。 必要に応じて、プロバイダーは、特定の受信者を表すカスタム受信者を作成できます。 ただし、プロバイダーが詳細な情報を含む受信者エントリを生成できる場合は、そのエントリを作成する必要があります。 たとえば、トランスポート プロバイダーがアドレス帳プロバイダーの受信者形式に関する十分な情報を持ち、その形式の受信者の有効なエントリ識別子を作成できる場合は、エントリ識別子を作成する必要があります。
  
転送できないプロパティを受信した場合、トランスポート プロバイダーは新しいメッセージに保存しません。 ただし、トランスポート プロバイダーは、受信した送信可能なすべてのプロパティを新しいメッセージに格納する必要があります。
  
受信メッセージが配信レポートまたは配信不能レポートであり、トランスポート プロバイダーが [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) メソッドを使用して元のメッセージからレポートを生成できない場合、プロバイダー自体が適切なプロパティをメッセージに設定する必要があります。 ただし、トランスポート プロバイダーは、メッセージのプロパティ [(PidTagEntryId)](pidtagentryid-canonical-property.md) **PR_ENTRYIDを設定** できません。
  
処理後に受信メッセージを適切な MAPI メッセージ ストアに保存するには、トランスポート プロバイダーが [IMAPIProp::SaveChanges メソッドを呼び出](imapiprop-savechanges.md) します。 トランスポート プロバイダーが MAPI スプーラーに渡すメッセージがない場合は **、SaveChanges** を呼び出さずに **StartMessage** 呼び出しから返すことによって、受信メッセージを停止できます。
  
**StartMessage** 呼び出し中にトランスポート プロバイダーが開くすべてのオブジェクトは、戻る前に解放する必要があります。 ただし、プロバイダーは、MAPI スプーラーが最初に lpMessage パラメーターで渡したメッセージ オブジェクト  _を解放する必要_ があります。 
  
**StartMessage が** エラーを返した場合、変更を保存せずにプロセス内のメッセージが解放され、失われます。 この場合、トランスポート プロバイダーは [、IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) メソッドへの呼び出しで NOTIFY_CRITICAL_ERROR フラグを渡し [、IXPLogon::P oll](ixplogon-poll.md) メソッドを呼び出して、重大なエラー状態にあることを MAPI スプーラーに通知する必要があります。 
  
詳細については [、「MAPI スプーラーとの対話」を参照してください](interacting-with-the-mapi-spooler.md)。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

