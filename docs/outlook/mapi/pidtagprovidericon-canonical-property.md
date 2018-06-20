---
title: PidTagProviderIcon の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 92407d56bd095135ac1c6c292aa4b1da4755e93c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803215"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="7bb35-103">PidTagProviderIcon の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7bb35-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="7bb35-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7bb35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7bb35-105">カスタム アイコンまたは MAPI プロバイダーのオンラインとオフラインの両方の状態で Microsoft Office Outlook のステータス バーに表示されるアイコンを指定する Unicode 文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7bb35-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7bb35-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7bb35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7bb35-107">PR_PROVIDER_ICON、PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="7bb35-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="7bb35-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7bb35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7bb35-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="7bb35-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="7bb35-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="7bb35-110">Data type:</span></span>  <br/> |<span data-ttu-id="7bb35-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7bb35-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7bb35-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7bb35-112">Area:</span></span>  <br/> |<span data-ttu-id="7bb35-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="7bb35-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bb35-114">備考</span><span class="sxs-lookup"><span data-stu-id="7bb35-114">Remarks</span></span>

<span data-ttu-id="7bb35-115">これらのプロパティは、オンラインの状態での MAPI プロバイダーを表すカスタム アイコンを含むリソース ファイルを指定し、必要に応じて、オフラインの状態でもう 1 つのカスタム アイコンです。</span><span class="sxs-lookup"><span data-stu-id="7bb35-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="7bb35-116">Outlook は、常に Unicode 表示形式でこれらのプロパティを要求します。</span><span class="sxs-lookup"><span data-stu-id="7bb35-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="7bb35-117">次のプロパティの値がモジュール mymod32.dll から ID 1001 のアイコンを読み込むし、オンライン状態のアイコンを使用するように Outlook に指示するたとえば、: `mymod32.dll,#1001`。</span><span class="sxs-lookup"><span data-stu-id="7bb35-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="7bb35-118">オフライン状態のプロバイダーに固有のアイコンがないため、この例では、ステータス バーの Outlook の標準オフライン アイコンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bb35-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="7bb35-119">次のプロパティの値もオフライン状態に使用する同じモジュールの ID 1002 のアイコンをロードするモジュールの mymod32.dll から ID 1001 のアイコンを読み込むし、オンラインの状態のアイコンを使用する Outlook に指示します。 `mymod32.dll,#1001,#1002`。</span><span class="sxs-lookup"><span data-stu-id="7bb35-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="7bb35-120">ステータス バーに [Outlook] アイコンを使用しません。</span><span class="sxs-lookup"><span data-stu-id="7bb35-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="7bb35-121">既定では、カスタム アイコンを指定しない場合、プロバイダーがオンライン状態とオフライン状態の Outlook の既定のアイコンで表されます。</span><span class="sxs-lookup"><span data-stu-id="7bb35-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="7bb35-122">プロバイダーでは、ステータス バーのアイコンの横に表示される表示名をオプションで指定できます。</span><span class="sxs-lookup"><span data-stu-id="7bb35-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="7bb35-123">詳細については、 **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bb35-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7bb35-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7bb35-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7bb35-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7bb35-125">Header files</span></span>

<span data-ttu-id="7bb35-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7bb35-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7bb35-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7bb35-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7bb35-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7bb35-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7bb35-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7bb35-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7bb35-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="7bb35-130">See also</span></span>



[<span data-ttu-id="7bb35-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7bb35-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7bb35-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7bb35-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7bb35-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7bb35-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7bb35-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7bb35-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

