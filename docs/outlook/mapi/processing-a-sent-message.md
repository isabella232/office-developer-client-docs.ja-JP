---
title: 送信されたメッセージの処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 880731bf204778cde21da6cd9024a3ca86c6f6a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351066"
---
# <a name="processing-a-sent-message"></a>送信されたメッセージの処理

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信メッセージは送信された後で、送信トレイフォルダーに残したり、送信メッセージを保持するように指定されたフォルダーに移動したり、削除したりできます。 処理の種類は、メッセージストアのプロパティが設定されているかどうかによって異なります。
  
- **PR_DELETE_AFTER_SUBMIT**([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID**([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT**はブール型のプロパティで、送信後にメッセージを削除する場合は TRUE に設定し、それ以外の場合は FALSE に設定します。 **PR_SENTMAIL_ENTRYID**は、フォルダーのエントリ識別子です。 このプロパティが設定されている場合は、送信されたメッセージをこのエントリ識別子で表されるフォルダーに移動する必要があります。 保存されたメッセージには、通常、それらを送信するための最後のメッセージストアまたはトランスポートプロバイダーの id が設定されます。 
  
どちらか一方または両方のプロパティを設定する必要はありませんが、両方とも設定することはできません。 ただし、 **PR_SENTMAIL_ENTRYID**を設定する場合は、有効なエントリ識別子を含める必要があります。 
  
次の表では、これらのプロパティが送信メッセージの処理に与える影響について説明します。
  
|||
|:-----|:-----|
|どちらのプロパティも設定されていない場合:  <br/> |メッセージを送信元のフォルダー (通常は送信トレイ) に残します。  <br/> |
|**PR_SENTMAIL_ENTRYID**が設定されている場合:  <br/> |メッセージを指示されたフォルダーに移動します。  <br/> |
|**PR_DELETE_AFTER_SUBMIT**が設定されている場合:  <br/> |メッセージを削除します。  <br/> |
   

