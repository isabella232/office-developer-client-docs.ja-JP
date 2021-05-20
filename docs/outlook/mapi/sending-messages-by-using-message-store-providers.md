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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437610"
---
# <a name="sending-messages-by-using-message-store-providers"></a>メッセージ ストア プロバイダーを使用したメッセージ送信

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーは、送信メッセージの送信をサポートする必要はありません (つまり、クライアント アプリケーションがメッセージ ストア プロバイダーを使用してメッセージを送信する機能)。 クライアント アプリケーションは、メッセージの送信中にメッセージ ストアを使用する必要があります。メッセージのデータは、ユーザーがメッセージの作成を終了した時点から、MAPI スプーラーがメッセージをトランスポート プロバイダーに送信して基になるメッセージング システムに送信する時間の間のどこかに格納する必要があります。 メッセージ ストア プロバイダーが送信メッセージの送信をサポートしていない場合は、既定のメッセージ ストアとして使用できません。
  
メッセージの送信をサポートするには、メッセージ ストア プロバイダーが次の操作を行う必要があります。
  
- 送信メッセージ キューを実装します。
    
- メッセージ ストアで作成されたメッセージ オブジェクトで [IMessage::SubmitMessage](imessage-submitmessage.md) メソッドをサポートします。 
    
- MAPI スプーラーに固有の **IMsgStore** メソッドをサポートします [。IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) [、IMsgStore::GetOutgoingQueue、IMsgStore::NotifyNewMail、](imsgstore-getoutgoingqueue.md)および [IMsgStore::SetLockState](imsgstore-setlockstate.md)です。 [](imsgstore-notifynewmail.md)
    
**SetLockState** メソッドは、MAPI スプーラーとクライアントの間で適切に相互運用を行う場合に重要です。 MAPI スプーラーが送信メッセージ **で SetLockState** を呼び出す場合、メッセージ ストア プロバイダーはクライアントがメッセージを開く必要があります。 クライアントが MAPI スプーラーによってロックされているメッセージを開く場合、メッセージ ストア プロバイダーはメッセージ をMAPI_E_NO_ACCESS。 MAPI スプーラーによってメッセージがロックされている間にストアがシャットダウンされた場合、メッセージのロック状態が永続的である必要はなされません。 
  
MAPI スプーラーが送信メッセージをロックしたかどうかに関係なく、メッセージ ストア プロバイダーは、送信メッセージ キュー内のメッセージを書き込み用に開くことを許可しない必要があります。 クライアントが MAPI_MODIFY フラグを指定して送信メッセージで [IMSgStore::OpenEntry](imsgstore-openentry.md) メソッドを呼び出した場合、呼び出しは失敗し、MAPI_E_SUBMITTED。 クライアント アプリケーションが MAPI_BEST_ACCESS フラグ付き送信メッセージで **OpenEntry** を呼び出す場合、メッセージ ストア プロバイダーはメッセージへの読み取り専用アクセスを許可する必要があります。 
  
MAPI スプーラーでメッセージを処理する場合、メッセージ ストア プロバイダーは、メッセージの **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) プロパティを SUBMITFLAG_LOCKED に設定します。 このSUBMITFLAG_LOCKEDは、MAPI スプーラーが排他的に使用するためにメッセージをロックした状態を示します。 PR_SUBMIT_FLAGS **SUBMITFLAG_PREPROCESS** のもう 1 つの値は、トランスポート プロバイダーによって登録された 1 つ以上のプリプロセッサ関数によってメッセージが前処理を必要とする場合に設定されます。
  
次の手順では、メッセージ ストア、トランスポート、MAPI スプーラーがどのように対話して、クライアントから 1 つ以上の受信者にメッセージを送信するかについて説明します。 
  
クライアント アプリケーションは [、IMessage::SubmitMessage メソッドを呼び出](imessage-submitmessage.md) します。 **SubmitMessage では**、メッセージ ストア プロバイダーは次の処理を行います。
  
1. [IMAPISupport::P repareSubmit を呼び出します](imapisupport-preparesubmit.md)。 MAPI がエラーを返す場合、メッセージ ストア プロバイダーは、そのエラーをクライアントに返します。
    
2. メッセージの MSGFLAG_SUBMIT **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティPR_MESSAGE_FLAGSビットを設定します。
    
3. 受信者テーブルに **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティの列が表示され、メッセージを送信するトランスポートがまだ責任を負っていないかどうかを示す FALSE に設定します。
    
4. プロパティ[(PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)プロパティPR_CLIENT_SUBMIT_TIME日付と時刻を設定します。 
    
5. [IMAPISupport::ExpandRecips を呼び出して、次](imapisupport-expandrecips.md)の操作を行います。 
    
    1. すべての個人用配布リストとカスタム受信者を展開し、変更された表示名を元の名前に置き換える。
        
    2. 重複する名前を削除します。
        
    3. 必要な前処理を確認し、前処理が必要な場合は、NEEDS_PREPROCESSING フラグと **、MAPI** 用に予約されている PR_PREPROCESS ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) プロパティを設定します。 
        
    4. メッセージ ストアNEEDS_SPOOLERトランスポートと密に結合され、すべての受信者を処理できない場合は、このフラグを設定します。 
    
6. メッセージ フラグが設定されている場合はNEEDS_PREPROCESSINGタスクを実行します。
    
    1. メッセージを送信キューに入れ、SUBMITFLAG_PREPROCESS プロパティに **PR_SUBMIT_FLAGSします。** 
        
    2. キューが変更された MAPI スプーラーに通知します。
        
    3. クライアントに制御を返し、MAPI スプーラーでメッセージ フローを続行します。 MAPI スプーラーは、次のタスクを実行します。 
    
       1. [IMsgStore::SetLockState を呼び出してメッセージをロックします](imsgstore-setlockstate.md)。
            
       2. 登録の順序ですべての前処理関数を呼び出して、必要な前処理を実行します。 トランスポート プロバイダーは [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) を呼び出して、前処理関数を登録します。 
            
       3. 開 [いているメッセージで IMessage::SubmitMessage](imessage-submitmessage.md) を呼び出して、前処理が完了したとメッセージ ストアに示します。 
    
前処理が存在しない場合、または前処理が実行され、MAPI スプーラーが **SubmitMessage** と呼ばれる場合、メッセージ ストア プロバイダーはクライアント プロセスで次の処理を実行します。 
  
- メッセージ ストアがトランスポートに緊密に結合され、NEEDS_SPOOLER フラグが [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)から返された場合は、次のタスクを実行します。
    
   - 処理できる受信者を処理します。
    
   - 処理する **PR_RESPONSIBILITY** のプロパティを TRUE に設定します。 
    
   - この緊密に結合されたストアとトランスポートに対してすべての受信者が知られている場合は、次のタスクを実行します。 
    
     - メッセージが前処理された場合、またはメッセージ ストア プロバイダーが MAPI スプーラーにメッセージ処理を完了する必要がある場合は [、IMAPISupport::CompleteMsg](imapisupport-completemsg.md) を呼び出します。 メッセージ フローは MAPI スプーラーで続行されます。 
    
     - メッセージが前処理されていないか、メッセージ ストア プロバイダーが MAPI スプーラーにメッセージ処理を完了しない場合は、次のタスクを実行します。
    
       1. 設定されている場合は、PR_SENTMAIL_ENTRYID **(** [PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティのエントリ識別子によって識別されるフォルダーにメッセージをコピーします。
            
       2. プロパティ ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md) **)** プロパティが TRUE にPR_DELETE_AFTER_SUBMITメッセージを削除します。
            
       3. メッセージがロックされている場合は、メッセージのロックを解除します。
            
       4. クライアントに返します。 メッセージ フローが完了しました。
    
  - メッセージが前処理された場合、またはプロバイダーが MAPI スプーラーにメッセージ処理を完了する必要がある場合は、次のタスクを実行します。
    
    1. [IMAPISupport::CompleteMsg を呼び出します](imapisupport-completemsg.md)。 
          
    2. MAPI スプーラーを使用してメッセージ フローを続行します。 詳細については [、「Sending Messages: MAPI スプーラー タスク」を参照してください](sending-messages-mapi-spooler-tasks.md)。
    
  - メッセージが前処理されていない場合、またはプロバイダーがスプーラーにメッセージ処理を完了しない場合は、次のタスクを実行します。
    
    1. 設定されている場合は、PR_SENTMAIL_ENTRYID プロパティのエントリ識別子 **によって識別されるフォルダーにメッセージ** をコピーします。 
        
    2. プロパティが TRUE に設定 **されている場合PR_DELETE_AFTER_SUBMIT** メッセージを削除します。 
        
    3. メッセージがロックされている場合は、メッセージのロックを解除します。 
        
    4. 呼び出し元に戻ります。 メッセージ フローが完了しました。
    
- メッセージ ストアがトランスポートに緊密に結合されていない場合、すべての受信者がメッセージ ストアに知られているか、NEEDS_SPOOLER フラグが設定されている場合は、次のタスクを実行します。
    
  1. メッセージを送信キューに入れ、SUBMITFLAG_PREPROCESS プロパティに **PR_SUBMIT_FLAGSします。** 
    
  2. テーブル通知を生成して、送信キューが変更された MAPI スプーラーに通知します。 
    
  3. クライアントに戻り、メッセージ フローは MAPI スプーラーによって実行される一連のタスクを続行します。
    
## <a name="see-also"></a>関連項目

- [���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

