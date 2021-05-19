---
title: PidLidEmail2OriginalDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7fb7e5afa6a1c050a5d91274bc4f82439fb98640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337962"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a><span data-ttu-id="9cb7d-103">PidLidEmail2OriginalDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9cb7d-103">PidLidEmail2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="9cb7d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cb7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cb7d-105">連絡先に指定された電子メール アドレスに対応する 2 番目の表示名を指定します。</span><span class="sxs-lookup"><span data-stu-id="9cb7d-105">Specifies the second display name that corresponds to the email address specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9cb7d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9cb7d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9cb7d-107">dispidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="9cb7d-107">dispidEmail2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="9cb7d-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="9cb7d-108">Property set:</span></span>  <br/> |<span data-ttu-id="9cb7d-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="9cb7d-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="9cb7d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9cb7d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9cb7d-111">0x00008094</span><span class="sxs-lookup"><span data-stu-id="9cb7d-111">0x00008094</span></span>  <br/> |
|<span data-ttu-id="9cb7d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9cb7d-112">Data type:</span></span>  <br/> |<span data-ttu-id="9cb7d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9cb7d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9cb7d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="9cb7d-114">Area:</span></span>  <br/> |<span data-ttu-id="9cb7d-115">Contact</span><span class="sxs-lookup"><span data-stu-id="9cb7d-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cb7d-116">注釈</span><span class="sxs-lookup"><span data-stu-id="9cb7d-116">Remarks</span></span>

<span data-ttu-id="9cb7d-117">**dispidEmail2AddrType** ([PidLidEmail2AddressType)](pidlidemail2addresstype-canonical-property.md)プロパティの値が "SMTP" の場合、それぞれの **PidLidEmail2OriginalDisplayName** プロパティの値は、それぞれの **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) プロパティの値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="9cb7d-117">If the value of the **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) property is "SMTP", the value of the respective **PidLidEmail2OriginalDisplayName** property should equal the value of the respective **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="9cb7d-118">このプロパティの目的は **、dispidEmail2EmailAddress** のアドレスと同等の代替のユーザーフレンドリーなアドレスを表示します。</span><span class="sxs-lookup"><span data-stu-id="9cb7d-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail2EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9cb7d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9cb7d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9cb7d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9cb7d-120">Protocol specifications</span></span>

<span data-ttu-id="9cb7d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cb7d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cb7d-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="9cb7d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9cb7d-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cb7d-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cb7d-124">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9cb7d-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9cb7d-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9cb7d-125">Header files</span></span>

<span data-ttu-id="9cb7d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9cb7d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9cb7d-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9cb7d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9cb7d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9cb7d-128">See also</span></span>



[<span data-ttu-id="9cb7d-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9cb7d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9cb7d-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9cb7d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9cb7d-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9cb7d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9cb7d-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9cb7d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

