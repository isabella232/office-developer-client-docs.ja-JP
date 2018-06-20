---
title: PidLidAddressBookProviderEmailList の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4eb2897c1834715f3d937ef7946998943b386aef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801734"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="b20a9-103">PidLidAddressBookProviderEmailList の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b20a9-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="b20a9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b20a9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b20a9-105">連絡先に設定する電子メール アドレスのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="b20a9-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b20a9-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b20a9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b20a9-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="b20a9-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="b20a9-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b20a9-108">Property set:</span></span>  <br/> |<span data-ttu-id="b20a9-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="b20a9-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="b20a9-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b20a9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b20a9-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="b20a9-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="b20a9-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b20a9-112">Data type:</span></span>  <br/> |<span data-ttu-id="b20a9-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="b20a9-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="b20a9-114">領域:</span><span class="sxs-lookup"><span data-stu-id="b20a9-114">Area:</span></span>  <br/> |<span data-ttu-id="b20a9-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="b20a9-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b20a9-116">備考</span><span class="sxs-lookup"><span data-stu-id="b20a9-116">Remarks</span></span>

<span data-ttu-id="b20a9-117">このプロパティでは、各 PT_LONG 値は、プロパティ内で一意である必要があり、次の表の値のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b20a9-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="b20a9-118">このプロパティが設定されている場合、 **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) のプロパティも設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b20a9-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="b20a9-119">互いに同期された 2 つのプロパティを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b20a9-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="b20a9-120">たとえば、 **dispidABPEmailList**の値のいずれかが"0x00000000"の場合、 **dispidABPArrayType**が"0x00000001"のビットに設定します。</span><span class="sxs-lookup"><span data-stu-id="b20a9-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="b20a9-121">**値**</span><span class="sxs-lookup"><span data-stu-id="b20a9-121">**Value**</span></span>|<span data-ttu-id="b20a9-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="b20a9-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b20a9-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b20a9-123">0x00000000</span></span>  <br/> |<span data-ttu-id="b20a9-124">連絡先の Email1 が定義されています。</span><span class="sxs-lookup"><span data-stu-id="b20a9-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="b20a9-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b20a9-125">0x00000001</span></span>  <br/> |<span data-ttu-id="b20a9-126">連絡先の電子メール 2 が定義されています。</span><span class="sxs-lookup"><span data-stu-id="b20a9-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="b20a9-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b20a9-127">0x00000002</span></span>  <br/> |<span data-ttu-id="b20a9-128">連絡先の電子メール 3 が定義されています。</span><span class="sxs-lookup"><span data-stu-id="b20a9-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="b20a9-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b20a9-129">0x00000003</span></span>  <br/> |<span data-ttu-id="b20a9-130">連絡先の勤務先ファックスが定義されています。</span><span class="sxs-lookup"><span data-stu-id="b20a9-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="b20a9-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b20a9-131">0x00000004</span></span>  <br/> |<span data-ttu-id="b20a9-132">連絡先の自宅の fax が定義されています。</span><span class="sxs-lookup"><span data-stu-id="b20a9-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="b20a9-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="b20a9-133">0x00000005</span></span>  <br/> |<span data-ttu-id="b20a9-134">連絡先のプライマリ fax が定義されています。</span><span class="sxs-lookup"><span data-stu-id="b20a9-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b20a9-135">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b20a9-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b20a9-136">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b20a9-136">Protocol specifications</span></span>

<span data-ttu-id="b20a9-137">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b20a9-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b20a9-138">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b20a9-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b20a9-139">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b20a9-139">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b20a9-140">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b20a9-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b20a9-141">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b20a9-141">Header files</span></span>

<span data-ttu-id="b20a9-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b20a9-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="b20a9-143">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b20a9-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b20a9-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="b20a9-144">See also</span></span>



[<span data-ttu-id="b20a9-145">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b20a9-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b20a9-146">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b20a9-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b20a9-147">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b20a9-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b20a9-148">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b20a9-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

