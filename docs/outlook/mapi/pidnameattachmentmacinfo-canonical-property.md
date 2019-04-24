---
title: PidNameAttachmentMacInfo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAttachmentMacInfo
api_type:
- COM
ms.assetid: c46656d5-2cb1-45eb-9f66-9c2b6e3315cf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d2a7fcf06c4e09f46c0d50f9e5f8897874c5f9a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360929"
---
# <a name="pidnameattachmentmacinfo-canonical-property"></a><span data-ttu-id="405fc-103">PidNameAttachmentMacInfo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="405fc-103">PidNameAttachmentMacInfo Canonical Property</span></span>

  
  
<span data-ttu-id="405fc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="405fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="405fc-105">Macintosh ベースの電子メールクライアントによって使用される適切なヘッダーとリソースフォークデータから成る [RFC3282] 添付ファイルの値を格納します。</span><span class="sxs-lookup"><span data-stu-id="405fc-105">Contains an [RFC3282] attachment value that is comprised of appropriate header and resource fork data used by Macintosh-based email clients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="405fc-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="405fc-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="405fc-107">なし</span><span class="sxs-lookup"><span data-stu-id="405fc-107">None</span></span>  <br/> |
|<span data-ttu-id="405fc-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="405fc-108">Property set:</span></span>  <br/> |<span data-ttu-id="405fc-109">PSETID_Attachment</span><span class="sxs-lookup"><span data-stu-id="405fc-109">PSETID_Attachment</span></span>  <br/> |
|<span data-ttu-id="405fc-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="405fc-110">Property name:</span></span>  <br/> |<span data-ttu-id="405fc-111">attachmentmacinfo</span><span class="sxs-lookup"><span data-stu-id="405fc-111">AttachmentMacInfo</span></span>  <br/> |
|<span data-ttu-id="405fc-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="405fc-112">Data type:</span></span>  <br/> |<span data-ttu-id="405fc-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="405fc-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="405fc-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="405fc-114">Area:</span></span>  <br/> |<span data-ttu-id="405fc-115">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="405fc-115">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="405fc-116">解説</span><span class="sxs-lookup"><span data-stu-id="405fc-116">Remarks</span></span>

<span data-ttu-id="405fc-117">詳細については、「OXCMAIL section 2.2.4.2 Apple ファイル形式」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="405fc-117">For more information, see MS-OXCMAIL section 2.2.4.2 Apple File Formats.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="405fc-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="405fc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="405fc-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="405fc-119">Protocol specifications</span></span>

<span data-ttu-id="405fc-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="405fc-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="405fc-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="405fc-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="405fc-122">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="405fc-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="405fc-123">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="405fc-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="405fc-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="405fc-124">Header files</span></span>

<span data-ttu-id="405fc-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="405fc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="405fc-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="405fc-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="405fc-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="405fc-127">See also</span></span>



[<span data-ttu-id="405fc-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="405fc-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="405fc-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="405fc-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="405fc-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="405fc-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="405fc-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="405fc-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

