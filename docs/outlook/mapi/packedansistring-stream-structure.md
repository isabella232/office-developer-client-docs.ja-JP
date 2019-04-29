---
title: PackedAnsiString Stream 構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404506"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="0a542-103">PackedAnsiString Stream 構造</span><span class="sxs-lookup"><span data-stu-id="0a542-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="0a542-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a542-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a542-105">PackedAnsiString stream 構造体には、Microsoft Outlook が実行されているコンピューターの ansi コードページに基づいて、文字列の ansi 表現が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0a542-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="0a542-106">この文字列は、null 文字で終了していません。</span><span class="sxs-lookup"><span data-stu-id="0a542-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="0a542-107">このストリームの Data 要素は、次に示す順序で互いに続けて、リトルエンディアンバイト順に格納されます。</span><span class="sxs-lookup"><span data-stu-id="0a542-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="0a542-108">実際に存在するデータ要素は、ANSI 表現の文字列の長さによって決まります。</span><span class="sxs-lookup"><span data-stu-id="0a542-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="0a542-109">ANSI 表現が255バイト未満の文字列の場合、データ要素は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0a542-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="0a542-110">length: BYTE (1 バイト) (バイト数)。文字列の ANSI 表現の長さ。</span><span class="sxs-lookup"><span data-stu-id="0a542-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="0a542-111">文字: CHAR の配列。</span><span class="sxs-lookup"><span data-stu-id="0a542-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="0a542-112">この配列の数は、Length data 要素と同じです。</span><span class="sxs-lookup"><span data-stu-id="0a542-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="0a542-113">配列内のデータは、文字列の ANSI 表現です。</span><span class="sxs-lookup"><span data-stu-id="0a542-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="0a542-114">ANSI 表記に 255 ~ 65535 バイトの文字列が含まれている場合、データ要素は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0a542-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="0a542-115">プレフィックス: BYTE (1 バイト)、255 (0xff) の値。</span><span class="sxs-lookup"><span data-stu-id="0a542-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="0a542-116">length: WORD (2 バイト)。文字列の ANSI 表現の長さをバイト数で指定します。</span><span class="sxs-lookup"><span data-stu-id="0a542-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="0a542-117">文字: CHAR の配列。</span><span class="sxs-lookup"><span data-stu-id="0a542-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="0a542-118">この配列の数は、Length data 要素と同じです。</span><span class="sxs-lookup"><span data-stu-id="0a542-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="0a542-119">配列内のデータは、文字列の ANSI 表現です。</span><span class="sxs-lookup"><span data-stu-id="0a542-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a542-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="0a542-120">See also</span></span>



[<span data-ttu-id="0a542-121">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="0a542-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="0a542-122">Stream 構造体</span><span class="sxs-lookup"><span data-stu-id="0a542-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="0a542-123">fielddefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="0a542-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

