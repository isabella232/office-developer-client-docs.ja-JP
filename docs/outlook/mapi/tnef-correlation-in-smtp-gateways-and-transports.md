---
title: SMTP ゲートウェイとトランスポートの TNEF 相関
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3cd51f3f48c236a17ee49f65368672ee849a5ed0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578481"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>SMTP ゲートウェイとトランスポートの TNEF 相関

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
インターネット ベースのシステム (SMTP を使用するシステム) に接続するゲートウェイとトランスポートは、MessageID SMTP ヘッダーの値と **PR_TNEF_CORRELATION_KEY** プロパティを使用して TNEF の相関関係を実装します。 
  
送信メッセージの MessageID ヘッダーの値は **、PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) プロパティにコピーし、TNEF ストリームの [attMAPIProps](attmapiprops.md) 属性でエンコードする必要があります。 このプロパティ **PR_TNEF_CORRELATION_KEY** バイナリ プロパティですが、MessageID は文字列です。null ターミネーターは、コピーと比較に含める必要があります。 
  
この手法は、MAPI ベースのメッセージング システムをインターネットに接続する Microsoft のすべてのソフトウェアで使用Microsoft Exchange Server。 この手法は、相互運用性を最大化するために、MAPI クライアントをサポートするシステムに接続する SMTP ゲートウェイおよびトランスポートで使用する必要があります。
  

