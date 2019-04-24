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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351598"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーから MAPI スプーラーへの受信メッセージの転送を開始します。
  
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
    
 _lpmessage_
  
> 順番読み取り/書き込みアクセス許可を持つメッセージオブジェクト (受信メッセージを表す) へのポインター。これは、そのメッセージにアクセスして操作するためにトランスポートプロバイダーによって使用されます。 このオブジェクトは、トランスポートプロバイダーが**IXPLogon:: startmessage**の呼び出しから戻るまで有効です。
    
 _lアウト msグリーン f_
  
> 読み上げメッセージに割り当てられている参照値へのポインター。 MAPI スプーラーは、この値を1に初期化してから、トランスポートプロバイダーへのポインターを返します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

mapi スプーラーは**IXPLogon:: startmessage**メソッドを呼び出して、トランスポートプロバイダーから mapi スプーラーへの受信メッセージの転送を開始します。 _lpmessage_によって示されたメッセージの使用をトランスポートプロバイダーが開始する前に、 [IXPLogon:: transportnotify](ixplogon-transportnotify.md)メソッドの呼び出しによって使用される可能性のある_lアウト msグリーン f_パラメーターにメッセージ参照を格納する必要があります。 
  
**startmessage**呼び出しの間、MAPI スプーラーは、メッセージの転送中に開かれたオブジェクトのメソッドを処理し、添付ファイルも処理します。 この処理には長い時間がかかることがあります。 トランスポートプロバイダーは、この処理中に多くの場合、MAPI スプーラーの[imapisupport:: SpoolerYield](imapisupport-spooleryield.md) callback 関数を呼び出して、他のシステムタスクに対する CPU 時間を解放することができます。 
  
トランスポートプロバイダーがメッセージに対して作成する受信者テーブル内のすべての受信者に、必要なすべてのアドレス指定プロパティが含まれている必要があります。 必要に応じて、プロバイダーは特定の受信者を表すカスタム受信者を作成できます。 ただし、プロバイダーが詳細情報を含む受信者エントリを作成できる場合は、そのようにする必要があります。 たとえば、アドレス帳プロバイダーの受信者の形式に関する十分な情報がトランスポートプロバイダーにある場合、その形式の受信者に対して有効なエントリ識別子を作成することができます。そのためには、エントリ識別子を作成する必要があります。
  
転送不能なテーブルプロパティが受信されていない場合、トランスポートプロバイダーはそれらを新しいメッセージに格納することはできません。 ただし、トランスポートプロバイダーは、新しいメッセージで受信するすべてのトランスポートテーブルプロパティを格納する必要があります。
  
受信メッセージが配信レポートまたは配信不能レポートで、トランスポートプロバイダーが[imapisupport:: StatusRecips](imapisupport-statusrecips.md)メソッドを使用して元のメッセージからレポートを生成できない場合は、プロバイダー自体に、次のようにメッセージを設定する必要があります。適切なプロパティ。 ただし、トランスポートプロバイダーは、メッセージの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを設定できません。
  
受信メッセージを適切な MAPI メッセージストアに処理した後に保存するには、トランスポートプロバイダーは[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 トランスポートプロバイダーが MAPI スプーラーに渡すメッセージを持っていない場合は、 **SaveChanges**を呼び出さずに**startmessage**呼び出しから戻って、受信メッセージを停止することができます。
  
**startmessage**呼び出し中にトランスポートプロバイダが開くすべてのオブジェクトは、戻る前に解放する必要があります。 ただし、プロバイダーは、MAPI スプーラーが最初に_lpmessage_パラメーターで渡したメッセージオブジェクトを解放することはできません。 
  
**startmessage**がエラーを返した場合は、変更が保存されていない状態で処理中のメッセージが解放され、失われます。 この場合、トランスポートプロバイダーは、NOTIFY_CRITICAL_ERROR フラグを[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドの呼び出しと共に渡し、 [IXPLogon::P oll](ixplogon-poll.md)メソッドを呼び出して、重大なエラー状態にあることを MAPI スプーラーに通知する必要があります。 
  
詳細については、「 [MAPI スプーラーとの対話](interacting-with-the-mapi-spooler.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

