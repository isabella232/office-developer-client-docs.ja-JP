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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326615"
---
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="eea86-103">PidTagAutoForwarded 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eea86-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="eea86-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eea86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eea86-105">クライアントが AutoForwarded ヘッダーフィールドを要求する場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="eea86-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eea86-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="eea86-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eea86-107">PR_AUTO_FORWARDED</span><span class="sxs-lookup"><span data-stu-id="eea86-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="eea86-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="eea86-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eea86-109">0x0005</span><span class="sxs-lookup"><span data-stu-id="eea86-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="eea86-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="eea86-110">Data type:</span></span>  <br/> |<span data-ttu-id="eea86-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="eea86-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="eea86-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="eea86-112">Area:</span></span>  <br/> |<span data-ttu-id="eea86-113">一般的なレポート</span><span class="sxs-lookup"><span data-stu-id="eea86-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eea86-114">解説</span><span class="sxs-lookup"><span data-stu-id="eea86-114">Remarks</span></span>

<span data-ttu-id="eea86-115">このプロパティが FALSE に設定されている場合、または使用されていない場合は、AutoForwarded header フィールドは作成されません。</span><span class="sxs-lookup"><span data-stu-id="eea86-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eea86-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="eea86-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eea86-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="eea86-117">Protocol specifications</span></span>

<span data-ttu-id="eea86-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eea86-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eea86-119">OXO プリフィックス付きのドキュメントで記述されているオブジェクトで使用される各プロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="eea86-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="eea86-120">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eea86-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eea86-121">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="eea86-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eea86-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="eea86-122">Header files</span></span>

<span data-ttu-id="eea86-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eea86-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="eea86-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="eea86-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="eea86-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="eea86-125">Mapitags.h</span></span>
  
> <span data-ttu-id="eea86-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eea86-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eea86-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="eea86-127">See also</span></span>



[<span data-ttu-id="eea86-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="eea86-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eea86-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eea86-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eea86-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eea86-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eea86-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eea86-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

