---
title: PidTagTextAttachmentCharset 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTextAttachmentCharset
api_type:
- COM
ms.assetid: d347c949-d0c3-4a36-8447-3fa01111cdc1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1db41bc5c7ea71d65d892da520d4258354eb53cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358815"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="e95f2-103">PidTagTextAttachmentCharset 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e95f2-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="e95f2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e95f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e95f2-105">メッセージ添付ファイルの文字セット値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e95f2-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e95f2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e95f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e95f2-107">なし</span><span class="sxs-lookup"><span data-stu-id="e95f2-107">None</span></span>  <br/> |
|<span data-ttu-id="e95f2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e95f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e95f2-109">0x371b</span><span class="sxs-lookup"><span data-stu-id="e95f2-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="e95f2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e95f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="e95f2-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e95f2-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e95f2-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e95f2-112">Area:</span></span>  <br/> |<span data-ttu-id="e95f2-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="e95f2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e95f2-114">解説</span><span class="sxs-lookup"><span data-stu-id="e95f2-114">Remarks</span></span>

<span data-ttu-id="e95f2-115">このプロパティのデータは、"charset" パラメーターが指定されている場合、"text/" で始まるコンテンツタイプの MIME ヘッダーフィールドから派生します。</span><span class="sxs-lookup"><span data-stu-id="e95f2-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e95f2-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e95f2-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e95f2-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e95f2-117">Protocol specifications</span></span>

<span data-ttu-id="e95f2-118">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e95f2-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e95f2-119">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="e95f2-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e95f2-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e95f2-120">Header files</span></span>

<span data-ttu-id="e95f2-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e95f2-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="e95f2-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e95f2-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="e95f2-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e95f2-123">Mapitags.h</span></span>
  
> <span data-ttu-id="e95f2-124">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e95f2-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e95f2-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="e95f2-125">See also</span></span>



[<span data-ttu-id="e95f2-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e95f2-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e95f2-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e95f2-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e95f2-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e95f2-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e95f2-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e95f2-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

