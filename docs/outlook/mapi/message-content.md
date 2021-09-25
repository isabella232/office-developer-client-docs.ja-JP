---
title: メッセージ コンテンツ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b1523d230ae49e8ca779bab12e5ce6264f6300dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592061"
---
# <a name="message-content"></a>メッセージ コンテンツ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ コンテンツには、MIME を使用するエンコードと uuencode を使用するエンコードの 2 つがあります。 MIME が優先エンコードです。 さらに、MAPI は **、TNEF** 情報を送信メッセージに含めるかどうかを制御する受信者ごとのプロパティ PR_SEND_RICH_INFO ([PidTagSendRichInfo)](pidtagsendrichinfo-canonical-property.md)を定義します。 したがって、メッセージ コンテンツをエンコードする方法は合計 4 種類あります。
  
- TNEF を含む MIME
    
- TNEF なしの MIME
    
- TNEF を含む uuencode
    
- TNEF のない uuencode
    
送信メッセージに MIME または uuencode を選択する方法は指定されていません。
  
次のプロパティは TNEF から除外 **されます: PR_SENDER_ \* *_、 _* PR_ATTACH_DATA_ \* *_、 _* PR_BODY。** 他のすべての送信可能なメッセージ プロパティは、TNEF ストリームに含まれます。
  
次の提案は、実装がサポートする方法を決定できるパラメーターの一覧を提供することを目的としています。
  
- 送信メッセージに MIME または uuencode を使用してエンコードするかどうかを指定します。ブール型 (boolean) です。
    
- 送信メッセージに使用する文字セット: string (charset パラメーターに直接コピー) または列挙 (内部で文字セット文字列に変換)。
    

