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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398340"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="696b1-103">PidTagAccess 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="696b1-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="696b1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="696b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="696b1-105">オブジェクトのクライアントに利用可能な操作を示すフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="696b1-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="696b1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="696b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="696b1-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="696b1-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="696b1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="696b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="696b1-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="696b1-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="696b1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="696b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="696b1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="696b1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="696b1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="696b1-112">Area:</span></span>  <br/> |<span data-ttu-id="696b1-113">コントロール プロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="696b1-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="696b1-114">備考</span><span class="sxs-lookup"><span data-stu-id="696b1-114">Remarks</span></span>

<span data-ttu-id="696b1-115">このプロパティは、クライアントに対しては読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="696b1-115">This property is read-only for the client.</span></span> <span data-ttu-id="696b1-116">ビットごと**または**次の表の値を 0 個以上の必要があります。</span><span class="sxs-lookup"><span data-stu-id="696b1-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="696b1-117">**名前**</span><span class="sxs-lookup"><span data-stu-id="696b1-117">**Name**</span></span>|<span data-ttu-id="696b1-118">**値**</span><span class="sxs-lookup"><span data-stu-id="696b1-118">**Value**</span></span>|<span data-ttu-id="696b1-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="696b1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="696b1-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="696b1-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="696b1-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="696b1-121">0x00000001</span></span>  <br/> |<span data-ttu-id="696b1-122">書き込み</span><span class="sxs-lookup"><span data-stu-id="696b1-122">Write</span></span>  <br/> |
|<span data-ttu-id="696b1-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="696b1-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="696b1-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="696b1-124">0x00000002</span></span>  <br/> |<span data-ttu-id="696b1-125">Read</span><span class="sxs-lookup"><span data-stu-id="696b1-125">Read</span></span>  <br/> |
|<span data-ttu-id="696b1-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="696b1-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="696b1-127">0x00000004</span><span class="sxs-lookup"><span data-stu-id="696b1-127">0x00000004</span></span>  <br/> |<span data-ttu-id="696b1-128">削除</span><span class="sxs-lookup"><span data-stu-id="696b1-128">Delete</span></span>  <br/> |
|<span data-ttu-id="696b1-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="696b1-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="696b1-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="696b1-130">0x00000008</span></span>  <br/> |<span data-ttu-id="696b1-131">フォルダー階層のサブフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="696b1-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="696b1-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="696b1-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="696b1-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="696b1-133">0x00000010</span></span>  <br/> |<span data-ttu-id="696b1-134">内容のメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="696b1-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="696b1-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="696b1-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="696b1-136">0x00000020</span><span class="sxs-lookup"><span data-stu-id="696b1-136">0x00000020</span></span>  <br/> |<span data-ttu-id="696b1-137">コンテンツに関連するメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="696b1-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="696b1-138">MAPI_ACCESS_DELETE、MAPI_ACCESS_MODIFY、および MAPI_ACCESS_READ のフラグがあるフォルダーとメッセージのオブジェクトと**PR_ACCESS**列の内容のテーブルと関連付けられている内容のテーブルで。</span><span class="sxs-lookup"><span data-stu-id="696b1-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="696b1-139">Folder オブジェクトだけでは、MAPI_ACCESS_CREATE_ASSOCIATED、MAPI_ACCESS_CREATE_CONTENTS、および MAPI_ACCESS_CREATE_HIERARCHY のフラグが見つかりました。</span><span class="sxs-lookup"><span data-stu-id="696b1-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="696b1-140">関連リソース</span><span class="sxs-lookup"><span data-stu-id="696b1-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="696b1-141">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="696b1-141">Protocol specifications</span></span>

<span data-ttu-id="696b1-142">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="696b1-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="696b1-143">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="696b1-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="696b1-144">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="696b1-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="696b1-145">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="696b1-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="696b1-146">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="696b1-146">Header files</span></span>

<span data-ttu-id="696b1-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="696b1-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="696b1-148">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="696b1-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="696b1-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="696b1-149">Mapitags.h</span></span>
  
> <span data-ttu-id="696b1-150">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="696b1-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="696b1-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="696b1-151">See also</span></span>



[<span data-ttu-id="696b1-152">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="696b1-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="696b1-153">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="696b1-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="696b1-154">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="696b1-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="696b1-155">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="696b1-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

