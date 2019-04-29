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
# <a name="property-identifiers-and-types"></a><span data-ttu-id="6c9e4-103">プロパティの識別子と種類</span><span class="sxs-lookup"><span data-stu-id="6c9e4-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="6c9e4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c9e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c9e4-105">すべての MAPI プロパティは、property タグで表されます。</span><span class="sxs-lookup"><span data-stu-id="6c9e4-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="6c9e4-106">プロパティタグは、上位16ビットのプロパティの識別子と、下位16ビットのプロパティの型を含む、32ビットの符号なし整数値です。</span><span class="sxs-lookup"><span data-stu-id="6c9e4-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="6c9e4-107">MAPI で定義されているすべてのプロパティのプロパティタグは、mapitags ヘッダーファイルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="6c9e4-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="6c9e4-108">プロパティ識別子は、プロパティがどのように使用されるか、およびそのプロパティの責任者を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c9e4-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="6c9e4-109">プロパティ識別子は MAPI で範囲に分割されます。範囲内の識別子は、その使用と所有権を示します。</span><span class="sxs-lookup"><span data-stu-id="6c9e4-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="6c9e4-110">プロパティの種類は、プロパティのデータの形式を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c9e4-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="6c9e4-111">MAPI は、すべての有効な種類を定義します。</span><span class="sxs-lookup"><span data-stu-id="6c9e4-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="6c9e4-112">新しいプロパティを作成するクライアントおよびサービスプロバイダーは、これらの種類のいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c9e4-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="6c9e4-113">すべてのプロパティの種類は、mapidefs.h ヘッダーファイルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="6c9e4-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

