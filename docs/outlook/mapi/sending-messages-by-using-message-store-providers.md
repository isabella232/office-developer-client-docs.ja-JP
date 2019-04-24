---
title: メッセージ ストア プロバイダーを使用したメッセージ送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b34714a230adb44417624d149d34ed6a14a2dfa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339684"
---
# <a name="sending-messages-by-using-message-store-providers"></a>メッセージ ストア プロバイダーを使用したメッセージ送信

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアプロバイダーは、送信メッセージの送信をサポートする必要はありません (つまり、クライアントアプリケーションがメッセージストアプロバイダーを使用してメッセージを送信できます)。 ユーザーがメッセージを送信する時間と MAPI スプーラーがメッセージをトランスポートプロバイダーに提供する時間との間にメッセージのデータを格納する必要があるため、クライアントアプリケーションはメッセージストアを使用する必要があります。基になるメッセージングシステムに送信します。 メッセージストアプロバイダーが送信メッセージの送信をサポートしていない場合、既定のメッセージストアとして使用することはできません。
  
メッセージの送信をサポートするには、メッセージストアプロバイダーが次のことを行う必要があります。
  
- 送信メッセージキューを実装します。
    
- メッセージストアに作成されたメッセージオブジェクトに対して[IMessage:: submitmessage](imessage-submitmessage.md)メソッドをサポートします。 
    
- MAPI スプーラーに固有の**IMsgStore**メソッド[IMsgStore:: FinishedMsg](imsgstore-finishedmsg.md)、 [IMsgStore:: getoutgoingqueue](imsgstore-getoutgoingqueue.md)、 [IMsgStore::](imsgstore-notifynewmail.md)NotifyNewMail、 [IMsgStore::](imsgstore-setlockstate.md)SetLockState をサポートします。
    
**SetLockState**メソッドは、MAPI スプーラーとクライアントを適切に相互運用するために重要です。 MAPI スプーラーが送信メッセージで**SetLockState**を呼び出した場合、メッセージストアプロバイダーは、クライアントがメッセージを開くことができないようにする必要があります。 クライアントが MAPI スプーラーによってロックされているメッセージを開こうとすると、メッセージストアプロバイダーは MAPI_E_NO_ACCESS を返す必要があります。 メッセージが MAPI スプーラーによってロックされている間にストアがシャットダウンされる場合に備えて、メッセージのロックされた状態を維持する必要はありません。 
  
MAPI スプーラーで送信メッセージがロックされているかどうかに関係なく、メッセージストアプロバイダーは、送信メッセージキュー内のメッセージが書き込み用に開かないようにする必要があります。 クライアントが MAPI_MODIFY フラグが設定された送信メッセージで[IMSgStore:: openentry](imsgstore-openentry.md)メソッドを呼び出すと、呼び出しは失敗し、MAPI_E_SUBMITTED が返されます。 クライアントアプリケーションが、MAPI_BEST_ACCESS フラグが設定された送信メッセージの**openentry**を呼び出す場合、メッセージストアプロバイダーは、メッセージへの読み取り専用アクセスを許可する必要があります。 
  
メッセージが MAPI スプーラーによって処理される場合、メッセージストアプロバイダーは、メッセージの**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) プロパティを SUBMITFLAG_LOCKED に設定します。 SUBMITFLAG_LOCKED 値は、MAPI スプーラーが排他的使用のためにメッセージをロックしたことを示します。 **PR_SUBMIT_FLAGS**、SUBMITFLAG_PREPROCESS のその他の値は、メッセージがトランスポートプロバイダーによって登録された1つ以上のプリプロセッサ関数の前処理を必要とするときに設定されます。
  
次の手順では、メッセージストア、トランスポート、および MAPI スプーラーが、クライアントから1人または複数の受信者にメッセージを送信する方法について説明します。 
  
クライアントアプリケーションは[IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出します。 **submitmessage**では、メッセージストアプロバイダーは次の処理を行います。
  
1. [imapisupport サポートを呼び出します。:P reparererererererererererere](imapisupport-preparesubmit.md) MAPI がエラーを返すと、メッセージストアプロバイダーはそのエラーをクライアントに返します。
    
2. メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティに、MSGFLAG_SUBMIT ビットを設定します。
    
3. 受信者テーブルに**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティの列が存在することを確認し、それを FALSE に設定して、トランスポートがメッセージの送信をまだ引き受けていないことを示します。
    
4. **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) プロパティで、発信元の日付と時刻を設定します。
    
5. [imapisupport:: ExpandRecips](imapisupport-expandrecips.md)を呼び出して、次の操作を行います。 
    
    1. すべての個人用配布リストとカスタム受信者を展開し、変更されたすべての表示名を元の名前に置き換えます。
        
    2. 重複する名前を削除します。
        
    3. 必要な前処理を確認し、前処理が必要な場合は、NEEDS_PREPROCESSING フラグと、MAPI 用に予約されている**PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) プロパティを設定します。 
        
    4. メッセージストアがトランスポートと密に結合しており、すべての受信者を処理できない場合は、NEEDS_SPOOLER フラグを設定します。 
    
6. NEEDS_PREPROCESSING メッセージフラグが設定されている場合に、次のタスクを実行します。
    
    1. SUBMITFLAG_PREPROCESS ビットが**PR_SUBMIT_FLAGS**プロパティに設定された状態で、メッセージを送信キューに格納します。 
        
    2. キューが変更されたことを MAPI スプーラーに通知します。
        
    3. クライアントに制御を戻し、メッセージフローを MAPI スプーラーで続行します。 MAPI スプーラーは、次のタスクを実行します。 
    
       1. [IMsgStore:: SetLockState](imsgstore-setlockstate.md)を呼び出して、メッセージをロックします。
            
       2. 登録の順序ですべての前処理関数を呼び出すことによって、必要な前処理を実行します。 トランスポートプロバイダーは、 [imapisupport:: registerpreprocessor プロセッサ](imapisupport-registerpreprocessor.md)を呼び出して前処理関数を登録します。 
            
       3. 処理が完了したことをメッセージストアに示すように、開いているメッセージの[IMessage:: submitmessage](imessage-submitmessage.md)を呼び出します。 
    
前処理がなかった場合、または前処理が行われていて、また、 **submitmessage**という名前の MAPI スプーラーがある場合、メッセージストアプロバイダーはクライアントプロセスで次の処理を行います。 
  
- メッセージストアがトランスポートに密接に結合されており、NEEDS_SPOOLER フラグが[imapisupport:: ExpandRecips](imapisupport-expandrecips.md)から返された場合は、次のタスクを実行します。
    
   - 処理できる受信者を処理します。
    
   - 処理するすべての受信者に対して、 **PR_RESPONSIBILITY**プロパティを TRUE に設定します。 
    
   - すべての受信者がこの密結合ストアとトランスポートに知られている場合は、次のタスクを実行します。 
    
     - メッセージがプリプロセスされた場合、またはメッセージストアプロバイダーが MAPI スプーラーでメッセージ処理を完了する必要がある場合は、 [imapisupport:: complete apisg](imapisupport-completemsg.md)を呼び出します。 メッセージフローは、MAPI スプーラーで続行されます。 
    
     - メッセージがプリプロセスされていない場合、またはメッセージストアプロバイダーが MAPI スプーラーでメッセージ処理を完了させない場合は、次のタスクを実行します。
    
       1. **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティで設定されている場合、エントリ識別子によって識別されるフォルダーにメッセージをコピーします。
            
       2. **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE に設定されている場合は、メッセージを削除します。
            
       3. ロックされている場合は、メッセージのロックを解除します。
            
       4. クライアントに戻ります。 メッセージフローが完了しました。
    
  - メッセージがプリプロセスされた場合、またはプロバイダーが MAPI スプーラーでメッセージ処理を完了する必要がある場合は、次のタスクを実行します。
    
    1. [imapisupport::](imapisupport-completemsg.md)全てを呼び出します。 
          
    2. MAPI スプーラーでメッセージフローを続行します。 詳細については、「[メッセージの送信: MAPI スプーラーのタスク](sending-messages-mapi-spooler-tasks.md)」を参照してください。
    
  - メッセージがプリプロセスされていないか、プロバイダーがメッセージ処理を完了しないようにするには、次のタスクを実行します。
    
    1. **PR_SENTMAIL_ENTRYID**プロパティで設定されている場合、エントリ識別子によって識別されるフォルダーにメッセージをコピーします。 
        
    2. **PR_DELETE_AFTER_SUBMIT**プロパティが TRUE に設定されている場合は、メッセージを削除します。 
        
    3. ロックされている場合は、メッセージのロックを解除します。 
        
    4. 呼び出し元に戻ります。 メッセージフローが完了しました。
    
- メッセージストアがトランスポートに密接に結合されておらず、すべての受信者がメッセージストアを認識していない場合、または NEEDS_SPOOLER フラグが設定されている場合は、次のタスクを実行します。
    
  1. **PR_SUBMIT_FLAGS**プロパティの SUBMITFLAG_PREPROCESS ビットを設定せずに、メッセージを送信キューに配置します。 
    
  2. テーブル通知を生成することによって、送信キューが変更されたことを MAPI スプーラーに通知します。 
    
  3. クライアントに戻り、メッセージフローは MAPI スプーラーによって実行される一連のタスクを続行します。
    
## <a name="see-also"></a>関連項目

- [���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

