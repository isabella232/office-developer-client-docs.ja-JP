---
title: MAPI トランスポート プロバイダー オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: de0334ee9a90da38e472571314136195c84a7866
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592704"
---
# <a name="mapi-transport-provider-objects"></a>MAPI トランスポート プロバイダー オブジェクト
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
だけでなく、標準のプロバイダーとログオン オブジェクトがすべてのサービス プロバイダーによって実装される、トランスポート プロバイダーは、状態オブジェクトを実装する必要があります。 その他のサービス プロバイダーの種類、状態オブジェクトを実装することは、省略可能です。 ただし、MAPI は、トランスポート プロバイダーの。 リモート サーバーからのメッセージ ヘッダーのダウンロードをサポートするトランスポート プロバイダーは、フォルダーと、テーブルにも実装します。 
  
各トランスポート プロバイダーは、対応するインターフェイスを実装できるオブジェクトを次に示します。 図では、MAPI またはクライアントは、オブジェクトのユーザーかどうかも示しています。
  
![トランスポート プロバイダーを実装するオブジェクト](media/amapi_66.gif "トランスポート プロバイダーを実装するオブジェクト")
  
## <a name="see-also"></a>関連項目

- [MAPI サービス プロバイダー オブジェクト](mapi-service-provider-objects.md)

