---
title: PidTagAnr 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cc5edf1c93ca94fb9d8cab302ccd8e96373cd94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581945"
---
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="34e0d-103">PidTagAnr 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="34e0d-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="34e0d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34e0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34e0d-105">アドレス帳コンテナーのコンテンツ テーブルのプロパティ制限で使用するための文字列値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="34e0d-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34e0d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="34e0d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="34e0d-107">PR_ANR、PR_ANR_A、PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="34e0d-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="34e0d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="34e0d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="34e0d-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="34e0d-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="34e0d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="34e0d-110">Data type:</span></span>  <br/> |<span data-ttu-id="34e0d-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="34e0d-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="34e0d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="34e0d-112">Area:</span></span>  <br/> |<span data-ttu-id="34e0d-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="34e0d-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34e0d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="34e0d-114">Remarks</span></span>

<span data-ttu-id="34e0d-115">これらのプロパティは、すべてのオブジェクトには属していません。それが[SPropertyRestriction](spropertyrestriction.md)構造体のアドレス帳のプロバイダーによって提供されています。</span><span class="sxs-lookup"><span data-stu-id="34e0d-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="34e0d-116">このプロパティには、対応するメッセージの受信者を検索するのには、アドレス帳コンテナーのコンテンツ テーブルを比較するあいまいな名前解決 (ANR) の文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="34e0d-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="34e0d-117">アドレス帳プロバイダーは、プロバイダーで定義されている一致のアルゴリズムを使用して**PR_ANR**と、内容のテーブル内の全てのエントリに関連付けられたプロパティの値を一致させます。</span><span class="sxs-lookup"><span data-stu-id="34e0d-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="34e0d-118">アルゴリズムの一部として、プロバイダーによっては、この一致で使用されている列が選択されます。</span><span class="sxs-lookup"><span data-stu-id="34e0d-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="34e0d-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) の列が頻繁に使用されます。**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) の列は、ユーザーの電子メール名が含まれている場合にも便利です。</span><span class="sxs-lookup"><span data-stu-id="34e0d-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="34e0d-120">あいまいな名前解決の詳細については、[アドレス帳の制限](address-book-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="34e0d-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="34e0d-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="34e0d-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="34e0d-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="34e0d-122">Protocol specifications</span></span>

<span data-ttu-id="34e0d-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0d-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e0d-124">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="34e0d-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="34e0d-125">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0d-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e0d-126">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="34e0d-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="34e0d-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="34e0d-127">Header files</span></span>

<span data-ttu-id="34e0d-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34e0d-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="34e0d-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="34e0d-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="34e0d-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="34e0d-130">Mapitags.h</span></span>
  
> <span data-ttu-id="34e0d-131">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="34e0d-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34e0d-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="34e0d-132">See also</span></span>



[<span data-ttu-id="34e0d-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="34e0d-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="34e0d-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="34e0d-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="34e0d-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="34e0d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="34e0d-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="34e0d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="34e0d-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="34e0d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="34e0d-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="34e0d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

