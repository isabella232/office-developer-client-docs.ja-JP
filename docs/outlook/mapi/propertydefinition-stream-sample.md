---
title: propertydefinition ストリームのサンプル
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
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="c3966-103">propertydefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="c3966-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="c3966-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3966-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3966-105">このトピックでは、propertydefinition stream の例について説明します。</span><span class="sxs-lookup"><span data-stu-id="c3966-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="c3966-106">stream には、 `TextField1`ユーザー定義フィールドの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c3966-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="c3966-107">この型は**テキスト**であり、定義は PropDefV2 形式になっています。</span><span class="sxs-lookup"><span data-stu-id="c3966-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="c3966-108">データダンプ</span><span class="sxs-lookup"><span data-stu-id="c3966-108">Data dump</span></span>

<span data-ttu-id="c3966-109">次に示すのは、バイナリエディターに表示されるストリームのデータダンプです。</span><span class="sxs-lookup"><span data-stu-id="c3966-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="c3966-110">ストリームオフセット</span><span class="sxs-lookup"><span data-stu-id="c3966-110">Stream offset</span></span>|<span data-ttu-id="c3966-111">データバイト</span><span class="sxs-lookup"><span data-stu-id="c3966-111">Data bytes</span></span>|<span data-ttu-id="c3966-112">ASCII データ</span><span class="sxs-lookup"><span data-stu-id="c3966-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="c3966-113">次に、propertydefinition ストリームのサンプルデータを解析します。</span><span class="sxs-lookup"><span data-stu-id="c3966-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="c3966-114">バージョン: Offset 0x0、2バイト: 0x0103 (PropDefV2)。</span><span class="sxs-lookup"><span data-stu-id="c3966-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="c3966-115">fielddefinitioncount: Offset 0x2、4バイト: 0x1 (1)。</span><span class="sxs-lookup"><span data-stu-id="c3966-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="c3966-116">fielddefinitions: Offset 0x6、1つの fielddefinitions stream の配列。</span><span class="sxs-lookup"><span data-stu-id="c3966-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="c3966-117">フラグ: オフセット0x6、4バイト: 0x45 (PDO_IS_CUSTOM |PDO_PRINT_SAVEAS |PDO_PRINT_SAVEAS_DEF)</span><span class="sxs-lookup"><span data-stu-id="c3966-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="c3966-118">VT: オフセット0xa、2バイト: 0x8 (**VT_BSTR**)。</span><span class="sxs-lookup"><span data-stu-id="c3966-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="c3966-119">DispId: Offset 0xC、4バイト: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="c3966-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="c3966-120">NmidNameLength: オフセット0x10、2バイト: 0xa (10)。</span><span class="sxs-lookup"><span data-stu-id="c3966-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="c3966-121">nmidname: Offset 0x12、10の wchars の配列。</span><span class="sxs-lookup"><span data-stu-id="c3966-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="c3966-122">Unicode 文字列値: "TextField1"。</span><span class="sxs-lookup"><span data-stu-id="c3966-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="c3966-123">nameansi: Offset 0x26, PackedAnsiString stream。</span><span class="sxs-lookup"><span data-stu-id="c3966-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="c3966-124">長さ: Offset 0x26、1バイト: 0xa (10)。</span><span class="sxs-lookup"><span data-stu-id="c3966-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="c3966-125">文字: Offset 0x27、10文字の配列。</span><span class="sxs-lookup"><span data-stu-id="c3966-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="c3966-126">ANSI 文字列の値: "TextField1"。</span><span class="sxs-lookup"><span data-stu-id="c3966-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="c3966-127">FormulaANSI: オフセット0x31、PackedAnsiString stream。</span><span class="sxs-lookup"><span data-stu-id="c3966-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="c3966-128">長さ: オフセット0x31、1バイト: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="c3966-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="c3966-129">文字: Offset 0x32、0文字の配列。</span><span class="sxs-lookup"><span data-stu-id="c3966-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="c3966-130">空の ANSI 文字列。</span><span class="sxs-lookup"><span data-stu-id="c3966-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="c3966-131">validationruleansi: Offset 0x32、PackedAnsiString stream。</span><span class="sxs-lookup"><span data-stu-id="c3966-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="c3966-132">長さ: Offset 0x32、1バイト: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="c3966-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="c3966-133">文字: Offset 0x33、0文字の配列。</span><span class="sxs-lookup"><span data-stu-id="c3966-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="c3966-134">空の ANSI 文字列。</span><span class="sxs-lookup"><span data-stu-id="c3966-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="c3966-135">validationtextansi: Offset 0x33, PackedAnsiString stream。</span><span class="sxs-lookup"><span data-stu-id="c3966-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="c3966-136">長さ: Offset 0x33、1バイト: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="c3966-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="c3966-137">文字: オフセット0x34、0文字の配列。</span><span class="sxs-lookup"><span data-stu-id="c3966-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="c3966-138">空の ANSI 文字列。</span><span class="sxs-lookup"><span data-stu-id="c3966-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="c3966-139">erroransi: オフセット0x34、PackedAnsiString stream。</span><span class="sxs-lookup"><span data-stu-id="c3966-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="c3966-140">長さ: オフセット0x34、1バイト: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="c3966-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="c3966-141">文字: Offset 0x35、0文字の配列。</span><span class="sxs-lookup"><span data-stu-id="c3966-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="c3966-142">空の ANSI 文字列。</span><span class="sxs-lookup"><span data-stu-id="c3966-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="c3966-143">internaltype: Offset 0x35、4バイト: 0x0 (iTypeString)。</span><span class="sxs-lookup"><span data-stu-id="c3966-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="c3966-144">skipblocks: オフセット0x39、一連の skipblocks ストリーム。</span><span class="sxs-lookup"><span data-stu-id="c3966-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="c3966-145">最初の skipblock</span><span class="sxs-lookup"><span data-stu-id="c3966-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="c3966-146">サイズ: オフセット0x39、4バイト: 0x15 (21)。</span><span class="sxs-lookup"><span data-stu-id="c3966-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="c3966-147">コンテンツ: Offset 0x3d、配列21バイト。</span><span class="sxs-lookup"><span data-stu-id="c3966-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="c3966-148">これは最初の skipblock ストリームなので、この配列には firstskipblockcontent ストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c3966-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="c3966-149">FieldName: Offset 0x3d、PackedUnicodeString stream。</span><span class="sxs-lookup"><span data-stu-id="c3966-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="c3966-150">長さ: Offset 0x3d、1バイト: 0xa (10)。</span><span class="sxs-lookup"><span data-stu-id="c3966-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="c3966-151">文字: オフセット0x3e、10の wchars の配列。</span><span class="sxs-lookup"><span data-stu-id="c3966-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="c3966-152">Unicode 文字列値: "TextField1"。</span><span class="sxs-lookup"><span data-stu-id="c3966-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="c3966-153">2番目の skipblock</span><span class="sxs-lookup"><span data-stu-id="c3966-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="c3966-154">サイズ: オフセット0x52、4バイト: 0x0 (0)。</span><span class="sxs-lookup"><span data-stu-id="c3966-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="c3966-155">これは、終了した skipblock ストリームです。</span><span class="sxs-lookup"><span data-stu-id="c3966-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3966-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="c3966-156">See also</span></span>

- [<span data-ttu-id="c3966-157">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="c3966-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="c3966-158">Stream 構造体</span><span class="sxs-lookup"><span data-stu-id="c3966-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="c3966-159">propertydefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="c3966-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="c3966-160">fielddefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="c3966-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="c3966-161">skipblock ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="c3966-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="c3966-162">firstskipblockcontent ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="c3966-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="c3966-163">PackedAnsiString Stream 構造</span><span class="sxs-lookup"><span data-stu-id="c3966-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="c3966-164">PackedUnicodeString Stream 構造</span><span class="sxs-lookup"><span data-stu-id="c3966-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

