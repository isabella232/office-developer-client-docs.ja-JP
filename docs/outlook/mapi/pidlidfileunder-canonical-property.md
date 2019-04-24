---
title: PidLidFileUnder 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnder
api_type:
- COM
ms.assetid: 55afc4bb-c5fc-4162-a293-7d82644b1965
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 02aa1766421f7c116eabac4c9661be1b5b1adee1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359571"
---
# <a name="pidlidfileunder-canonical-property"></a><span data-ttu-id="a84dd-103">PidLidFileUnder 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a84dd-103">PidLidFileUnder Canonical Property</span></span>

  
  
<span data-ttu-id="a84dd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a84dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a84dd-105">連絡先の一覧を表示するときに、連絡先をファイリングするときの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a84dd-105">Specifies the name under which the contact is filed when displaying a list of contacts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a84dd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a84dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a84dd-107">dispidfileunder</span><span class="sxs-lookup"><span data-stu-id="a84dd-107">dispidFileUnder</span></span>  <br/> |
|<span data-ttu-id="a84dd-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="a84dd-108">Property set:</span></span>  <br/> |<span data-ttu-id="a84dd-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="a84dd-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="a84dd-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a84dd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a84dd-111">0x00008005</span><span class="sxs-lookup"><span data-stu-id="a84dd-111">0x00008005</span></span>  <br/> |
|<span data-ttu-id="a84dd-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a84dd-112">Data type:</span></span>  <br/> |<span data-ttu-id="a84dd-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a84dd-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a84dd-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="a84dd-114">Area:</span></span>  <br/> |<span data-ttu-id="a84dd-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="a84dd-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a84dd-116">解説</span><span class="sxs-lookup"><span data-stu-id="a84dd-116">Remarks</span></span>

<span data-ttu-id="a84dd-117">このプロパティが連絡先にない場合、アプリケーションはこのプロパティを空の PT_UNICODE として扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a84dd-117">The application should treat this property as an empty PT_UNICODE if it is missing from the contact.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a84dd-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a84dd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a84dd-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a84dd-119">Protocol specifications</span></span>

<span data-ttu-id="a84dd-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a84dd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a84dd-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a84dd-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a84dd-122">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a84dd-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a84dd-123">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a84dd-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a84dd-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a84dd-124">Header files</span></span>

<span data-ttu-id="a84dd-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a84dd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a84dd-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a84dd-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a84dd-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="a84dd-127">See also</span></span>



[<span data-ttu-id="a84dd-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a84dd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a84dd-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a84dd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a84dd-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a84dd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a84dd-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a84dd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

