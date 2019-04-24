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
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344563"
---
# <a name="smtp-addresses"></a>SMTP アドレス

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
SMTP 電子メールアドレスの形式は、RFC 822 で定義されています。 MAPI コンポーネントは、その標準に準拠する任意のアドレスを処理する必要があります。 ただし、次のような特定の形式の RFC 822 アドレスは、MAPI アドレスを最適にエンコードします。
  
 _表示名_**\<** _電子メールアドレス_**\>**
  
山かっこは、リテラルとして含まれています。 空白は表示名によく見られます。引用符で囲む必要はありません。 一般的な住所は、RFC 1521 の coauthors のいずれかに属している次のようになります。
  
Nathaniel Borenstein \<nsb@bellcore.com\>
  
\<または @ などの SMTP アドレスで特別な意味を持つ文字が表示名に含まれている場合は、表示名全体を二重引用符で囲む必要があります。 送信メールで、電子メールアドレスと表示名の長さの合計が255文字を超えている場合は、表示名を削除する必要があります。
  
次に示すように、SMTP アドレスを MAPI プロパティにマップします。
  
|**SMTP アドレスコンポーネント**|**MAPI プロパティ**|
|:-----|:-----|
| すべての受信者の_表示名_  <br/> |**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| From フィールドの_表示名_  <br/> |**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| 送信者フィールドの_表示名_  <br/> |**PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _電子メールアドレス_ <br/> |**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|暗黙的、常に "SMTP"  <br/> |**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
受信メールのアドレスの表示名がない場合は、代わりにメールアドレス全体を使用する必要があります。 アドレスの種類は、常に SMTP です。
  
受信者のプロパティは、MAPI メッセージの受信者テーブルから取得されます。sender プロパティは、メッセージ自体から取得されます。
  

