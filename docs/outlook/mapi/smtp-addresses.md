---
title: SMTP アドレス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 913df302c86742c20849fdb62e83437ad27e6d0c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619730"
---
# <a name="smtp-addresses"></a>SMTP アドレス

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
SMTP 電子メール アドレスの形式は RFC 822 で定義されています。 MAPI コンポーネントは、その標準に準拠するアドレスを処理する必要があります。 ただし、MAPI アドレスを最適にエンコードする RFC 822 アドレスの特定の形式があります。
  
 _表示名_ **\<** _email-address_ **\>**
  
角かっこはリテラルとして含まれます。 空白は、表示名で一般的です。引用符で囲む必要はない。 一般的なアドレスは、RFC 1521 の共同編集者の 1 つに属する次のように見える場合があります。
  
ナサニエル・ボレンシュタイン \<nsb@bellcore.com\>
  
表示名に SMTP アドレス (@など) に特別な意味を持つ文字が含まれている場合は、表示名全体を二重引用符 \< で囲む必要があります。 送信メールでは、電子メール アドレスと表示名の合計長が 255 文字を超える場合は、表示名を削除する必要があります。
  
SMTP アドレスの各部分は、次のように MAPI プロパティにマップされます。
  
|**SMTP アドレス コンポーネント**|**MAPI プロパティ**|
|:-----|:-----|
| _すべての受信者の_ 表示名  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _[From] フィールド_ の表示名  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _送信者フィールドの_ 表示名  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _電子メール アドレス_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|暗黙的、常に "SMTP"  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
受信メールにアドレスの表示名がない場合は、代わりに電子メール アドレス全体を使用する必要があります。 アドレスの種類は常に SMTP です。
  
受信者のプロパティは、MAPI メッセージの受信者テーブルから取られます。sender プロパティは、メッセージ自体から取られます。
  

