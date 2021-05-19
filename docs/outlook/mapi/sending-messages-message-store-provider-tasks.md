---
title: メッセージの送信 メッセージ ストア プロバイダー のタスク
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: acbfd3ae-bfdc-4103-bed2-6bcf7b9c448c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: de29707c7a257ea0e7ad658622d2a3054487f8b5
ms.sourcegitcommit: adcf409d56b6cb25be6117f09794defa41ad6c0f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2019
ms.locfileid: "37495307"
---
# <a name="sending-messages-message-store-provider-tasks"></a>メッセージの送信: メッセージ ストア プロバイダーのタスク

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーは、クライアントがメッセージの [IMessage::SubmitMessage](imessage-submitmessage.md) メソッドを呼び出す際に、メッセージ送信プロセスに関与します。 複数のメッセージを送信する場合、メッセージ ストアは、クライアントが SubmitMessage 呼び出しに使用した順序と同じ順序で送信 **する必要** があります。 
  
メッセージ ストア プロバイダーは、MAPI スプーラーを含めるかどうかを決定します。 メッセージ ストア プロバイダーが密に結合されていない場合、メッセージには前処理が必要です。または密に結合されたストアとトランスポートがすべての受信者を処理できない場合は、MAPI スプーラーを使用する必要があります。 
  
次の手順では、メッセージを送信するためにメッセージ ストア プロバイダーに必要なタスクについて説明します。 
  
**IMessage::SubmitMessage では、メッセージ ストア プロバイダー**:
  
1. **メッセージ** の MSGFLAG_RESEND フラグが PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティに設定されている場合は [、IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md)を呼び出し、クライアントにエラーを返します。 **PrepareSubmit** は **、PR_RECIPIENT_TYPEの受信者** リスト内の各受信者のプロパティ [(PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)プロパティをチェックします。
    
   - 受信者が元のメッセージを受信しなかったことを示す MAPI_SUBMITTED フラグが設定されている場合 **、PrepareSubmit** はフラグをクリアし **、PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを TRUE に設定します。 
    
   - 受信者が元のメッセージを受信したことを示す MAPI_SUBMITTED フラグが設定されていない場合 **、PrepareSubmit** は PR_RECIPIENT_TYPE プロパティを **MAPI_P1** に変更し **、PR_RESPONSIBILITY** プロパティを TRUE に設定し **、PrepareSubmit** によって生成されたエラーをクライアントに返します。 
    
2. メッセージの MSGFLAG_SUBMIT プロパティのフラグを **設定PR_MESSAGE_FLAGSします** 。 
    
3. 受信者テーブルに PR_RESPONSIBILITY 列が含まれています。メッセージを送信する責任がまだないトランスポートを示す FALSE に設定します。 
    
4. プロパティ[(PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)プロパティPR_CLIENT_SUBMIT_TIME日付と時刻を設定します。 
    
5. [IMAPISupport::ExpandRecips を次の場所に呼び出](imapisupport-expandrecips.md)します。 
    
   - すべての個人用配布リストとカスタム受信者を展開し、変更された表示名を元の名前に置き換える。
   - 重複する名前を削除します。
   - 必要な前処理を確認し、前処理が必要な場合は、NEEDS_PREPROCESSING フラグと **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) プロパティ (MAPI 用に予約されたプロパティ) を設定します。 
   - メッセージ ストアNEEDS_SPOOLERトランスポートと密に結合され、すべての受信者を処理できない場合は、このフラグを設定します。 
    
6. メッセージ フラグが設定されている場合はNEEDS_PREPROCESSINGタスクを実行します。
    
   - メッセージを送信キューに入れ、SUBMITFLAG_PREPROCESS **(** [PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) プロパティに PR_SUBMIT_FLAGS ビットを設定します。
   - キューが変更された MAPI スプーラーに通知します。
   - クライアントに制御を返し、MAPI スプーラーでメッセージ フローを続行します。 
   - MAPI スプーラーは、次のタスクを実行します。
     - IMsgStore::SetLockState を呼び出してメッセージをロックします。 
     - 登録の順序ですべての前処理関数を呼び出して、必要な前処理を実行します。 トランスポート プロバイダーは IMAPISupport::RegisterPreprocessor を呼び出して、前処理関数を登録します。 
     - 開いているメッセージで IMessage::SubmitMessage を呼び出して、前処理が完了したとメッセージ ストアに示します。

<br/>

次の 2 つの手順は、前処理がない場合と、MAPI スプーラーが前処理が行われる場合に **SubmitMessage** を呼び出す場合に、クライアント プロセスで発生します。 

**メッセージ ストア プロバイダー**:

1. メッセージ ストアがトランスポートに緊密に結合され、NEEDS_SPOOLER フラグが [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)から返された場合は、次のタスクを実行します。
    
   - 処理できる受信者を処理します。
   - 処理する **PR_RESPONSIBILITY** のプロパティを TRUE に設定します。 
   - この緊密に結合されたストアとトランスポートに対してすべての受信者が知られている場合は、次のタスクを実行します。
     - メッセージが前処理された場合、またはメッセージ ストア プロバイダーが MAPI スプーラーにメッセージ処理を完了する必要がある場合は、IMAPISupport::CompleteMsg を呼び出して、メッセージング フックを呼び出すことができます。 次の手順で説明するように、メッセージ フローは MAPI スプーラーで続行されます。  
     - メッセージが前処理されていないか、メッセージ ストア プロバイダーが MAPI スプーラーにメッセージ処理を完了しない場合は、次のタスクを実行します。
       - 設定されている場合は、PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId) プロパティのエントリ識別子によって識別されるフォルダーにメッセージをコピーします。
       - プロパティ (PidTagDeleteAfterSubmit) プロパティが TRUE にPR_DELETE_AFTER_SUBMITメッセージを削除します。
       - メッセージがロックされている場合は、メッセージのロックを解除します。
       - クライアントに返します。 メッセージ フローが完了しました。 
   
2. メッセージ ストアがトランスポートに緊密に結合されていない場合、すべての受信者がメッセージ ストアに知られているか、NEEDS_SPOOLER フラグが設定されている場合は、次のタスクを実行します。
    
   - メッセージを送信キューに入れ、SUBMITFLAG_PREPROCESS プロパティに **PR_SUBMIT_FLAGSします。** 
   - テーブル通知を生成して、送信キューが変更された MAPI スプーラーに通知します。 
   - クライアントに戻り、メッセージ フローは MAPI スプーラーによって実行される一連のタスクを続行します。
    
MAPI スプーラーでメッセージを処理する場合、メッセージ ストア プロバイダーは、メッセージの PR_SUBMIT_FLAGS **プロパティを** SUBMITFLAG_LOCKED。 このSUBMITFLAG_LOCKEDは、MAPI スプーラーがメッセージを排他的に使用するためにロックした状態を示します。 PR_SUBMIT_FLAGS **SUBMITFLAG_PREPROCESS** のもう 1 つの値は、メッセージがトランスポート プロバイダーによって登録された 1 つ以上のプリプロセッサ関数によって前処理を必要とする場合に設定されます。 
  

