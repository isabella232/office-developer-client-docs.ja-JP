---
title: PidTagDefaultViewEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2c941ea43a19b51e46c00b37aa89f504c55f180a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587209"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a><span data-ttu-id="1a1ed-103">PidTagDefaultViewEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a1ed-103">PidTagDefaultViewEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1a1ed-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a1ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a1ed-105">フォルダーの既定のビューのエントリの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a1ed-105">Contains the entry identifier of a folder's default view.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a1ed-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1a1ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a1ed-107">PR_DEFAULT_VIEW_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1a1ed-107">PR_DEFAULT_VIEW_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1a1ed-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1a1ed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a1ed-109">0x3616</span><span class="sxs-lookup"><span data-stu-id="1a1ed-109">0x3616</span></span>  <br/> |
|<span data-ttu-id="1a1ed-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1a1ed-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a1ed-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1a1ed-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1a1ed-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1a1ed-112">Area:</span></span>  <br/> |<span data-ttu-id="1a1ed-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="1a1ed-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a1ed-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1a1ed-114">Remarks</span></span>

<span data-ttu-id="1a1ed-115">このプロパティは、最初のビューとして設定するフォルダー ビューのエントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="1a1ed-115">This property is the entry identifier of the folder view that should be set as the initial view.</span></span> <span data-ttu-id="1a1ed-116">「標準」ビューの最初のビューとして使用する場合、プロパティを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1a1ed-116">The property need not be set if the "Normal" view is to be used as the initial view.</span></span>
  
<span data-ttu-id="1a1ed-117">クライアント アプリケーションでは、フォルダーを開いた時にこのプロパティを取得でき、大幅なパフォーマンス向上を実現することができます。</span><span class="sxs-lookup"><span data-stu-id="1a1ed-117">A client application can obtain this property at the time it opens the folder and realize significant performance gains.</span></span> <span data-ttu-id="1a1ed-118">このプロパティは、コンテンツが関連付けられているテーブルを開くと、制限を送信するのではなく、既定のビューを取得するのにはショートカットとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="1a1ed-118">This property can be used as a shortcut to obtain the default view, instead of opening the associated contents table and submitting a restriction.</span></span>
  
<span data-ttu-id="1a1ed-119">サービス プロバイダーの[IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)メソッドの実装は、フォルダーにコピーする際、このプロパティをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="1a1ed-119">A service provider implementation of the [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) method can copy this property when it copies folders.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1a1ed-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1a1ed-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a1ed-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1a1ed-121">Protocol specifications</span></span>

<span data-ttu-id="1a1ed-122">[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a1ed-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a1ed-123">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="1a1ed-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a1ed-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1a1ed-124">Header files</span></span>

<span data-ttu-id="1a1ed-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a1ed-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a1ed-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1a1ed-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a1ed-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1a1ed-127">Mapitags.h</span></span>
  
> <span data-ttu-id="1a1ed-128">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a1ed-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a1ed-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a1ed-129">See also</span></span>



[<span data-ttu-id="1a1ed-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a1ed-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a1ed-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a1ed-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a1ed-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1a1ed-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a1ed-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1a1ed-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

