---
title: PidLidEmail1OriginalDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail1OriginalDisplayName
api_type:
- COM
ms.assetid: 991c2969-0180-4c7d-95ee-e62fd24d67ef
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a20ae8e3f19073bfb88d58db516a0e5f93d91445
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335043"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a><span data-ttu-id="9d0da-103">PidLidEmail1OriginalDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d0da-103">PidLidEmail1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="9d0da-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d0da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d0da-105">連絡先に対して指定されている電子メールアドレスに対応する最初の表示名を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d0da-105">Specifies the first display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d0da-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9d0da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d0da-107">dispidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="9d0da-107">dispidEmail1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="9d0da-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="9d0da-108">Property set:</span></span>  <br/> |<span data-ttu-id="9d0da-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="9d0da-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="9d0da-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9d0da-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9d0da-111">0x00008084</span><span class="sxs-lookup"><span data-stu-id="9d0da-111">0x00008084</span></span>  <br/> |
|<span data-ttu-id="9d0da-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9d0da-112">Data type:</span></span>  <br/> |<span data-ttu-id="9d0da-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9d0da-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9d0da-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="9d0da-114">Area:</span></span>  <br/> |<span data-ttu-id="9d0da-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="9d0da-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d0da-116">解説</span><span class="sxs-lookup"><span data-stu-id="9d0da-116">Remarks</span></span>

<span data-ttu-id="9d0da-117">**dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) プロパティの値が "SMTP" の場合、それぞれの**dispidEmail1OriginalDisplayName**プロパティの値は、それぞれ**のプロパティの値と等しくなければなりません。dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="9d0da-117">If the value of the **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail1OriginalDisplayName** property should equal the value of the respective **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="9d0da-118">このプロパティには、 **dispidEmail1EmailAddress**プロパティのユーザーフレンドリなアドレスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9d0da-118">This property displays an alternative user-friendly address that is equivalent to the one in the **dispidEmail1EmailAddress** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9d0da-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9d0da-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d0da-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9d0da-120">Protocol specifications</span></span>

<span data-ttu-id="9d0da-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d0da-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d0da-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d0da-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9d0da-123">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d0da-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d0da-124">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d0da-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d0da-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9d0da-125">Header files</span></span>

<span data-ttu-id="9d0da-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d0da-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d0da-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d0da-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d0da-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d0da-128">See also</span></span>



[<span data-ttu-id="9d0da-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9d0da-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d0da-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d0da-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d0da-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9d0da-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d0da-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9d0da-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

