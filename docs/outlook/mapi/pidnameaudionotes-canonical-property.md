---
title: PidNameAudioNotes 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAudioNotes
api_type:
- COM
ms.assetid: aec4d328-c192-4672-a478-b08442352794
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 188ddf13e623292e95a1af4af54cf4254d7b0345
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396282"
---
# <a name="pidnameaudionotes-canonical-property"></a><span data-ttu-id="d2822-103">PidNameAudioNotes 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d2822-103">PidNameAudioNotes Canonical Property</span></span>

  
  
<span data-ttu-id="d2822-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2822-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2822-105">ボイス メッセージに関連付けられている注釈テキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="d2822-105">Specifies the textual notes that are attached to a voice message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2822-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="d2822-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="d2822-107">UMAudioNotes</span><span class="sxs-lookup"><span data-stu-id="d2822-107">UMAudioNotes</span></span>  <br/> |
|<span data-ttu-id="d2822-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d2822-108">Property set:</span></span>  <br/> |<span data-ttu-id="d2822-109">PSETID_UnifiedMessaging</span><span class="sxs-lookup"><span data-stu-id="d2822-109">PSETID_UnifiedMessaging</span></span>  <br/> |
|<span data-ttu-id="d2822-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="d2822-110">Property name:</span></span>  <br/> |<span data-ttu-id="d2822-111">UMAudioNotes</span><span class="sxs-lookup"><span data-stu-id="d2822-111">UMAudioNotes</span></span>  <br/> |
|<span data-ttu-id="d2822-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d2822-112">Data type:</span></span>  <br/> |<span data-ttu-id="d2822-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d2822-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d2822-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="d2822-114">Area:</span></span>  <br/> |<span data-ttu-id="d2822-115">ユニファイド メッセージング</span><span class="sxs-lookup"><span data-stu-id="d2822-115">Unified messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2822-116">備考</span><span class="sxs-lookup"><span data-stu-id="d2822-116">Remarks</span></span>

<span data-ttu-id="d2822-117">閲覧、ボイス メッセージに直接オーディオ ノートを編集して、エンド ・ ユーザーを有効にするには、クライアントには、音声メッセージのオブジェクトのこのプロパティに追加されるメモのセットをユーザーが入力できる編集ボックスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="d2822-117">To enable an end user to read and edit audio notes directly on a voice message, a client provides an edit box where the user can type a set of notes that are added to this property of the voice message object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d2822-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d2822-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d2822-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d2822-119">Protocol specifications</span></span>

<span data-ttu-id="d2822-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2822-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2822-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2822-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d2822-122">[[MS OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2822-122">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2822-123">プロパティとは、ボイス メールと fax メッセージを表示するための許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d2822-123">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d2822-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d2822-124">Header files</span></span>

<span data-ttu-id="d2822-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2822-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2822-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2822-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2822-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2822-127">See also</span></span>



[<span data-ttu-id="d2822-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d2822-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2822-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d2822-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2822-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d2822-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2822-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d2822-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

