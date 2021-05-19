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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415055"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="b5340-103">PidTagReceiveFolderSettings 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b5340-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="b5340-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5340-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5340-105">メッセージ ストアの受信フォルダー設定のテーブルが含まれる。</span><span class="sxs-lookup"><span data-stu-id="b5340-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5340-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b5340-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5340-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="b5340-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="b5340-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b5340-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5340-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="b5340-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="b5340-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b5340-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5340-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="b5340-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="b5340-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b5340-112">Area:</span></span>  <br/> |<span data-ttu-id="b5340-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="b5340-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5340-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b5340-114">Remarks</span></span>

<span data-ttu-id="b5340-115">このプロパティは [、IMAPIProp::CopyTo](imapiprop-copyto.md) 操作で除外するか [、IMAPIProp::CopyProps 操作に含](imapiprop-copyprops.md) めできます。</span><span class="sxs-lookup"><span data-stu-id="b5340-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="b5340-116">型のプロパティPT_OBJECT [IMAPIProp::GetProps メソッドでは正常に取得](imapiprop-getprops.md) できません。その内容にアクセスするには [、IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを使用して、識別子を持つインターフェイスを要求IID_IMAPITable。</span><span class="sxs-lookup"><span data-stu-id="b5340-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="b5340-117">サービス プロバイダーは [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが設定されている場合は、それを報告する必要がありますが、設定されていない場合はオプションで報告できます。</span><span class="sxs-lookup"><span data-stu-id="b5340-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="b5340-118">表の内容を取得するには、クライアント アプリケーションが [IMsgStore::GetReceiveFolderTable メソッドを呼び出す必要](imsgstore-getreceivefoldertable.md) があります。</span><span class="sxs-lookup"><span data-stu-id="b5340-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="b5340-119">詳細については、「受信フォルダー テーブル [」を参照してください](receive-folder-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="b5340-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="b5340-120">このプロパティには、メッセージ ストアの受信フォルダーのマッピングのテーブルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5340-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="b5340-121">この **プロパティで OpenProperty** を呼び出すのは、メッセージ ストアで **GetReceiveFolderTable** を呼び出すのと同じです。</span><span class="sxs-lookup"><span data-stu-id="b5340-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b5340-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b5340-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b5340-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b5340-123">Header files</span></span>

<span data-ttu-id="b5340-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5340-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5340-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b5340-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5340-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b5340-126">Mapitags.h</span></span>
  
> <span data-ttu-id="b5340-127">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="b5340-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5340-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b5340-128">See also</span></span>



[<span data-ttu-id="b5340-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b5340-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5340-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b5340-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5340-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b5340-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5340-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b5340-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

