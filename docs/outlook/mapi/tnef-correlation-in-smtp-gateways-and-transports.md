---
title: SMTP ゲートウェイとトランスポートの TNEF 相関
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413669"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>SMTP ゲートウェイとトランスポートの TNEF 相関

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
インターネット ベースのシステム (SMTP を使用するシステム) に接続するゲートウェイとトランスポートは、MessageID SMTP ヘッダーの値と **PR_TNEF_CORRELATION_KEY** プロパティを使用して TNEF の相関関係を実装します。 
  
送信メッセージの MessageID ヘッダーの値は **、PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) プロパティにコピーし、TNEF ストリームの [attMAPIProps](attmapiprops.md) 属性でエンコードする必要があります。 このプロパティ **PR_TNEF_CORRELATION_KEY** バイナリ プロパティですが、MessageID は文字列です。null ターミネーターは、コピーと比較に含める必要があります。 
  
この手法は、MAPI ベースのメッセージング システムをインターネットに接続する Microsoft のすべてのソフトウェアで使用Microsoft Exchange Server。 この手法は、相互運用性を最大化するために、MAPI クライアントをサポートするシステムに接続する SMTP ゲートウェイおよびトランスポートで使用する必要があります。
  

