---
title: Transport-Neutral Encapsulation Format (TNEF)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: '最終更新日: 2013 年 3 月 12 日'
ms.openlocfilehash: 440c27b019b91ec8c2c02e37850d2768a273559b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591934"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Transport-Neutral Encapsulation Format (TNEF)

 
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
TNEF は、MAPI プロパティのセットを変換するための形式: MAPI メッセージ-シリアル データ ストリームにします。 TNEF 関数は、これらのプロパティを直接サポートしていないメッセージング システムを通じて送信するための MAPI メッセージのプロパティをエンコードするために必要とするトランスポート プロバイダーによって主に使用します。 など、SMTP ベースのトランスポートでは、SMTP メッセージの構造体に直接表現されていない**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) などのプロパティをエンコードするために TNEF を使用します。
  
TNEF の実装では、特定の MAPI プロパティに対応する、いくつかの TNEF 固有の属性を定義します。 TNEF ストリームに、それぞれの MAPI プロパティをエンコードするためには、これらの属性が使用されます。 特殊な属性を定義するさらに、それに対応する特定の属性を持たない任意の MAPI プロパティをカプセル化するのにを使用することができます。 これらの属性が定義されている理由: 統一されたすべての MAPI プロパティのエンコードを使用するだけではなく、TNEF を使用している MAPI 準拠のソフトウェアとの下位互換性を有効にするのには。
  
このセクションの残りの部分では、TNEF ストリームでは、MAPI プロパティと TNEF 属性では、TNEF の特定の属性の重要な考慮事項とのマッピングの構文、構造体について説明します。
  

