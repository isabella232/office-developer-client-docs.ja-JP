---
title: PidLidAddressBookProviderEmailList 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348483"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="c8da2-103">PidLidAddressBookProviderEmailList 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c8da2-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="c8da2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8da2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8da2-105">連絡先に設定する電子アドレスプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="c8da2-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8da2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c8da2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8da2-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="c8da2-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="c8da2-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="c8da2-108">Property set:</span></span>  <br/> |<span data-ttu-id="c8da2-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="c8da2-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="c8da2-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c8da2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c8da2-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="c8da2-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="c8da2-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c8da2-112">Data type:</span></span>  <br/> |<span data-ttu-id="c8da2-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="c8da2-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="c8da2-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="c8da2-114">Area:</span></span>  <br/> |<span data-ttu-id="c8da2-115">Contact</span><span class="sxs-lookup"><span data-stu-id="c8da2-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8da2-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c8da2-116">Remarks</span></span>

<span data-ttu-id="c8da2-117">このPT_LONGの各値は、プロパティ内で一意である必要があります。次の表のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8da2-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="c8da2-118">このプロパティを設定する場合は **、dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) プロパティも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8da2-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="c8da2-119">これら 2 つのプロパティは、互いに同期し続けなければならない。</span><span class="sxs-lookup"><span data-stu-id="c8da2-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="c8da2-120">たとえば **、dispidABPEmailList** の値の 1 つが "0x00000000" の場合 **、dispidABPArrayType** にはビット "0x00000001" が設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8da2-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="c8da2-121">**値**</span><span class="sxs-lookup"><span data-stu-id="c8da2-121">**Value**</span></span>|<span data-ttu-id="c8da2-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="c8da2-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8da2-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8da2-123">0x00000000</span></span>  <br/> |<span data-ttu-id="c8da2-124">Email1 は連絡先に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="c8da2-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="c8da2-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c8da2-125">0x00000001</span></span>  <br/> |<span data-ttu-id="c8da2-126">Email2 は連絡先に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="c8da2-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="c8da2-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c8da2-127">0x00000002</span></span>  <br/> |<span data-ttu-id="c8da2-128">Email3 は連絡先に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="c8da2-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="c8da2-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="c8da2-129">0x00000003</span></span>  <br/> |<span data-ttu-id="c8da2-130">ビジネス FAX は連絡先に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="c8da2-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="c8da2-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c8da2-131">0x00000004</span></span>  <br/> |<span data-ttu-id="c8da2-132">ホーム FAX は連絡先に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="c8da2-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="c8da2-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c8da2-133">0x00000005</span></span>  <br/> |<span data-ttu-id="c8da2-134">プライマリ FAX は連絡先に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="c8da2-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c8da2-135">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c8da2-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8da2-136">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c8da2-136">Protocol specifications</span></span>

<span data-ttu-id="c8da2-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8da2-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8da2-138">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="c8da2-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8da2-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8da2-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8da2-140">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c8da2-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8da2-141">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c8da2-141">Header files</span></span>

<span data-ttu-id="c8da2-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8da2-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8da2-143">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c8da2-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8da2-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="c8da2-144">See also</span></span>



[<span data-ttu-id="c8da2-145">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c8da2-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8da2-146">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c8da2-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8da2-147">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c8da2-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8da2-148">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c8da2-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

