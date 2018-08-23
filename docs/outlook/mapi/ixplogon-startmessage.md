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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3758cf72aa79dbf500138e96872352950fafbd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801263"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**適用対象**: Outlook 
  
MAPI スプーラーをトランスポート プロバイダーからの受信メッセージの転送を開始します。
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpMessage_
  
> [in]オブジェクトへのポインターをメッセージ (受信メッセージを表す) にアクセスしてそのメッセージを操作するトランスポート プロバイダーによって使用される、読み取り/書き込み権限を持っています。 トランスポート プロバイダーは、 **IXPLogon::StartMessage**への呼び出しから制御が戻った後、このオブジェクトは有効期限のままになります。
    
 _lpulMsgRef_
  
> [out]メッセージに割り当てられている参照の値へのポインター。 MAPI スプーラーは、トランスポート プロバイダーへのポインターを返す前に、1 にこの値を初期化します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

MAPI スプーラーは、MAPI スプーラーをトランスポート プロバイダーからの受信メッセージの転送を開始するのには**IXPLogon::StartMessage**メソッドを呼び出します。 _LpMessage_が指すメッセージに使用するトランスポート プロバイダーが開始されると、前に[IXPLogon::TransportNotify](ixplogon-transportnotify.md)メソッドを呼び出すことで潜在的な使用に対応する_lpulMsgRef_パラメーターにメッセージの参照が格納される必要があります。 
  
**StartMessage**の呼び出し中に MAPI スプーラーは、メッセージの転送中に開かれるオブジェクトのメソッドを処理しもすべての添付ファイルを処理します。 この処理時間がかかることができます。 トランスポート プロバイダーは、他のシステム タスクの CPU 時間を解放するには、この処理中に頻繁に、MAPI スプーラーの[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)コールバック関数を呼び出すことができます。 
  
トランスポート プロバイダーを作成、メッセージの受信者テーブル内のすべての受信者には、必要なすべてのアドレス指定プロパティを含める必要があります。 必要に応じて、プロバイダーは、特定の受信者を表すためのカスタム受信者を作成できます。 ただし、プロバイダーが複数の情報が含まれる受信者のエントリを生成できる場合に行ってください。 など、トランスポート プロバイダーにその形式の受信者のエントリの有効な識別子を構築できます、アドレス帳プロバイダーの受信者の形式について十分な情報がある場合は、エントリの識別子を作成する必要があります。
  
Nontransmittable プロパティは、受信した場合トランスポート プロバイダーは、保存しないようにして新しいメッセージにします。 ただし、トランスポート プロバイダーは、新しいメッセージを受信するすべての転送可能なプロパティを格納する必要があります。
  
着信メッセージが配信レポートまたは配信不能レポートには、トランスポート プロバイダーは、 [IMAPISupport::StatusRecips](imapisupport-statusrecips.md)メソッドを使用して、元のメッセージからレポートを生成することは、プロバイダーする必要があります自体を先に設定のメッセージ適切なプロパティです。 ただし、トランスポート プロバイダーは、メッセージの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティを設定できません。
  
処理後、適切な MAPI メッセージ ・ ストアに受信メッセージを保存するには、トランスポート プロバイダーは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 トランスポート プロバイダーがすべてのメッセージを MAPI スプーラーを無効にするのには、 **SaveChanges**を呼び出すことがなく、 **StartMessage**の呼び出しから返すことで、着信メッセージを停止できます。
  
返す前に**StartMessage**の呼び出し中に、トランスポート プロバイダーが表示されるすべてのオブジェクトを解放するようにします。 ただし、プロバイダーでは、MAPI スプーラーが最初_lpMessage_パラメーターに渡されるメッセージ オブジェクトは開放しなければなりません。 
  
**StartMessage**がエラーを返した場合プロセス内のメッセージは変更内容を保存せずにリリースがされ、失われます。 この例では、トランスポート プロバイダーは[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出して、NOTIFY_CRITICAL_ERROR フラグを渡すし、MAPI スプーラーの重大なエラー状態であることを通知するために[IXPLogon::Poll](ixplogon-poll.md)メソッドを呼び出す必要があります。 
  
詳細については、 [MAPI スプーラーと対話する](interacting-with-the-mapi-spooler.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

