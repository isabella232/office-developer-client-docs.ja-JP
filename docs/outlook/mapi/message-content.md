---
title: メッセージコンテンツ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357002"
---
# <a name="message-content"></a>メッセージコンテンツ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージコンテンツには2つのエンコード方式があります。1つは MIME を使用し、もう1つは uuencode を使用します。 MIME は推奨されるエンコーディングです。 さらに、MAPI は、送信メッセージに TNEF 情報を含める必要があるかどうかを管理する、受信者ごとのプロパティである**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) を定義します。 そのため、メッセージコンテンツをエンコードする方法は合計4つあります。
  
- TNEF を使用した MIME
    
- TNEF なしの MIME
    
- TNEF を使用した uuencode
    
- TNEF なしの uuencode
    
送信メッセージに対して MIME または uuencode を選択する方法が指定されていません。
  
次のプロパティは、TNEF から除外されます。 **\*PR_SENDER_**、 **PR_ATTACH_DATA_\***、 **PR_BODY**。 その他のすべての転送テーブルのメッセージプロパティは、TNEF ストリームに含まれています。
  
次の推奨事項は、実装がサポートする方法を決定できるパラメーターの一覧を提供することを目的としています。
  
- 送信メッセージに MIME または uuencode を使用してエンコードするかどうか: boolean。
    
- 送信メッセージに使用する文字セット: string (charset パラメーターに直接コピーされる) または列挙 (内部的に文字セット文字列に変換されます)。
    

