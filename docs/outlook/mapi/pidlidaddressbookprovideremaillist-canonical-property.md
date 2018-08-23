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
ms.openlocfilehash: 4eb2897c1834715f3d937ef7946998943b386aef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801734"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="30dc1-103">PidLidAddressBookProviderEmailList 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="30dc1-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="30dc1-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30dc1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30dc1-105">連絡先に設定する電子メール アドレスのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="30dc1-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30dc1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="30dc1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30dc1-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="30dc1-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="30dc1-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="30dc1-108">Property set:</span></span>  <br/> |<span data-ttu-id="30dc1-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="30dc1-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="30dc1-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="30dc1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="30dc1-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="30dc1-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="30dc1-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="30dc1-112">Data type:</span></span>  <br/> |<span data-ttu-id="30dc1-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="30dc1-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="30dc1-114">領域:</span><span class="sxs-lookup"><span data-stu-id="30dc1-114">Area:</span></span>  <br/> |<span data-ttu-id="30dc1-115">Contact</span><span class="sxs-lookup"><span data-stu-id="30dc1-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30dc1-116">注釈</span><span class="sxs-lookup"><span data-stu-id="30dc1-116">Remarks</span></span>

<span data-ttu-id="30dc1-117">このプロパティでは、各 PT_LONG 値は、プロパティ内で一意である必要があり、次の表の値のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30dc1-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="30dc1-118">このプロパティが設定されている場合、 **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) のプロパティも設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="30dc1-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="30dc1-119">互いに同期された 2 つのプロパティを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30dc1-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="30dc1-120">たとえば、 **dispidABPEmailList**の値のいずれかが"0x00000000"の場合、 **dispidABPArrayType**が"0x00000001"のビットに設定します。</span><span class="sxs-lookup"><span data-stu-id="30dc1-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="30dc1-121">**値**</span><span class="sxs-lookup"><span data-stu-id="30dc1-121">**Value**</span></span>|<span data-ttu-id="30dc1-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="30dc1-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30dc1-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30dc1-123">0x00000000</span></span>  <br/> |<span data-ttu-id="30dc1-124">連絡先の Email1 が定義されています。</span><span class="sxs-lookup"><span data-stu-id="30dc1-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="30dc1-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="30dc1-125">0x00000001</span></span>  <br/> |<span data-ttu-id="30dc1-126">連絡先の電子メール 2 が定義されています。</span><span class="sxs-lookup"><span data-stu-id="30dc1-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="30dc1-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="30dc1-127">0x00000002</span></span>  <br/> |<span data-ttu-id="30dc1-128">連絡先の電子メール 3 が定義されています。</span><span class="sxs-lookup"><span data-stu-id="30dc1-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="30dc1-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="30dc1-129">0x00000003</span></span>  <br/> |<span data-ttu-id="30dc1-130">連絡先の勤務先ファックスが定義されています。</span><span class="sxs-lookup"><span data-stu-id="30dc1-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="30dc1-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="30dc1-131">0x00000004</span></span>  <br/> |<span data-ttu-id="30dc1-132">連絡先の自宅の fax が定義されています。</span><span class="sxs-lookup"><span data-stu-id="30dc1-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="30dc1-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="30dc1-133">0x00000005</span></span>  <br/> |<span data-ttu-id="30dc1-134">連絡先のプライマリ fax が定義されています。</span><span class="sxs-lookup"><span data-stu-id="30dc1-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="30dc1-135">関連リソース</span><span class="sxs-lookup"><span data-stu-id="30dc1-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="30dc1-136">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="30dc1-136">Protocol specifications</span></span>

<span data-ttu-id="30dc1-137">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30dc1-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30dc1-138">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="30dc1-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="30dc1-139">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30dc1-139">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30dc1-140">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="30dc1-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="30dc1-141">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="30dc1-141">Header files</span></span>

<span data-ttu-id="30dc1-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30dc1-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="30dc1-143">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="30dc1-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30dc1-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="30dc1-144">See also</span></span>



[<span data-ttu-id="30dc1-145">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="30dc1-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30dc1-146">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="30dc1-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30dc1-147">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="30dc1-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30dc1-148">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="30dc1-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

