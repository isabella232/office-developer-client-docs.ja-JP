---
title: メッセージを送信するメッセージストアプロバイダーのタスク
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: acbfd3ae-bfdc-4103-bed2-6bcf7b9c448c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b65113e59b236b1f13596627a8669ae458f76369
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338431"
---
# <a name="sending-messages-message-store-provider-tasks"></a>メッセージの送信: メッセージストアプロバイダーのタスク

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアプロバイダーは、クライアントがメッセージの[IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出したときに、メッセージ送信プロセスに関与します。 複数のメッセージが送信される場合、メッセージストアは、その送信メッセージ呼び出しに使用されたのと**** 同じ順序でメッセージを送信する必要があります。 
  
メッセージストアプロバイダーは、MAPI スプーラーを含めるかどうかを決定します。 メッセージストアプロバイダーが密結合されていない場合、メッセージには前処理が必要です。または、密結合ストアとトランスポートはすべての受信者を処理できません。 MAPI スプーラーが関与する必要があります。 
  
次の手順では、メッセージを送信するためにメッセージストアプロバイダーに必要なタスクについて説明します。 
  
**IMessage:: submitmessage で、メッセージストアプロバイダーは**次のようになります。
  
1. MSGFLAG_RESEND フラグが**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティに設定されている場合にメッセージを再送信し、クライアントにエラーを返す場合は、 [imapisupport を呼び出します。](imapisupport-preparesubmit.md) **PrepareSubmit**は、メッセージの受信者の一覧に含まれる各受信者の**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティをチェックします。
    
   - 受信者が元のメッセージを受信しなかったことを示す MAPI_SUBMITTED フラグが設定されている場合、 **PrepareSubmit**はフラグをクリアし、 **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを TRUE に設定します。 
    
   - MAPI_SUBMITTED フラグが設定されておらず、受信者が元のメッセージを受信したことを示している場合、 **PrepareSubmit**は**PR_RECIPIENT_TYPE**プロパティを MAPI_P1 に変更し、 **PR_RESPONSIBILITY**プロパティを TRUE に設定して、クライアントに対して**PrepareSubmit**によって生成されたエラー。 
    
2. メッセージの**PR_MESSAGE_FLAGS**プロパティに MSGFLAG_SUBMIT フラグを設定します。 
    
3. recipient テーブルに**PR_RESPONSIBILITY**の列が存在することを確認し、メッセージの送信に関してまだ責任を負っていないトランスポートがないことを示すために FALSE に設定します。 
    
4. **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) プロパティで、発信元の日付と時刻を設定します。
    
5. [imapisupport:: ExpandRecips](imapisupport-expandrecips.md)を呼び出します。 
    
   - すべての個人用配布リストとカスタム受信者を展開し、変更されたすべての表示名を元の名前に置き換えます。
   - 重複する名前を削除します。
   - 必要な前処理を確認し、前処理が必要な場合は、NEEDS_PREPROCESSING フラグおよび**PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) プロパティ (MAPI 用に予約されているプロパティ) を設定します。 
   - メッセージストアがトランスポートと密に結合しており、すべての受信者を処理できない場合は、NEEDS_SPOOLER フラグを設定します。 
    
6. NEEDS_PREPROCESSING メッセージフラグが設定されている場合に、次のタスクを実行します。
    
   - SUBMITFLAG_PREPROCESS ビットを**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) プロパティに設定して、メッセージを送信キューに配置します。
   - キューが変更されたことを MAPI スプーラーに通知します。
   - クライアントに制御を戻し、メッセージフローを MAPI スプーラーで続行します。 
   - MAPI スプーラーは、次のタスクを実行します。
     - IMsgStore:: SetLockState を呼び出して、メッセージをロックします。 
     - 登録の順序ですべての前処理関数を呼び出すことによって、必要な前処理を実行します。 トランスポートプロバイダーは、imapisupport:: registerpreprocessor プロセッサを呼び出して前処理関数を登録します。 
     - 処理が完了したことをメッセージストアに示すように、開いているメッセージの IMessage:: submitmessage を呼び出します。

<br/>

前処理が行われていない場合、および MAPI スプーラーが前処理**メッセージ**を呼び出した場合、クライアントプロセスでは次の2つの手順が発生します。 

**メッセージストアプロバイダー**:

1. メッセージストアがトランスポートに密接に結合されており、NEEDS_SPOOLER フラグが[imapisupport:: ExpandRecips](imapisupport-expandrecips.md)から返された場合は、次のタスクを実行します。
    
   - 処理できる受信者を処理します。
   - 処理するすべての受信者に対して、 **PR_RESPONSIBILITY**プロパティを TRUE に設定します。 
   - すべての受信者がこの密結合ストアとトランスポートに知られている場合は、次のタスクを実行します。
     - メッセージがプリプロセスされた場合、またはメッセージストアプロバイダーが MAPI スプーラーでメッセージ処理を完了しようとしている場合は、メッセージのフックを呼び出すことができるようにします。 次の手順で説明するように、メッセージフローは MAPI スプーラーで続行されます。  
     - メッセージがプリプロセスされていない場合、またはメッセージストアプロバイダーが MAPI スプーラーでメッセージ処理を完了させない場合は、次のタスクを実行します。
       - PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId) プロパティで設定されている場合、エントリ識別子によって識別されるフォルダーにメッセージをコピーします。
       - PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit) プロパティが TRUE に設定されている場合は、メッセージを削除します。
       - ロックされている場合は、メッセージのロックを解除します。
       - クライアントに戻ります。 メッセージフローが完了しました。 
   
2. メッセージストアがトランスポートに密接に結合されておらず、すべての受信者がメッセージストアを認識していない場合、または NEEDS_SPOOLER フラグが設定されている場合は、次のタスクを実行します。
    
   - **PR_SUBMIT_FLAGS**プロパティの SUBMITFLAG_PREPROCESS ビットを設定せずに、メッセージを送信キューに配置します。 
   - テーブル通知を生成することによって、送信キューが変更されたことを MAPI スプーラーに通知します。 
   - クライアントに戻り、メッセージフローは MAPI スプーラーによって実行される一連のタスクを続行します。
    
メッセージが MAPI スプーラーによって処理される場合、メッセージストアプロバイダーは、メッセージの**PR_SUBMIT_FLAGS**プロパティを SUBMITFLAG_LOCKED に設定します。 SUBMITFLAG_LOCKED フラグは、MAPI スプーラーが排他的使用のためにメッセージをロックしたことを示します。 **PR_SUBMIT_FLAGS、** SUBMITFLAG_PREPROCESS のその他の値は、メッセージがトランスポートプロバイダーによって登録された1つ以上のプリプロセッサ関数の前処理を必要とするときに設定されます。 
  

