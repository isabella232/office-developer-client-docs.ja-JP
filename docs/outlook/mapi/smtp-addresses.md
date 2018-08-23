---
title: SMTP アドレス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9bc77e3226066dc88bbaf4f4efc324825add8919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803970"
---
# <a name="smtp-addresses"></a>SMTP アドレス

  
  
**適用対象**: Outlook 
  
SMTP 電子メール アドレスの形式は、RFC 822 で定義されます。 MAPI コンポーネントでは、その標準に準拠している任意のアドレスを処理する必要があります。 ただし、RFC 822 アドレス MAPI アドレスを記述する方式の特定のフォームがあります。
  
 _表示名_**\<** _e メール アドレス_**\>**
  
山かっこでは、リテラル文字列として含まれています。 空白は、共通の表示名です。それらを引用されません必要があります。 一般的なアドレスは、このいずれか、RFC 1521 の共同のいずれかに属するのようになります。
  
Nathaniel Borenstein \<nsb@bellcore.com\>
  
表示名には、次のように、SMTP アドレスに特別な意味がある文字が含まれている場合\<または @、全体の表示名を二重引用符で囲む必要があります。 、送信メールの名が 255 文字を超えるプラスの電子メール アドレスの長さの合計を表示する場合、表示名を削除する必要があります。
  
SMTP アドレスの部分は、MAPI のプロパティに次のようにマップします。
  
|**SMTP アドレスのコンポーネント**|**MAPI プロパティ**|
|:-----|:-----|
| すべての受信者の_表示名_  <br/> |**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| フィールドの_表示名_  <br/> |**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| [送信者] フィールドの_表示名_  <br/> |**PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _電子メール アドレス_ <br/> |**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|暗黙に、常に"SMTP"  <br/> |**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
受信メールのアドレスの表示名がない場合は、全体の電子メール アドレスを代わりに使用する必要があります。 アドレス タイプは SMTP では常にします。
  
受信者のプロパティは、MAPI メッセージの受信者テーブルから取得されます。センダーのプロパティは、メッセージ自体から取得されます。
  

