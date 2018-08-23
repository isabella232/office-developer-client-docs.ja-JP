---
title: メッセージのメッセージ ストア プロバイダーのタスクを送信します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: acbfd3ae-bfdc-4103-bed2-6bcf7b9c448c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4af052cdbd354d321a1d9e1dd0feb004501c8eb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587615"
---
# <a name="sending-messages-message-store-provider-tasks"></a>メッセージの送信: メッセージ ストア プロバイダーのタスク

**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ ストア プロバイダーは、クライアントがメッセージの[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出すと、プロセスを送信するメッセージに関連する取得します。 複数のメッセージを送信する場合は、メッセージ ・ ストアの**SubmitMessage**呼び出しのクライアントが使用されることと同じ順序でを送信する必要があります。 
  
メッセージ ストア プロバイダーでは、MAPI スプーラーが参加するかどうかを指定します。 メッセージ ストア プロバイダーが密に結合されていない場合、メッセージは、プリプロセスを必要とまたは密結合のストアとトランスポートを処理できないすべての受信者、MAPI スプーラーが関与している必要があります。 
  
次の手順では、メッセージ ストア プロバイダーのメッセージを送信するために必要なタスクについて説明します。 
  
**IMessage::SubmitMessage では、メッセージは、プロバイダーを格納**します。
  
1. メッセージ、MSGFLAG_RESEND フラグを**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティに設定があり、クライアントにエラーを返す場合は、 [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md)を呼び出します。 **PrepareSubmit**は、メッセージの宛先リストの各受信者の**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) のプロパティをチェックします。
    
   - MAPI_SUBMITTED フラグが設定されている場合、受信者が元のメッセージを受信しなかったことを示す**PrepareSubmit**フラグをクリアし、**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを TRUE に設定します。 
    
   - MAPI_SUBMITTED フラグが設定されていない場合、受信者に、元のメッセージを受け取ったことを示す**PrepareSubmit** 、 **PR_RECIPIENT_TYPE**プロパティを MAPI_P1 に変更**れない**プロパティを TRUE に設定してを返しますクライアントに**PrepareSubmit**によって生成されたエラーです。 
    
2. メッセージの**PR_MESSAGE_FLAGS**プロパティに MSGFLAG_SUBMIT フラグを設定します。 
    
3. **れない**受信者テーブルの列が存在し、まだと仮定しての責任、メッセージを送信するためのトランスポートが含まれていないことを示すために FALSE に設定します。 
    
4. **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) のプロパティの元の日時を設定します。
    
5. [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)を呼び出します。 
    
   - すべての個人用配布リストとカスタム受信者を展開し、すべての変更された表示名を元の名前に置き換えます。
   - 重複した名前を削除します。
   - 必要な処理を確認し、前処理が必要な場合、NEEDS_PREPROCESSING フラグと**PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) は、MAPI の予約済みのプロパティを設定します。 
   - メッセージ ・ ストアは、トランスポートと密接に関連し、すべての受信者を処理できない場合は、NEEDS_SPOOLER フラグを設定します。 
    
6. NEEDS_PREPROCESSING メッセージのフラグが設定されている場合は、次のタスクを実行します。
    
   - **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) プロパティで設定された SUBMITFLAG_PREPROCESS ビットを使用して、送信キューにメッセージを配置します。
   - MAPI スプーラー キューが変更されたことを通知します。
   - 、クライアントに制御を返しますし、メッセージ フロー、MAPI スプーラーを無効にします。 
   - MAPI スプーラーは、次のタスクを実行します。
     - IMsgStore::SetLockState を呼び出すことによって、メッセージをロックします。 
     - すべての登録の順序でプリプロセッサ関数を呼び出すことによって必要な前処理を実行します。 トランスポート プロバイダーでは、前処理の関数を登録するのには IMAPISupport::RegisterPreprocessor を呼び出します。 
     - メッセージ ・ ストアに事前処理が完了したことを示すメッセージを開いた状態で IMessage::SubmitMessage を呼び出します。

<br/>

かどうかがなく、前処理が処理された場合に、MAPI スプーラーが**SubmitMessage**を呼び出すと、次の 2 つの手順はクライアント プロセスで発生します。 

**メッセージは、プロバイダーを格納**します。

1. メッセージ ・ ストアは、トランスポートに密に結合し、NEEDS_SPOOLER フラグは、 [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)から返された場合は、次のタスクを実行します。
    
   - 処理可能なすべての受信者を処理します。
   - **れない**プロパティを設定しますが、処理するすべての受信者。 
   - このストアの密結合とトランスポートのすべての受信者がわかっている場合は、次のタスクを実行します。
     - メッセージのプリプロセスまたは、メッセージ ・ ストア プロバイダーの要望をお勧めするため、メッセージのフックを呼び出すことができるメッセージの処理を完了するのには MAPI スプーラーは、IMAPISupport::CompleteMsg を呼び出します。 メッセージ フローは、次の手順に従って、MAPI スプーラーを続行します。  
     - メッセージのプリプロセスがしないか、メッセージ ストア プロバイダーは、メッセージの処理を完了するのには MAPI スプーラーを希望しない場合は、次のタスクを実行します。
       - コピーの場合、PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId) プロパティでは、エントリ id によって識別されたフォルダーにメッセージを設定します。
       - PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit) プロパティが TRUE に設定されている場合は、メッセージを削除します。
       - ロックされている場合、メッセージのロックを解除します。
       - クライアントに返します。 メッセージ フローは、完了です。 
   
2. トランスポートにメッセージ ・ ストアが密に結合されない、メッセージ ・ ストアに知られていたすべての受信者または NEEDS_SPOOLER フラグが設定されている場合は、次のタスクを実行します。
    
   - **PR_SUBMIT_FLAGS**プロパティに SUBMITFLAG_PREPROCESS ビットを設定せず、送信キューにメッセージを配置します。 
   - 発信キューは、テーブルの通知を生成することによって変更された MAPI スプーラーに通知します。 
   - クライアント、およびメッセージの流れに戻りますが、MAPI スプーラーが実行するタスクのセットを使用して続行します。
    
メッセージは、MAPI スプーラーによって処理されるには、メッセージ ストア プロバイダーは、メッセージの**PR_SUBMIT_FLAGS**プロパティを SUBMITFLAG_LOCKED に設定します。 SUBMITFLAG_LOCKED フラグは、MAPI スプーラーが、排他的使用のためのメッセージをロックしていることを示します。 メッセージが 1 つ以上のプリプロセッサ関数を使用して、トランスポート プロバイダーが登録されている前処理を必要とする場合、 **PR_SUBMIT_FLAGS** SUBMITFLAG_PREPROCESS の他の値が設定されています。 
  

