---
title: PidTagLastModificationTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 653bdf26988c46be5f866cfbda331510c5a54afd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575708"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a><span data-ttu-id="1de75-103">PidTagLastModificationTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1de75-103">PidTagLastModificationTime Canonical Property</span></span>

  
  
<span data-ttu-id="1de75-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1de75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1de75-105">日付と時刻のオブジェクトまたはサブオブジェクトの最終変更日時が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1de75-105">Contains the date and time when the object or subobject was last modified.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1de75-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1de75-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1de75-107">PR_LAST_MODIFICATION_TIME</span><span class="sxs-lookup"><span data-stu-id="1de75-107">PR_LAST_MODIFICATION_TIME</span></span>  <br/> |
|<span data-ttu-id="1de75-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1de75-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1de75-109">0x3008</span><span class="sxs-lookup"><span data-stu-id="1de75-109">0x3008</span></span>  <br/> |
|<span data-ttu-id="1de75-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1de75-110">Data type:</span></span>  <br/> |<span data-ttu-id="1de75-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1de75-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1de75-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1de75-112">Area:</span></span>  <br/> |<span data-ttu-id="1de75-113">メッセージの時刻</span><span class="sxs-lookup"><span data-stu-id="1de75-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1de75-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1de75-114">Remarks</span></span>

<span data-ttu-id="1de75-115">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) のプロパティと同じ値には、このプロパティは設定が最初にします。</span><span class="sxs-lookup"><span data-stu-id="1de75-115">This property is initially set to the same value as the **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) property.</span></span> <span data-ttu-id="1de75-116">添付ファイルの下位オブジェクトを更新できます、必要に応じて、ネイティブ ファイル システムによって保持される最後の変更時刻をコピーすることによって。</span><span class="sxs-lookup"><span data-stu-id="1de75-116">Attachment subobjects can update it as necessary by copying the last modification time maintained by the native file system.</span></span> <span data-ttu-id="1de75-117">クライアント アプリケーションは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの最初の呼び出しまで、このプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1de75-117">A client application can set this property until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="1de75-118">プロバイダーは、すべての**IMAPIProp::SaveChanges**の呼び出し中に**PR_LAST_MODIFICATION_TIME**を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1de75-118">From then on the provider should update **PR_LAST_MODIFICATION_TIME** during every **IMAPIProp::SaveChanges** call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1de75-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1de75-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1de75-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1de75-120">Protocol specifications</span></span>

<span data-ttu-id="1de75-121">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1de75-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1de75-122">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="1de75-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="1de75-123">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1de75-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1de75-124">サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="1de75-124">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="1de75-125">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1de75-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1de75-126">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1de75-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1de75-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1de75-127">Header files</span></span>

<span data-ttu-id="1de75-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1de75-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="1de75-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1de75-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="1de75-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1de75-130">Mapitags.h</span></span>
  
> <span data-ttu-id="1de75-131">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1de75-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1de75-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="1de75-132">See also</span></span>



[<span data-ttu-id="1de75-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1de75-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1de75-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1de75-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1de75-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1de75-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1de75-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1de75-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

