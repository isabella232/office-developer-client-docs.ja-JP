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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8295ae6904f503ca831a00c1f35ac08596b5358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428775"
---
# <a name="pidtagdefaultprofile-canonical-property"></a><span data-ttu-id="ba708-103">PidTagDefaultProfile 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ba708-103">PidTagDefaultProfile Canonical Property</span></span>

  
  
<span data-ttu-id="ba708-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba708-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba708-105">メッセージング ユーザー プロファイルが MAPI 既定のプロファイルの場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="ba708-105">Contains TRUE if a messaging user profile is the MAPI default profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ba708-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ba708-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ba708-107">PR_DEFAULT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="ba708-107">PR_DEFAULT_PROFILE</span></span>  <br/> |
|<span data-ttu-id="ba708-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ba708-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ba708-109">0x3D04</span><span class="sxs-lookup"><span data-stu-id="ba708-109">0x3D04</span></span>  <br/> |
|<span data-ttu-id="ba708-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ba708-110">Data type:</span></span>  <br/> |<span data-ttu-id="ba708-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ba708-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ba708-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ba708-112">Area:</span></span>  <br/> |<span data-ttu-id="ba708-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="ba708-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba708-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ba708-114">Remarks</span></span>

<span data-ttu-id="ba708-115">このプロパティは、任意のオブジェクトのプロパティとして表示されるのではなく、プロファイル テーブルの列としてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="ba708-115">This property does not appear as a property of any object but only as a column in a profile table.</span></span> <span data-ttu-id="ba708-116">クライアント アプリケーションは [、IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) メソッドを使用して既定のプロファイルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="ba708-116">A client application can use the [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) method to designate the default profile.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ba708-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ba708-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ba708-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ba708-118">Header files</span></span>

<span data-ttu-id="ba708-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ba708-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ba708-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ba708-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ba708-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ba708-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ba708-122">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ba708-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba708-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="ba708-123">See also</span></span>



[<span data-ttu-id="ba708-124">PidTagDefaultStore 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ba708-124">PidTagDefaultStore Canonical Property</span></span>](pidtagdefaultstore-canonical-property.md)


[<span data-ttu-id="ba708-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ba708-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ba708-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ba708-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ba708-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ba708-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ba708-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ba708-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

