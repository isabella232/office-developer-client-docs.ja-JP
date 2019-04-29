---
title: プロパティの識別子と種類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: caba60b7059d1c1f8f0440aeb55abb88801fbc9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437218"
---
# <a name="property-identifiers-and-types"></a>プロパティの識別子と種類

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべての MAPI プロパティは、property タグで表されます。 プロパティタグは、上位16ビットのプロパティの識別子と、下位16ビットのプロパティの型を含む、32ビットの符号なし整数値です。 MAPI で定義されているすべてのプロパティのプロパティタグは、mapitags ヘッダーファイルに含まれています。
  
プロパティ識別子は、プロパティがどのように使用されるか、およびそのプロパティの責任者を示すために使用されます。 プロパティ識別子は MAPI で範囲に分割されます。範囲内の識別子は、その使用と所有権を示します。 
  
プロパティの種類は、プロパティのデータの形式を示すために使用されます。 MAPI は、すべての有効な種類を定義します。 新しいプロパティを作成するクライアントおよびサービスプロバイダーは、これらの種類のいずれかを使用する必要があります。 すべてのプロパティの種類は、mapidefs.h ヘッダーファイルに含まれています。
  

