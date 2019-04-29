---
title: PidTagIpmSentMailEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSentMailEntryId
api_type:
- HeaderDef
ms.assetid: f6877435-6b26-4060-924f-a65591ad9538
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fd29afc93bc952bb619dfac752fae232bf7991cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437323"
---
# <a name="pidtagipmsentmailentryid-canonical-property"></a><span data-ttu-id="9c7ac-103">PidTagIpmSentMailEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9c7ac-103">PidTagIpmSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="9c7ac-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c7ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c7ac-105">標準の個人間メッセージ (IPM) の送信済みアイテムフォルダーのエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="9c7ac-105">Contains the entry identifier of the standard interpersonal message (IPM) Sent Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c7ac-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9c7ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9c7ac-107">PR_IPM_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9c7ac-107">PR_IPM_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="9c7ac-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9c7ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9c7ac-109">0x35e4</span><span class="sxs-lookup"><span data-stu-id="9c7ac-109">0x35E4</span></span>  <br/> |
|<span data-ttu-id="9c7ac-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9c7ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="9c7ac-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9c7ac-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9c7ac-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9c7ac-112">Area:</span></span>  <br/> |<span data-ttu-id="9c7ac-113">フォルダー</span><span class="sxs-lookup"><span data-stu-id="9c7ac-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c7ac-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9c7ac-114">Remarks</span></span>

<span data-ttu-id="9c7ac-115">送信後、個人間メッセージは通常、[送信済みアイテム] フォルダーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="9c7ac-115">After being sent, interpersonal messages are usually placed in the Sent Items folder.</span></span> <span data-ttu-id="9c7ac-116">クライアントは、このプロパティを使用して、送信されたメッセージに対して**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9c7ac-116">A client can use this property to set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property on a submitted message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9c7ac-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9c7ac-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9c7ac-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9c7ac-118">Header files</span></span>

<span data-ttu-id="9c7ac-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c7ac-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9c7ac-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9c7ac-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9c7ac-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9c7ac-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9c7ac-122">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9c7ac-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c7ac-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c7ac-123">See also</span></span>



[<span data-ttu-id="9c7ac-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9c7ac-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9c7ac-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9c7ac-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9c7ac-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9c7ac-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9c7ac-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9c7ac-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

