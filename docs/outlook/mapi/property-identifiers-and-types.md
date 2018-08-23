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
# <a name="property-identifiers-and-types"></a><span data-ttu-id="bfeef-103">プロパティの識別子と型</span><span class="sxs-lookup"><span data-stu-id="bfeef-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="bfeef-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfeef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfeef-105">すべての MAPI プロパティは、プロパティ タグで表されます。</span><span class="sxs-lookup"><span data-stu-id="bfeef-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="bfeef-106">プロパティ タグは、高でのプロパティの識別子を格納する 32 ビット符号なし整数値が 16 ビットを注文し、下位のプロパティの型は、16 ビットを注文します。</span><span class="sxs-lookup"><span data-stu-id="bfeef-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="bfeef-107">Mapitags.h ヘッダー ファイルでは、MAPI によって定義されたプロパティのすべてのプロパティ タグが含まれます。</span><span class="sxs-lookup"><span data-stu-id="bfeef-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="bfeef-108">プロパティ識別子を使用して、プロパティの使用およびその責任者を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfeef-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="bfeef-109">プロパティ識別子は、MAPI によって範囲に分かれています。識別子が範囲に該当する場所は、その使用法と所有権を示します。</span><span class="sxs-lookup"><span data-stu-id="bfeef-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="bfeef-110">プロパティの型を使用して、プロパティのデータの形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfeef-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="bfeef-111">MAPI は、すべての有効な型を定義します。</span><span class="sxs-lookup"><span data-stu-id="bfeef-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="bfeef-112">クライアントと新しいプロパティを作成するサービス プロバイダーは、これらの種類のいずれかで使用しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="bfeef-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="bfeef-113">Mapidefs.h ヘッダー ファイルでは、すべてのプロパティの種類が含まれます。</span><span class="sxs-lookup"><span data-stu-id="bfeef-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

