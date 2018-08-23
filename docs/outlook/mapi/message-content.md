---
title: メッセージの内容
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 85bd3f7db53f195295405fb0b02c25f084786a67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586082"
---
# <a name="message-content"></a>メッセージの内容

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージの内容の 2 つの可能なエンコーディングがあります: 1 つ、他の MIME を使用して uuencode を使用しています。 MIME は、使用するエンコーディングします。 さらに、MAPI は、 **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) は、送信メッセージで TNEF 情報を含める必要があるかどうかを指定する、受信者ごとのプロパティを定義します。 これは合計で 4 つの方法のメッセージ コンテンツのエンコードがあります。
  
- TNEF で MIME します。
    
- MIME TNEF なし
    
- TNEF で uuencode
    
- uuencode TNEF なし
    
MIME または uuencode 送信メッセージ用に選択する方法が指定されていません。
  
次のプロパティは TNEF から除外されます: **PR_SENDER_\***、 **PR_ATTACH_DATA_\***、 **PR_BODY**。 TNEF ストリームでは、他のすべてのメッセージを送信できるプロパティが含まれます。
  
実装がサポートする方法を決定するパラメーターの一覧を提供するは、次の方法が適しています。
  
- 送信メッセージの MIME または uuencode を使用してエンコードするかどうか: ブール値です。
    
- 送信メッセージに使用する一連の文字: (文字セット パラメーターに直接コピーされます) の文字列または (内部で変換する文字セットの文字列) を列挙します。
    

