---
title: PidTagMailPermission の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4cc97647c60322783050abbebd18726434632a43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802960"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="9d0c5-103">PidTagMailPermission の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="9d0c5-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="9d0c5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d0c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d0c5-105">メッセージングのユーザーがメッセージを送信する許可されている場合 TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d0c5-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d0c5-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="9d0c5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d0c5-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="9d0c5-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="9d0c5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9d0c5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d0c5-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="9d0c5-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="9d0c5-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="9d0c5-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d0c5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9d0c5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9d0c5-112">領域:</span><span class="sxs-lookup"><span data-stu-id="9d0c5-112">Area:</span></span>  <br/> |<span data-ttu-id="9d0c5-113">Address</span><span class="sxs-lookup"><span data-stu-id="9d0c5-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d0c5-114">備考</span><span class="sxs-lookup"><span data-stu-id="9d0c5-114">Remarks</span></span>

<span data-ttu-id="9d0c5-115">このプロパティが設定されていない MAPI により真の価値を持つものとして扱います。</span><span class="sxs-lookup"><span data-stu-id="9d0c5-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="9d0c5-116">一部のエントリがいない、メールが有効な企業のディレクトリに false を指定するには、このプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="9d0c5-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9d0c5-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9d0c5-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9d0c5-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9d0c5-118">Header files</span></span>

<span data-ttu-id="9d0c5-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d0c5-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d0c5-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d0c5-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d0c5-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9d0c5-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9d0c5-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d0c5-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d0c5-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d0c5-123">See also</span></span>



[<span data-ttu-id="9d0c5-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d0c5-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d0c5-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d0c5-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d0c5-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="9d0c5-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d0c5-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="9d0c5-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

