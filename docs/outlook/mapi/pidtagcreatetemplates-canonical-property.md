---
title: PidTagCreateTemplates の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 82da274670c9266a746defcf6bbd5dbcf621901b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802646"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="cd132-103">PidTagCreateTemplates の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="cd132-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="cd132-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cd132-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cd132-105">ダイアログ ボックス テンプレートのエントリの識別子を格納している埋め込みテーブル オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cd132-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd132-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="cd132-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd132-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="cd132-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="cd132-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cd132-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd132-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="cd132-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="cd132-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="cd132-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd132-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="cd132-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="cd132-112">領域:</span><span class="sxs-lookup"><span data-stu-id="cd132-112">Area:</span></span>  <br/> |<span data-ttu-id="cd132-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="cd132-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd132-114">備考</span><span class="sxs-lookup"><span data-stu-id="cd132-114">Remarks</span></span>

<span data-ttu-id="cd132-115">コンテナーの内部オブジェクトを作成するテンプレートについては、このプロパティの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cd132-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="cd132-116">結果のオブジェクトは、コンテナー内に作成できるテンプレートをすべてのエントリの識別子を提供する一時テーブルです。</span><span class="sxs-lookup"><span data-stu-id="cd132-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="cd132-117">テンプレート オブジェクトを作成するには、一時テーブルから**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) の列の値に、コンテナー オブジェクトの**CreateEntry**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cd132-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cd132-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cd132-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cd132-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="cd132-119">Header files</span></span>

<span data-ttu-id="cd132-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd132-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd132-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cd132-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd132-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cd132-122">Mapitags.h</span></span>
  
> <span data-ttu-id="cd132-123">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cd132-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd132-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd132-124">See also</span></span>



[<span data-ttu-id="cd132-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="cd132-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="cd132-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cd132-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd132-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cd132-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd132-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="cd132-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd132-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="cd132-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

