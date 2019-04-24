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
ms.openlocfilehash: e816af2ce60b4c06ae14f720cf7c36d58468d09d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350723"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a><span data-ttu-id="7ba9b-103">PidTagWizardNoPstPage 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7ba9b-103">PidTagWizardNoPstPage Canonical Property</span></span>

  
  
<span data-ttu-id="7ba9b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ba9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ba9b-105">プロファイルウィザードで個人用メッセージストア (PST) のページを非表示にする場合は、このプロパティには TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7ba9b-105">This property contains TRUE if the profile wizard is to suppress the personal message store (PST) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7ba9b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7ba9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7ba9b-107">PR_WIZARD_NO_PST_PAGE</span><span class="sxs-lookup"><span data-stu-id="7ba9b-107">PR_WIZARD_NO_PST_PAGE</span></span>  <br/> |
|<span data-ttu-id="7ba9b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7ba9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7ba9b-109">0x6700</span><span class="sxs-lookup"><span data-stu-id="7ba9b-109">0x6700</span></span>  <br/> |
|<span data-ttu-id="7ba9b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7ba9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="7ba9b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7ba9b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7ba9b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7ba9b-112">Area:</span></span>  <br/> |<span data-ttu-id="7ba9b-113">Exchange 管理</span><span class="sxs-lookup"><span data-stu-id="7ba9b-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ba9b-114">解説</span><span class="sxs-lookup"><span data-stu-id="7ba9b-114">Remarks</span></span>

<span data-ttu-id="7ba9b-115">サービスプロバイダーは、 [launchwizardentry](launchwizardentry.md)関数プロトタイプに基づいて関数を呼び出すときに、このプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7ba9b-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="7ba9b-116">このプロパティは、ユーザーダイアログの間、プロバイダーが PST ページを表示しないようにすることを、プロファイルウィザードに通知します。</span><span class="sxs-lookup"><span data-stu-id="7ba9b-116">This property tells the profile wizard that the provider does not want the PST page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7ba9b-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7ba9b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7ba9b-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7ba9b-118">Header files</span></span>

<span data-ttu-id="7ba9b-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7ba9b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="7ba9b-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7ba9b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="7ba9b-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="7ba9b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="7ba9b-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7ba9b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ba9b-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="7ba9b-123">See also</span></span>



[<span data-ttu-id="7ba9b-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7ba9b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7ba9b-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7ba9b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7ba9b-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7ba9b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7ba9b-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7ba9b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

