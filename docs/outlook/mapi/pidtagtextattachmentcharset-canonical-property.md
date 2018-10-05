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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401539"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="49576-103">PidTagTextAttachmentCharset 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="49576-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="49576-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49576-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49576-105">メッセージの添付ファイルの文字セットの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="49576-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49576-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="49576-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49576-107">なし</span><span class="sxs-lookup"><span data-stu-id="49576-107">None</span></span>  <br/> |
|<span data-ttu-id="49576-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="49576-108">Identifier:</span></span>  <br/> |<span data-ttu-id="49576-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="49576-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="49576-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="49576-110">Data type:</span></span>  <br/> |<span data-ttu-id="49576-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="49576-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="49576-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="49576-112">Area:</span></span>  <br/> |<span data-ttu-id="49576-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="49576-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49576-114">備考</span><span class="sxs-lookup"><span data-stu-id="49576-114">Remarks</span></span>

<span data-ttu-id="49576-115">開始されるコンテンツ タイプの MIME ヘッダー フィールドのこのプロパティのデータには"テキストと""charset"パラメーターが存在する場合、します。</span><span class="sxs-lookup"><span data-stu-id="49576-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="49576-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="49576-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49576-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="49576-117">Protocol specifications</span></span>

<span data-ttu-id="49576-118">[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49576-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49576-119">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="49576-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49576-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="49576-120">Header files</span></span>

<span data-ttu-id="49576-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49576-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="49576-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="49576-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="49576-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="49576-123">Mapitags.h</span></span>
  
> <span data-ttu-id="49576-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="49576-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49576-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="49576-125">See also</span></span>



[<span data-ttu-id="49576-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="49576-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49576-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="49576-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49576-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="49576-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49576-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="49576-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

