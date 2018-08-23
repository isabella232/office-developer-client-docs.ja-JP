---
title: PidTagDefaultProfile 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a315f1564f2980ad16ce2ba3da2308960f7d4b88
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578893"
---
# <a name="pidtagdefaultprofile-canonical-property"></a><span data-ttu-id="2d301-103">PidTagDefaultProfile 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2d301-103">PidTagDefaultProfile Canonical Property</span></span>

  
  
<span data-ttu-id="2d301-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d301-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d301-105">メッセージング ユーザー プロファイルが既定の MAPI プロファイルの場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="2d301-105">Contains TRUE if a messaging user profile is the MAPI default profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2d301-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2d301-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2d301-107">PR_DEFAULT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="2d301-107">PR_DEFAULT_PROFILE</span></span>  <br/> |
|<span data-ttu-id="2d301-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2d301-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2d301-109">0x3D04</span><span class="sxs-lookup"><span data-stu-id="2d301-109">0x3D04</span></span>  <br/> |
|<span data-ttu-id="2d301-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2d301-110">Data type:</span></span>  <br/> |<span data-ttu-id="2d301-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2d301-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2d301-112">領域:</span><span class="sxs-lookup"><span data-stu-id="2d301-112">Area:</span></span>  <br/> |<span data-ttu-id="2d301-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="2d301-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d301-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2d301-114">Remarks</span></span>

<span data-ttu-id="2d301-115">プロファイル テーブルに列としてのみですが、任意のオブジェクトのプロパティとしては、このプロパティは表示されません。</span><span class="sxs-lookup"><span data-stu-id="2d301-115">This property does not appear as a property of any object but only as a column in a profile table.</span></span> <span data-ttu-id="2d301-116">クライアント アプリケーションは、既定のプロファイルを指定するのには[IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md)メソッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="2d301-116">A client application can use the [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) method to designate the default profile.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2d301-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2d301-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2d301-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2d301-118">Header files</span></span>

<span data-ttu-id="2d301-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d301-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="2d301-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2d301-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="2d301-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2d301-121">Mapitags.h</span></span>
  
> <span data-ttu-id="2d301-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2d301-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d301-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="2d301-123">See also</span></span>



[<span data-ttu-id="2d301-124">PidTagDefaultStore 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2d301-124">PidTagDefaultStore Canonical Property</span></span>](pidtagdefaultstore-canonical-property.md)


[<span data-ttu-id="2d301-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2d301-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2d301-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2d301-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2d301-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2d301-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2d301-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2d301-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

