---
title: PidTagWizardNoPstPage 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ae1f5b62c59c2e9a1c02c1a2fc0ee91ef1e19387
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562982"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a><span data-ttu-id="4ab98-103">PidTagWizardNoPstPage 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4ab98-103">PidTagWizardNoPstPage Canonical Property</span></span>

  
  
<span data-ttu-id="4ab98-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ab98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ab98-105">このプロパティには、プロファイル ウィザードは、個人メッセージ ストア (PST) のページを非表示にする場合は TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4ab98-105">This property contains TRUE if the profile wizard is to suppress the personal message store (PST) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ab98-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4ab98-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ab98-107">PR_WIZARD_NO_PST_PAGE</span><span class="sxs-lookup"><span data-stu-id="4ab98-107">PR_WIZARD_NO_PST_PAGE</span></span>  <br/> |
|<span data-ttu-id="4ab98-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4ab98-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ab98-109">0x6700</span><span class="sxs-lookup"><span data-stu-id="4ab98-109">0x6700</span></span>  <br/> |
|<span data-ttu-id="4ab98-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4ab98-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ab98-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4ab98-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4ab98-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4ab98-112">Area:</span></span>  <br/> |<span data-ttu-id="4ab98-113">Exchange の管理</span><span class="sxs-lookup"><span data-stu-id="4ab98-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ab98-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4ab98-114">Remarks</span></span>

<span data-ttu-id="4ab98-115">サービス プロバイダーは、 [LAUNCHWIZARDENTRY](launchwizardentry.md)関数のプロトタイプでは関数を呼び出すときにこのプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4ab98-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="4ab98-116">このプロパティは、プロバイダーがユーザー ダイアログ ボックスの中に表示される PST のページをしないことをプロファイル ウィザードに指示します。</span><span class="sxs-lookup"><span data-stu-id="4ab98-116">This property tells the profile wizard that the provider does not want the PST page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4ab98-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4ab98-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4ab98-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4ab98-118">Header files</span></span>

<span data-ttu-id="4ab98-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ab98-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ab98-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4ab98-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ab98-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4ab98-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4ab98-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4ab98-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ab98-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ab98-123">See also</span></span>



[<span data-ttu-id="4ab98-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4ab98-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ab98-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4ab98-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ab98-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4ab98-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ab98-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4ab98-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

