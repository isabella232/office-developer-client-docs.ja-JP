---
title: PackedAnsiString ストリーム構造
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
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="ffbac-103">PackedAnsiString ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="ffbac-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="ffbac-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffbac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffbac-105">PackedAnsiString ストリーム構造には、Microsoft が実行されているコンピューターの ANSI コード ページに基づいて、文字列の ANSI 表現Outlook含まれます。</span><span class="sxs-lookup"><span data-stu-id="ffbac-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="ffbac-106">この文字列は null 文字で終了されません。</span><span class="sxs-lookup"><span data-stu-id="ffbac-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="ffbac-107">このストリーム内のデータ要素は、次に示す順序で、お互いに直後に続く、リトル エンディアン バイト順に格納されます。</span><span class="sxs-lookup"><span data-stu-id="ffbac-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="ffbac-108">実際に存在するデータ要素は、ANSI 表現の文字列の長さによって異なっています。</span><span class="sxs-lookup"><span data-stu-id="ffbac-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="ffbac-109">ANSI 表記が 255 バイト未満の文字列の場合、データ要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ffbac-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="ffbac-110">長さ: BYTE (1 バイト)、文字列の ANSI 表記の長さ (バイト数)。</span><span class="sxs-lookup"><span data-stu-id="ffbac-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="ffbac-111">文字: CHAR の配列。</span><span class="sxs-lookup"><span data-stu-id="ffbac-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="ffbac-112">この配列の数は、Length データ要素と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="ffbac-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="ffbac-113">配列内のデータは、文字列の ANSI 表記です。</span><span class="sxs-lookup"><span data-stu-id="ffbac-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="ffbac-114">ANSI 表現に 255 ~ 65535 バイトが含まれる文字列の場合、データ要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ffbac-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="ffbac-115">プレフィックス: BYTE (1 バイト)、値 255 (0xff)。</span><span class="sxs-lookup"><span data-stu-id="ffbac-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="ffbac-116">長さ: 文字列の ANSI 表記の WORD (2 バイト)、長さ (バイト数)。</span><span class="sxs-lookup"><span data-stu-id="ffbac-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="ffbac-117">文字: CHAR の配列。</span><span class="sxs-lookup"><span data-stu-id="ffbac-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="ffbac-118">この配列の数は、Length データ要素と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="ffbac-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="ffbac-119">配列内のデータは、文字列の ANSI 表記です。</span><span class="sxs-lookup"><span data-stu-id="ffbac-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffbac-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="ffbac-120">See also</span></span>



[<span data-ttu-id="ffbac-121">Outlookアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="ffbac-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="ffbac-122">Stream 構造</span><span class="sxs-lookup"><span data-stu-id="ffbac-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="ffbac-123">FieldDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="ffbac-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

