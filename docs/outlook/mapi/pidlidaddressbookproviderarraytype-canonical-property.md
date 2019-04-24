---
title: PidLidAddressBookProviderArrayType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 68396f210aab465da9cec4a74a3c24cc4e8578a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348441"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="18a7a-103">PidLidAddressBookProviderArrayType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="18a7a-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="18a7a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18a7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18a7a-105">連絡先の電子メールアドレスの状態を指定し、ビットフラグのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="18a7a-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18a7a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="18a7a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18a7a-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="18a7a-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="18a7a-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="18a7a-108">Property set:</span></span>  <br/> |<span data-ttu-id="18a7a-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="18a7a-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="18a7a-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="18a7a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="18a7a-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="18a7a-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="18a7a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="18a7a-112">Data type:</span></span>  <br/> |<span data-ttu-id="18a7a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="18a7a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="18a7a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="18a7a-114">Area:</span></span>  <br/> |<span data-ttu-id="18a7a-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="18a7a-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18a7a-116">解説</span><span class="sxs-lookup"><span data-stu-id="18a7a-116">Remarks</span></span>

<span data-ttu-id="18a7a-117">**dispidABPArrayType**プロパティの値は、連絡先オブジェクトの状態を指定するフラグの組み合わせである必要があります。</span><span class="sxs-lookup"><span data-stu-id="18a7a-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="18a7a-118">各フラグは、次の表で指定されています。</span><span class="sxs-lookup"><span data-stu-id="18a7a-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="18a7a-119">このプロパティが設定されている場合は、 **dispidabpemaillist** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) プロパティも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18a7a-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="18a7a-120">これら2つのプロパティは、互いに同期しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="18a7a-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="18a7a-121">たとえば、 **dispidABPArrayType**にビット "0x00000001 set" が含まれている場合、 **dispidabpemaillist**の値の1つは "0x00000000" である必要があります。</span><span class="sxs-lookup"><span data-stu-id="18a7a-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="18a7a-122">**若干**</span><span class="sxs-lookup"><span data-stu-id="18a7a-122">**Bit**</span></span>|<span data-ttu-id="18a7a-123">**説明**</span><span class="sxs-lookup"><span data-stu-id="18a7a-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18a7a-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18a7a-124">0x00000001</span></span>  <br/> |<span data-ttu-id="18a7a-125">Email1 が連絡先に対して定義されている。</span><span class="sxs-lookup"><span data-stu-id="18a7a-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="18a7a-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="18a7a-126">0x00000002</span></span>  <br/> |<span data-ttu-id="18a7a-127">Email2 が連絡先に対して定義されている。</span><span class="sxs-lookup"><span data-stu-id="18a7a-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="18a7a-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="18a7a-128">0x00000004</span></span>  <br/> |<span data-ttu-id="18a7a-129">Email3 が連絡先に対して定義されている。</span><span class="sxs-lookup"><span data-stu-id="18a7a-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="18a7a-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="18a7a-130">0x00000008</span></span>  <br/> |<span data-ttu-id="18a7a-131">連絡先に対して会社の fax が定義されている。</span><span class="sxs-lookup"><span data-stu-id="18a7a-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="18a7a-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18a7a-132">0x00000010</span></span>  <br/> |<span data-ttu-id="18a7a-133">自宅 fax は連絡先に対して定義されています。</span><span class="sxs-lookup"><span data-stu-id="18a7a-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="18a7a-134">0x00000020</span><span class="sxs-lookup"><span data-stu-id="18a7a-134">0x00000020</span></span>  <br/> |<span data-ttu-id="18a7a-135">連絡先に対して、プライマリ fax が定義されている。</span><span class="sxs-lookup"><span data-stu-id="18a7a-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="18a7a-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="18a7a-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18a7a-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="18a7a-137">Protocol specifications</span></span>

<span data-ttu-id="18a7a-138">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18a7a-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18a7a-139">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="18a7a-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18a7a-140">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18a7a-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18a7a-141">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="18a7a-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18a7a-142">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="18a7a-142">Header files</span></span>

<span data-ttu-id="18a7a-143">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18a7a-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="18a7a-144">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="18a7a-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18a7a-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="18a7a-145">See also</span></span>



[<span data-ttu-id="18a7a-146">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="18a7a-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18a7a-147">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="18a7a-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18a7a-148">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="18a7a-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18a7a-149">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="18a7a-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

