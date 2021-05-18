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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ce08ba971662b7f5060e6b24a6d2c5ee1a921d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327966"
---
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="8bc51-103">PidTagAnr 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8bc51-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="8bc51-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bc51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bc51-105">アドレス帳コンテナーのコンテンツ テーブルのプロパティ制限で使用する文字列値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8bc51-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8bc51-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8bc51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8bc51-107">PR_ANR、PR_ANR_A、PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="8bc51-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="8bc51-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8bc51-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8bc51-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="8bc51-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="8bc51-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8bc51-110">Data type:</span></span>  <br/> |<span data-ttu-id="8bc51-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8bc51-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8bc51-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8bc51-112">Area:</span></span>  <br/> |<span data-ttu-id="8bc51-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="8bc51-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bc51-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8bc51-114">Remarks</span></span>

<span data-ttu-id="8bc51-115">これらのプロパティは、どのオブジェクトにも属していない。 [SPropertyRestriction](spropertyrestriction.md) 構造体のアドレス帳プロバイダーによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="8bc51-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="8bc51-116">このプロパティには、アドレス帳コンテナーのコンテンツ テーブルに対してテストして、対応するメッセージ受信者を検索できるあいまいな名前解決 (ANR) 文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8bc51-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="8bc51-117">アドレス帳プロバイダーは、プロバイダー定義の照合アルゴリズムPR_ANRを使用して、コンテンツ テーブル **内のすべての** エントリに対して、PR_ANRおよび関連付けられたプロパティの値と一致します。</span><span class="sxs-lookup"><span data-stu-id="8bc51-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="8bc51-118">この一致で使用される列は、アルゴリズムの一部としてプロバイダーによって選択されます。</span><span class="sxs-lookup"><span data-stu-id="8bc51-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="8bc51-119">**[PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 列が最も一般的に使用されます。**[PR_ACCOUNT** ] ([PidTagAccount](pidtagaccount-canonical-property.md)) 列は、ユーザーの電子メール名が含まれている場合にも便利です。</span><span class="sxs-lookup"><span data-stu-id="8bc51-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="8bc51-120">あいまいな名前解決の詳細については、「アドレス帳の [制限」を参照してください](address-book-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="8bc51-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8bc51-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8bc51-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8bc51-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8bc51-122">Protocol specifications</span></span>

<span data-ttu-id="8bc51-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bc51-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bc51-124">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="8bc51-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8bc51-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bc51-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bc51-126">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8bc51-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8bc51-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8bc51-127">Header files</span></span>

<span data-ttu-id="8bc51-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8bc51-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="8bc51-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8bc51-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="8bc51-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8bc51-130">Mapitags.h</span></span>
  
> <span data-ttu-id="8bc51-131">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8bc51-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8bc51-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="8bc51-132">See also</span></span>



[<span data-ttu-id="8bc51-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="8bc51-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="8bc51-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="8bc51-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="8bc51-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8bc51-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8bc51-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8bc51-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8bc51-137">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8bc51-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8bc51-138">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8bc51-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

