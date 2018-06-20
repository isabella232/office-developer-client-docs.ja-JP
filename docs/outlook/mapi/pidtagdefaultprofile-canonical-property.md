---
title: PidTagDefaultProfile の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6cd255c60987ec7a279e509aa2925a8029cce62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802649"
---
# <a name="pidtagdefaultprofile-canonical-property"></a><span data-ttu-id="e98fe-103">PidTagDefaultProfile の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e98fe-103">PidTagDefaultProfile Canonical Property</span></span>

  
  
<span data-ttu-id="e98fe-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e98fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e98fe-105">メッセージング ユーザー プロファイルが既定の MAPI プロファイルの場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="e98fe-105">Contains TRUE if a messaging user profile is the MAPI default profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e98fe-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="e98fe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e98fe-107">PR_DEFAULT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="e98fe-107">PR_DEFAULT_PROFILE</span></span>  <br/> |
|<span data-ttu-id="e98fe-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e98fe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e98fe-109">0x3D04</span><span class="sxs-lookup"><span data-stu-id="e98fe-109">0x3D04</span></span>  <br/> |
|<span data-ttu-id="e98fe-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="e98fe-110">Data type:</span></span>  <br/> |<span data-ttu-id="e98fe-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e98fe-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e98fe-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e98fe-112">Area:</span></span>  <br/> |<span data-ttu-id="e98fe-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="e98fe-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e98fe-114">備考</span><span class="sxs-lookup"><span data-stu-id="e98fe-114">Remarks</span></span>

<span data-ttu-id="e98fe-115">プロファイル テーブルに列としてのみですが、任意のオブジェクトのプロパティとしては、このプロパティは表示されません。</span><span class="sxs-lookup"><span data-stu-id="e98fe-115">This property does not appear as a property of any object but only as a column in a profile table.</span></span> <span data-ttu-id="e98fe-116">クライアント アプリケーションは、既定のプロファイルを指定するのには[IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md)メソッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="e98fe-116">A client application can use the [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) method to designate the default profile.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e98fe-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e98fe-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e98fe-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e98fe-118">Header files</span></span>

<span data-ttu-id="e98fe-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e98fe-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="e98fe-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e98fe-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="e98fe-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e98fe-121">Mapitags.h</span></span>
  
> <span data-ttu-id="e98fe-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e98fe-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e98fe-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="e98fe-123">See also</span></span>



[<span data-ttu-id="e98fe-124">PidTagDefaultStore の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e98fe-124">PidTagDefaultStore Canonical Property</span></span>](pidtagdefaultstore-canonical-property.md)


[<span data-ttu-id="e98fe-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e98fe-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e98fe-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e98fe-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e98fe-127">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e98fe-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e98fe-128">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e98fe-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

