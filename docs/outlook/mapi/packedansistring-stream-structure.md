---
title: PackedAnsiString ストリームの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4e919270efb196cda845581830cc4a918012b385
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578977"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="9c03f-103">PackedAnsiString ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="9c03f-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="9c03f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c03f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c03f-105">PackedAnsiString ストリームの構造体には、ANSI 形式 Microsoft Outlook を実行しているコンピューターの ANSI コード ページに基づいて、文字列にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9c03f-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="9c03f-106">この文字列は null 文字で終了していません。</span><span class="sxs-lookup"><span data-stu-id="9c03f-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="9c03f-107">このストリーム内のデータ要素は、以下に示す順序で互いのすぐ後、リトル エンディアンのバイト順で格納されます。</span><span class="sxs-lookup"><span data-stu-id="9c03f-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="9c03f-108">存在する実際のデータ要素は、ANSI 形式の文字列の長さによって異なります。</span><span class="sxs-lookup"><span data-stu-id="9c03f-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="9c03f-109">ANSI 形式には、255 バイト未満の場合が含まれている文字列のデータ要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9c03f-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="9c03f-110">長さ: バイト (1 バイト) で、ANSI 文字列表現の長さをバイト数で。</span><span class="sxs-lookup"><span data-stu-id="9c03f-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="9c03f-111">文字: 文字の配列。</span><span class="sxs-lookup"><span data-stu-id="9c03f-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="9c03f-112">この配列は長さのデータ要素になります。</span><span class="sxs-lookup"><span data-stu-id="9c03f-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="9c03f-113">配列内のデータは、文字列の ANSI 形式です。</span><span class="sxs-lookup"><span data-stu-id="9c03f-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="9c03f-114">ANSI 形式には、255 ~ 65535 バイトが含まれている文字列のデータ要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9c03f-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="9c03f-115">プレフィックス: バイト (1 バイト) で、値の 255 (0 xff) です。</span><span class="sxs-lookup"><span data-stu-id="9c03f-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="9c03f-116">長さ: ワード (2 バイト) で、ANSI 文字列表現の長さをバイト数で。</span><span class="sxs-lookup"><span data-stu-id="9c03f-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="9c03f-117">文字: 文字の配列。</span><span class="sxs-lookup"><span data-stu-id="9c03f-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="9c03f-118">この配列は長さのデータ要素になります。</span><span class="sxs-lookup"><span data-stu-id="9c03f-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="9c03f-119">配列内のデータは、文字列の ANSI 形式です。</span><span class="sxs-lookup"><span data-stu-id="9c03f-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c03f-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c03f-120">See also</span></span>



[<span data-ttu-id="9c03f-121">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="9c03f-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="9c03f-122">ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="9c03f-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="9c03f-123">FieldDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="9c03f-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

