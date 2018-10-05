---
title: PidTagAutoForwarded 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAutoForwarded
api_type:
- HeaderDef
ms.assetid: 1ba40cc2-ba27-4d75-9682-c536cf3a0d58
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 25d1bb121df6470f5038a2106587e3f5b37f6bb7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386363"
---
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="f7123-103">PidTagAutoForwarded 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f7123-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="f7123-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7123-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7123-105">クライアントは、X-MS の Exchange の組織に自動転送されたヘッダー フィールドを要求した場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="f7123-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7123-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f7123-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7123-107">PR_AUTO_FORWARDED</span><span class="sxs-lookup"><span data-stu-id="f7123-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="f7123-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f7123-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7123-109">0x0005</span><span class="sxs-lookup"><span data-stu-id="f7123-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="f7123-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f7123-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7123-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f7123-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f7123-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f7123-112">Area:</span></span>  <br/> |<span data-ttu-id="f7123-113">一般エラー報告</span><span class="sxs-lookup"><span data-stu-id="f7123-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7123-114">備考</span><span class="sxs-lookup"><span data-stu-id="f7123-114">Remarks</span></span>

<span data-ttu-id="f7123-115">このプロパティ false を指定または使用していない、X-MS の Exchange の組織に自動転送されたヘッダー フィールドは作成されません。</span><span class="sxs-lookup"><span data-stu-id="f7123-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f7123-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f7123-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7123-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f7123-117">Protocol specifications</span></span>

<span data-ttu-id="f7123-118">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7123-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7123-119">MS の OXO のプレフィクスの付いたドキュメントで説明されているオブジェクトで使用されている各プロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="f7123-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="f7123-120">[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7123-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7123-121">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="f7123-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7123-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f7123-122">Header files</span></span>

<span data-ttu-id="f7123-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7123-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7123-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f7123-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7123-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7123-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f7123-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f7123-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7123-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7123-127">See also</span></span>



[<span data-ttu-id="f7123-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f7123-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7123-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f7123-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7123-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f7123-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7123-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f7123-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

