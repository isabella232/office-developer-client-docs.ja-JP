---
title: PidNameRightsManagementLicense の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c75cb480b9a1a7ffdcff9c0f9b49aabba746fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802372"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="e9d6f-103">PidNameRightsManagementLicense の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e9d6f-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="e9d6f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9d6f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9d6f-105">権限が管理された電子メール メッセージの使用ライセンスをキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="e9d6f-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9d6f-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="e9d6f-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="e9d6f-107">なし</span><span class="sxs-lookup"><span data-stu-id="e9d6f-107">None</span></span>  <br/> |
|<span data-ttu-id="e9d6f-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e9d6f-108">Property set:</span></span>  <br/> |<span data-ttu-id="e9d6f-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="e9d6f-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="e9d6f-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="e9d6f-110">Property name:</span></span>  <br/> |<span data-ttu-id="e9d6f-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="e9d6f-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="e9d6f-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="e9d6f-112">Data type:</span></span>  <br/> |<span data-ttu-id="e9d6f-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="e9d6f-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="e9d6f-114">領域:</span><span class="sxs-lookup"><span data-stu-id="e9d6f-114">Area:</span></span>  <br/> |<span data-ttu-id="e9d6f-115">メッセージのセキュリティ保護します。</span><span class="sxs-lookup"><span data-stu-id="e9d6f-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9d6f-116">備考</span><span class="sxs-lookup"><span data-stu-id="e9d6f-116">Remarks</span></span>

<span data-ttu-id="e9d6f-117">権限が管理された電子メール メッセージのプロパティがある場合、この複数のバイナリ プロパティの最初の値は、([RFC1950] で指定) と同じ ZLIB 圧縮使用ライセンスを権限管理された電子メール メッセージを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9d6f-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e9d6f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e9d6f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9d6f-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e9d6f-119">Protocol specifications</span></span>

<span data-ttu-id="e9d6f-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9d6f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9d6f-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9d6f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9d6f-122">[[MS OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9d6f-122">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9d6f-123">権限管理でエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="e9d6f-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9d6f-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e9d6f-124">Header files</span></span>

<span data-ttu-id="e9d6f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9d6f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9d6f-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9d6f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9d6f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9d6f-127">See also</span></span>



[<span data-ttu-id="e9d6f-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9d6f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9d6f-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9d6f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9d6f-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e9d6f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9d6f-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e9d6f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

