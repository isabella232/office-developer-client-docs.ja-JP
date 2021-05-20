---
title: PidTagCreateTemplates 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438184"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="2ccb5-103">PidTagCreateTemplates 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ccb5-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="2ccb5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ccb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ccb5-105">ダイアログ ボックス テンプレートエントリ識別子を含む埋め込みテーブル オブジェクトが含まれる。</span><span class="sxs-lookup"><span data-stu-id="2ccb5-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ccb5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2ccb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ccb5-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="2ccb5-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="2ccb5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2ccb5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ccb5-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="2ccb5-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="2ccb5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2ccb5-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ccb5-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="2ccb5-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="2ccb5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2ccb5-112">Area:</span></span>  <br/> |<span data-ttu-id="2ccb5-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="2ccb5-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ccb5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2ccb5-114">Remarks</span></span>

<span data-ttu-id="2ccb5-115">コンテナー内に作成できるテンプレート オブジェクトを確認するには、このプロパティの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2ccb5-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="2ccb5-116">結果のオブジェクトは、コンテナー内に作成できるすべてのテンプレートのエントリ識別子を与える 1 回きりテーブルです。</span><span class="sxs-lookup"><span data-stu-id="2ccb5-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="2ccb5-117">テンプレート オブジェクトを作成するには、コンテナー オブジェクトの **CreateEntry** メソッド **を PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 列の値を 1 回のテーブルから呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2ccb5-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ccb5-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2ccb5-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2ccb5-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2ccb5-119">Header files</span></span>

<span data-ttu-id="2ccb5-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ccb5-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ccb5-121">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ccb5-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ccb5-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ccb5-122">Mapitags.h</span></span>
  
> <span data-ttu-id="2ccb5-123">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="2ccb5-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ccb5-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ccb5-124">See also</span></span>



[<span data-ttu-id="2ccb5-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="2ccb5-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="2ccb5-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2ccb5-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ccb5-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ccb5-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ccb5-128">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2ccb5-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ccb5-129">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2ccb5-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

