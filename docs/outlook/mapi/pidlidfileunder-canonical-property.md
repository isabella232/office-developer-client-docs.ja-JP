---
title: PidLidFileUnder の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnder
api_type:
- COM
ms.assetid: 55afc4bb-c5fc-4162-a293-7d82644b1965
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: aa0a7f958ed1a5ed4140e87e25bd540123616568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801972"
---
# <a name="pidlidfileunder-canonical-property"></a><span data-ttu-id="8eeb0-103">PidLidFileUnder の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8eeb0-103">PidLidFileUnder Canonical Property</span></span>

  
  
<span data-ttu-id="8eeb0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8eeb0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8eeb0-105">連絡先の一覧を表示するときに連絡先を提出する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="8eeb0-105">Specifies the name under which the contact is filed when displaying a list of contacts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8eeb0-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8eeb0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8eeb0-107">dispidFileUnder</span><span class="sxs-lookup"><span data-stu-id="8eeb0-107">dispidFileUnder</span></span>  <br/> |
|<span data-ttu-id="8eeb0-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8eeb0-108">Property set:</span></span>  <br/> |<span data-ttu-id="8eeb0-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="8eeb0-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="8eeb0-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8eeb0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8eeb0-111">0x00008005</span><span class="sxs-lookup"><span data-stu-id="8eeb0-111">0x00008005</span></span>  <br/> |
|<span data-ttu-id="8eeb0-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8eeb0-112">Data type:</span></span>  <br/> |<span data-ttu-id="8eeb0-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8eeb0-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8eeb0-114">領域:</span><span class="sxs-lookup"><span data-stu-id="8eeb0-114">Area:</span></span>  <br/> |<span data-ttu-id="8eeb0-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="8eeb0-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8eeb0-116">備考</span><span class="sxs-lookup"><span data-stu-id="8eeb0-116">Remarks</span></span>

<span data-ttu-id="8eeb0-117">連絡先に表示されない場合、アプリケーションは、空の PT_UNICODE としてこのプロパティを扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="8eeb0-117">The application should treat this property as an empty PT_UNICODE if it is missing from the contact.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8eeb0-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8eeb0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8eeb0-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8eeb0-119">Protocol specifications</span></span>

<span data-ttu-id="8eeb0-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eeb0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8eeb0-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8eeb0-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8eeb0-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eeb0-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8eeb0-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8eeb0-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8eeb0-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8eeb0-124">Header files</span></span>

<span data-ttu-id="8eeb0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8eeb0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8eeb0-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8eeb0-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8eeb0-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="8eeb0-127">See also</span></span>



[<span data-ttu-id="8eeb0-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8eeb0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8eeb0-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8eeb0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8eeb0-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8eeb0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8eeb0-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8eeb0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

