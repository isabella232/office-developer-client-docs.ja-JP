---
title: PropertyDefinition ストリームのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 63a8141221c0ff7a8c6ffee20587b682386f87b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406662"
---
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="43b4a-103">PropertyDefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="43b4a-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="43b4a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43b4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43b4a-105">このトピックでは、PropertyDefinition ストリームの例について説明します。</span><span class="sxs-lookup"><span data-stu-id="43b4a-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="43b4a-106">ストリームには、ユーザー定義フィールドの定義が含まれます  `TextField1` 。</span><span class="sxs-lookup"><span data-stu-id="43b4a-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="43b4a-107">型は **Text** で、定義は PropDefV2 形式です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="43b4a-108">データ ダンプ</span><span class="sxs-lookup"><span data-stu-id="43b4a-108">Data dump</span></span>

<span data-ttu-id="43b4a-109">バイナリ エディターに表示されるストリームのデータ ダンプを次に示します。</span><span class="sxs-lookup"><span data-stu-id="43b4a-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="43b4a-110">ストリーム のオフセット</span><span class="sxs-lookup"><span data-stu-id="43b4a-110">Stream offset</span></span>|<span data-ttu-id="43b4a-111">データ バイト</span><span class="sxs-lookup"><span data-stu-id="43b4a-111">Data bytes</span></span>|<span data-ttu-id="43b4a-112">ASCII データ</span><span class="sxs-lookup"><span data-stu-id="43b4a-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="43b4a-113">PropertyDefinition ストリームのサンプル データの解析を次に示します。</span><span class="sxs-lookup"><span data-stu-id="43b4a-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="43b4a-114">バージョン: オフセット 0x0 2 バイト: 0x0103 (PropDefV2)。</span><span class="sxs-lookup"><span data-stu-id="43b4a-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="43b4a-115">FieldDefinitionCount: オフセット 0x2、4 バイト: 0x1 (1)。</span><span class="sxs-lookup"><span data-stu-id="43b4a-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="43b4a-116">FieldDefinitions: オフセット0x6、1 FieldDefinition ストリームの配列です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="43b4a-117">フラグ: オフセット 0x6、4 バイト: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF)。</span><span class="sxs-lookup"><span data-stu-id="43b4a-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="43b4a-118">VT: オフセット 0xA、2 バイト: 0x8 **(** VT_BSTR)。</span><span class="sxs-lookup"><span data-stu-id="43b4a-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="43b4a-119">DispId: オフセット 0xC、4 バイト: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="43b4a-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="43b4a-120">NmidNameLength: オフセット 0x10、2 バイト: 0xA (10)。</span><span class="sxs-lookup"><span data-stu-id="43b4a-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="43b4a-121">NmidName: オフセット0x12 10 WCHARs の配列です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="43b4a-122">Unicode 文字列値: "TextField1"</span><span class="sxs-lookup"><span data-stu-id="43b4a-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="43b4a-123">NameANSI: Offset 0x26 PackedAnsiString ストリーム。</span><span class="sxs-lookup"><span data-stu-id="43b4a-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="43b4a-124">長さ: オフセット0x26、1 バイト: 0xA (10) です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="43b4a-125">文字: オフセット0x27、10 文字の配列です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="43b4a-126">ANSI 文字列値: "TextField1"</span><span class="sxs-lookup"><span data-stu-id="43b4a-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="43b4a-127">FormulaANSI: Offset 0x31 PackedAnsiString ストリーム。</span><span class="sxs-lookup"><span data-stu-id="43b4a-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="43b4a-128">長さ: オフセット0x31、1 バイト: 0x0 (0) です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="43b4a-129">文字: オフセット0x32、0 文字の配列です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="43b4a-130">ANSI 文字列を空にします。</span><span class="sxs-lookup"><span data-stu-id="43b4a-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="43b4a-131">ValidationRuleANSI: Offset 0x32 PackedAnsiString ストリーム。</span><span class="sxs-lookup"><span data-stu-id="43b4a-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="43b4a-132">長さ: オフセット0x32、1 バイト: 0x0 (0) です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="43b4a-133">文字: オフセット0x33、0 文字の配列です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="43b4a-134">ANSI 文字列を空にします。</span><span class="sxs-lookup"><span data-stu-id="43b4a-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="43b4a-135">ValidationTextANSI: Offset 0x33 PackedAnsiString ストリーム。</span><span class="sxs-lookup"><span data-stu-id="43b4a-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="43b4a-136">長さ: オフセット0x33、1 バイト: 0x0 (0) です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="43b4a-137">文字: オフセット0x34、0 文字の配列です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="43b4a-138">ANSI 文字列を空にします。</span><span class="sxs-lookup"><span data-stu-id="43b4a-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="43b4a-139">ErrorANSI: Offset 0x34、PackedAnsiString ストリーム。</span><span class="sxs-lookup"><span data-stu-id="43b4a-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="43b4a-140">長さ: オフセット0x34、1 バイト: 0x0 (0) です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="43b4a-141">文字: オフセット0x35、0 文字の配列です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="43b4a-142">ANSI 文字列を空にします。</span><span class="sxs-lookup"><span data-stu-id="43b4a-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="43b4a-143">InternalType: Offset 0x35、4 バイト: 0x0 (iTypeString)。</span><span class="sxs-lookup"><span data-stu-id="43b4a-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="43b4a-144">SkipBlocks: 一連0x39一連の SkipBlock ストリームをオフセットします。</span><span class="sxs-lookup"><span data-stu-id="43b4a-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="43b4a-145">First SkipBlock</span><span class="sxs-lookup"><span data-stu-id="43b4a-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="43b4a-146">Size: Offset 0x39、4 バイト: 0x15 (21)。</span><span class="sxs-lookup"><span data-stu-id="43b4a-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="43b4a-147">コンテンツ: オフセット0x3D 21 バイトの配列。</span><span class="sxs-lookup"><span data-stu-id="43b4a-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="43b4a-148">これは最初の SkipBlock ストリームなので、この配列には FirstSkipBlockContent ストリームが含まれます。</span><span class="sxs-lookup"><span data-stu-id="43b4a-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="43b4a-149">FieldName: オフセット 0x3D PackedUnicodeString ストリーム。</span><span class="sxs-lookup"><span data-stu-id="43b4a-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="43b4a-150">長さ: オフセット0x3D、1 バイト: 0xA (10)。</span><span class="sxs-lookup"><span data-stu-id="43b4a-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="43b4a-151">文字: オフセット0x3E、10 WCHA の配列です。</span><span class="sxs-lookup"><span data-stu-id="43b4a-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="43b4a-152">Unicode 文字列値: "TextField1"</span><span class="sxs-lookup"><span data-stu-id="43b4a-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="43b4a-153">Second SkipBlock</span><span class="sxs-lookup"><span data-stu-id="43b4a-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="43b4a-154">Size: Offset 0x52、4 バイト: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="43b4a-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="43b4a-155">これは終了する SkipBlock ストリームです。</span><span class="sxs-lookup"><span data-stu-id="43b4a-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43b4a-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="43b4a-156">See also</span></span>

- [<span data-ttu-id="43b4a-157">Outlookアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="43b4a-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="43b4a-158">Stream 構造</span><span class="sxs-lookup"><span data-stu-id="43b4a-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="43b4a-159">PropertyDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="43b4a-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="43b4a-160">FieldDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="43b4a-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="43b4a-161">SkipBlock ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="43b4a-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="43b4a-162">FirstSkipBlockContent ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="43b4a-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="43b4a-163">PackedAnsiString ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="43b4a-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="43b4a-164">PackedUnicodeString ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="43b4a-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

