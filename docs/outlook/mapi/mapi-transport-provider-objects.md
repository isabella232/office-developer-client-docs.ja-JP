---
title: MAPI トランスポートプロバイダーのオブジェクト
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
# <a name="mapi-transport-provider-objects"></a>MAPI トランスポートプロバイダーのオブジェクト
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのサービスプロバイダーで実装されている標準のプロバイダーおよびログオンオブジェクトに加えて、status オブジェクトを実装するには、トランスポートプロバイダーが必要です。 その他のサービスプロバイダーの種類については、status オブジェクトを実装することはオプションです。 ただし、MAPI はトランスポートプロバイダーに対して必須です。 リモートサーバーからのメッセージヘッダーのダウンロードをサポートするトランスポートプロバイダーも、フォルダーとテーブルを実装します。 
  
次の図は、トランスポートプロバイダーが対応するインターフェイスと共に実装できる各オブジェクトを示しています。 この図は、MAPI またはクライアントがオブジェクトのユーザーであるかどうかも示しています。
  
![トランスポートプロバイダーが実装するオブジェクト](media/amapi_66.gif "トランスポートプロバイダーが実装するオブジェクト")
  
## <a name="see-also"></a>関連項目

- [MAPI サービスプロバイダオブジェクト](mapi-service-provider-objects.md)

