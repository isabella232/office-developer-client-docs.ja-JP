---
title: ストア プロバイダーによってメッセージを使用してメッセージを送信します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: aaba816ca7efab6cee939087a18332561f31b81b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803865"
---
# <a name="sending-messages-by-using-message-store-providers"></a>ストア プロバイダーによってメッセージを使用してメッセージを送信します。

**適用対象**: Outlook 
  
メッセージ ストア プロバイダーは、送信メッセージの送信 (つまり、クライアント アプリケーションがメッセージを送信するメッセージ ストア プロバイダーを使用する機能) をサポートする必要はありません。 クライアント アプリケーションをどこかに格納されているメッセージのデータがある必要がありますので、メッセージを送信するときに、メッセージ ストアを使用する必要があるユーザーが完了するまでの間と、MAPI スプーラー用のトランスポート プロバイダーにメッセージを提供する時間を構成します。基になるメッセージング システムに送信します。 メッセージ ストア プロバイダーが送信メッセージの送信をサポートしていない場合は、既定のメッセージ ストアとして使用できません。
  
メッセージの送信をサポートするために、メッセージ ストア プロバイダーは、次の。
  
- 送信のメッセージ キューを実装します。
    
- メッセージ ・ ストア内に作成したメッセージ オブジェクトの[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドをサポートします。 
    
- MAPI スプーラーに特有の**IMsgStore**メソッドをサポートします。 [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)、 [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)、 [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)、および[IMsgStore::SetLockState](imsgstore-setlockstate.md)。
    
**SetLockState**メソッドは、MAPI スプーラーとクライアントの間の適切な相互運用のために重要です。 MAPI スプーラーを呼び出すと**SetLockState**に送信するメッセージ、メッセージ ストア プロバイダーにする必要がありますクライアントがメッセージを開くことできません。 クライアントは、MAPI スプーラーによってロックされているメッセージを開くと、メッセージ ストア プロバイダーは、MAPI_E_NO_ACCESS を返す必要があります。 メッセージのロックされた状態は、ストアがシャット ダウンされるメッセージは、MAPI スプーラーによってロックされている場合に、持続的ではありません。 
  
かどうか、MAPI スプーラーに送信するメッセージをロックすることに関係なくメッセージ ストア プロバイダーは書き込み用に開かれる送信メッセージ キューにメッセージをできません。 場合は、クライアントでは、MAPI_MODIFY フラグを使用して送信メッセージの[IMSgStore::OpenEntry](imsgstore-openentry.md)メソッドを呼び出し、呼び出しは失敗し、MAPI_E_SUBMITTED を返す必要があります。 クライアント アプリケーションは、MAPI_BEST_ACCESS フラグを使用して送信メッセージに**OpenEntry**を呼び出し、メッセージ ストア プロバイダーは、メッセージを読み取り専用のアクセスを許可する必要があります。 
  
メッセージは、MAPI スプーラーによって処理されるには、メッセージ ストア プロバイダーは、メッセージの**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) のプロパティを SUBMITFLAG_LOCKED に設定します。 SUBMITFLAG_LOCKED 値は、MAPI スプーラーが、排他的使用のためのメッセージをロックしていることを示します。 メッセージが 1 つ以上のプリプロセッサ関数を使用して、トランスポート プロバイダーが登録されている前処理を必要とする場合、 **PR_SUBMIT_FLAGS**SUBMITFLAG_PREPROCESS の他の値が設定されています。
  
次の手順では、メッセージ ・ ストア、トランスポート、および MAPI スプーラーがクライアントから 1 つまたは複数の受信者にメッセージを送信するのにはどのようにやり取りする方法について説明します。 
  
クライアント アプリケーションでは、 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出します。 **SubmitMessage**、メッセージ ストア プロバイダーは、次の。
  
1. [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md)を呼び出します。 MAPI がエラーを返した場合、メッセージ ストア プロバイダーは、クライアントにそのエラーを返します。
    
2. MSGFLAG_SUBMIT、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティ、メッセージ内のビットを設定します。
    
3. **れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティで受信者テーブルの列し、トランスポートがまだいると見なすことがないメッセージを送信するための責任を示すために FALSE に設定してあることを保証します。
    
4. **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) のプロパティの元の日時を設定します。
    
5. 次に[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)を呼び出します。 
    
    1. すべての個人用配布リストとカスタム受信者を展開し、すべての変更された表示名を元の名前に置き換えます。
        
    2. 重複した名前を削除します。
        
    3. 必要な処理を確認し、前処理が必要な場合、NEEDS_PREPROCESSING フラグと**PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) は、MAPI で予約されているを設定します。 
        
    4. メッセージ ・ ストアは、トランスポートと密接に関連し、すべての受信者を処理できない場合は、NEEDS_SPOOLER フラグを設定します。 
    
6. NEEDS_PREPROCESSING メッセージのフラグが設定されている場合は、次のタスクを実行します。
    
    1. **PR_SUBMIT_FLAGS**プロパティで設定された SUBMITFLAG_PREPROCESS ビットを使用して、送信キューにメッセージを配置します。 
        
    2. MAPI スプーラー キューが変更されたことを通知します。
        
    3. 、クライアントに制御を返しますし、メッセージ フロー、MAPI スプーラーを無効にします。 MAPI スプーラーは、次のタスクを実行します。 
    
       1. [IMsgStore::SetLockState](imsgstore-setlockstate.md)を呼び出すことによって、メッセージをロックします。
            
       2. すべての登録の順序でプリプロセッサ関数を呼び出すことによって必要な前処理を実行します。 トランスポート プロバイダーでは、前処理の関数を登録するのには[IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md)を呼び出します。 
            
       3. その前処理を格納したメッセージを示すメッセージを開いた状態で[IMessage::SubmitMessage](imessage-submitmessage.md)の呼び出しは、完了です。 
    
前処理、されていないかがあった場合の前処理スクリプトと**SubmitMessage**と呼ばれる、MAPI スプーラー メッセージ ストア プロバイダーは、クライアント プロセスで、次。 
  
- メッセージ ・ ストアは、トランスポートに密に結合し、NEEDS_SPOOLER フラグは、 [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)から返された場合は、次のタスクを実行します。
    
   - 処理可能なすべての受信者を処理します。
    
   - **れない**プロパティを設定しますが、処理するすべての受信者。 
    
   - このストアの密結合とトランスポートのすべての受信者がわかっている場合は、次のタスクを実行します。 
    
     - [IMAPISupport::CompleteMsg](imapisupport-completemsg.md)を呼び出す場合は、メッセージのプリプロセスまたはメッセージ ストア プロバイダーは、完全なメッセージを処理する MAPI スプーラーを希望しています。 メッセージの流れは、MAPI スプーラーを続行します。 
    
     - メッセージのプリプロセスがしないか、メッセージ ストア プロバイダーは、メッセージの処理を完了するのには MAPI スプーラーを希望しない場合は、次のタスクを実行します。
    
       1. コピーの場合は**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティでは、エントリ id によって識別されたフォルダーにメッセージを設定します。
            
       2. **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE に設定されている場合は、メッセージを削除します。
            
       3. ロックされている場合、メッセージのロックを解除します。
            
       4. クライアントに返します。 メッセージ フローは、完了です。
    
  - メッセージのプリプロセスまたはプロバイダーは、メッセージの処理を完了するのには MAPI スプーラーを希望する場合は、次のタスクを実行します。
    
    1. [IMAPISupport::CompleteMsg](imapisupport-completemsg.md)を呼び出します。 
          
    2. MAPI スプーラーとメッセージのフローを継続します。 詳細についてを参照してください[を送信するメッセージ: MAPI スプーラー タスク](sending-messages-mapi-spooler-tasks.md)。
    
  - メッセージのプリプロセスがしないか、プロバイダーは、メッセージの処理を完了するのにはスプーラーを希望しない場合は、次のタスクを実行します。
    
    1. コピーの場合、 **PR_SENTMAIL_ENTRYID**プロパティでは、エントリ id によって識別されたフォルダーにメッセージを設定します。 
        
    2. **PR_DELETE_AFTER_SUBMIT**プロパティが TRUE に設定されている場合は、メッセージを削除します。 
        
    3. ロックされている場合、メッセージのロックを解除します。 
        
    4. 呼び出し元に戻ります。 メッセージ フローは、完了です。
    
- トランスポートにメッセージ ・ ストアが密に結合されない、メッセージ ・ ストアに知られていたすべての受信者または NEEDS_SPOOLER フラグが設定されている場合は、次のタスクを実行します。
    
  1. **PR_SUBMIT_FLAGS**プロパティに SUBMITFLAG_PREPROCESS ビットを設定せず、送信キューにメッセージを配置します。 
    
  2. 発信キューは、テーブルの通知を生成することによって変更された MAPI スプーラーに通知します。 
    
  3. クライアント、およびメッセージの流れに戻りますが、MAPI スプーラーが実行するタスクのセットを使用して続行します。
    
## <a name="see-also"></a>関連項目

- [���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

