---
title: プロパティの識別子と型
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 423992e0485e8e3092cfc4126164576906d51149
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567064"
---
# <a name="property-identifiers-and-types"></a>プロパティの識別子と型

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
すべての MAPI プロパティは、プロパティ タグで表されます。 プロパティ タグは、高でのプロパティの識別子を格納する 32 ビット符号なし整数値が 16 ビットを注文し、下位のプロパティの型は、16 ビットを注文します。 Mapitags.h ヘッダー ファイルでは、MAPI によって定義されたプロパティのすべてのプロパティ タグが含まれます。
  
プロパティ識別子を使用して、プロパティの使用およびその責任者を指定します。 プロパティ識別子は、MAPI によって範囲に分かれています。識別子が範囲に該当する場所は、その使用法と所有権を示します。 
  
プロパティの型を使用して、プロパティのデータの形式を指定します。 MAPI は、すべての有効な型を定義します。 クライアントと新しいプロパティを作成するサービス プロバイダーは、これらの種類のいずれかで使用しなければなりません。 Mapidefs.h ヘッダー ファイルでは、すべてのプロパティの種類が含まれます。
  

