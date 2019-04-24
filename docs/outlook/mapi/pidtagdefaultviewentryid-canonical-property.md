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
ms.openlocfilehash: 6d284782de86b603e6bbe190931a85cd9196c88b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270015"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a><span data-ttu-id="2a48f-103">PidTagDefaultViewEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2a48f-103">PidTagDefaultViewEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="2a48f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a48f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a48f-105">フォルダーの既定のビューのエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="2a48f-105">Contains the entry identifier of a folder's default view.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a48f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2a48f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a48f-107">PR_DEFAULT_VIEW_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2a48f-107">PR_DEFAULT_VIEW_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="2a48f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2a48f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a48f-109">0x3616</span><span class="sxs-lookup"><span data-stu-id="2a48f-109">0x3616</span></span>  <br/> |
|<span data-ttu-id="2a48f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2a48f-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a48f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2a48f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2a48f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2a48f-112">Area:</span></span>  <br/> |<span data-ttu-id="2a48f-113">MAPI コンテナー</span><span class="sxs-lookup"><span data-stu-id="2a48f-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a48f-114">解説</span><span class="sxs-lookup"><span data-stu-id="2a48f-114">Remarks</span></span>

<span data-ttu-id="2a48f-115">このプロパティは、初期ビューとして設定する必要があるフォルダービューのエントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="2a48f-115">This property is the entry identifier of the folder view that should be set as the initial view.</span></span> <span data-ttu-id="2a48f-116">[標準] ビューを初期ビューとして使用する場合は、プロパティを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2a48f-116">The property need not be set if the "Normal" view is to be used as the initial view.</span></span>
  
<span data-ttu-id="2a48f-117">クライアントアプリケーションは、フォルダーを開いたときにこのプロパティを取得して、パフォーマンスを大幅に向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="2a48f-117">A client application can obtain this property at the time it opens the folder and realize significant performance gains.</span></span> <span data-ttu-id="2a48f-118">このプロパティは、関連する contents テーブルを開かずに制限を送信するのではなく、既定のビューを取得するためのショートカットとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a48f-118">This property can be used as a shortcut to obtain the default view, instead of opening the associated contents table and submitting a restriction.</span></span>
  
<span data-ttu-id="2a48f-119">[imapifolder:: copyfolder](imapifolder-copyfolder.md)メソッドのサービスプロバイダー実装は、フォルダーをコピーするときにこのプロパティをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="2a48f-119">A service provider implementation of the [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) method can copy this property when it copies folders.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2a48f-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2a48f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2a48f-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2a48f-121">Protocol specifications</span></span>

<span data-ttu-id="2a48f-122">[[OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a48f-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a48f-123">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="2a48f-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2a48f-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="2a48f-124">Header files</span></span>

<span data-ttu-id="2a48f-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a48f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a48f-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2a48f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2a48f-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="2a48f-127">Mapitags.h</span></span>
  
> <span data-ttu-id="2a48f-128">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2a48f-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a48f-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a48f-129">See also</span></span>



[<span data-ttu-id="2a48f-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2a48f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a48f-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2a48f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a48f-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2a48f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a48f-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2a48f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

