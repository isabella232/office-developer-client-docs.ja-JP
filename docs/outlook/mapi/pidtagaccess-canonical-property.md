---
title: PidTagAccess 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316514"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="90888-103">PidTagAccess 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="90888-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="90888-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90888-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90888-105">オブジェクトに対してクライアントが使用できる操作を示すフラグのビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="90888-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90888-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="90888-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90888-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="90888-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="90888-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="90888-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90888-109">0x0ff4</span><span class="sxs-lookup"><span data-stu-id="90888-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="90888-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="90888-110">Data type:</span></span>  <br/> |<span data-ttu-id="90888-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="90888-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="90888-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="90888-112">Area:</span></span>  <br/> |<span data-ttu-id="90888-113">アクセス制御のプロパティ</span><span class="sxs-lookup"><span data-stu-id="90888-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90888-114">解説</span><span class="sxs-lookup"><span data-stu-id="90888-114">Remarks</span></span>

<span data-ttu-id="90888-115">このプロパティはクライアントに対して値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="90888-115">This property is read-only for the client.</span></span> <span data-ttu-id="90888-116">このパラメーターは、次\*\*\*\* の表の0個以上の値のビット単位の or 演算である必要があります。</span><span class="sxs-lookup"><span data-stu-id="90888-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="90888-117">**名前**</span><span class="sxs-lookup"><span data-stu-id="90888-117">**Name**</span></span>|<span data-ttu-id="90888-118">**値**</span><span class="sxs-lookup"><span data-stu-id="90888-118">**Value**</span></span>|<span data-ttu-id="90888-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="90888-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="90888-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="90888-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="90888-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="90888-121">0x00000001</span></span>  <br/> |<span data-ttu-id="90888-122">書き込み</span><span class="sxs-lookup"><span data-stu-id="90888-122">Write</span></span>  <br/> |
|<span data-ttu-id="90888-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="90888-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="90888-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="90888-124">0x00000002</span></span>  <br/> |<span data-ttu-id="90888-125">読み取り</span><span class="sxs-lookup"><span data-stu-id="90888-125">Read</span></span>  <br/> |
|<span data-ttu-id="90888-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="90888-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="90888-127">0x00000004</span><span class="sxs-lookup"><span data-stu-id="90888-127">0x00000004</span></span>  <br/> |<span data-ttu-id="90888-128">削除</span><span class="sxs-lookup"><span data-stu-id="90888-128">Delete</span></span>  <br/> |
|<span data-ttu-id="90888-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="90888-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="90888-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="90888-130">0x00000008</span></span>  <br/> |<span data-ttu-id="90888-131">フォルダー階層にサブフォルダーを作成する</span><span class="sxs-lookup"><span data-stu-id="90888-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="90888-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="90888-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="90888-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90888-133">0x00000010</span></span>  <br/> |<span data-ttu-id="90888-134">コンテンツメッセージを作成する</span><span class="sxs-lookup"><span data-stu-id="90888-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="90888-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="90888-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="90888-136">0x00000020</span><span class="sxs-lookup"><span data-stu-id="90888-136">0x00000020</span></span>  <br/> |<span data-ttu-id="90888-137">関連するコンテンツメッセージを作成する</span><span class="sxs-lookup"><span data-stu-id="90888-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="90888-138">MAPI_ACCESS_DELETE、MAPI_ACCESS_MODIFY、および MAPI_ACCESS_READ フラグは、フォルダーとメッセージオブジェクト、および contents tables および関連する contents テーブルの**PR_ACCESS**列にあります。</span><span class="sxs-lookup"><span data-stu-id="90888-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="90888-139">MAPI_ACCESS_CREATE_ASSOCIATED、MAPI_ACCESS_CREATE_CONTENTS、および MAPI_ACCESS_CREATE_HIERARCHY フラグは、folder オブジェクトでのみ検出されます。</span><span class="sxs-lookup"><span data-stu-id="90888-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="90888-140">関連リソース</span><span class="sxs-lookup"><span data-stu-id="90888-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90888-141">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="90888-141">Protocol specifications</span></span>

<span data-ttu-id="90888-142">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90888-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90888-143">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="90888-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90888-144">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90888-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90888-145">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="90888-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90888-146">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="90888-146">Header files</span></span>

<span data-ttu-id="90888-147">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90888-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="90888-148">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="90888-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="90888-149">Mapitags</span><span class="sxs-lookup"><span data-stu-id="90888-149">Mapitags.h</span></span>
  
> <span data-ttu-id="90888-150">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="90888-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90888-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="90888-151">See also</span></span>



[<span data-ttu-id="90888-152">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="90888-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90888-153">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="90888-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90888-154">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="90888-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90888-155">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="90888-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

