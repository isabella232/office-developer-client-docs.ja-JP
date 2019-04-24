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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ae124cb94cff5be0a655386d31f1bf2c82f66a85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351591"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーが配信するメッセージを MAPI スプーラーに指定します。
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番メッセージの送信方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
BEGIN_DEFERRED 
  
> MAPI スプーラーは、以前に延期されたメッセージでトランスポートプロバイダーを呼び出しています。 メッセージのエントリ識別子は、延期されたときと同じです。 NOTIFY_SENTDEFERRED フラグを使用して[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドを使用することにより、メッセージはエントリ id を MAPI スプーラーに戻すことによって延期されました。 
    
 _lpmessage_
  
> 順番読み取り/書き込みアクセス許可を持つメッセージオブジェクト (配信するメッセージを表す) へのポインター。これは、トランスポートプロバイダーがそのメッセージにアクセスして操作するために使用します。 このオブジェクトは、トランスポートプロバイダーが[IXPLogon:: endmessage](ixplogon-endmessage.md)メソッドの次の呼び出しから戻るまで有効です。 
    
 _lアウト msグリーン f_
  
> 読み上げトランスポートプロバイダーが、このメッセージに割り当てた参照値を返す変数へのポインター。 MAPI スプーラーは、このメッセージに対する以降の呼び出しでこの参照値を渡します。 MAPI スプーラーは値を0に初期化してから、トランスポートプロバイダーに返します。
    
 _lpulReturnParm_
  
> 読み上げ**submitmessage**によって返される MAPI_E_WAIT または MAPI_E_NETWORK_ERROR ERROR の値に対応する変数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
MAPI_E_BUSY 
  
> トランスポートプロバイダーが別の操作を実行しているため、メッセージを処理できません。 プロバイダーは、この戻り値を使用して、処理が発生していないこと、および MAPI スプーラーが**endmessage**を呼び出すことができないことを示す必要があります。 MAPI スプーラーは、後で**submitmessage**呼び出しを再試行します。 
    
MAPI_E_CANCEL 
  
> トランスポートプロバイダーは、MAPI スプーラーが以前の**SpoolerNotify**呼び出しでメッセージを再送信することを要求しましたが、条件は変更されたため、メッセージを再送信しないでください。 MAPI スプーラーは、別のものを処理するためにに進みます。 
    
MAPI_E_NETWORK_ERROR 
  
> ネットワークエラーにより、操作が正常に完了しませんでした。 _lpulReturnParm_パラメーターは、MAPI スプーラーでメッセージが再送信されるまでの経過時間 (秒数) に設定する必要があります。 
    
MAPI_E_NOT_ME 
  
> トランスポートプロバイダーは、このメッセージを処理できません。 MAPI スプーラーは、別のトランスポートプロバイダーの検索を試みる必要があります。 プロバイダーは、この戻り値を使用して、処理が発生していないこと、および MAPI スプーラーが**endmessage**を呼び出すことができないことを示す必要があります。
    
MAPI_E_WAIT 
  
> 一時的な問題により、トランスポートプロバイダーがメッセージを処理できなくなります。 _lpulReturnParm_パラメーターは、MAPI スプーラーでメッセージが再送信されるまでの経過時間 (秒数) に設定する必要があります。 
    
## <a name="remarks"></a>解説

MAPI スプーラーは、トランスポートプロバイダーが配信するメッセージを持っているときに、 **IXPLogon:: submitmessage**メソッドを呼び出します。 メッセージは、 _lpmessage_パラメーターを使用してトランスポートプロバイダーに渡されます。 
  
プロバイダーがメッセージを受け入れる準備ができている場合は、 _lアウト msグリーン f_パラメーターを使用して参照値を返し、渡されたオブジェクトを処理して、適切な値 (通常は S_OK) を返します。 プロバイダーが転送を処理する準備ができていない場合は、エラー値を返し、必要に応じて、 _lpulReturnParm_の別の mapi の戻り値を返して、メッセージを再送信するまでに mapi スプーラーが待機する時間を指定します。 
  
このメソッドのトランスポートプロバイダーの実装では、次のことを行うことができます。
  
- メッセージを内部キューに配置して、送信を待機します。場合によっては、メッセージをローカルストレージにコピーして、を返します。
    
- 実際の送信を実行し、送信が完了したときに、成功または失敗のどちらかを試行します。
    
- リソースを確認した後、メッセージを送信するかどうかを決定します。 この例では、リソースが空いている場合、プロバイダーはリソースをロックし、メッセージを準備して送信できます。 リソースがビジー状態である場合、プロバイダーはメッセージを準備し、後で送信を延期することができます。
    
メッセージ転送に推奨される方法は、トランスポートプロバイダーと、システムリソースに対して競合する予期されるプロセス数によって異なります。 
  
**submitmessage**呼び出しの間、トランスポートプロバイダーは、message オブジェクトからのメッセージデータの転送を制御します。 ただし、トランスポートプロバイダーは、データを転送する前に、 _lアウト msグリーン f_でポインターを返す参照値をメッセージに割り当てる必要があります。 そのためには、処理中の任意の時点で MAPI スプーラーは[IXPLogon:: transportnotify](ixplogon-transportnotify.md)メソッドを NOTIFY_CANCEL_MESSAGE flag セットで呼び出して、開いているオブジェクトを解放し、メッセージ転送を停止する必要があることをプロバイダーに通知することができます。 
  
トランスポートプロバイダーは、メッセージの転送不能なテーブルプロパティを送信することはできません。 そのようなプロパティが見つかったら、次のプロパティを処理する必要があります。 プロバイダーは、送信されたメッセージコンテンツの一部として MAPI_P1 受信者情報を表示しないように、すべての努力を行う必要があります。プロバイダーは、アドレス指定のためにのみこの受信者情報を使用する必要があります。 MAPI_P1 の受信者は、メッセージの再送信に使用される内部で生成された受信者です。送信されないようにする必要があります。 代わりに、他の受信者を使用して受信者情報を送信します。 この方法の目的は、再送者が元の受信者とまったく同じ受信者テーブルを表示することを許可することです。
  
**submitmessage**呼び出しの間、MAPI スプーラーは、メッセージの転送中に開かれるオブジェクトのメソッドを処理し、添付ファイルを処理します。 この処理には長い時間がかかることがあります。 トランスポートプロバイダーは、この処理中に多くの場合、MAPI スプーラーの[imapisupport:: SpoolerYield](imapisupport-spooleryield.md)メソッドを呼び出して、他のシステムタスクの CPU 時間を解放できます。 
  
すべてのメッセージの受信者は、MAPI スプーラーが最初に渡されたメッセージの recipient テーブルに表示されます。 トランスポートプロバイダーは、エントリ識別子、アドレスの種類、またはその両方に基づいて処理できる受信者のみを処理する必要があります。また、 **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティが TRUE に設定されていません。 **PR_RESPONSIBILITY**が既に TRUE に設定されている場合、別のトランスポートプロバイダーがその受信者を処理しています。 受信者が受信者のメッセージを処理できるかどうかを判断するために、プロバイダーがその受信者の十分な処理を完了した場合、渡されたメッセージの受信者の**PR_RESPONSIBILITY**プロパティを TRUE に設定する必要があります。 通常、メッセージの配信が完了した後、プロバイダーはこの判断を行います。 
  
通常、トランスポートプロバイダーは、メッセージデータの転送が完了するまで、 **submitmessage**呼び出しからは戻りません。 エラーが返されない場合、MAPI スプーラーからプロバイダーへの次の呼び出しは、 [IXPLogon:: endmessage](ixplogon-endmessage.md)メソッドの呼び出しです。 
  
**submitmessage**がエラーを返した場合、MAPI スプーラーは変更を保存せずに、処理中のメッセージを解放します。 トランスポートプロバイダーがメッセージの変更を保存する必要がある場合は、返す前にメッセージに対して[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要があります。 
  
トランスポートの問題が原因でエラーが発生した場合、MAPI スプーラーはそのメッセージを保持しますが、 _lpulReturnParm_で返された値に基づいてトランスポートプロバイダーへのメッセージの送信を遅らせます。 **submitmessage**からの戻り値が MAPI_E_WAIT または MAPI_E_NETWORK_ERROR の場合、トランスポートプロバイダーはその値を入力する必要があります。 重大なエラー状態が発生した場合、トランスポートプロバイダーは、NOTIFY_CRITICAL_ERROR フラグを使用して[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出す必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

