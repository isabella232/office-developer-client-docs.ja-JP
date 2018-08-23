---
title: IXPLogonSubmitMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.SubmitMessage
api_type:
- COM
ms.assetid: a261ba0d-cb56-4935-b745-1d4bbd0b8b9d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 28e7874d1e61c0a4fe0ad702f206ca03a9a1096a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575876"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI スプーラーがメッセージを配信するトランスポート プロバイダーを持っていることを示します。
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]メッセージの送信方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
BEGIN_DEFERRED 
  
> MAPI スプーラーは既に遅延されたメッセージのトランスポート プロバイダーを呼び出しています。 メッセージのエントリ id は、それが延期された場合と同じです。 メッセージは、MAPI スプーラーを無効に NOTIFY_SENTDEFERRED フラグを指定して[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを使用して、そのエントリの識別子を渡すことによって延期されました。 
    
 _lpMessage_
  
> [in]トランスポート プロバイダーを使用してアクセスし、そのメッセージを操作する、読み取り/書き込み権限を持っている (配信されるメッセージを表す)、メッセージ オブジェクトへのポインター。 トランスポート プロバイダーは、 [IXPLogon::EndMessage](ixplogon-endmessage.md)メソッドへの後続の呼び出しから制御が戻った後、このオブジェクトは有効期限のままになります。 
    
 _lpulMsgRef_
  
> [out]トランスポート プロバイダーがそれには、このメッセージに割り当てられている参照の値を返します。 変数へのポインター。 MAPI スプーラーは、このメッセージの後続の呼び出しでこの参照値を渡します。 MAPI スプーラーは、トランスポート プロバイダーを返す前に 0 に値を初期化します。
    
 _lpulReturnParm_
  
> [out]**SubmitMessage**によって返される MAPI_E_WAIT または MAPI_E_NETWORK_ERROR のエラー値に対応する変数へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
MAPI_E_BUSY 
  
> トランスポート プロバイダーは、別の操作を実行しているために、メッセージを処理できません。 プロバイダーでは、処理が発生していないことと、MAPI スプーラーが**EndMessage**を呼び出す必要がありますいないことを示すためにこの戻り値を使用する必要があります。 MAPI スプーラーは、 **SubmitMessage**の呼び出しを後で再試行されます。 
    
MAPI_E_CANCEL 
  
> トランスポート プロバイダーは、 **SpoolerNotify**呼び出しの前にメッセージを MAPI スプーラーが再送信を要求された条件が変更されたため、メッセージを再送しない必要があります。 MAPI スプーラーが他の何かの処理に進みます。 
    
MAPI_E_NETWORK_ERROR 
  
> ネットワーク エラーでは、操作が正常に完了できませんでした。 _LpulReturnParm_パラメーターは、MAPI スプーラーが、メッセージを再送信するまでの秒数を設定する必要があります。 
    
MAPI_E_NOT_ME 
  
> トランスポート プロバイダーは、このメッセージを処理できません。 別のトランスポート プロバイダーを検索するのには、MAPI スプーラーを無効してください。 プロバイダーでは、処理が発生していないことと、MAPI スプーラーが**EndMessage**を呼び出す必要がありますいないことを示すためにこの戻り値を使用する必要があります。
    
MAPI_E_WAIT 
  
> 一時的な問題では、トランスポート プロバイダーがメッセージを処理できなくなります。 _LpulReturnParm_パラメーターは、MAPI スプーラーが、メッセージを再送信するまでの秒数を設定する必要があります。 
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、必要があるメッセージを配信するトランスポート プロバイダーの場合、 **IXPLogon::SubmitMessage**メソッドを呼び出します。 メッセージは、 _lpMessage_パラメーターを使用して、トランスポート プロバイダーに渡されます。 
  
プロバイダーがメッセージを受信する準備ができた場合は、 _lpulMsgRef_パラメーター、プロセス、渡されたオブジェクトを使用して参照値を返すし、適切な値 (通常は S_OK) を返すする必要があります。 プロバイダーが転送を処理する準備ができていない場合は、エラー値を返す必要があり、必要に応じて、別の MAPI 戻り値でメッセージを再送信する前に、MAPI スプーラーが待機する時間の長さを示すために_lpulReturnParm_ 。 
  
このメソッドの実装をトランスポート プロバイダーは、次に行うことができます。
  
- 可能性のあるローカル ・ ストレージにメッセージをコピー、転送を待機する内部のキューにメッセージを配置しを返します。
    
- 実際の転送を実行し、転送が完了すると、正常終了または失敗のいずれかを取得しようとします。
    
- 関連するリソースを確認した後にメッセージを送信するかどうかを決定します。 この例では、リソースが空の場合は、プロバイダー リソースをロック、メッセージを準備して提出できること。 リソースがビジー状態の場合は、プロバイダーはメッセージを準備し、後で送信を延期できます。
    
メッセージの伝送のための手法をお勧めは、トランスポート プロバイダーやプロセスがシステム リソースの競合の数によって異なります。 
  
**SubmitMessage**の呼び出し中には、トランスポート プロバイダーは、メッセージ オブジェクトからのメッセージのデータの転送を制御します。 ただし、トランスポート プロバイダーは、先にポインターを返します_lpulMsgRef_データを転送する前に、メッセージに参照値を割り当てる必要があります。 MAPI スプーラー プロセス中に任意の時点で NOTIFY_CANCEL_MESSAGE フラグを指定して[IXPLogon::TransportNotify](ixplogon-transportnotify.md)メソッドを呼び出すことができますので設定ことを示すプロバイダーは任意の開いているオブジェクトを解放するメッセージの転送を停止します。 
  
トランスポート プロバイダーは、メッセージの任意の nontransmittable プロパティを送信することはできません。 このようなプロパティが検出されるに移動します、次のプロパティを処理します。 プロバイダーは、送信されたメッセージのコンテンツの一部として MAPI_P1 の受信者情報を表示しないように、あらゆる努力をする必要があります。プロバイダーは、目的のアドレスに対してのみ、この受信者の情報を使用してください。 MAPI_P1 の受信者は、メッセージを再送信に使用される内部で生成された受信者です。それらは転送されませんする必要があります。 代わりに、他の受信者を使用して、受信者情報を送信するためです。 この方法の目的は、元の受信者として正確な同じ受信者テーブルを表示する受信者を再送信を許可するように。
  
**SubmitMessage**の呼び出し中に MAPI スプーラーは、メッセージの転送中に開かれているオブジェクトのメソッドを処理し、すべての添付ファイルを処理します。 この処理時間がかかることができます。 トランスポート プロバイダーは、他のシステム タスクの CPU 時間を解放するには、この処理中に頻繁に、MAPI スプーラーの[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)メソッドを呼び出すことができます。 
  
すべてのメッセージ受信者は、MAPI スプーラーが最初に渡されるメッセージの受信者テーブルに表示されます。 トランスポート プロバイダーに処理可能な受信者のみを処理する必要があります-エントリ id、アドレスの種類、またはその両方に基づいて-をしていない、**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを TRUE に設定するとします。 **れない**は既に TRUE に設定されている別のトランスポート プロバイダーがその受信者を処理します。 プロバイダーには、その受信者にメッセージを処理できるかどうかを判断するのには受信者のための十分な処理が完了すると、その必要がありますその受信者の**れない**プロパティを設定、渡されたメッセージの場合は TRUE。 通常、メッセージの配信が完了した後、プロバイダーは、この決定により、です。 
  
通常、トランスポート プロバイダーを返さない**SubmitMessage**の呼び出しからのメッセージ データの転送が完了するまでです。 エラーが返されない場合プロバイダーに、MAPI スプーラーから次の呼び出しは、 [IXPLogon::EndMessage](ixplogon-endmessage.md)メソッドを呼び出しです。 
  
**SubmitMessage**がエラーを返した場合、MAPI スプーラーは変更を保存せずプロセス内のメッセージを解放します。 トランスポート プロバイダーでは、メッセージの変更を保存する必要がある場合は、戻る前にメッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すする必要があります。 
  
トランスポートの問題が原因で発生するエラーが発生した場合、MAPI スプーラーが、メッセージを保持ですが、 _lpulReturnParm_で返される値に基づいてトランスポート プロバイダーは、メッセージを再送信することなきます。 トランスポート プロバイダーはする必要があります**SubmitMessage**からの戻り値の値が MAPI_E_WAIT または MAPI_E_NETWORK_ERROR である場合に、その値を入力します。 重大なエラー状態が発生した場合、トランスポート プロバイダーは、NOTIFY_CRITICAL_ERROR フラグを指定して[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出す必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

