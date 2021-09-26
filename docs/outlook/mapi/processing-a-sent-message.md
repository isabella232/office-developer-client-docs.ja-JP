---
title: 送信メッセージの処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 969977764539c05735704f9bceea45c2c84036e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624406"
---
# <a name="processing-a-sent-message"></a>送信メッセージの処理

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信メッセージは、送信後に送信ボックス フォルダーに残したり、送信済みメッセージを保持するために指定されたフォルダーに移動したり、削除したりできます。 処理の種類は、メッセージ ストアのプロパティを設定したかどうかによって異なります。
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** はブール型 (Boolean) のプロパティで、メッセージが送信された後に削除する必要がある場合は TRUE に設定され、それ以外の場合は FALSE に設定されます。 **PR_SENTMAIL_ENTRYID** は、フォルダーのエントリ識別子です。 このプロパティを設定すると、送信されたメッセージをこのエントリ識別子で表されるフォルダーに移動する必要があります。 保存されたメッセージは、通常、最後に送信するメッセージ ストアまたはトランスポート プロバイダーの ID を持っています。 
  
どちらか一方または他のプロパティを設定するか、これらのプロパティのどちらも設定する必要がありますが、両方を設定する必要はありません。 ただし、この値を設定 **PR_SENTMAIL_ENTRYID、** 有効なエントリ識別子が含まれている必要があります。 
  
次の表では、これらのプロパティが送信メッセージの処理に与える影響について説明します。
  
|||
|:-----|:-----|
|どちらのプロパティも設定しない場合:  <br/> |メッセージは、送信されたフォルダー (通常は送信箱) に残します。  <br/> |
|この **PR_SENTMAIL_ENTRYID** 設定されている場合は、次の値を使用します。  <br/> |メッセージを指定したフォルダーに移動します。  <br/> |
|この **PR_DELETE_AFTER_SUBMIT** 設定されている場合は、次の値を使用します。  <br/> |メッセージを削除する。  <br/> |
   

