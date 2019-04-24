---
title: PidTagEmsAbServer 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fba49b052a51bd498f61fc115f630d08fc6c8926
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335799"
---
# <a name="pidtagemsabserver-canonical-property"></a><span data-ttu-id="6998d-103">PidTagEmsAbServer 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6998d-103">PidTagEmsAbServer Canonical Property</span></span>

  
  
<span data-ttu-id="6998d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6998d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6998d-105">オフラインシナリオのアドレス帳コンテナーのパス、またはアドレス帳コンテナーが存在するグローバルカタログサーバーの完全修飾ドメイン名のどちらかをオンラインシナリオで指定します。</span><span class="sxs-lookup"><span data-stu-id="6998d-105">Specifies either the path of an address book container in an offline scenario or the fully qualified domain name of the global catalog server where the address book container resides in an online scenario.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="6998d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6998d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6998d-107">PR_EMS_AB_SERVER、PR_EMS_AB_SERVER_A、PR_EMS_AB_SERVER_W</span><span class="sxs-lookup"><span data-stu-id="6998d-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span></span>  <br/> |
|<span data-ttu-id="6998d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6998d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6998d-109">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="6998d-109">0xFFFE</span></span>  <br/> |
|<span data-ttu-id="6998d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6998d-110">Data type:</span></span>  <br/> |<span data-ttu-id="6998d-111">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="6998d-111">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="6998d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="6998d-112">Area:</span></span>  <br/> |<span data-ttu-id="6998d-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="6998d-113">Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6998d-114">解説</span><span class="sxs-lookup"><span data-stu-id="6998d-114">Remarks</span></span>

<span data-ttu-id="6998d-115">このプロパティでは、UNICODE プラットフォームで\*\*\*\* `UNICODE`シンボルをコンパイルしたときにプロパティの種類が PT_UNICODE にリセットさ\*\*\*\* れ、 `UNICODE`シンボルを使用してコンパイルされていない場合は PT_STRING8 になります。</span><span class="sxs-lookup"><span data-stu-id="6998d-115">This property has the property type reset to **PT_UNICODE** when it is compiled with the  `UNICODE` symbol on a Unicode platform, and to **PT_STRING8** when it is not compiled with the  `UNICODE` symbol.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6998d-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6998d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6998d-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6998d-117">Protocol specifications</span></span>

<span data-ttu-id="6998d-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6998d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6998d-119">プロパティセットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6998d-119">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6998d-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="6998d-120">Header files</span></span>

<span data-ttu-id="6998d-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6998d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="6998d-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6998d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="6998d-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="6998d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="6998d-124">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6998d-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6998d-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="6998d-125">See also</span></span>



[<span data-ttu-id="6998d-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6998d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6998d-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6998d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6998d-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6998d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6998d-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6998d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

