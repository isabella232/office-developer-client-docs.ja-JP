---
title: PidLidContactCharacterSet 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactCharacterSet
api_type:
- COM
ms.assetid: a167e199-a9b2-47f9-a90e-2abc7c29828c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0329147463db38fb8c547214788366444daed312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319706"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a><span data-ttu-id="d8530-103">PidLidContactCharacterSet 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d8530-103">PidLidContactCharacterSet Canonical Property</span></span>

  
  
<span data-ttu-id="d8530-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8530-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8530-105">この連絡先に使用する文字セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="d8530-105">Specifies the character set used for this contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8530-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d8530-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8530-107">dispidContactCharSet</span><span class="sxs-lookup"><span data-stu-id="d8530-107">dispidContactCharSet</span></span>  <br/> |
|<span data-ttu-id="d8530-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="d8530-108">Property set:</span></span>  <br/> |<span data-ttu-id="d8530-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="d8530-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="d8530-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d8530-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d8530-111">0x00008023</span><span class="sxs-lookup"><span data-stu-id="d8530-111">0x00008023</span></span>  <br/> |
|<span data-ttu-id="d8530-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d8530-112">Data type:</span></span>  <br/> |<span data-ttu-id="d8530-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d8530-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d8530-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="d8530-114">Area:</span></span>  <br/> |<span data-ttu-id="d8530-115">Contact</span><span class="sxs-lookup"><span data-stu-id="d8530-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8530-116">注釈</span><span class="sxs-lookup"><span data-stu-id="d8530-116">Remarks</span></span>

<span data-ttu-id="d8530-117">アプリケーションは、このプロパティを使用して **、dispidFileUnder** [(PidLidFileUnder)](pidlidfileunder-canonical-property.md)プロパティ **、dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) プロパティ、 **および dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) プロパティの文字セット依存リストを生成できます。</span><span class="sxs-lookup"><span data-stu-id="d8530-117">Applications can use this property to aid in generating a character-set dependent list of choices for the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) , and **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) properties.</span></span> <span data-ttu-id="d8530-118">プロパティの値が "0x00000000" または "0x00000001" の場合、アプリケーションはプロパティを設定されていないと処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8530-118">If the value of the property is "0x00000000" or "0x00000001", applications should treat the property as not being set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d8530-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d8530-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d8530-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d8530-120">Protocol specifications</span></span>

<span data-ttu-id="d8530-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8530-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8530-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="d8530-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d8530-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8530-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8530-124">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d8530-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d8530-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d8530-125">Header files</span></span>

<span data-ttu-id="d8530-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d8530-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d8530-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d8530-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8530-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8530-128">See also</span></span>



[<span data-ttu-id="d8530-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d8530-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d8530-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d8530-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d8530-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d8530-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d8530-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d8530-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

