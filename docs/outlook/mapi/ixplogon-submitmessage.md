---
title: IXPLogonSubmitMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.SubmitMessage
api_type:
- COM
ms.assetid: a261ba0d-cb56-4935-b745-1d4bbd0b8b9d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0d7a58e0aea54c40f44609dcf51e968762f04edf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571550"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーにトランスポート プロバイダーが配信するメッセージが含まれています。
  
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
  
> [in]メッセージの送信方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
BEGIN_DEFERRED 
  
> MAPI スプーラーは、以前に延期されたメッセージを含むトランスポート プロバイダーを呼び出しています。 メッセージのエントリ識別子は、延期された場合と同じです。 メッセージは [、IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) メソッドを NOTIFY_SENTDEFERRED フラグと一緒に使用して、MAPI スプーラーにエントリ識別子を渡して延期されました。 
    
 _lpMessage_
  
> [in]読み取り/書き込みアクセス許可を持つメッセージ オブジェクト (配信するメッセージを表す) へのポインター。トランスポート プロバイダーは、そのメッセージにアクセスして操作するために使用します。 このオブジェクトは、トランスポート プロバイダーが [IXPLogon::EndMessage](ixplogon-endmessage.md) メソッドへの後続の呼び出しから戻るまで有効です。 
    
 _lpulMsgRef_
  
> [out]トランスポート プロバイダーが、このメッセージに割り当てられた参照値を返す変数へのポインター。 MAPI スプーラーは、このメッセージの後続の呼び出しでこの参照値を渡します。 MAPI スプーラーは、トランスポート プロバイダーに返す前に値を 0 に初期化します。
    
 _lpulReturnParm_
  
> [out] **SubmitMessage** によって返されるエラー値またはエラー値に対応MAPI_E_WAIT変数MAPI_E_NETWORK_ERRORポインターです。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
MAPI_E_BUSY 
  
> トランスポート プロバイダーは、別の操作を実行するために、メッセージを処理できません。 プロバイダーは、この戻り値を使用して、処理が発生し、MAPI スプーラーが EndMessage を呼び出す必要がないかどうかを **示す必要があります**。 MAPI スプーラーは、後で **SubmitMessage 呼び出しを** 再試行します。 
    
MAPI_E_CANCEL 
  
> トランスポート プロバイダーは、MAPI スプーラーが以前のスプーラー **Notify** 呼び出しでメッセージを再送信することを要求したが、その後、条件が変更され、メッセージを再送信する必要はありません。 MAPI スプーラーは、他の処理に進むでしょう。 
    
MAPI_E_NETWORK_ERROR 
  
> ネットワーク エラーによって、操作が正常に完了しなかった。 _lpulReturnParm_ パラメーターは、MAPI スプーラーがメッセージを再送信するまでに経過する秒の数に設定する必要があります。 
    
MAPI_E_NOT_ME 
  
> トランスポート プロバイダーは、このメッセージを処理できません。 MAPI スプーラーは、別のトランスポート プロバイダーを検索しようとする必要があります。 プロバイダーは、この戻り値を使用して、処理が発生し、MAPI スプーラーが EndMessage を呼び出す必要がないかどうかを **示す必要があります**。
    
MAPI_E_WAIT 
  
> 一時的な問題により、トランスポート プロバイダーはメッセージを処理しきれな。 _lpulReturnParm_ パラメーターは、MAPI スプーラーがメッセージを再送信するまでに経過する秒の数に設定する必要があります。 
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、トランスポート プロバイダーが配信するメッセージがある場合に **IXPLogon::SubmitMessage** メソッドを呼び出します。 メッセージは、lpMessage パラメーターを使用してトランスポート  _プロバイダーに渡_ されます。 
  
プロバイダーがメッセージを受け入れる準備ができている場合は  _、lpulMsgRef_ パラメーターを使用して参照値を返し、渡されたオブジェクトを処理し、適切な値 (通常は S_OK) を返す必要があります。 プロバイダーが転送を処理する準備がされていない場合は、エラー値を返し、必要に応じて  _lpulReturnParm_ の別の MAPI 戻り値を返して、MAPI スプーラーがメッセージを再送信するまでに待機する時間を示す必要があります。 
  
トランスポート プロバイダーによるこのメソッドの実装では、次の操作を実行できます。
  
- メッセージを内部キューに入れて、転送を待ち、メッセージをローカル ストレージにコピーして戻す可能性があります。
    
- 実際の送信を実行し、正常または失敗した場合に送信が完了した場合に返します。
    
- 関係するリソースを確認した後でメッセージを送信するかどうかを決定します。 この場合、リソースが空きである場合、プロバイダーはリソースをロックし、メッセージを準備し、送信できます。 リソースがビジー状態の場合、プロバイダーはメッセージを準備し、後で送信を延期できます。
    
メッセージ送信の推奨手法は、トランスポート プロバイダーと、システム リソースと競合する予想されるプロセス数によって異なります。 
  
**SubmitMessage 呼び出し** 中に、トランスポート プロバイダーはメッセージ オブジェクトからのメッセージ データの転送を制御します。 ただし、トランスポート プロバイダーは、データを転送する前に  _、lpulMsgRef_ でポインターを返すメッセージに参照値を割り当てる必要があります。 この処理は、プロセス中の任意の時点で、MAPI スプーラーが NOTIFY_CANCEL_MESSAGE フラグを設定して [IXPLogon::TransportNotify](ixplogon-transportnotify.md) メソッドを呼び出して、開いているオブジェクトを解放し、メッセージ転送を停止する必要があるというメッセージをプロバイダーに知らされる可能性があるからです。 
  
トランスポート プロバイダーは、メッセージの非送信可能なプロパティを送信できません。 そのようなプロパティを見つけたら、次のプロパティを処理する必要があります。 プロバイダーは、送信されたメッセージコンテンツの一部としてMAPI_P1情報を表示しなくあらゆる努力をする必要があります。プロバイダーは、この受信者情報をアドレス指定の目的でのみ使用する必要があります。 MAPI_P1受信者は、メッセージの再送信に使用される内部的に生成された受信者です。送信する必要があります。 代わりに、他の受信者を使用して受信者情報を送信します。 この配置の目的は、受信者が元の受信者とまったく同じ受信者テーブルを再送信して表示を許可する目的です。
  
**SubmitMessage 呼び出** し中に、MAPI スプーラーはメッセージの転送中に開いたオブジェクトのメソッドを処理し、添付ファイルを処理します。 この処理には長い時間がかかる場合があります。 トランスポート プロバイダーは、この処理中に MAPI スプーラーの [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) メソッドを頻繁に呼び出して、他のシステム タスクの CPU 時間を解放できます。 
  
すべてのメッセージ受信者は、MAPI スプーラーが最初に渡したメッセージの受信者テーブルに表示されます。 トランスポート プロバイダーは、エントリ識別子、アドレスの種類、または両方に基づいて処理できる受信者のみを処理し **、PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティが TRUE に設定されていない必要があります。 既 **PR_RESPONSIBILITY** TRUE に設定されている場合、別のトランスポート プロバイダーが受信者を処理しました。 プロバイダーが受信者のメッセージを処理できるかどうかを判断するために十分な処理が完了したら、渡されたメッセージで受信者の **PR_RESPONSIBILITY** プロパティを TRUE に設定する必要があります。 通常、プロバイダーはメッセージ配信が完了した後でこの決定を行います。 
  
通常、トランスポート プロバイダーは、メッセージ データの転送が完了するまで **SubmitMessage** 呼び出しから返されません。 エラーが返されない場合、MAPI スプーラーからプロバイダーへの次の呼び出しは [、IXPLogon::EndMessage](ixplogon-endmessage.md) メソッドへの呼び出しです。 
  
**SubmitMessage が** エラーを返す場合、MAPI スプーラーは変更を保存せずにメッセージを処理中に解放します。 トランスポート プロバイダーがメッセージの変更を保存する必要がある場合は、返す前にメッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出す必要があります。 
  
トランスポートの問題が原因でエラーが発生した場合、MAPI スプーラーはメッセージを保持しますが  _、lpulReturnParm_ で返される値に基づいてトランスポート プロバイダーへのメッセージの再送信が遅延します。 **SubmitMessage** からの戻り値が指定されている場合、トランスポート プロバイダーは、その値を入力MAPI_E_WAITまたはMAPI_E_NETWORK_ERROR。 重大なエラー状態が発生した場合、トランスポート プロバイダーは [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) メソッドを呼び出し、NOTIFY_CRITICAL_ERRORする必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

