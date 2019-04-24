---
title: PidTagDefaultPostMessageClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0ab904625d3a23462a4fedf3b64f49c54b34ad28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357905"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a><span data-ttu-id="b6928-103">PidTagDefaultPostMessageClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b6928-103">PidTagDefaultPostMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="b6928-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6928-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6928-105">ユーザー設定フォームのメッセージクラスの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b6928-105">Contains the name of a custom form Message class.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6928-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b6928-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6928-107">PR_DEF_POST_MSGCLASS</span><span class="sxs-lookup"><span data-stu-id="b6928-107">PR_DEF_POST_MSGCLASS</span></span>  <br/> |
|<span data-ttu-id="b6928-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b6928-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6928-109">0x36E5</span><span class="sxs-lookup"><span data-stu-id="b6928-109">0x36E5</span></span>  <br/> |
|<span data-ttu-id="b6928-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b6928-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6928-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="b6928-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="b6928-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b6928-112">Area:</span></span>  <br/> |<span data-ttu-id="b6928-113">MAPI コンテナー</span><span class="sxs-lookup"><span data-stu-id="b6928-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6928-114">解説</span><span class="sxs-lookup"><span data-stu-id="b6928-114">Remarks</span></span>

<span data-ttu-id="b6928-115">このプロパティがフォルダーに設定されている場合、値には、完全に基本メッセージクラス (たとえば、"IPM.連絡先フォルダーまたは IPM.予定表フォルダーの場合)、または基本メッセージクラス (例: "IPM.contact. mycontact ")。</span><span class="sxs-lookup"><span data-stu-id="b6928-115">If this property is set on a folder, the value must contain either exactly the base message class (for example, "IPM.Contact" for a contacts folder or "IPM.Appointment" for a calendar folder), or begin with the base message class (for example, "IPM.Contact.MyContact").</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b6928-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b6928-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b6928-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b6928-117">Protocol specifications</span></span>

<span data-ttu-id="b6928-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6928-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6928-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b6928-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b6928-120">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6928-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6928-121">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6928-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b6928-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="b6928-122">Header files</span></span>

<span data-ttu-id="b6928-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6928-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6928-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b6928-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6928-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="b6928-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b6928-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b6928-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6928-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6928-127">See also</span></span>



[<span data-ttu-id="b6928-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b6928-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6928-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b6928-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6928-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b6928-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6928-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b6928-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

