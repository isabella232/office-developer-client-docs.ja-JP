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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399866"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a><span data-ttu-id="a5de7-103">PidLidEmail1OriginalDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a5de7-103">PidLidEmail1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="a5de7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5de7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5de7-105">連絡先に対して指定されている電子メール アドレスに対応する最初の表示名を指定します。</span><span class="sxs-lookup"><span data-stu-id="a5de7-105">Specifies the first display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5de7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a5de7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5de7-107">dispidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="a5de7-107">dispidEmail1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="a5de7-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a5de7-108">Property set:</span></span>  <br/> |<span data-ttu-id="a5de7-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="a5de7-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="a5de7-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a5de7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a5de7-111">0x00008084</span><span class="sxs-lookup"><span data-stu-id="a5de7-111">0x00008084</span></span>  <br/> |
|<span data-ttu-id="a5de7-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a5de7-112">Data type:</span></span>  <br/> |<span data-ttu-id="a5de7-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a5de7-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a5de7-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="a5de7-114">Area:</span></span>  <br/> |<span data-ttu-id="a5de7-115">Contact</span><span class="sxs-lookup"><span data-stu-id="a5de7-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5de7-116">備考</span><span class="sxs-lookup"><span data-stu-id="a5de7-116">Remarks</span></span>

<span data-ttu-id="a5de7-117">**DispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) プロパティの値が"SMTP"の場合は、それぞれの**dispidEmail1OriginalDisplayName**プロパティの値と同じにそれぞれの**の値dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="a5de7-117">If the value of the **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail1OriginalDisplayName** property should equal the value of the respective **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="a5de7-118">このプロパティには、 **dispidEmail1EmailAddress**プロパティの 1 つに相当する代替のユーザー ・ フレンドリーなアドレスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5de7-118">This property displays an alternative user-friendly address that is equivalent to the one in the **dispidEmail1EmailAddress** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a5de7-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a5de7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5de7-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a5de7-120">Protocol specifications</span></span>

<span data-ttu-id="a5de7-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5de7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5de7-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a5de7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5de7-123">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5de7-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5de7-124">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a5de7-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5de7-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a5de7-125">Header files</span></span>

<span data-ttu-id="a5de7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5de7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5de7-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a5de7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5de7-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a5de7-128">See also</span></span>



[<span data-ttu-id="a5de7-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a5de7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5de7-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a5de7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5de7-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a5de7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5de7-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a5de7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

