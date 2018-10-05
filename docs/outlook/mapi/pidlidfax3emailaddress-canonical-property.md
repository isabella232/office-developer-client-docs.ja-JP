---
title: PidLidFax3EmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFax3EmailAddress
api_type:
- COM
ms.assetid: 8b53c307-1a01-4c94-b6db-9fcb840ce390
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9118152a6024647f62694a09d3a39326dfed6e37
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383955"
---
# <a name="pidlidfax3emailaddress-canonical-property"></a><span data-ttu-id="6ab33-103">PidLidFax3EmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ab33-103">PidLidFax3EmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="6ab33-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ab33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ab33-105">連絡先の電子メール アドレスはの他の fax アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ab33-105">Specifies the email address of the contact's other fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ab33-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6ab33-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ab33-107">dispidFax3EmailAddress</span><span class="sxs-lookup"><span data-stu-id="6ab33-107">dispidFax3EmailAddress</span></span>  <br/> |
|<span data-ttu-id="6ab33-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6ab33-108">Property set:</span></span>  <br/> |<span data-ttu-id="6ab33-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="6ab33-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="6ab33-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6ab33-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6ab33-111">0x000080D3</span><span class="sxs-lookup"><span data-stu-id="6ab33-111">0x000080D3</span></span>  <br/> |
|<span data-ttu-id="6ab33-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6ab33-112">Data type:</span></span>  <br/> |<span data-ttu-id="6ab33-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6ab33-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6ab33-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="6ab33-114">Area:</span></span>  <br/> |<span data-ttu-id="6ab33-115">Contact</span><span class="sxs-lookup"><span data-stu-id="6ab33-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ab33-116">備考</span><span class="sxs-lookup"><span data-stu-id="6ab33-116">Remarks</span></span>

<span data-ttu-id="6ab33-117">このプロパティは、存在する場合、含める必要があります、ユーザーが読み取り可能な表示名の後に、"@"文字、fax 番号の後に。</span><span class="sxs-lookup"><span data-stu-id="6ab33-117">This property, if present, should contain a user-readable display name, followed by the "@" character, followed by a fax number.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6ab33-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6ab33-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ab33-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6ab33-119">Protocol specifications</span></span>

<span data-ttu-id="6ab33-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ab33-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ab33-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6ab33-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ab33-122">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ab33-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ab33-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ab33-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ab33-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6ab33-124">Header files</span></span>

<span data-ttu-id="6ab33-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ab33-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ab33-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6ab33-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ab33-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ab33-127">See also</span></span>



[<span data-ttu-id="6ab33-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ab33-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ab33-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ab33-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ab33-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6ab33-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ab33-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6ab33-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

