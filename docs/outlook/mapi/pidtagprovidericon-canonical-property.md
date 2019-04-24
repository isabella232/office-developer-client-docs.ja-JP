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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286461"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="86c5a-103">PidTagProviderIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="86c5a-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="86c5a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86c5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86c5a-105">オンライン状態とオフライン状態の両方で、Microsoft Office Outlook ステータスバーの MAPI プロバイダーに対して表示されるカスタムアイコンまたはアイコンを指定する Unicode 文字列が格納されています。</span><span class="sxs-lookup"><span data-stu-id="86c5a-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86c5a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="86c5a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86c5a-107">PR_PROVIDER_ICON、PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="86c5a-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="86c5a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="86c5a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="86c5a-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="86c5a-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="86c5a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="86c5a-110">Data type:</span></span>  <br/> |<span data-ttu-id="86c5a-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="86c5a-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="86c5a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="86c5a-112">Area:</span></span>  <br/> |<span data-ttu-id="86c5a-113">MAPI メッセージストア</span><span class="sxs-lookup"><span data-stu-id="86c5a-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86c5a-114">解説</span><span class="sxs-lookup"><span data-stu-id="86c5a-114">Remarks</span></span>

<span data-ttu-id="86c5a-115">これらのプロパティは、オンライン状態の MAPI プロバイダーを表すカスタムアイコンを含むリソースファイルを指定します。また、オプションでオフライン状態の別のカスタムアイコンを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="86c5a-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="86c5a-116">Outlook では、これらのプロパティは常に Unicode 表記で要求されます。</span><span class="sxs-lookup"><span data-stu-id="86c5a-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="86c5a-117">たとえば、次のプロパティ値は、Outlook がモジュール mymod32 からアイコン ID 1001 を読み込んで、そのアイコンをオンライン状態`mymod32.dll,#1001`に使用するように指示します。</span><span class="sxs-lookup"><span data-stu-id="86c5a-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="86c5a-118">この場合、オフライン状態のプロバイダー固有のアイコンはないため、ステータスバーには標準の Outlook オフラインアイコンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="86c5a-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="86c5a-119">次のプロパティ値は、Outlook がモジュール mymod32 からアイコン id 1001 をロードして、そのアイコンをオンライン状態で使用するように指示します。また、この同じモジュールからアイコン id 1002 を読み込んで`mymod32.dll,#1001,#1002`オフライン状態に使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="86c5a-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="86c5a-120">ステータスバーでは、Outlook アイコンは使用されません。</span><span class="sxs-lookup"><span data-stu-id="86c5a-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="86c5a-121">既定では、カスタムアイコンが指定されていない場合、プロバイダーは、オンライン状態およびオフライン状態の Outlook の既定のアイコンで表されます。</span><span class="sxs-lookup"><span data-stu-id="86c5a-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="86c5a-122">プロバイダーは、必要に応じて、ステータスバーのアイコンの横に表示される表示名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="86c5a-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="86c5a-123">詳細については、「 **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86c5a-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="86c5a-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="86c5a-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="86c5a-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="86c5a-125">Header files</span></span>

<span data-ttu-id="86c5a-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86c5a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="86c5a-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="86c5a-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="86c5a-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="86c5a-128">Mapitags.h</span></span>
  
> <span data-ttu-id="86c5a-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="86c5a-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86c5a-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="86c5a-130">See also</span></span>



[<span data-ttu-id="86c5a-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="86c5a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86c5a-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="86c5a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86c5a-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="86c5a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86c5a-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="86c5a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

