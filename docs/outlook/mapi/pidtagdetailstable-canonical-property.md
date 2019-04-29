---
title: PidTagDetailsTable 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419255"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="629f2-103">PidTagDetailsTable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="629f2-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="629f2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="629f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="629f2-105">埋め込みの表示テーブルオブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="629f2-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="629f2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="629f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="629f2-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="629f2-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="629f2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="629f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="629f2-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="629f2-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="629f2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="629f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="629f2-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="629f2-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="629f2-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="629f2-112">Area:</span></span>  <br/> |<span data-ttu-id="629f2-113">MAPI コンテナー</span><span class="sxs-lookup"><span data-stu-id="629f2-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="629f2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="629f2-114">Remarks</span></span>

<span data-ttu-id="629f2-115">このプロパティを、オブジェクトの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドに渡すと、表示テーブルを作成できる[IMAPITable](imapitableiunknown.md)インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="629f2-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="629f2-116">MAPI では、このテーブルを使用して、 [IAddrBook::D etails](iaddrbook-details.md)呼び出しへの応答として、アドレス帳オブジェクトのプロパティシートを表示します。</span><span class="sxs-lookup"><span data-stu-id="629f2-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="629f2-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="629f2-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="629f2-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="629f2-118">Header files</span></span>

<span data-ttu-id="629f2-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="629f2-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="629f2-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="629f2-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="629f2-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="629f2-121">Mapitags.h</span></span>
  
> <span data-ttu-id="629f2-122">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="629f2-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="629f2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="629f2-123">See also</span></span>



[<span data-ttu-id="629f2-124">PidTagCreateTemplates 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="629f2-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="629f2-125">PidTagSearch 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="629f2-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="629f2-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="629f2-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="629f2-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="629f2-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="629f2-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="629f2-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="629f2-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="629f2-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

