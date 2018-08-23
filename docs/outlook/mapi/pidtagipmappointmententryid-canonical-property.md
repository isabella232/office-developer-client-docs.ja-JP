---
title: PidTagIpmAppointmentEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmAppointmentEntryId
api_type:
- HeaderDef
ms.assetid: a6e8c8fb-b76a-4a73-b112-6399e4d94233
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 231b905c4288379384530c7b35200eefb63479d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802905"
---
# <a name="pidtagipmappointmententryid-canonical-property"></a><span data-ttu-id="1c8cb-103">PidTagIpmAppointmentEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1c8cb-103">PidTagIpmAppointmentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1c8cb-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c8cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c8cb-105">Outlook の予定表フォルダーの**エントリ Id**が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-105">Contains the **EntryID** of the Outlook Calendar folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c8cb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1c8cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c8cb-107">PR_IPM_APPOINTMENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1c8cb-107">PR_IPM_APPOINTMENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1c8cb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1c8cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c8cb-109">0x36D0</span><span class="sxs-lookup"><span data-stu-id="1c8cb-109">0x36D0</span></span>  <br/> |
|<span data-ttu-id="1c8cb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1c8cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c8cb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1c8cb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1c8cb-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1c8cb-112">Area:</span></span>  <br/> |<span data-ttu-id="1c8cb-113">Folder</span><span class="sxs-lookup"><span data-stu-id="1c8cb-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c8cb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1c8cb-114">Remarks</span></span>

<span data-ttu-id="1c8cb-115">このプロパティは、[受信トレイ] フォルダーで、メッセージ ・ ストアのルート フォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="1c8cb-116">特定のメッセージ ストアのプロパティにアクセスするには、次の。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-116">To access the property on a specific message store, do the following.</span></span> 
  
1. <span data-ttu-id="1c8cb-117">最初に、受信トレイ フォルダー内のプロパティを探します。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="1c8cb-118">[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を使用すると、受信トレイ フォルダーの**エントリ Id**への参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="1c8cb-119">**IMsgStore::GetReceiveFolder**が成功した場合は、受信トレイを開き、 **IMAPIFolder**オブジェクトへの参照を取得する、受信トレイと[IMsgStore::OpenEntry](imsgstore-openentry.md)の**エントリ Id**への参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="1c8cb-120">**IMsgStore::OpenEntry**が成功した場合は、目的のプロパティを取得する**IMAPIFolder**オブジェクトと[IMAPIProp::GetProps](imapiprop-getprops.md)に返される参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="1c8cb-121">1、2、または 3 の手順が失敗した場合は、ルート フォルダーのプロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="1c8cb-122">そのためには、 **IMsgStore::OpenEntry**、 **lpEntryID**のメッセージ ・ ストアのルート フォルダーを開き、 **IMAPIFolder**オブジェクトへの参照を取得するのには NULL を指定するを使用します。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="1c8cb-123">ルート フォルダーを開くときに成功した場合は、目的のプロパティを取得するのには、 **IMAPIFolder**オブジェクトと**IMAPIProp::GetProps**に返される参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="1c8cb-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1c8cb-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c8cb-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1c8cb-125">Protocol specifications</span></span>

<span data-ttu-id="1c8cb-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c8cb-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c8cb-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c8cb-128">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c8cb-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c8cb-129">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1c8cb-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1c8cb-130">Header files</span></span>

<span data-ttu-id="1c8cb-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c8cb-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c8cb-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="1c8cb-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1c8cb-133">Mapitags.h</span></span>
  
> <span data-ttu-id="1c8cb-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c8cb-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c8cb-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="1c8cb-135">See also</span></span>



[<span data-ttu-id="1c8cb-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1c8cb-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c8cb-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1c8cb-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c8cb-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1c8cb-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c8cb-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1c8cb-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

