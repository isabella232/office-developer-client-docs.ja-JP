---
title: PackedUnicodeString ストリーム構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fc20c259f30ded2f96f3bf314e74207bebcac980
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422615"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="8a497-103">PackedUnicodeString ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="8a497-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="8a497-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a497-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a497-105">PackedUnicodeString ストリーム構造には、文字列の Unicode (UTF-16) 表記が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8a497-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="8a497-106">この文字列は null 文字で終了されません。</span><span class="sxs-lookup"><span data-stu-id="8a497-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="8a497-107">このストリーム内のデータ要素は、次に示す順序で、お互いに直後に続く、リトル エンディアン バイト順に格納されます。</span><span class="sxs-lookup"><span data-stu-id="8a497-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="8a497-108">実際に存在するデータ要素は、UTF-16 表記の文字列の長さに依存します。</span><span class="sxs-lookup"><span data-stu-id="8a497-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="8a497-109">UTF-16 表記が 255 WCHA 未満の文字列の場合、データ要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8a497-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="8a497-110">長さ: BYTE (1 バイト)、文字列の UTF-16 表記の長さ (WCHARs の数)。</span><span class="sxs-lookup"><span data-stu-id="8a497-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="8a497-111">文字: WCHAR の配列。</span><span class="sxs-lookup"><span data-stu-id="8a497-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="8a497-112">この配列の数は、Length データ要素と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="8a497-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="8a497-113">配列内のデータは、文字列の UTF-16 表記です。</span><span class="sxs-lookup"><span data-stu-id="8a497-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="8a497-114">UTF-16 表記に 255 ~ 65535 WCHA が含まれる文字列の場合、データ要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8a497-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="8a497-115">プレフィックス: BYTE (1 バイト)、値 255 (0xff)。</span><span class="sxs-lookup"><span data-stu-id="8a497-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="8a497-116">長さ: 文字列の UTF-16 表記の WORD (2 バイト)、WCHARs の数の長さ。</span><span class="sxs-lookup"><span data-stu-id="8a497-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="8a497-117">文字: WCHAR の配列。</span><span class="sxs-lookup"><span data-stu-id="8a497-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="8a497-118">この配列の数は、Length データ要素と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="8a497-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="8a497-119">配列内のデータは、文字列の UTF-16 表記です。</span><span class="sxs-lookup"><span data-stu-id="8a497-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a497-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="8a497-120">See also</span></span>



[<span data-ttu-id="8a497-121">Outlookアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="8a497-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="8a497-122">Stream 構造</span><span class="sxs-lookup"><span data-stu-id="8a497-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="8a497-123">FieldDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="8a497-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

