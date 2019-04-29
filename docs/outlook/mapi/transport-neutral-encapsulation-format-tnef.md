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
ms.openlocfilehash: d902039fa1081e30947ddd8f70ead9ae7acec06a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428691"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Transport-Neutral Encapsulation Format (TNEF)

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
TNEF は、一連の MAPI プロパティ (MAPI メッセージ) を連続したデータ ストリームに変換するための形式です。 TNEF 関数は、主に、これらのプロパティを直接サポートしていないメッセージングシステムを経由して送信するために MAPI メッセージプロパティをエンコードする必要があるトランスポートプロバイダーによって使用されます。 たとえば、smtp ベースのトランスポートは TNEF を使用して、 **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) などのプロパティをエンコードします。これは、smtp メッセージの構造に直接表現されているわけではありません。
  
tnef 実装では、いくつかの tnef 固有の属性が定義されています。これらはそれぞれ特定の MAPI プロパティに対応しています。 これらの属性は、それぞれの MAPI プロパティを TNEF ストリームにエンコードするために使用されます。 さらに、特定の属性を持たない MAPI プロパティをカプセル化するために使用できる特別な属性が定義されています。 これらの属性が定義されている理由は、すべての mapi プロパティに対して均一なエンコード方法を使用するのではなく、TNEF を使用している mapi に準拠していないソフトウェアとの下位互換性を有効にすることです。
  
このセクションの残りの部分では、tnef ストリームの構造と構文、MAPI プロパティと TNEF 属性間のマッピング、および特定の TNEF 属性に関する重要な考慮事項について説明します。
  

