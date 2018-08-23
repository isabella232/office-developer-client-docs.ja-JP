---
title: 送信したメッセージの処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0cea1a1008ecbff698b757d6c67af5c279954656
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803677"
---
# <a name="processing-a-sent-message"></a>送信したメッセージの処理

  
  
**適用対象**: Outlook 
  
それらが送信された後、送信メッセージの数をおくことができますを保持するために指定されたフォルダーに移動されているフォルダーは、メッセージを送信または削除、[送信トレイ] にします。 処理の種類は、かどうか設定したメッセージ ・ ストア ・ プロパティによって異なります。
  
- **PR_DELETE_AFTER_SUBMIT**([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID**([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT**は、それ以外の場合、送信後にメッセージを削除する場合は TRUE、FALSE に設定、ブール型プロパティです。 **PR_SENTMAIL_ENTRYID**は、フォルダーのエントリ id です。 このプロパティを設定すると、このエントリの識別子によって表されるフォルダーに送信したメッセージを移動する必要があります。 保存されたメッセージは通常の最後のメッセージ ・ ストア id を持っているか、転送を送信するプロバイダーです。 
  
セット、両方ではありませんが、いずれか 1 つ、またはこれらのプロパティのどちらも必要があります。 ただし、 **PR_SENTMAIL_ENTRYID**を設定した場合、有効なエントリの識別子を含める必要があります。 
  
次の表は、どのようにこれらのプロパティに影響を与える送信メッセージに対して行う操作について説明します。
  
|||
|:-----|:-----|
|場合は 2 つのプロパティを設定します。  <br/> |(通常、[送信トレイ]) の送信、元のフォルダーにメッセージを残します。  <br/> |
|場合は**PR_SENTMAIL_ENTRYID**が設定されます。  <br/> |指定されたフォルダーにメッセージを移動します。  <br/> |
|場合は**PR_DELETE_AFTER_SUBMIT**が設定されます。  <br/> |メッセージを削除します。  <br/> |
   

