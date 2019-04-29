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
# <a name="pidtagdefaultprofile-canonical-property"></a><span data-ttu-id="e1bb0-103">PidTagDefaultProfile 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e1bb0-103">PidTagDefaultProfile Canonical Property</span></span>

  
  
<span data-ttu-id="e1bb0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1bb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1bb0-105">メッセージングユーザープロファイルが MAPI の既定のプロファイルの場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e1bb0-105">Contains TRUE if a messaging user profile is the MAPI default profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1bb0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e1bb0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1bb0-107">PR_DEFAULT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="e1bb0-107">PR_DEFAULT_PROFILE</span></span>  <br/> |
|<span data-ttu-id="e1bb0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e1bb0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1bb0-109">0x3d04</span><span class="sxs-lookup"><span data-stu-id="e1bb0-109">0x3D04</span></span>  <br/> |
|<span data-ttu-id="e1bb0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e1bb0-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1bb0-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e1bb0-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e1bb0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e1bb0-112">Area:</span></span>  <br/> |<span data-ttu-id="e1bb0-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="e1bb0-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1bb0-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e1bb0-114">Remarks</span></span>

<span data-ttu-id="e1bb0-115">このプロパティは、オブジェクトのプロパティとして表示されませんが、プロファイルテーブル内の列としてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1bb0-115">This property does not appear as a property of any object but only as a column in a profile table.</span></span> <span data-ttu-id="e1bb0-116">クライアントアプリケーションは[IProfAdmin:: setdefaultprofile](iprofadmin-setdefaultprofile.md)メソッドを使用して、既定のプロファイルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="e1bb0-116">A client application can use the [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) method to designate the default profile.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e1bb0-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e1bb0-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e1bb0-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e1bb0-118">Header files</span></span>

<span data-ttu-id="e1bb0-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1bb0-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1bb0-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e1bb0-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1bb0-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e1bb0-121">Mapitags.h</span></span>
  
> <span data-ttu-id="e1bb0-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e1bb0-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1bb0-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1bb0-123">See also</span></span>



[<span data-ttu-id="e1bb0-124">PidTagDefaultStore 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e1bb0-124">PidTagDefaultStore Canonical Property</span></span>](pidtagdefaultstore-canonical-property.md)


[<span data-ttu-id="e1bb0-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e1bb0-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1bb0-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e1bb0-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1bb0-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e1bb0-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1bb0-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e1bb0-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

