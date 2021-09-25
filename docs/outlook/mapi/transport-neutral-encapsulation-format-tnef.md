---
title: Transport-Neutral Encapsulation Format (TNEF)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: '最終更新日: 2013 年 3 月 12 日'
ms.openlocfilehash: 22ba19f374421656317196080e6a22153700f851
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590911"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Transport-Neutral Encapsulation Format (TNEF)

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
TNEF は、一連の MAPI プロパティ (MAPI メッセージ) を連続したデータ ストリームに変換するための形式です。 TNEF 関数は、主に、これらのプロパティを直接サポートしないメッセージング システムを介して送信するために MAPI メッセージ プロパティをエンコードする必要があるトランスポート プロバイダーによって使用されます。 たとえば、SMTP ベースのトランスポートは TNEF を使用して **、SMTP** メッセージの構造に直接表現されていない PR_SENT_REPRESENTING_NAME ([PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)などのプロパティをエンコードします。
  
TNEF 実装では、複数の TNEF 固有の属性を定義します。それぞれの属性は、特定の MAPI プロパティに対応します。 これらの属性は、それぞれの MAPI プロパティを TNEF ストリームにエンコードするために使用されます。 さらに、特定の属性が対応していない MAPI プロパティをカプセル化するために使用できる特別な属性が定義されています。 これらの属性が定義されている理由は、すべての MAPI プロパティに対して単に統一エンコード方式を使用する代わりに、TNEF を使用している MAPI 準拠以外のソフトウェアとの下位互換性を有効にしている理由です。
  
このセクションの残りの部分では、TNEF ストリームの構造と構文、MAPI プロパティと TNEF 属性間のマッピング、および特定の TNEF 属性に関する重要な考慮事項について説明します。
  

