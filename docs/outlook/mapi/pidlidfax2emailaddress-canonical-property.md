---
title: PidLidFax2EmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFax2EmailAddress
api_type:
- COM
ms.assetid: 119c00cf-b7df-4354-aef8-575429e5ab3c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 16b1ebeb67b48c62bcccc804415d962831f13d7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801926"
---
# <a name="pidlidfax2emailaddress-canonical-property"></a><span data-ttu-id="6e5a3-103">PidLidFax2EmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6e5a3-103">PidLidFax2EmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="6e5a3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e5a3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e5a3-105">連絡先の自宅の fax アドレスの電子メール アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="6e5a3-105">Specifies the email address of the contact's home fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e5a3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6e5a3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e5a3-107">dispidFax2EmailAddress</span><span class="sxs-lookup"><span data-stu-id="6e5a3-107">dispidFax2EmailAddress</span></span>  <br/> |
|<span data-ttu-id="6e5a3-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6e5a3-108">Property set:</span></span>  <br/> |<span data-ttu-id="6e5a3-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="6e5a3-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="6e5a3-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6e5a3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6e5a3-111">0x000080C3</span><span class="sxs-lookup"><span data-stu-id="6e5a3-111">0x000080C3</span></span>  <br/> |
|<span data-ttu-id="6e5a3-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6e5a3-112">Data type:</span></span>  <br/> |<span data-ttu-id="6e5a3-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6e5a3-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6e5a3-114">領域:</span><span class="sxs-lookup"><span data-stu-id="6e5a3-114">Area:</span></span>  <br/> |<span data-ttu-id="6e5a3-115">Contact</span><span class="sxs-lookup"><span data-stu-id="6e5a3-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e5a3-116">注釈</span><span class="sxs-lookup"><span data-stu-id="6e5a3-116">Remarks</span></span>

<span data-ttu-id="6e5a3-117">このプロパティは、存在する場合、含める必要があります、ユーザーが読み取り可能な表示名の後に、"@"文字、fax 番号の後に。</span><span class="sxs-lookup"><span data-stu-id="6e5a3-117">This property, if present, should contain a user-readable display name, followed by the "@" character, followed by a fax number.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6e5a3-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6e5a3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e5a3-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6e5a3-119">Protocol specifications</span></span>

<span data-ttu-id="6e5a3-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e5a3-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e5a3-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6e5a3-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e5a3-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e5a3-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e5a3-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6e5a3-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e5a3-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6e5a3-124">Header files</span></span>

<span data-ttu-id="6e5a3-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e5a3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e5a3-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6e5a3-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e5a3-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e5a3-127">See also</span></span>



[<span data-ttu-id="6e5a3-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6e5a3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e5a3-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6e5a3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e5a3-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6e5a3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e5a3-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6e5a3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

