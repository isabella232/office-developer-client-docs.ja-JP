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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348483"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="fc764-103">PidLidAddressBookProviderEmailList 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fc764-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="fc764-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc764-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc764-105">連絡先に設定されている電子アドレスのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="fc764-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc764-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fc764-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc764-107">dispidabpemaillist</span><span class="sxs-lookup"><span data-stu-id="fc764-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="fc764-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="fc764-108">Property set:</span></span>  <br/> |<span data-ttu-id="fc764-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="fc764-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="fc764-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fc764-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fc764-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="fc764-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="fc764-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fc764-112">Data type:</span></span>  <br/> |<span data-ttu-id="fc764-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="fc764-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="fc764-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="fc764-114">Area:</span></span>  <br/> |<span data-ttu-id="fc764-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="fc764-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc764-116">解説</span><span class="sxs-lookup"><span data-stu-id="fc764-116">Remarks</span></span>

<span data-ttu-id="fc764-117">このプロパティの各 PT_LONG 値は、プロパティで一意である必要があり、次の表のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc764-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="fc764-118">このプロパティが設定されている場合は、 **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) プロパティも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc764-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="fc764-119">これら2つのプロパティは、互いに同期しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc764-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="fc764-120">たとえば、 **dispidabpemaillist**の値のいずれかが "0x00000000" の場合、 **dispidABPArrayType**にはビット "0x00000001" が設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc764-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="fc764-121">**値**</span><span class="sxs-lookup"><span data-stu-id="fc764-121">**Value**</span></span>|<span data-ttu-id="fc764-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="fc764-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc764-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc764-123">0x00000000</span></span>  <br/> |<span data-ttu-id="fc764-124">Email1 が連絡先に対して定義されている。</span><span class="sxs-lookup"><span data-stu-id="fc764-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="fc764-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fc764-125">0x00000001</span></span>  <br/> |<span data-ttu-id="fc764-126">Email2 が連絡先に対して定義されている。</span><span class="sxs-lookup"><span data-stu-id="fc764-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="fc764-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fc764-127">0x00000002</span></span>  <br/> |<span data-ttu-id="fc764-128">Email3 が連絡先に対して定義されている。</span><span class="sxs-lookup"><span data-stu-id="fc764-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="fc764-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="fc764-129">0x00000003</span></span>  <br/> |<span data-ttu-id="fc764-130">連絡先に対して会社の fax が定義されている。</span><span class="sxs-lookup"><span data-stu-id="fc764-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="fc764-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="fc764-131">0x00000004</span></span>  <br/> |<span data-ttu-id="fc764-132">自宅 fax は連絡先に対して定義されています。</span><span class="sxs-lookup"><span data-stu-id="fc764-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="fc764-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="fc764-133">0x00000005</span></span>  <br/> |<span data-ttu-id="fc764-134">連絡先に対して、プライマリ fax が定義されている。</span><span class="sxs-lookup"><span data-stu-id="fc764-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="fc764-135">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fc764-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc764-136">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fc764-136">Protocol specifications</span></span>

<span data-ttu-id="fc764-137">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc764-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc764-138">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fc764-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc764-139">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc764-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc764-140">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fc764-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc764-141">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="fc764-141">Header files</span></span>

<span data-ttu-id="fc764-142">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc764-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc764-143">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fc764-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc764-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc764-144">See also</span></span>



[<span data-ttu-id="fc764-145">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fc764-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc764-146">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fc764-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc764-147">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fc764-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc764-148">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fc764-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

