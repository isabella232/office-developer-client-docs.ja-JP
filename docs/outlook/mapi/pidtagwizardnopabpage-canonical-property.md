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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fc971be76dbaa83176f207411f9f125ffee386cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424463"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a><span data-ttu-id="19d20-103">PidTagWizardNoPabPage 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="19d20-103">PidTagWizardNoPabPage Canonical Property</span></span>

  
  
<span data-ttu-id="19d20-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19d20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19d20-105">プロファイル ウィザードが個人用アドレス帳 (PAB) ページを非表示にしている場合、このプロパティには TRUE が含まれる。</span><span class="sxs-lookup"><span data-stu-id="19d20-105">This property contains TRUE if the profile wizard is to suppress the personal address book (PAB) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19d20-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="19d20-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19d20-107">PR_WIZARD_NO_PAB_PAGE</span><span class="sxs-lookup"><span data-stu-id="19d20-107">PR_WIZARD_NO_PAB_PAGE</span></span>  <br/> |
|<span data-ttu-id="19d20-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="19d20-108">Identifier:</span></span>  <br/> |<span data-ttu-id="19d20-109">0x6701</span><span class="sxs-lookup"><span data-stu-id="19d20-109">0x6701</span></span>  <br/> |
|<span data-ttu-id="19d20-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="19d20-110">Data type:</span></span>  <br/> |<span data-ttu-id="19d20-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="19d20-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="19d20-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="19d20-112">Area:</span></span>  <br/> |<span data-ttu-id="19d20-113">Exchange管理</span><span class="sxs-lookup"><span data-stu-id="19d20-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19d20-114">注釈</span><span class="sxs-lookup"><span data-stu-id="19d20-114">Remarks</span></span>

<span data-ttu-id="19d20-115">サービス プロバイダーは [、LAUNCHWIZARDENTRY](launchwizardentry.md) 関数プロトタイプに基づいて関数を呼び出す場合に、このプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="19d20-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="19d20-116">このプロパティは、プロバイダーがユーザー ダイアログの間に PAB ページを表示したくないとプロファイル ウィザードに指示します。</span><span class="sxs-lookup"><span data-stu-id="19d20-116">This property tells the profile wizard that the provider does not want the PAB page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="19d20-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="19d20-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="19d20-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="19d20-118">Header files</span></span>

<span data-ttu-id="19d20-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19d20-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="19d20-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="19d20-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="19d20-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="19d20-121">Mapitags.h</span></span>
  
> <span data-ttu-id="19d20-122">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="19d20-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19d20-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="19d20-123">See also</span></span>



[<span data-ttu-id="19d20-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="19d20-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19d20-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="19d20-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19d20-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="19d20-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19d20-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="19d20-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

