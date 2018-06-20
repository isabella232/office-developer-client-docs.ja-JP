---
title: PidTagWizardNoPstPage の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b94e1f2d66f89d680cc738968342de0fbcee5cda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19803670"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a><span data-ttu-id="cc3a2-103">PidTagWizardNoPstPage の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="cc3a2-103">PidTagWizardNoPstPage Canonical Property</span></span>

  
  
<span data-ttu-id="cc3a2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cc3a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cc3a2-105">このプロパティには、プロファイル ウィザードは、個人メッセージ ストア (PST) のページを非表示にする場合は TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cc3a2-105">This property contains TRUE if the profile wizard is to suppress the personal message store (PST) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc3a2-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="cc3a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc3a2-107">PR_WIZARD_NO_PST_PAGE</span><span class="sxs-lookup"><span data-stu-id="cc3a2-107">PR_WIZARD_NO_PST_PAGE</span></span>  <br/> |
|<span data-ttu-id="cc3a2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cc3a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc3a2-109">0x6700</span><span class="sxs-lookup"><span data-stu-id="cc3a2-109">0x6700</span></span>  <br/> |
|<span data-ttu-id="cc3a2-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="cc3a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc3a2-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="cc3a2-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="cc3a2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="cc3a2-112">Area:</span></span>  <br/> |<span data-ttu-id="cc3a2-113">Exchange の管理</span><span class="sxs-lookup"><span data-stu-id="cc3a2-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc3a2-114">備考</span><span class="sxs-lookup"><span data-stu-id="cc3a2-114">Remarks</span></span>

<span data-ttu-id="cc3a2-115">サービス プロバイダーは、 [LAUNCHWIZARDENTRY](launchwizardentry.md)関数のプロトタイプでは関数を呼び出すときにこのプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cc3a2-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="cc3a2-116">このプロパティは、プロバイダーがユーザー ダイアログ ボックスの中に表示される PST のページをしないことをプロファイル ウィザードに指示します。</span><span class="sxs-lookup"><span data-stu-id="cc3a2-116">This property tells the profile wizard that the provider does not want the PST page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cc3a2-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cc3a2-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cc3a2-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="cc3a2-118">Header files</span></span>

<span data-ttu-id="cc3a2-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc3a2-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc3a2-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cc3a2-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc3a2-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cc3a2-121">Mapitags.h</span></span>
  
> <span data-ttu-id="cc3a2-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cc3a2-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc3a2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="cc3a2-123">See also</span></span>



[<span data-ttu-id="cc3a2-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cc3a2-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc3a2-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cc3a2-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc3a2-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="cc3a2-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc3a2-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="cc3a2-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

