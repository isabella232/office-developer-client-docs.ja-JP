---
title: PidLidSharingRemoteName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteName
api_type:
- COM
ms.assetid: be975f74-4b95-45a4-bbee-959fa8e4ad45
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fc3324cb686733f06b9cc0945c93b7df2e5980ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802171"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="63a94-103">PidLidSharingRemoteName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="63a94-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="63a94-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63a94-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63a94-105">共有されているリモート コンピューターのフォルダーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="63a94-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="63a94-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="63a94-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63a94-107">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="63a94-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="63a94-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="63a94-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="63a94-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="63a94-109">Property set:</span></span>  <br/> |<span data-ttu-id="63a94-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="63a94-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="63a94-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="63a94-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="63a94-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="63a94-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="63a94-113">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="63a94-113">Data type:</span></span>  <br/> |<span data-ttu-id="63a94-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="63a94-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="63a94-115">領域:</span><span class="sxs-lookup"><span data-stu-id="63a94-115">Area:</span></span>  <br/> |<span data-ttu-id="63a94-116">共有</span><span class="sxs-lookup"><span data-stu-id="63a94-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63a94-117">備考</span><span class="sxs-lookup"><span data-stu-id="63a94-117">Remarks</span></span>

<span data-ttu-id="63a94-118">このプロパティは、共有されているフォルダーの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63a94-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="63a94-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="63a94-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63a94-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="63a94-120">Protocol specifications</span></span>

<span data-ttu-id="63a94-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63a94-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63a94-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="63a94-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63a94-123">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63a94-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63a94-124">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="63a94-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63a94-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="63a94-125">Header files</span></span>

<span data-ttu-id="63a94-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63a94-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="63a94-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="63a94-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63a94-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="63a94-128">See also</span></span>



[<span data-ttu-id="63a94-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="63a94-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63a94-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="63a94-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63a94-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="63a94-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63a94-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="63a94-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

