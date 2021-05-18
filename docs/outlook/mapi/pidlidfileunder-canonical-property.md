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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 02aa1766421f7c116eabac4c9661be1b5b1adee1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359571"
---
# <a name="pidlidfileunder-canonical-property"></a><span data-ttu-id="ed791-103">PidLidFileUnder 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed791-103">PidLidFileUnder Canonical Property</span></span>

  
  
<span data-ttu-id="ed791-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed791-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed791-105">連絡先の一覧を表示するときに連絡先をファイルする名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ed791-105">Specifies the name under which the contact is filed when displaying a list of contacts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed791-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ed791-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed791-107">dispidFileUnder</span><span class="sxs-lookup"><span data-stu-id="ed791-107">dispidFileUnder</span></span>  <br/> |
|<span data-ttu-id="ed791-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="ed791-108">Property set:</span></span>  <br/> |<span data-ttu-id="ed791-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="ed791-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="ed791-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ed791-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ed791-111">0x00008005</span><span class="sxs-lookup"><span data-stu-id="ed791-111">0x00008005</span></span>  <br/> |
|<span data-ttu-id="ed791-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ed791-112">Data type:</span></span>  <br/> |<span data-ttu-id="ed791-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ed791-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ed791-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="ed791-114">Area:</span></span>  <br/> |<span data-ttu-id="ed791-115">Contact</span><span class="sxs-lookup"><span data-stu-id="ed791-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed791-116">注釈</span><span class="sxs-lookup"><span data-stu-id="ed791-116">Remarks</span></span>

<span data-ttu-id="ed791-117">アプリケーションは、連絡先に存在PT_UNICODE、このプロパティを空のプロパティとして扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed791-117">The application should treat this property as an empty PT_UNICODE if it is missing from the contact.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ed791-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ed791-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed791-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ed791-119">Protocol specifications</span></span>

<span data-ttu-id="ed791-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed791-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed791-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="ed791-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ed791-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed791-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed791-123">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ed791-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed791-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ed791-124">Header files</span></span>

<span data-ttu-id="ed791-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed791-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed791-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed791-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed791-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed791-127">See also</span></span>



[<span data-ttu-id="ed791-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ed791-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed791-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed791-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed791-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ed791-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed791-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ed791-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

