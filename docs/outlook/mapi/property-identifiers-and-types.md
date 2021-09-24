---
title: プロパティ識別子と型
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f1fefed6006dd90b200b8dfdc4ed4337a40a0186
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550177"
---
# <a name="property-identifiers-and-types"></a>プロパティ識別子と型

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべての MAPI プロパティは、プロパティ タグによって表されます。 プロパティ タグは、高次 16 ビットのプロパティの識別子と、低次 16 ビットのプロパティの型を含む 32 ビットの符号なし整数値です。 MAPI で定義されているプロパティのプロパティ タグはすべて、mapitags.h ヘッダー ファイルに含まれています。
  
プロパティ識別子は、プロパティが使用されるプロパティと、そのプロパティの責任者を示すために使用されます。 プロパティ識別子は、MAPI で範囲に分割されます。識別子が範囲内にある場合は、その使用と所有権を示します。 
  
プロパティの種類は、プロパティのデータの形式を示すために使用されます。 MAPI は、すべての有効な型を定義します。 新しいプロパティを作成するクライアントとサービス プロバイダーは、次のいずれかの種類を使用する必要があります。 すべてのプロパティの種類は、mapidefs.h ヘッダー ファイルに含まれています。
  

