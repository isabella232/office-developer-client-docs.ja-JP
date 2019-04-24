---
title: PidNameRightsManagementLicense 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 889b823a55c39ebc19e52c8cc9a1d078a5732a01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315023"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="f7c16-103">PidNameRightsManagementLicense 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f7c16-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="f7c16-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7c16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7c16-105">権限が管理された電子メールメッセージの使用ライセンスをキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="f7c16-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7c16-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="f7c16-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="f7c16-107">なし</span><span class="sxs-lookup"><span data-stu-id="f7c16-107">None</span></span>  <br/> |
|<span data-ttu-id="f7c16-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="f7c16-108">Property set:</span></span>  <br/> |<span data-ttu-id="f7c16-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="f7c16-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="f7c16-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="f7c16-110">Property name:</span></span>  <br/> |<span data-ttu-id="f7c16-111">drmlicense</span><span class="sxs-lookup"><span data-stu-id="f7c16-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="f7c16-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f7c16-112">Data type:</span></span>  <br/> |<span data-ttu-id="f7c16-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="f7c16-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="f7c16-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="f7c16-114">Area:</span></span>  <br/> |<span data-ttu-id="f7c16-115">セキュリティで保護されたメッセージング</span><span class="sxs-lookup"><span data-stu-id="f7c16-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7c16-116">解説</span><span class="sxs-lookup"><span data-stu-id="f7c16-116">Remarks</span></span>

<span data-ttu-id="f7c16-117">権限が管理された電子メールメッセージにこのプロパティが存在する場合、この複数バイナリプロパティの最初の値には、権限が管理されている電子メールメッセージのために [RFC1950] で指定されている ZLIB が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7c16-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f7c16-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f7c16-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7c16-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f7c16-119">Protocol specifications</span></span>

<span data-ttu-id="f7c16-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7c16-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7c16-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f7c16-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7c16-122">[[OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7c16-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7c16-123">権限が管理されたエンコード済みメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7c16-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7c16-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="f7c16-124">Header files</span></span>

<span data-ttu-id="f7c16-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7c16-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7c16-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f7c16-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7c16-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7c16-127">See also</span></span>



[<span data-ttu-id="f7c16-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f7c16-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7c16-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f7c16-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7c16-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f7c16-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7c16-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f7c16-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

