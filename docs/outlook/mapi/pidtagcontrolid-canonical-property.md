---
title: PidTagControlId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 799f83b397cbef9d7dcb6c9a88154b88afe35675
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19802632"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="731f2-103">PidTagControlId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="731f2-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="731f2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="731f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="731f2-105">ダイアログ ボックスで使用されているコントロールの一意の識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="731f2-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="731f2-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="731f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="731f2-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="731f2-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="731f2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="731f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="731f2-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="731f2-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="731f2-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="731f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="731f2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="731f2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="731f2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="731f2-112">Area:</span></span>  <br/> |<span data-ttu-id="731f2-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="731f2-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="731f2-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="731f2-114">Remarks</span></span>

<span data-ttu-id="731f2-115">このプロパティには、コントロールの一意の識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="731f2-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="731f2-116">この識別子には、 [GUID](guid.md)の構造体と、 **LONG**型のバイナリ値を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="731f2-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="731f2-117">ダイアログ ボックス内のすべてのコントロールは、サービス プロバイダーを識別するのには、同じ**GUID**を使用する必要があり、各コントロールは、一意で使用する**コントロールが競合していないことを確認します**。</span><span class="sxs-lookup"><span data-stu-id="731f2-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="731f2-118">このプロパティは、通知で使用されます。</span><span class="sxs-lookup"><span data-stu-id="731f2-118">This property is used in notifications.</span></span> <span data-ttu-id="731f2-119">などのディスプレイ テーブルに送信された通知は、更新するコントロールを一意に識別するには、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="731f2-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="731f2-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="731f2-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="731f2-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="731f2-121">Header files</span></span>

<span data-ttu-id="731f2-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="731f2-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="731f2-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="731f2-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="731f2-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="731f2-124">Mapitags.h</span></span>
  
> <span data-ttu-id="731f2-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="731f2-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="731f2-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="731f2-126">See also</span></span>



[<span data-ttu-id="731f2-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="731f2-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="731f2-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="731f2-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="731f2-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="731f2-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="731f2-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="731f2-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

