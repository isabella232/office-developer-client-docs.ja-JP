---
title: プロパティ識別子と型
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7f31162e669af6efaf9e935c7c400d105c1321c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803691"
---
# <a name="property-identifiers-and-types"></a><span data-ttu-id="dfe73-103">プロパティ識別子と型</span><span class="sxs-lookup"><span data-stu-id="dfe73-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="dfe73-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dfe73-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dfe73-105">すべての MAPI プロパティは、プロパティ タグで表されます。</span><span class="sxs-lookup"><span data-stu-id="dfe73-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="dfe73-106">プロパティ タグは、高でのプロパティの識別子を格納する 32 ビット符号なし整数値が 16 ビットを注文し、下位のプロパティの型は、16 ビットを注文します。</span><span class="sxs-lookup"><span data-stu-id="dfe73-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="dfe73-107">Mapitags.h ヘッダー ファイルでは、MAPI によって定義されたプロパティのすべてのプロパティ タグが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dfe73-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="dfe73-108">プロパティ識別子を使用して、プロパティの使用およびその責任者を指定します。</span><span class="sxs-lookup"><span data-stu-id="dfe73-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="dfe73-109">プロパティ識別子は、MAPI によって範囲に分かれています。識別子が範囲に該当する場所は、その使用法と所有権を示します。</span><span class="sxs-lookup"><span data-stu-id="dfe73-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="dfe73-110">プロパティの型を使用して、プロパティのデータの形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="dfe73-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="dfe73-111">MAPI は、すべての有効な型を定義します。</span><span class="sxs-lookup"><span data-stu-id="dfe73-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="dfe73-112">クライアントと新しいプロパティを作成するサービス プロバイダーは、これらの種類のいずれかで使用しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="dfe73-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="dfe73-113">Mapidefs.h ヘッダー ファイルでは、すべてのプロパティの種類が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dfe73-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

