---
title: PidLidEmail3OriginalDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail3OriginalDisplayName
api_type:
- COM
ms.assetid: f3fa392a-c3b1-46dd-bf9b-5ce310719542
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e69bcde35bcfec7746893ee18423aca3a24a6c4a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389079"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a><span data-ttu-id="2b506-103">PidLidEmail3OriginalDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2b506-103">PidLidEmail3OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="2b506-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b506-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b506-105">連絡先に対して指定されている電子メール アドレスに対応する 3 つ目の表示名を指定します。</span><span class="sxs-lookup"><span data-stu-id="2b506-105">Specifies the third display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b506-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2b506-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b506-107">dispidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="2b506-107">dispidEmail3OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="2b506-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2b506-108">Property set:</span></span>  <br/> |<span data-ttu-id="2b506-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="2b506-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="2b506-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2b506-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2b506-111">0x000080A4</span><span class="sxs-lookup"><span data-stu-id="2b506-111">0x000080A4</span></span>  <br/> |
|<span data-ttu-id="2b506-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2b506-112">Data type:</span></span>  <br/> |<span data-ttu-id="2b506-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2b506-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2b506-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="2b506-114">Area:</span></span>  <br/> |<span data-ttu-id="2b506-115">Contact</span><span class="sxs-lookup"><span data-stu-id="2b506-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b506-116">備考</span><span class="sxs-lookup"><span data-stu-id="2b506-116">Remarks</span></span>

<span data-ttu-id="2b506-117">**DispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) プロパティの値が"SMTP"の場合は、それぞれの**dispidEmail3OriginalDisplayName**プロパティの値と同じにそれぞれの**の値dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="2b506-117">If the value of the **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail3OriginalDisplayName** property should equal the value of the respective **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span></span> <span data-ttu-id="2b506-118">このプロパティの目的では、 **dispidEmail3EmailAddress**の 1 つに相当する代替のユーザー ・ フレンドリーなアドレスを表示します。</span><span class="sxs-lookup"><span data-stu-id="2b506-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail3EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2b506-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2b506-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2b506-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2b506-120">Protocol specifications</span></span>

<span data-ttu-id="2b506-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b506-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b506-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2b506-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2b506-123">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b506-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b506-124">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2b506-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2b506-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2b506-125">Header files</span></span>

<span data-ttu-id="2b506-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b506-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b506-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2b506-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b506-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b506-128">See also</span></span>



[<span data-ttu-id="2b506-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2b506-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b506-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2b506-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b506-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2b506-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b506-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2b506-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

