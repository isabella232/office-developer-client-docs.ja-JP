---
title: トランスポート プロバイダーの種類
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 38cf068c8f05dcd540973760ffe228eb81dbeef8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566263"
---
# <a name="types-of-transport-providers"></a>トランスポート プロバイダーの種類

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのトランスポート プロバイダーは、次のようなさまざまな標準機能をサポートしています。
  
- 基になるメッセージング システムに適切なセキュリティを提供する。
    
- 基になるメッセージング システムからのメッセージの送受信。
    
- MAPI スプーラーとクライアント アプリケーションが適切に使用できるよう、トランスポート プロバイダーがサポートするアドレスの種類を公開します。
    
- 特定の受信者の配信を受け入れる。
    
さらに、MAPI では、特定のメッセージング システムに特化した 2 種類のプロバイダーがサポートされています。
  
|**トランスポートの種類**|**追加された機能**|
|:-----|:-----|
|リモート トランスポート  <br/> |リモート接続されたクライアントとの相互運用性を有効にします。  <br/> |
|TNEF トランスポート  <br/> |MAPI プロパティをサポートしていないメッセージング システムで保持できます。  <br/> |
   
TNEF トランスポートは、MAPI プロパティの異なるセットをサポートするメッセージング システム間でメッセージを変換するために使用されます。 TNEF トランスポートでは、MAPI [ITnef : IUnknown](itnefiunknown.md) インターフェイスを使用して、宛先システムが直接表現できないプロパティを、メッセージに添付できるバイナリ データ ストリームに変換します。 後で、別の TNEF トランスポートで **ITnef** を使用してデータ ストリームをデコードし、元の MAPI プロパティをクライアント アプリケーションで使用できます。 さらに、トランスポートでカスタム メッセージ クラスをサポートする必要がある場合は、TNEF のサポートが必要です。 TNEF トランスポートの実装の詳細については、「セキュリティ トランスポート プロバイダー [の開発TNEF-Enabledを参照してください](developing-a-tnef-enabled-transport-provider.md)。
  
トランスポート プロバイダーがこれらの種類の 1 つではない場合は、ターゲット プラットフォームで使用できる基本的な MAPI 関数とネットワーク機能を使用してトランスポート プロバイダーを実装する必要があります。
  

