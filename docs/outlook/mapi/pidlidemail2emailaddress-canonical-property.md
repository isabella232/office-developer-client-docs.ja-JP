---
title: PidLidEmail2EmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2EmailAddress
api_type:
- COM
ms.assetid: 89b33a24-395a-4a3f-bc05-a44529399d7c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e73b69f95bc942b8998655ee1ee86d9195ae35c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338571"
---
# <a name="pidlidemail2emailaddress-canonical-property"></a><span data-ttu-id="729a1-103">PidLidEmail2EmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="729a1-103">PidLidEmail2EmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="729a1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="729a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="729a1-105">連絡先の2番目の電子メールアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="729a1-105">Specifies the second email address of the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="729a1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="729a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="729a1-107">dispidEmail2EmailAddress</span><span class="sxs-lookup"><span data-stu-id="729a1-107">dispidEmail2EmailAddress</span></span>  <br/> |
|<span data-ttu-id="729a1-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="729a1-108">Property set:</span></span>  <br/> |<span data-ttu-id="729a1-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="729a1-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="729a1-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="729a1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="729a1-111">0x00008093</span><span class="sxs-lookup"><span data-stu-id="729a1-111">0x00008093</span></span>  <br/> |
|<span data-ttu-id="729a1-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="729a1-112">Data type:</span></span>  <br/> |<span data-ttu-id="729a1-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="729a1-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="729a1-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="729a1-114">Area:</span></span>  <br/> |<span data-ttu-id="729a1-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="729a1-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="729a1-116">解説</span><span class="sxs-lookup"><span data-stu-id="729a1-116">Remarks</span></span>

<span data-ttu-id="729a1-117">このプロパティの値は、この電子メールアドレスに対して指定されているアドレスの種類に対して適切である必要があります。</span><span class="sxs-lookup"><span data-stu-id="729a1-117">The value of this property must be appropriate for the address type specified for this email address.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="729a1-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="729a1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="729a1-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="729a1-119">Protocol specifications</span></span>

<span data-ttu-id="729a1-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="729a1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="729a1-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="729a1-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="729a1-122">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="729a1-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="729a1-123">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="729a1-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="729a1-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="729a1-124">Header files</span></span>

<span data-ttu-id="729a1-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="729a1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="729a1-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="729a1-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="729a1-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="729a1-127">See also</span></span>



[<span data-ttu-id="729a1-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="729a1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="729a1-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="729a1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="729a1-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="729a1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="729a1-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="729a1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

