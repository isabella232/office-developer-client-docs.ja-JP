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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316514"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="f2293-103">PidTagAccess 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2293-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="f2293-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2293-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2293-105">オブジェクトのクライアントで使用できる操作を示すフラグのビットマスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f2293-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2293-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f2293-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2293-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f2293-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="f2293-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f2293-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f2293-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="f2293-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="f2293-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f2293-110">Data type:</span></span>  <br/> |<span data-ttu-id="f2293-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f2293-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f2293-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f2293-112">Area:</span></span>  <br/> |<span data-ttu-id="f2293-113">アクセス制御のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f2293-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2293-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f2293-114">Remarks</span></span>

<span data-ttu-id="f2293-115">このプロパティは、クライアントの読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="f2293-115">This property is read-only for the client.</span></span> <span data-ttu-id="f2293-116">次の表の 0 以上の値のビット形式 **の OR** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2293-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="f2293-117">**名前**</span><span class="sxs-lookup"><span data-stu-id="f2293-117">**Name**</span></span>|<span data-ttu-id="f2293-118">**値**</span><span class="sxs-lookup"><span data-stu-id="f2293-118">**Value**</span></span>|<span data-ttu-id="f2293-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="f2293-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f2293-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f2293-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="f2293-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f2293-121">0x00000001</span></span>  <br/> |<span data-ttu-id="f2293-122">書き込み</span><span class="sxs-lookup"><span data-stu-id="f2293-122">Write</span></span>  <br/> |
|<span data-ttu-id="f2293-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="f2293-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="f2293-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f2293-124">0x00000002</span></span>  <br/> |<span data-ttu-id="f2293-125">Read</span><span class="sxs-lookup"><span data-stu-id="f2293-125">Read</span></span>  <br/> |
|<span data-ttu-id="f2293-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="f2293-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="f2293-127">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f2293-127">0x00000004</span></span>  <br/> |<span data-ttu-id="f2293-128">削除</span><span class="sxs-lookup"><span data-stu-id="f2293-128">Delete</span></span>  <br/> |
|<span data-ttu-id="f2293-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="f2293-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="f2293-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f2293-130">0x00000008</span></span>  <br/> |<span data-ttu-id="f2293-131">フォルダー階層にサブフォルダーを作成する</span><span class="sxs-lookup"><span data-stu-id="f2293-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="f2293-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="f2293-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="f2293-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2293-133">0x00000010</span></span>  <br/> |<span data-ttu-id="f2293-134">コンテンツ メッセージの作成</span><span class="sxs-lookup"><span data-stu-id="f2293-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="f2293-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="f2293-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="f2293-136">0x00000020</span><span class="sxs-lookup"><span data-stu-id="f2293-136">0x00000020</span></span>  <br/> |<span data-ttu-id="f2293-137">関連付けられたコンテンツ メッセージを作成する</span><span class="sxs-lookup"><span data-stu-id="f2293-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="f2293-138">フォルダー MAPI_ACCESS_DELETE、MAPI_ACCESS_MODIFY、MAPI_ACCESS_READ の各フラグは、フォルダーオブジェクトとメッセージ オブジェクト、およびコンテンツ テーブルおよび関連するコンテンツ テーブルの **PR_ACCESS** 列にあります。</span><span class="sxs-lookup"><span data-stu-id="f2293-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="f2293-139">フォルダー MAPI_ACCESS_CREATE_ASSOCIATED、MAPI_ACCESS_CREATE_CONTENTS、MAPI_ACCESS_CREATE_HIERARCHYフラグは、フォルダー オブジェクトでのみ検出されます。</span><span class="sxs-lookup"><span data-stu-id="f2293-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f2293-140">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f2293-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f2293-141">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f2293-141">Protocol specifications</span></span>

<span data-ttu-id="f2293-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2293-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2293-143">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="f2293-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f2293-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2293-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2293-145">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="f2293-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f2293-146">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f2293-146">Header files</span></span>

<span data-ttu-id="f2293-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2293-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2293-148">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f2293-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="f2293-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f2293-149">Mapitags.h</span></span>
  
> <span data-ttu-id="f2293-150">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f2293-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2293-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2293-151">See also</span></span>



[<span data-ttu-id="f2293-152">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f2293-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2293-153">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2293-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2293-154">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f2293-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2293-155">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f2293-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

