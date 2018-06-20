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
ms.openlocfilehash: 2d7311857ff54ef253fd00634671f4a510443f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801476"
---
# <a name="mapi-transport-provider-objects"></a>MAPI トランスポート プロバイダー オブジェクト
  
**適用されます**: Outlook 
  
だけでなく、標準のプロバイダーとログオン オブジェクトがすべてのサービス プロバイダーによって実装される、トランスポート プロバイダーは、状態オブジェクトを実装する必要があります。 その他のサービス プロバイダーの種類、状態オブジェクトを実装することは、省略可能です。 ただし、MAPI は、トランスポート プロバイダーの。 リモート サーバーからのメッセージ ヘッダーのダウンロードをサポートするトランスポート プロバイダーは、フォルダーと、テーブルにも実装します。 
  
各トランスポート プロバイダーは、対応するインターフェイスを実装できるオブジェクトを次に示します。 図では、MAPI またはクライアントは、オブジェクトのユーザーかどうかも示しています。
  
![トランスポート プロバイダーを実装するオブジェクト](media/amapi_66.gif "トランスポート プロバイダーを実装するオブジェクト")
  
## <a name="see-also"></a>関連項目

- [MAPI サービス プロバイダー オブジェクト](mapi-service-provider-objects.md)

