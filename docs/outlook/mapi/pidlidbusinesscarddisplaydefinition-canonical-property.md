---
title: PidLidBusinessCardDisplayDefinition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 34d29b9a15cc6f5a3f88a6477738eb63904e1fdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801839"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a><span data-ttu-id="5f361-103">PidLidBusinessCardDisplayDefinition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f361-103">PidLidBusinessCardDisplayDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="5f361-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f361-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f361-105">電子名刺として連絡先を表示するためのユーザーのカスタマイズの詳細情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5f361-105">Contains user-customization details for displaying a contact as a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f361-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5f361-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f361-107">dispidBCDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="5f361-107">dispidBCDisplayDefinition</span></span>  <br/> |
|<span data-ttu-id="5f361-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5f361-108">Property set:</span></span>  <br/> |<span data-ttu-id="5f361-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="5f361-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="5f361-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5f361-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5f361-111">0x00008040</span><span class="sxs-lookup"><span data-stu-id="5f361-111">0x00008040</span></span>  <br/> |
|<span data-ttu-id="5f361-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5f361-112">Data type:</span></span>  <br/> |<span data-ttu-id="5f361-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5f361-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5f361-114">領域:</span><span class="sxs-lookup"><span data-stu-id="5f361-114">Area:</span></span>  <br/> |<span data-ttu-id="5f361-115">Contact</span><span class="sxs-lookup"><span data-stu-id="5f361-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f361-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5f361-116">Remarks</span></span>

<span data-ttu-id="5f361-117">名刺のレイアウトは、イメージとテキスト フィールドの数として表されます。</span><span class="sxs-lookup"><span data-stu-id="5f361-117">The layout of a business card can be represented as an image and a number of text fields.</span></span> <span data-ttu-id="5f361-118">イメージには、連絡先の写真、または [名刺の画像のいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5f361-118">The image can be either a contact photo, or a card picture.</span></span> <span data-ttu-id="5f361-119">テキスト フィールドは、連絡先を設定する別のプロパティと、ユーザーが指定したオプションのカスタマイズされたラベル文字列からの値で構成されます。</span><span class="sxs-lookup"><span data-stu-id="5f361-119">Text fields consist of a value from another property set on the contact and an optional customized label string provided by the user.</span></span> <span data-ttu-id="5f361-120">複数バイトの値がバッファーにリトル エンディアン形式で格納されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5f361-120">Note that multi-byte values are stored in little-endian format in the buffer.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f361-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5f361-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f361-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5f361-122">Protocol specifications</span></span>

<span data-ttu-id="5f361-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f361-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f361-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5f361-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f361-125">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f361-125">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f361-126">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f361-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f361-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5f361-127">Header files</span></span>

<span data-ttu-id="5f361-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f361-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f361-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5f361-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f361-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f361-130">See also</span></span>



[<span data-ttu-id="5f361-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f361-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f361-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f361-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f361-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5f361-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f361-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5f361-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

