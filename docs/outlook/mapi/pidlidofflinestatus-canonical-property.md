---
title: PidLidOfflineStatus の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 34f50766c2c45d85bbb0bd9e12d32c5dd87e3cac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802061"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="98f4a-103">PidLidOfflineStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="98f4a-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="98f4a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98f4a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98f4a-105">[MS LISTSWS] を実装するサーバー上のドキュメント ファイルの状態を決定します。</span><span class="sxs-lookup"><span data-stu-id="98f4a-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98f4a-106">関連するプロパティ</span><span class="sxs-lookup"><span data-stu-id="98f4a-106">Associated properties</span></span>  <br/> |<span data-ttu-id="98f4a-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="98f4a-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="98f4a-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="98f4a-108">Property set:</span></span>  <br/> |<span data-ttu-id="98f4a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="98f4a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="98f4a-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="98f4a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="98f4a-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="98f4a-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="98f4a-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="98f4a-112">Data type:</span></span>  <br/> |<span data-ttu-id="98f4a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="98f4a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="98f4a-114">領域:</span><span class="sxs-lookup"><span data-stu-id="98f4a-114">Area:</span></span>  <br/> |<span data-ttu-id="98f4a-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="98f4a-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98f4a-116">備考</span><span class="sxs-lookup"><span data-stu-id="98f4a-116">Remarks</span></span>

<span data-ttu-id="98f4a-117">次の表は、このプロパティの値を示しています。</span><span class="sxs-lookup"><span data-stu-id="98f4a-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="98f4a-118">**値**</span><span class="sxs-lookup"><span data-stu-id="98f4a-118">**Value**</span></span>|<span data-ttu-id="98f4a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="98f4a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98f4a-120">0</span><span class="sxs-lookup"><span data-stu-id="98f4a-120">0</span></span>  <br/> |<span data-ttu-id="98f4a-121">ドキュメントがチェック アウトされていません。</span><span class="sxs-lookup"><span data-stu-id="98f4a-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="98f4a-122">1</span><span class="sxs-lookup"><span data-stu-id="98f4a-122">1</span></span>  <br/> |<span data-ttu-id="98f4a-123">ドキュメントが現在のユーザーにチェック アウトします。</span><span class="sxs-lookup"><span data-stu-id="98f4a-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="98f4a-124">2</span><span class="sxs-lookup"><span data-stu-id="98f4a-124">2</span></span>  <br/> |<span data-ttu-id="98f4a-125">ドキュメントがチェック アウトされていません、ですが、現在のユーザーが現在のコンピューター上で編集するために保存するファイルのコピーを持っています。</span><span class="sxs-lookup"><span data-stu-id="98f4a-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="98f4a-126">このプロパティは、ローカルで計算されがサーバーに送信されません、いつでもユーザーが別のアカウントにアイテムをドラッグしない限り。</span><span class="sxs-lookup"><span data-stu-id="98f4a-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="98f4a-127">その場合は、ユーザー定義のカスタム プロパティとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="98f4a-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="98f4a-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="98f4a-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98f4a-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="98f4a-129">Protocol specifications</span></span>

<span data-ttu-id="98f4a-130">[MS OXPROPS]</span><span class="sxs-lookup"><span data-stu-id="98f4a-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="98f4a-131">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="98f4a-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98f4a-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="98f4a-132">Header files</span></span>

<span data-ttu-id="98f4a-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98f4a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="98f4a-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="98f4a-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98f4a-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="98f4a-135">See also</span></span>



[<span data-ttu-id="98f4a-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="98f4a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98f4a-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="98f4a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98f4a-138">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="98f4a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98f4a-139">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="98f4a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

