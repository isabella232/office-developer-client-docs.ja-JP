---
title: PidTagControlId 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416021"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="98d13-103">PidTagControlId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="98d13-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="98d13-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98d13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98d13-105">ダイアログ ボックスで使用されるコントロールの一意の識別子を含む。</span><span class="sxs-lookup"><span data-stu-id="98d13-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98d13-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="98d13-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98d13-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="98d13-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="98d13-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="98d13-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98d13-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="98d13-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="98d13-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="98d13-110">Data type:</span></span>  <br/> |<span data-ttu-id="98d13-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="98d13-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="98d13-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="98d13-112">Area:</span></span>  <br/> |<span data-ttu-id="98d13-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="98d13-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98d13-114">注釈</span><span class="sxs-lookup"><span data-stu-id="98d13-114">Remarks</span></span>

<span data-ttu-id="98d13-115">このプロパティには、コントロールの一意の識別子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="98d13-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="98d13-116">この識別子には [、GUID](guid.md) 構造と LONG 型のバイナリ値が含 **まれている必要があります**。</span><span class="sxs-lookup"><span data-stu-id="98d13-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="98d13-117">ダイアログ ボックス内のすべてのコントロールは同じ **GUID** を使用してサービス プロバイダーを識別し、各コントロールは一意の **LONG** 値を使用してコントロールが衝突しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="98d13-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="98d13-118">このプロパティは、通知で使用されます。</span><span class="sxs-lookup"><span data-stu-id="98d13-118">This property is used in notifications.</span></span> <span data-ttu-id="98d13-119">たとえば、表示テーブルに送信される通知は、更新するコントロールを一意に識別するためにこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98d13-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="98d13-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="98d13-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="98d13-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="98d13-121">Header files</span></span>

<span data-ttu-id="98d13-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98d13-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="98d13-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="98d13-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="98d13-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98d13-124">Mapitags.h</span></span>
  
> <span data-ttu-id="98d13-125">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="98d13-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98d13-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="98d13-126">See also</span></span>



[<span data-ttu-id="98d13-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="98d13-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98d13-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="98d13-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98d13-129">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="98d13-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98d13-130">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="98d13-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

