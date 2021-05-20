---
title: MAPI トランスポート プロバイダー オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430358"
---
# <a name="mapi-transport-provider-objects"></a>MAPI トランスポート プロバイダー オブジェクト
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのサービス プロバイダーによって実装される標準のプロバイダー オブジェクトとログオン オブジェクトに加えて、状態オブジェクトを実装するためにトランスポート プロバイダーが必要です。 その他のサービス プロバイダーの種類では、status オブジェクトの実装はオプションです。 ただし、MAPI はトランスポート プロバイダーに対して必要です。 リモート サーバーからのメッセージ ヘッダーのダウンロードをサポートするトランスポート プロバイダーは、フォルダーとテーブルも実装します。 
  
次の図は、トランスポート プロバイダーが対応するインターフェイスで実装できる各オブジェクトを示しています。 図は、MAPI またはクライアントがオブジェクトのユーザーかどうかを示します。
  
![トランスポート プロバイダーが実装するオブジェクト](media/amapi_66.gif "トランスポート プロバイダーが実装するオブジェクト")
  
## <a name="see-also"></a>関連項目

- [MAPI サービス プロバイダー オブジェクト](mapi-service-provider-objects.md)

