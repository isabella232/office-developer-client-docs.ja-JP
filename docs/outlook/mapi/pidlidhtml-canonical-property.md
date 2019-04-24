---
title: PidLidHtml 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidHtml
api_type:
- COM
ms.assetid: 5598cbaf-cb9a-4d3a-b123-9108a7aa7c1c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dd80c969c3ef7af280248d9570e684cd7278e9e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357576"
---
# <a name="pidlidhtml-canonical-property"></a><span data-ttu-id="fca17-103">PidLidHtml 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fca17-103">PidLidHtml Canonical Property</span></span>

  
  
<span data-ttu-id="fca17-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fca17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fca17-105">連絡先のビジネス Web ページの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="fca17-105">Specifies the contact's business Web page URL.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fca17-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fca17-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fca17-107">dispidhtml</span><span class="sxs-lookup"><span data-stu-id="fca17-107">dispidHTML</span></span>  <br/> |
|<span data-ttu-id="fca17-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="fca17-108">Property set:</span></span>  <br/> |<span data-ttu-id="fca17-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="fca17-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="fca17-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fca17-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fca17-111">0x0000802b</span><span class="sxs-lookup"><span data-stu-id="fca17-111">0x0000802B</span></span>  <br/> |
|<span data-ttu-id="fca17-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fca17-112">Data type:</span></span>  <br/> |<span data-ttu-id="fca17-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fca17-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fca17-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="fca17-114">Area:</span></span>  <br/> |<span data-ttu-id="fca17-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="fca17-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fca17-116">解説</span><span class="sxs-lookup"><span data-stu-id="fca17-116">Remarks</span></span>

<span data-ttu-id="fca17-117">このプロパティの値が存在する場合は、 **PR_BUSINESS_HOME_PAGE** ([PidTagBusinessHomePage](pidtagbusinesshomepage-canonical-property.md)) プロパティの値と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="fca17-117">The value of this property, if present, should be the same as the value of the **PR_BUSINESS_HOME_PAGE** ([PidTagBusinessHomePage](pidtagbusinesshomepage-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fca17-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fca17-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fca17-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fca17-119">Protocol specifications</span></span>

<span data-ttu-id="fca17-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fca17-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fca17-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fca17-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fca17-122">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fca17-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fca17-123">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fca17-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fca17-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="fca17-124">Header files</span></span>

<span data-ttu-id="fca17-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fca17-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fca17-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fca17-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fca17-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="fca17-127">See also</span></span>



[<span data-ttu-id="fca17-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fca17-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fca17-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fca17-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fca17-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fca17-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fca17-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fca17-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

