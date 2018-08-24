---
title: PropertyDefinition ストリームのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fc216302cb68be4b0e9d57f60f491adebcba1975
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573930"
---
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="6223e-103">PropertyDefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="6223e-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="6223e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6223e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6223e-105">PropertyDefinition ストリームの例について説明します。</span><span class="sxs-lookup"><span data-stu-id="6223e-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="6223e-106">ストリームには、ユーザー定義のフィールドの定義が含まれている`TextField1`。</span><span class="sxs-lookup"><span data-stu-id="6223e-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="6223e-107">型は、**テキスト**、および PropDefV2 の形式では、定義します。</span><span class="sxs-lookup"><span data-stu-id="6223e-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="6223e-108">データのダンプ</span><span class="sxs-lookup"><span data-stu-id="6223e-108">Data dump</span></span>

<span data-ttu-id="6223e-109">次のストリームのデータのダンプがバイナリ エディターで表示します。</span><span class="sxs-lookup"><span data-stu-id="6223e-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="6223e-110">ストリームのオフセット</span><span class="sxs-lookup"><span data-stu-id="6223e-110">Stream offset</span></span>|<span data-ttu-id="6223e-111">データのバイト数</span><span class="sxs-lookup"><span data-stu-id="6223e-111">Data bytes</span></span>|<span data-ttu-id="6223e-112">ASCII データ</span><span class="sxs-lookup"><span data-stu-id="6223e-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="6223e-113">PropertyDefinition ストリームのサンプル データの解析は、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="6223e-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="6223e-114">バージョン: 0x0 では、2 バイトのオフセット: 0x0103 (PropDefV2)。</span><span class="sxs-lookup"><span data-stu-id="6223e-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="6223e-115">FieldDefinitionCount: 0x2、4 バイトのオフセット: 0x1 (1)。</span><span class="sxs-lookup"><span data-stu-id="6223e-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="6223e-116">FieldDefinitions: 0x6、1 の FieldDefinition ストリームの配列をオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="6223e-117">フラグ: 0x6、4 バイトのオフセット: 0x45 (PDO_IS_CUSTOM |PDO_PRINT_SAVEAS |PDO_PRINT_SAVEAS_DEF)。</span><span class="sxs-lookup"><span data-stu-id="6223e-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="6223e-118">VT: オフセットの 2 バイトの 0 xa: 0x8 (**VT_BSTR**)。</span><span class="sxs-lookup"><span data-stu-id="6223e-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="6223e-119">DispId: 0 xc、4 バイトのオフセット: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="6223e-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="6223e-120">NmidNameLength: 0x10、2 バイトのオフセット: 0 xa (10)。</span><span class="sxs-lookup"><span data-stu-id="6223e-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="6223e-121">NmidName: 0x12, WCHARs が 10 の配列のオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="6223e-122">Unicode 文字列の値:「TextField1」です。</span><span class="sxs-lookup"><span data-stu-id="6223e-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="6223e-123">NameANSI: 0x26、PackedAnsiString ストリームをオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="6223e-124">長さ: オフセット 0x26、1 バイト: 0 xa (10)。</span><span class="sxs-lookup"><span data-stu-id="6223e-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="6223e-125">文字: 0x27、10 文字の配列をオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="6223e-126">ANSI 文字列の値:「TextField1」です。</span><span class="sxs-lookup"><span data-stu-id="6223e-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="6223e-127">FormulaANSI: オフセットれました、PackedAnsiString のストリーム。</span><span class="sxs-lookup"><span data-stu-id="6223e-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="6223e-128">長さ: オフセットれました、1 バイト: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="6223e-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="6223e-129">文字: 0x32、0 文字の配列をオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="6223e-130">空の ANSI 文字列。</span><span class="sxs-lookup"><span data-stu-id="6223e-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="6223e-131">ValidationRuleANSI: 0x32、PackedAnsiString ストリームをオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="6223e-132">長さ: オフセット 0x32、1 バイト: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="6223e-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="6223e-133">文字: 0x33、0 文字の配列をオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="6223e-134">空の ANSI 文字列。</span><span class="sxs-lookup"><span data-stu-id="6223e-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="6223e-135">ValidationTextANSI: 0x33、PackedAnsiString ストリームをオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="6223e-136">長さ: オフセット 0x33、1 バイト: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="6223e-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="6223e-137">文字: は、0x34, 0 の文字の配列をオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="6223e-138">空の ANSI 文字列。</span><span class="sxs-lookup"><span data-stu-id="6223e-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="6223e-139">ErrorANSI: 0x34, PackedAnsiString ストリームをオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="6223e-140">長さ: オフセット 0x34, 1 バイト: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="6223e-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="6223e-141">文字: 0x35、文字数が 0 の配列のオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="6223e-142">空の ANSI 文字列。</span><span class="sxs-lookup"><span data-stu-id="6223e-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="6223e-143">InternalType: 0x35、4 バイトのオフセット: 0x0 (iTypeString)。</span><span class="sxs-lookup"><span data-stu-id="6223e-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="6223e-144">SkipBlocks: 0x39、一連の SkipBlock ストリームのオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="6223e-145">最初の SkipBlock</span><span class="sxs-lookup"><span data-stu-id="6223e-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="6223e-146">サイズ: 0x39、4 バイトのオフセット: 0x15 (21)。</span><span class="sxs-lookup"><span data-stu-id="6223e-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="6223e-147">コンテンツ: 0x3D、21 のバイト配列をオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="6223e-148">これは最初の SkipBlock ストリームでは、この配列には、FirstSkipBlockContent ストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6223e-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="6223e-149">フィールド名: 0x3D、PackedUnicodeString ストリームをオフセットします。</span><span class="sxs-lookup"><span data-stu-id="6223e-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="6223e-150">長さ: オフセット 0x3D、1 バイト: 0 xa (10)。</span><span class="sxs-lookup"><span data-stu-id="6223e-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="6223e-151">文字: オフセット 0x3E、WCHARs の 10 個の配列です。</span><span class="sxs-lookup"><span data-stu-id="6223e-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="6223e-152">Unicode 文字列の値:「TextField1」です。</span><span class="sxs-lookup"><span data-stu-id="6223e-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="6223e-153">2 番目の SkipBlock</span><span class="sxs-lookup"><span data-stu-id="6223e-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="6223e-154">サイズ: 使用、4 バイトのオフセット: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="6223e-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="6223e-155">これは、終端の SkipBlock ストリームです。</span><span class="sxs-lookup"><span data-stu-id="6223e-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6223e-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="6223e-156">See also</span></span>

- [<span data-ttu-id="6223e-157">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="6223e-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="6223e-158">ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="6223e-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="6223e-159">PropertyDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="6223e-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="6223e-160">FieldDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="6223e-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="6223e-161">SkipBlock ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="6223e-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="6223e-162">FirstSkipBlockContent ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="6223e-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="6223e-163">PackedAnsiString ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="6223e-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="6223e-164">PackedUnicodeString ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="6223e-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

