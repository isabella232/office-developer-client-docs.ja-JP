---
title: PidTagProviderIcon 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425639"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="c5f87-103">PidTagProviderIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c5f87-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="c5f87-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5f87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5f87-105">オンライン状態とオフライン状態の両方の Microsoft Office Outlook ステータス バーに MAPI プロバイダーに表示するカスタム アイコンまたはアイコンを指定する Unicode 文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c5f87-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5f87-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c5f87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5f87-107">PR_PROVIDER_ICON、PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="c5f87-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="c5f87-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c5f87-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5f87-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="c5f87-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="c5f87-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c5f87-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5f87-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c5f87-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c5f87-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c5f87-112">Area:</span></span>  <br/> |<span data-ttu-id="c5f87-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="c5f87-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5f87-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c5f87-114">Remarks</span></span>

<span data-ttu-id="c5f87-115">これらのプロパティは、オンライン状態の MAPI プロバイダーを表すカスタム アイコンを含むリソース ファイルを指定し、必要に応じてオフライン状態の別のカスタム アイコンを指定します。</span><span class="sxs-lookup"><span data-stu-id="c5f87-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="c5f87-116">Outlook常に Unicode 表記でこれらのプロパティを要求します。</span><span class="sxs-lookup"><span data-stu-id="c5f87-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="c5f87-117">たとえば、次のプロパティ値は、Outlook にモジュール mymod32.dll からアイコン ID 1001 を読み込み、そのアイコンをオンライン状態に使用するように指示します `mymod32.dll,#1001` 。</span><span class="sxs-lookup"><span data-stu-id="c5f87-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="c5f87-118">オフライン状態のプロバイダー固有のアイコンは表示されませんので、この場合、標準のオフライン Outlookアイコンがステータス バーで使用されます。</span><span class="sxs-lookup"><span data-stu-id="c5f87-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="c5f87-119">次のプロパティ値は、Outlook に対して、モジュール mymod32.dll からアイコン ID 1001 を読み込み、そのアイコンをオンライン状態に使用し、この同じモジュールからアイコン ID 1002 を読み込み、オフライン状態に使用するように指示します。 `mymod32.dll,#1001,#1002`</span><span class="sxs-lookup"><span data-stu-id="c5f87-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="c5f87-120">ステータス Outlookアイコンは使用されません。</span><span class="sxs-lookup"><span data-stu-id="c5f87-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="c5f87-121">既定では、カスタム アイコンが指定されていない場合、プロバイダーはオンライン状態とオフライン状態Outlook既定のアイコンで表されます。</span><span class="sxs-lookup"><span data-stu-id="c5f87-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="c5f87-122">プロバイダーは、必要に応じて、ステータス バーのアイコンの横に表示する表示名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c5f87-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="c5f87-123">詳細については、「PR_PROVIDER_DISPLAY_NAME_W **(** [PidTagProviderDisplayName)」を参照してください](pidtagproviderdisplayname-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="c5f87-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c5f87-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c5f87-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c5f87-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c5f87-125">Header files</span></span>

<span data-ttu-id="c5f87-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5f87-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5f87-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c5f87-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5f87-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c5f87-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c5f87-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c5f87-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5f87-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="c5f87-130">See also</span></span>



[<span data-ttu-id="c5f87-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c5f87-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5f87-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c5f87-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5f87-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c5f87-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5f87-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c5f87-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

