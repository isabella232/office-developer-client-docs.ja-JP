---
title: PidTagDelegateFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392278"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="de3eb-103">PidTagDelegateFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="de3eb-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="de3eb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de3eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de3eb-105">代理人が代理人の秘密のメッセージ オブジェクトを表示するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="de3eb-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de3eb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="de3eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de3eb-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="de3eb-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="de3eb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="de3eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de3eb-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="de3eb-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="de3eb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="de3eb-110">Data type:</span></span>  <br/> |<span data-ttu-id="de3eb-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="de3eb-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="de3eb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="de3eb-112">Area:</span></span>  <br/> |<span data-ttu-id="de3eb-113">クラスによって定義されたメッセージ送信できます。</span><span class="sxs-lookup"><span data-stu-id="de3eb-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de3eb-114">備考</span><span class="sxs-lookup"><span data-stu-id="de3eb-114">Remarks</span></span>

<span data-ttu-id="de3eb-115">このプロパティの各エントリを次の値のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de3eb-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="de3eb-116">**Flag**</span><span class="sxs-lookup"><span data-stu-id="de3eb-116">**Flag**</span></span>|<span data-ttu-id="de3eb-117">**値**</span><span class="sxs-lookup"><span data-stu-id="de3eb-117">**Value**</span></span>|<span data-ttu-id="de3eb-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="de3eb-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de3eb-119">HidePrivate</span><span class="sxs-lookup"><span data-stu-id="de3eb-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="de3eb-120">0</span><span class="sxs-lookup"><span data-stu-id="de3eb-120">0</span></span>  <br/> |<span data-ttu-id="de3eb-121">プライベート メッセージ オブジェクトを表示するのにはデリゲートを使用できませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="de3eb-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="de3eb-122">ShowPrivate</span><span class="sxs-lookup"><span data-stu-id="de3eb-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="de3eb-123">1</span><span class="sxs-lookup"><span data-stu-id="de3eb-123">1</span></span>  <br/> |<span data-ttu-id="de3eb-124">デリゲートは、オブジェクトのプライベート メッセージを表示するのにはできます。</span><span class="sxs-lookup"><span data-stu-id="de3eb-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="de3eb-125">代理人の情報オブジェクトにこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de3eb-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="de3eb-126">"ShowPrivate"の値は、オブジェクトのプライベート メッセージが表示されるようにするのには、代理人が要求していることを示します。</span><span class="sxs-lookup"><span data-stu-id="de3eb-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="de3eb-127">この設定は、代理人の校閲者、作成者、または編集者の役割を持っているすべてのフォルダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="de3eb-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="de3eb-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="de3eb-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de3eb-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="de3eb-129">Protocol specifications</span></span>

<span data-ttu-id="de3eb-130">[[MS OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de3eb-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de3eb-131">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="de3eb-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de3eb-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="de3eb-132">Header files</span></span>

<span data-ttu-id="de3eb-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de3eb-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="de3eb-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="de3eb-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="de3eb-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="de3eb-135">Mapitags.h</span></span>
  
> <span data-ttu-id="de3eb-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de3eb-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de3eb-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="de3eb-137">See also</span></span>



[<span data-ttu-id="de3eb-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="de3eb-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de3eb-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="de3eb-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de3eb-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="de3eb-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de3eb-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="de3eb-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

