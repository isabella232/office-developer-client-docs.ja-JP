---
title: PidLidContactCharacterSet 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactCharacterSet
api_type:
- COM
ms.assetid: a167e199-a9b2-47f9-a90e-2abc7c29828c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0329147463db38fb8c547214788366444daed312
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384865"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a><span data-ttu-id="aaf0f-103">PidLidContactCharacterSet 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aaf0f-103">PidLidContactCharacterSet Canonical Property</span></span>

  
  
<span data-ttu-id="aaf0f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaf0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aaf0f-105">この連絡先に使用する文字セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="aaf0f-105">Specifies the character set used for this contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aaf0f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="aaf0f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aaf0f-107">dispidContactCharSet</span><span class="sxs-lookup"><span data-stu-id="aaf0f-107">dispidContactCharSet</span></span>  <br/> |
|<span data-ttu-id="aaf0f-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="aaf0f-108">Property set:</span></span>  <br/> |<span data-ttu-id="aaf0f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="aaf0f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="aaf0f-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="aaf0f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="aaf0f-111">0x00008023</span><span class="sxs-lookup"><span data-stu-id="aaf0f-111">0x00008023</span></span>  <br/> |
|<span data-ttu-id="aaf0f-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="aaf0f-112">Data type:</span></span>  <br/> |<span data-ttu-id="aaf0f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="aaf0f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="aaf0f-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="aaf0f-114">Area:</span></span>  <br/> |<span data-ttu-id="aaf0f-115">Contact</span><span class="sxs-lookup"><span data-stu-id="aaf0f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aaf0f-116">備考</span><span class="sxs-lookup"><span data-stu-id="aaf0f-116">Remarks</span></span>

<span data-ttu-id="aaf0f-117">アプリケーションは、 **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md))、 **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) と**dispidFileUnderId のオプションの文字セットの依存リストを生成する場合に支援するためにこのプロパティを使用することができます。**([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="aaf0f-117">Applications can use this property to aid in generating a character-set dependent list of choices for the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) , and **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) properties.</span></span> <span data-ttu-id="aaf0f-118">プロパティの値が"0x00000000"または"0x00000001"の場合は、アプリケーションとして設定されていないプロパティを扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="aaf0f-118">If the value of the property is "0x00000000" or "0x00000001", applications should treat the property as not being set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aaf0f-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="aaf0f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aaf0f-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="aaf0f-120">Protocol specifications</span></span>

<span data-ttu-id="aaf0f-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aaf0f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aaf0f-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="aaf0f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aaf0f-123">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aaf0f-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aaf0f-124">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="aaf0f-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aaf0f-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="aaf0f-125">Header files</span></span>

<span data-ttu-id="aaf0f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aaf0f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="aaf0f-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="aaf0f-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aaf0f-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="aaf0f-128">See also</span></span>



[<span data-ttu-id="aaf0f-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="aaf0f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aaf0f-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="aaf0f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aaf0f-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="aaf0f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aaf0f-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="aaf0f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

