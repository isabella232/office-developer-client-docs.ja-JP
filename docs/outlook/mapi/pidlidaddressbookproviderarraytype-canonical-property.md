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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 68396f210aab465da9cec4a74a3c24cc4e8578a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348441"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="ea9eb-103">PidLidAddressBookProviderArrayType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ea9eb-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="ea9eb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea9eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea9eb-105">連絡先の電子アドレスの状態を指定し、ビット フラグのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ea9eb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ea9eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea9eb-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="ea9eb-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="ea9eb-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="ea9eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="ea9eb-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="ea9eb-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="ea9eb-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ea9eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ea9eb-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="ea9eb-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="ea9eb-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ea9eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="ea9eb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ea9eb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ea9eb-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="ea9eb-114">Area:</span></span>  <br/> |<span data-ttu-id="ea9eb-115">Contact</span><span class="sxs-lookup"><span data-stu-id="ea9eb-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea9eb-116">注釈</span><span class="sxs-lookup"><span data-stu-id="ea9eb-116">Remarks</span></span>

<span data-ttu-id="ea9eb-117">**dispidABPArrayType** プロパティの値は、連絡先オブジェクトの状態を指定するフラグの組み合わせである必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="ea9eb-118">次の表では、個々のフラグを指定します。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="ea9eb-119">このプロパティを設定する場合は **、dispidABPEmailList** [(PidLidAddressBookProviderEmailList)](pidlidaddressbookprovideremaillist-canonical-property.md)プロパティも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="ea9eb-120">これら 2 つのプロパティは、互いに同期し続けなければならない。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="ea9eb-121">たとえば **、dispidABPArrayType** にビット "0x00000001 セット" がある場合 **、dispidABPEmailList** の値の 1 つは "0x00000000" である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="ea9eb-122">**ビット**</span><span class="sxs-lookup"><span data-stu-id="ea9eb-122">**Bit**</span></span>|<span data-ttu-id="ea9eb-123">**説明**</span><span class="sxs-lookup"><span data-stu-id="ea9eb-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ea9eb-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea9eb-124">0x00000001</span></span>  <br/> |<span data-ttu-id="ea9eb-125">Email1 は連絡先に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="ea9eb-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea9eb-126">0x00000002</span></span>  <br/> |<span data-ttu-id="ea9eb-127">Email2 は連絡先に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="ea9eb-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea9eb-128">0x00000004</span></span>  <br/> |<span data-ttu-id="ea9eb-129">Email3 は連絡先に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="ea9eb-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ea9eb-130">0x00000008</span></span>  <br/> |<span data-ttu-id="ea9eb-131">ビジネス FAX は連絡先に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="ea9eb-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea9eb-132">0x00000010</span></span>  <br/> |<span data-ttu-id="ea9eb-133">ホーム FAX は連絡先に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="ea9eb-134">0x00000020</span><span class="sxs-lookup"><span data-stu-id="ea9eb-134">0x00000020</span></span>  <br/> |<span data-ttu-id="ea9eb-135">プライマリ FAX は連絡先に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ea9eb-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ea9eb-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ea9eb-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ea9eb-137">Protocol specifications</span></span>

<span data-ttu-id="ea9eb-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea9eb-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea9eb-139">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ea9eb-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea9eb-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea9eb-141">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ea9eb-142">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ea9eb-142">Header files</span></span>

<span data-ttu-id="ea9eb-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea9eb-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea9eb-144">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ea9eb-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea9eb-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="ea9eb-145">See also</span></span>



[<span data-ttu-id="ea9eb-146">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ea9eb-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea9eb-147">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ea9eb-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea9eb-148">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ea9eb-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea9eb-149">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ea9eb-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

