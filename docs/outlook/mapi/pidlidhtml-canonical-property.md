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
ms.openlocfilehash: 636aa4d7f20dbd33676bbe65f38f6a9fab25a347
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587524"
---
# <a name="pidlidhtml-canonical-property"></a><span data-ttu-id="cb266-103">PidLidHtml 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb266-103">PidLidHtml Canonical Property</span></span>

  
  
<span data-ttu-id="cb266-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb266-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb266-105">連絡先のビジネスの Web ページの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="cb266-105">Specifies the contact's business Web page URL.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb266-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="cb266-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb266-107">dispidHTML</span><span class="sxs-lookup"><span data-stu-id="cb266-107">dispidHTML</span></span>  <br/> |
|<span data-ttu-id="cb266-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="cb266-108">Property set:</span></span>  <br/> |<span data-ttu-id="cb266-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="cb266-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="cb266-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="cb266-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cb266-111">0x0000802B</span><span class="sxs-lookup"><span data-stu-id="cb266-111">0x0000802B</span></span>  <br/> |
|<span data-ttu-id="cb266-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cb266-112">Data type:</span></span>  <br/> |<span data-ttu-id="cb266-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cb266-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cb266-114">領域:</span><span class="sxs-lookup"><span data-stu-id="cb266-114">Area:</span></span>  <br/> |<span data-ttu-id="cb266-115">Contact</span><span class="sxs-lookup"><span data-stu-id="cb266-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb266-116">注釈</span><span class="sxs-lookup"><span data-stu-id="cb266-116">Remarks</span></span>

<span data-ttu-id="cb266-117">このプロパティの値は、存在する場合、必要があります**PR_BUSINESS_HOME_PAGE** ([PidTagBusinessHomePage](pidtagbusinesshomepage-canonical-property.md)) プロパティの値と同じです。</span><span class="sxs-lookup"><span data-stu-id="cb266-117">The value of this property, if present, should be the same as the value of the **PR_BUSINESS_HOME_PAGE** ([PidTagBusinessHomePage](pidtagbusinesshomepage-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cb266-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cb266-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb266-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cb266-119">Protocol specifications</span></span>

<span data-ttu-id="cb266-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb266-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb266-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cb266-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb266-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb266-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb266-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="cb266-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb266-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="cb266-124">Header files</span></span>

<span data-ttu-id="cb266-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb266-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb266-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cb266-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb266-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="cb266-127">See also</span></span>



[<span data-ttu-id="cb266-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb266-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb266-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb266-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb266-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cb266-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb266-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cb266-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

