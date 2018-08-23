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
ms.openlocfilehash: 1f528332c52664ac472670566c905d36dac65bfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565530"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="8f341-103">PidNameRightsManagementLicense 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8f341-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="8f341-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f341-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f341-105">権限が管理された電子メール メッセージの使用ライセンスをキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="8f341-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8f341-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="8f341-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="8f341-107">なし</span><span class="sxs-lookup"><span data-stu-id="8f341-107">None</span></span>  <br/> |
|<span data-ttu-id="8f341-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8f341-108">Property set:</span></span>  <br/> |<span data-ttu-id="8f341-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="8f341-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="8f341-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="8f341-110">Property name:</span></span>  <br/> |<span data-ttu-id="8f341-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="8f341-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="8f341-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8f341-112">Data type:</span></span>  <br/> |<span data-ttu-id="8f341-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="8f341-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="8f341-114">領域:</span><span class="sxs-lookup"><span data-stu-id="8f341-114">Area:</span></span>  <br/> |<span data-ttu-id="8f341-115">メッセージのセキュリティ保護します。</span><span class="sxs-lookup"><span data-stu-id="8f341-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f341-116">注釈</span><span class="sxs-lookup"><span data-stu-id="8f341-116">Remarks</span></span>

<span data-ttu-id="8f341-117">権限が管理された電子メール メッセージのプロパティがある場合、この複数のバイナリ プロパティの最初の値は、([RFC1950] で指定) と同じ ZLIB 圧縮使用ライセンスを権限管理された電子メール メッセージを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f341-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8f341-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8f341-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8f341-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8f341-119">Protocol specifications</span></span>

<span data-ttu-id="8f341-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f341-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f341-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8f341-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8f341-122">[[MS OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f341-122">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f341-123">権限管理でエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="8f341-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8f341-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8f341-124">Header files</span></span>

<span data-ttu-id="8f341-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8f341-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f341-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8f341-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f341-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="8f341-127">See also</span></span>



[<span data-ttu-id="8f341-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8f341-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f341-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8f341-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f341-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8f341-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f341-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8f341-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

