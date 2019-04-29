---
title: folderuserfields ストリームのサンプル
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
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="7d99d-103">folderuserfields ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="7d99d-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="7d99d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d99d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d99d-105">このトピックでは、folderuserfields ストリームの例について説明します。</span><span class="sxs-lookup"><span data-stu-id="7d99d-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="7d99d-106">stream には、 `TextField1`ユーザー定義フィールドの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7d99d-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="7d99d-107">この型は**テキスト**であり、folderuserfields ストリームには、folderuserfields ansi と folderuserfields の両方の unicode パーツが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7d99d-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="7d99d-108">詳細については、「[フォルダーフィールドストリームの構造](folder-fields-stream-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d99d-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="7d99d-109">データダンプ</span><span class="sxs-lookup"><span data-stu-id="7d99d-109">Data dump</span></span>

<span data-ttu-id="7d99d-110">次に示すのは、バイナリエディターに表示されるストリームのデータダンプです。</span><span class="sxs-lookup"><span data-stu-id="7d99d-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="7d99d-111">ストリームオフセット</span><span class="sxs-lookup"><span data-stu-id="7d99d-111">Stream offset</span></span>|<span data-ttu-id="7d99d-112">データバイト</span><span class="sxs-lookup"><span data-stu-id="7d99d-112">Data bytes</span></span>|<span data-ttu-id="7d99d-113">ASCII データ</span><span class="sxs-lookup"><span data-stu-id="7d99d-113">ASCII data</span></span>|
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
   

<span data-ttu-id="7d99d-114">次に、 **folderuserfields**ストリームのサンプルデータを解析します。</span><span class="sxs-lookup"><span data-stu-id="7d99d-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="7d99d-115">folderuserフィールド ansi: Offset 0x0。</span><span class="sxs-lookup"><span data-stu-id="7d99d-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="7d99d-116">fielddefinitioncount: Offset 0x0、4バイト: 0x00000002 (2)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="7d99d-117">fielddefinitions: Offset 0x4、配列 2 folderfielddefinitiona streams。</span><span class="sxs-lookup"><span data-stu-id="7d99d-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="7d99d-118">**最初の配列要素**:</span><span class="sxs-lookup"><span data-stu-id="7d99d-118">**First array element**:</span></span>
    
    - <span data-ttu-id="7d99d-119">FieldType: Offset 0x4、4バイト: 0x00000001 (ftstring)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="7d99d-120">FieldNameLength: オフセット0x8、2バイト: 0x000a (10)</span><span class="sxs-lookup"><span data-stu-id="7d99d-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="7d99d-121">FieldName: オフセット0xa、10文字の配列。</span><span class="sxs-lookup"><span data-stu-id="7d99d-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="7d99d-122">ANSI 文字列の値: "TextField1"。</span><span class="sxs-lookup"><span data-stu-id="7d99d-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="7d99d-123">Common: Offset 0x14。</span><span class="sxs-lookup"><span data-stu-id="7d99d-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="7d99d-124">propsetguid: Offset 0x14, 16 バイト: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="7d99d-125">fcapm: Offset 0x24、4バイト: 0x80000007 (FCAPM_CAN_EDIT |FCAPM_CAN_SORT |FCAPM_CAN_GROUP |FCAPM_CAN_EDIT_IN_ITEM)</span><span class="sxs-lookup"><span data-stu-id="7d99d-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="7d99d-126">dwstring: Offset 0x28、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-127">dwbitmap: Offset 0x2C、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-128">dwdisplay: Offset 0x30、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-129">ifmt: オフセット0x34、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-130">wszFormulaLength: オフセット0x38、2バイト: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="7d99d-131">wszFormula: オフセット0x3a、0 wchars の配列。</span><span class="sxs-lookup"><span data-stu-id="7d99d-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="7d99d-132">空の文字列値。</span><span class="sxs-lookup"><span data-stu-id="7d99d-132">Empty string value.</span></span>
    
    <span data-ttu-id="7d99d-133">**2 番目の配列要素**:</span><span class="sxs-lookup"><span data-stu-id="7d99d-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="7d99d-134">FieldType: オフセット0x3a、4バイト: 0x00000000 (ftnone)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="7d99d-135">FieldNameLength: オフセット0x3e、2バイト: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="7d99d-136">FieldName: オフセット0x40、0文字の配列。</span><span class="sxs-lookup"><span data-stu-id="7d99d-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="7d99d-137">空の文字列値。</span><span class="sxs-lookup"><span data-stu-id="7d99d-137">Empty string value.</span></span>
      
    - <span data-ttu-id="7d99d-138">Common: オフセット0x40。</span><span class="sxs-lookup"><span data-stu-id="7d99d-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="7d99d-139">propsetguid: Offset 0x40、16バイト: {00000000-0000-0000-0000-000000000000} (GUID_NULL)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="7d99d-140">fcapm: オフセット0x50、4バイト: 0x00000000 (0)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="7d99d-141">dwstring: Offset 0x54、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-142">dwbitmap: Offset 0x58、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-143">dwdisplay: Offset 0x5C、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-144">ifmt: オフセット0x60、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-145">wszFormulaLength: Offset 0x64、2バイト: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="7d99d-146">wszFormula: オフセット0x66、0 wchars の配列。</span><span class="sxs-lookup"><span data-stu-id="7d99d-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="7d99d-147">空の文字列値。</span><span class="sxs-lookup"><span data-stu-id="7d99d-147">Empty string value.</span></span>
    
- <span data-ttu-id="7d99d-148">folderuserフィールド unicode: Offset 0x66。</span><span class="sxs-lookup"><span data-stu-id="7d99d-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="7d99d-149">fielddefinitioncount: Offset 0x66、4バイト: 0x00000002 (2)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="7d99d-150">fielddefinitions: Offset 0x6a、配列 2 folderfielddefinitionw streams。</span><span class="sxs-lookup"><span data-stu-id="7d99d-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="7d99d-151">**最初の配列要素**:</span><span class="sxs-lookup"><span data-stu-id="7d99d-151">**First array element**:</span></span>
    
    - <span data-ttu-id="7d99d-152">FieldType: Offset 0x6a、4バイト: 0x00000001 (ftstring)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="7d99d-153">FieldNameLength: オフセット0x6e、2バイト: 0x000a (10)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="7d99d-154">FieldName: Offset 0x70、10の wchars の配列。</span><span class="sxs-lookup"><span data-stu-id="7d99d-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="7d99d-155">Unicode 文字列値: "TextField1"。</span><span class="sxs-lookup"><span data-stu-id="7d99d-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="7d99d-156">Common: オフセット0x84。</span><span class="sxs-lookup"><span data-stu-id="7d99d-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="7d99d-157">propsetguid: Offset 0x84、16バイト: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="7d99d-158">fcapm: オフセット0x94、4バイト: 0x80000007 (FCAPM_CAN_EDIT |FCAPM_CAN_SORT |FCAPM_CAN_GROUP |FCAPM_CAN_EDIT_IN_ITEM)</span><span class="sxs-lookup"><span data-stu-id="7d99d-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="7d99d-159">dwstring: Offset 0x98、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-160">dwbitmap: オフセット0x9c、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-161">dwdisplay: Offset 0xa0、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-162">ifmt: Offset 0xa4、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-163">wszFormulaLength: Offset 0xa8、2バイト: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="7d99d-164">wszFormula: Offset 0xaa、配列 0 wchars。</span><span class="sxs-lookup"><span data-stu-id="7d99d-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="7d99d-165">空の文字列値。</span><span class="sxs-lookup"><span data-stu-id="7d99d-165">Empty string value.</span></span>
    
    <span data-ttu-id="7d99d-166">**2 番目の配列要素**:</span><span class="sxs-lookup"><span data-stu-id="7d99d-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="7d99d-167">FieldType: Offset 0xaa、4バイト: 0x00000000 (ftnone)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="7d99d-168">FieldNameLength: Offset 0xae、2バイト: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="7d99d-169">FieldName: オフセット0xb0、0 wchars の配列。</span><span class="sxs-lookup"><span data-stu-id="7d99d-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="7d99d-170">空の文字列値。</span><span class="sxs-lookup"><span data-stu-id="7d99d-170">Empty string value.</span></span>
      
    - <span data-ttu-id="7d99d-171">Common: オフセット0xb0。</span><span class="sxs-lookup"><span data-stu-id="7d99d-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="7d99d-172">propsetguid: Offset 0xb0、16バイト: {00000000-0000-0000-0000-000000000000} (GUID_NULL)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="7d99d-173">fcapm: Offset 0xC0、4バイト: 0x00000000 (0)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="7d99d-174">dwstring: Offset 0xc4、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-175">dwbitmap: Offset 0xc8、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-176">dwdisplay: Offset 0xcc、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-177">ifmt: Offset 0xD0、4バイト: 0x00000000。</span><span class="sxs-lookup"><span data-stu-id="7d99d-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="7d99d-178">wszFormulaLength: Offset 0xD4、2バイト: 0x0000 (0)。</span><span class="sxs-lookup"><span data-stu-id="7d99d-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="7d99d-179">wszFormula: Offset 0xD6、0 wchars の配列。</span><span class="sxs-lookup"><span data-stu-id="7d99d-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="7d99d-180">空の文字列値。</span><span class="sxs-lookup"><span data-stu-id="7d99d-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d99d-181">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d99d-181">See also</span></span>

- [<span data-ttu-id="7d99d-182">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="7d99d-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="7d99d-183">propertydefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="7d99d-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="7d99d-184">fielddefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="7d99d-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="7d99d-185">skipblock ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="7d99d-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="7d99d-186">firstskipblockcontent ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="7d99d-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="7d99d-187">PackedAnsiString Stream 構造</span><span class="sxs-lookup"><span data-stu-id="7d99d-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="7d99d-188">PackedUnicodeString Stream 構造</span><span class="sxs-lookup"><span data-stu-id="7d99d-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

