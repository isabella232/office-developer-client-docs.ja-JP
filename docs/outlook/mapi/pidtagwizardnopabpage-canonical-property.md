---
title: PidTagWizardNoPabPage 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPabPage
api_type:
- COM
ms.assetid: 9cec22cd-798d-41f6-9ebd-c7354f2162c2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b393155d00b47fa8cce23c1b5ac7043237a58983
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803689"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a><span data-ttu-id="9d318-103">PidTagWizardNoPabPage 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d318-103">PidTagWizardNoPabPage Canonical Property</span></span>

  
  
<span data-ttu-id="9d318-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d318-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d318-105">このプロパティには、プロファイル ウィザードでは、個人用アドレス帳 (PAB) のページを非表示にする場合は TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d318-105">This property contains TRUE if the profile wizard is to suppress the personal address book (PAB) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d318-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9d318-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d318-107">PR_WIZARD_NO_PAB_PAGE</span><span class="sxs-lookup"><span data-stu-id="9d318-107">PR_WIZARD_NO_PAB_PAGE</span></span>  <br/> |
|<span data-ttu-id="9d318-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9d318-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d318-109">0x6701</span><span class="sxs-lookup"><span data-stu-id="9d318-109">0x6701</span></span>  <br/> |
|<span data-ttu-id="9d318-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9d318-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d318-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9d318-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9d318-112">領域:</span><span class="sxs-lookup"><span data-stu-id="9d318-112">Area:</span></span>  <br/> |<span data-ttu-id="9d318-113">Exchange の管理</span><span class="sxs-lookup"><span data-stu-id="9d318-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d318-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9d318-114">Remarks</span></span>

<span data-ttu-id="9d318-115">サービス プロバイダーは、 [LAUNCHWIZARDENTRY](launchwizardentry.md)関数のプロトタイプでは関数を呼び出すときにこのプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9d318-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="9d318-116">このプロパティは、プロバイダーがユーザー ダイアログ ボックスの中に表示される個人用アドレス帳ページをしないことをプロファイル ウィザードに指示します。</span><span class="sxs-lookup"><span data-stu-id="9d318-116">This property tells the profile wizard that the provider does not want the PAB page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9d318-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9d318-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9d318-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9d318-118">Header files</span></span>

<span data-ttu-id="9d318-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d318-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d318-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d318-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d318-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9d318-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9d318-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d318-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d318-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d318-123">See also</span></span>



[<span data-ttu-id="9d318-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d318-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d318-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d318-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d318-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9d318-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d318-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9d318-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

