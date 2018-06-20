---
title: PidTagTextAttachmentCharset の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c728799832b10ad2d4533a9a040582b67054baad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803642"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="26e96-103">PidTagTextAttachmentCharset の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="26e96-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="26e96-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26e96-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26e96-105">メッセージの添付ファイルの文字セットの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="26e96-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26e96-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="26e96-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26e96-107">なし</span><span class="sxs-lookup"><span data-stu-id="26e96-107">None</span></span>  <br/> |
|<span data-ttu-id="26e96-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="26e96-108">Identifier:</span></span>  <br/> |<span data-ttu-id="26e96-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="26e96-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="26e96-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="26e96-110">Data type:</span></span>  <br/> |<span data-ttu-id="26e96-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="26e96-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="26e96-112">領域:</span><span class="sxs-lookup"><span data-stu-id="26e96-112">Area:</span></span>  <br/> |<span data-ttu-id="26e96-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="26e96-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26e96-114">備考</span><span class="sxs-lookup"><span data-stu-id="26e96-114">Remarks</span></span>

<span data-ttu-id="26e96-115">開始されるコンテンツ タイプの MIME ヘッダー フィールドのこのプロパティのデータには"テキストと""charset"パラメーターが存在する場合、します。</span><span class="sxs-lookup"><span data-stu-id="26e96-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="26e96-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="26e96-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="26e96-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="26e96-117">Protocol specifications</span></span>

<span data-ttu-id="26e96-118">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26e96-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26e96-119">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="26e96-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="26e96-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="26e96-120">Header files</span></span>

<span data-ttu-id="26e96-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26e96-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="26e96-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="26e96-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="26e96-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="26e96-123">Mapitags.h</span></span>
  
> <span data-ttu-id="26e96-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="26e96-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26e96-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="26e96-125">See also</span></span>



[<span data-ttu-id="26e96-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="26e96-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26e96-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="26e96-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26e96-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="26e96-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26e96-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="26e96-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

