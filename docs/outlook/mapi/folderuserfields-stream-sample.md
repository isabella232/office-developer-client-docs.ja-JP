---
title: FolderUserFields ストリームのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e5251a619c70221987847830897ba349d63fd9cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433977"
---
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="0bcfc-103">FolderUserFields ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="0bcfc-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="0bcfc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bcfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bcfc-105">このトピックでは、FolderUserFields ストリームの例について説明します。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="0bcfc-106">ストリームには、ユーザー定義フィールドの定義が含まれます  `TextField1` 。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="0bcfc-107">型は **Text** で、FolderUserFields ストリームには FolderUserFieldsAnsi と FolderUserFieldsUnicode パーツの両方が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="0bcfc-108">詳細については、「Folder [Fields Stream Structures」を参照してください](folder-fields-stream-structures.md)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="0bcfc-109">データ ダンプ</span><span class="sxs-lookup"><span data-stu-id="0bcfc-109">Data dump</span></span>

<span data-ttu-id="0bcfc-110">バイナリ エディターに表示されるストリームのデータ ダンプを次に示します。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="0bcfc-111">ストリーム のオフセット</span><span class="sxs-lookup"><span data-stu-id="0bcfc-111">Stream offset</span></span>|<span data-ttu-id="0bcfc-112">データ バイト</span><span class="sxs-lookup"><span data-stu-id="0bcfc-112">Data bytes</span></span>|<span data-ttu-id="0bcfc-113">ASCII データ</span><span class="sxs-lookup"><span data-stu-id="0bcfc-113">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `02 00 00 00 01 00 00 00 0A 00 54 65 78 74 46 69` <br/> | `..........TextFi` <br/> |
| `0000000010` <br/> | `65 6C 64 31 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `eld1).......A...` <br/> |
| `0000000020` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `0000000030` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000040` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000050` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000060` <br/> | `00 00 00 00 00 00 02 00 00 00 01 00 00 00 0A 00` <br/> | `................` <br/> |
| `0000000070` <br/> | `54 00 65 00 78 00 74 00 46 00 69 00 65 00 6C 00` <br/> | `T.e.x.t.F.i.e.l.` <br/> |
| `0000000080` <br/> | `64 00 31 00 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `d.1.).......A...` <br/> |
| `0000000090` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `00000000A0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000B0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000C0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000D0` <br/> | `00 00 00 00 00 00` <br/> | `......` <br/> |
   

<span data-ttu-id="0bcfc-114">**FolderUserFields** ストリームのサンプル データの解析を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="0bcfc-115">FolderUserFieldsAnsi: オフセット 0x0。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="0bcfc-116">FieldDefinitionCount: オフセット 0x0、4 バイト: 0x00000002 (2) です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="0bcfc-117">FieldDefinitions: Offset 0x4、2 つの FolderFieldDefinitionA ストリームの配列。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="0bcfc-118">**最初の配列要素**:</span><span class="sxs-lookup"><span data-stu-id="0bcfc-118">**First array element**:</span></span>
    
    - <span data-ttu-id="0bcfc-119">FieldType: オフセット 0x4、4 バイト: 0x00000001 (ftString)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="0bcfc-120">FieldNameLength: オフセット 0x8、2 バイト: 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="0bcfc-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="0bcfc-121">FieldName: オフセット0xA、10 の CHARs の配列です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="0bcfc-122">ANSI 文字列値: "TextField1"</span><span class="sxs-lookup"><span data-stu-id="0bcfc-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="0bcfc-123">共通: オフセット0x14。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="0bcfc-124">PropSetGuid: オフセット 0x14、16 バイト: {00020329-00000-0000-C000-0000-0000000046} (PS_PUBLIC_STRINGS)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="0bcfc-125">fcapm: オフセット 0x24、4 バイト: 0x80000007 (FCAPM_CAN_EDIT|FCAPM_CAN_SORT|FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="0bcfc-126">dwString: オフセット 0x28、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-127">dwBitmap: オフセット 0x2C、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-128">dwDisplay: オフセット 0x30、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-129">iFmt: オフセット0x34、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-130">wszFormulaLength: オフセット 0x38、2 バイト: 0x0000 (0) です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="0bcfc-131">wszFormula: オフセット0x3A 0 WCHARs の配列です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="0bcfc-132">空の文字列値。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-132">Empty string value.</span></span>
    
    <span data-ttu-id="0bcfc-133">**2 番目の配列要素**:</span><span class="sxs-lookup"><span data-stu-id="0bcfc-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="0bcfc-134">FieldType: オフセット 0x3A、4 バイト: 0x00000000 (ftNone)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="0bcfc-135">FieldNameLength: オフセット 0x3E、2 バイト: 0x0000 (0) です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="0bcfc-136">FieldName: オフセット0x40、0 の CHARs の配列です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="0bcfc-137">空の文字列値。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-137">Empty string value.</span></span>
      
    - <span data-ttu-id="0bcfc-138">共通: オフセット0x40。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="0bcfc-139">PropSetGuid: オフセット 0x40、16 バイト: {00000000-0000-0000-0000-000000000000} (GUID_NULL)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="0bcfc-140">fcapm: オフセット 0x50、4 バイト: 0x00000000 (0)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="0bcfc-141">dwString: オフセット 0x54、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-142">dwBitmap: オフセット 0x58、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-143">dwDisplay: オフセット 0x5C、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-144">iFmt: オフセット0x60、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-145">wszFormulaLength: オフセット 0x64、2 バイト: 0x0000 (0) です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="0bcfc-146">wszFormula: オフセット0x66 0 WCHARs の配列です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="0bcfc-147">空の文字列値。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-147">Empty string value.</span></span>
    
- <span data-ttu-id="0bcfc-148">FolderUserFieldsUnicode: オフセット0x66。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="0bcfc-149">FieldDefinitionCount: オフセット 0x66、4 バイト: 0x00000002 (2)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="0bcfc-150">FieldDefinitions: Offset 0x6A、2 つの FolderFieldDefinitionW ストリームの配列。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="0bcfc-151">**最初の配列要素**:</span><span class="sxs-lookup"><span data-stu-id="0bcfc-151">**First array element**:</span></span>
    
    - <span data-ttu-id="0bcfc-152">FieldType: オフセット 0x6A、4 バイト: 0x00000001 (ftString)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="0bcfc-153">FieldNameLength: オフセット 0x6E、2 バイト: 0x000A (10)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="0bcfc-154">FieldName: オフセット0x70 10 WCHARs の配列です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="0bcfc-155">Unicode 文字列値: "TextField1"</span><span class="sxs-lookup"><span data-stu-id="0bcfc-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="0bcfc-156">共通: オフセット0x84。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="0bcfc-157">PropSetGuid: オフセット 0x84、16 バイト: {00020329-00000-00000-C0000-0000000046} (PS_PUBLIC_STRINGS)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="0bcfc-158">fcapm: オフセット 0x94、4 バイト: 0x80000007 (FCAPM_CAN_EDIT|FCAPM_CAN_SORT|FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="0bcfc-159">dwString: オフセット 0x98、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-160">dwBitmap: オフセット 0x9C、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-161">dwDisplay: オフセット 0xA0、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-162">iFmt: オフセット 0xA4、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-163">wszFormulaLength: オフセット 0xA8、2 バイト: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="0bcfc-164">wszFormula: オフセット0xAA 0 WCHARs の配列です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="0bcfc-165">空の文字列値。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-165">Empty string value.</span></span>
    
    <span data-ttu-id="0bcfc-166">**2 番目の配列要素**:</span><span class="sxs-lookup"><span data-stu-id="0bcfc-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="0bcfc-167">FieldType: オフセット 0xAA、4 バイト: 0x00000000 (ftNone)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="0bcfc-168">FieldNameLength: オフセット 0xAE、2 バイト: 0x0000 (0) です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="0bcfc-169">FieldName: オフセット0xB0 0 WCHARs の配列です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="0bcfc-170">空の文字列値。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-170">Empty string value.</span></span>
      
    - <span data-ttu-id="0bcfc-171">共通: オフセット0xB0。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="0bcfc-172">PropSetGuid: オフセット 0xB0、16 バイト: {00000000-0000-0000-0000-000000000000} (GUID_NULL)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="0bcfc-173">fcapm: オフセット 0xC0、4 バイト: 0x00000000 (0)。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="0bcfc-174">dwString: オフセット 0xC4、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-175">dwBitmap: オフセット 0xC8、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-176">dwDisplay: オフセット 0xCC、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-177">iFmt: オフセット 0xD0、4 バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="0bcfc-178">wszFormulaLength: オフセット 0xD4、2 バイト: 0x0000 (0) です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="0bcfc-179">wszFormula: オフセット0xD6 0 WCHARs の配列です。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="0bcfc-180">空の文字列値。</span><span class="sxs-lookup"><span data-stu-id="0bcfc-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0bcfc-181">関連項目</span><span class="sxs-lookup"><span data-stu-id="0bcfc-181">See also</span></span>

- [<span data-ttu-id="0bcfc-182">Outlookアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="0bcfc-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="0bcfc-183">PropertyDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="0bcfc-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="0bcfc-184">FieldDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="0bcfc-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="0bcfc-185">SkipBlock ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="0bcfc-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="0bcfc-186">FirstSkipBlockContent ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="0bcfc-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="0bcfc-187">PackedAnsiString ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="0bcfc-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="0bcfc-188">PackedUnicodeString ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="0bcfc-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

