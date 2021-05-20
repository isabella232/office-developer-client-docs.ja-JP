---
title: プロパティ識別子と型
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
# <a name="property-identifiers-and-types"></a><span data-ttu-id="975bc-103">プロパティ識別子と型</span><span class="sxs-lookup"><span data-stu-id="975bc-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="975bc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="975bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="975bc-105">すべての MAPI プロパティは、プロパティ タグによって表されます。</span><span class="sxs-lookup"><span data-stu-id="975bc-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="975bc-106">プロパティ タグは、高次 16 ビットのプロパティの識別子と、低次 16 ビットのプロパティの型を含む 32 ビットの符号なし整数値です。</span><span class="sxs-lookup"><span data-stu-id="975bc-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="975bc-107">MAPI で定義されているプロパティのプロパティ タグはすべて、mapitags.h ヘッダー ファイルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="975bc-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="975bc-108">プロパティ識別子は、プロパティが使用されるプロパティと、そのプロパティの責任者を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="975bc-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="975bc-109">プロパティ識別子は、MAPI で範囲に分割されます。識別子が範囲内にある場合は、その使用と所有権を示します。</span><span class="sxs-lookup"><span data-stu-id="975bc-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="975bc-110">プロパティの種類は、プロパティのデータの形式を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="975bc-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="975bc-111">MAPI は、すべての有効な型を定義します。</span><span class="sxs-lookup"><span data-stu-id="975bc-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="975bc-112">新しいプロパティを作成するクライアントとサービス プロバイダーは、次のいずれかの種類を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="975bc-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="975bc-113">すべてのプロパティの種類は、mapidefs.h ヘッダー ファイルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="975bc-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

