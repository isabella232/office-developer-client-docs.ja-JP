---
title: PidTagReceiveFolderSettings 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356743"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="e44c5-103">PidTagReceiveFolderSettings 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e44c5-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="e44c5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e44c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e44c5-105">メッセージストアの受信フォルダー設定のテーブルが保存されています。</span><span class="sxs-lookup"><span data-stu-id="e44c5-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e44c5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e44c5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e44c5-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="e44c5-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="e44c5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e44c5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e44c5-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="e44c5-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="e44c5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e44c5-110">Data type:</span></span>  <br/> |<span data-ttu-id="e44c5-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="e44c5-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="e44c5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e44c5-112">Area:</span></span>  <br/> |<span data-ttu-id="e44c5-113">MAPI メッセージストア</span><span class="sxs-lookup"><span data-stu-id="e44c5-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e44c5-114">解説</span><span class="sxs-lookup"><span data-stu-id="e44c5-114">Remarks</span></span>

<span data-ttu-id="e44c5-115">このプロパティは、 [imapiprop:: CopyTo](imapiprop-copyto.md)操作で除外することも、 [imapiprop:: copyprops](imapiprop-copyprops.md)操作に含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="e44c5-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="e44c5-116">PT_OBJECT 型のプロパティとして、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドによって正常に取得することはできません。このコンテンツには、IID_IMAPITable という識別子を持つインターフェイスを要求する[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドによってアクセスされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e44c5-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="e44c5-117">サービスプロバイダーは、設定されている場合は[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドに報告する必要がありますが、設定されていない場合はレポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="e44c5-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="e44c5-118">表の内容を取得するには、クライアントアプリケーションは[IMsgStore:: getreceivefoldertable](imsgstore-getreceivefoldertable.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e44c5-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="e44c5-119">詳細については、「[受信フォルダーテーブル](receive-folder-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e44c5-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="e44c5-120">このプロパティには、メッセージストアの受信フォルダーのマッピングの表が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e44c5-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="e44c5-121">このプロパティで**openproperty**を呼び出すことは、メッセージストアで**getreceivefoldertable**を呼び出すことと同じです。</span><span class="sxs-lookup"><span data-stu-id="e44c5-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e44c5-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e44c5-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e44c5-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e44c5-123">Header files</span></span>

<span data-ttu-id="e44c5-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e44c5-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="e44c5-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e44c5-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="e44c5-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e44c5-126">Mapitags.h</span></span>
  
> <span data-ttu-id="e44c5-127">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e44c5-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e44c5-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e44c5-128">See also</span></span>



[<span data-ttu-id="e44c5-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e44c5-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e44c5-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e44c5-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e44c5-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e44c5-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e44c5-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e44c5-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

