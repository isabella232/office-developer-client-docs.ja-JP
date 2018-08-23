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
ms.openlocfilehash: e93325873f1d9e89bb591d136df04aa27403375f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803278"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="9d73d-103">PidTagReceiveFolderSettings 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d73d-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="9d73d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d73d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d73d-105">メッセージのテーブルが含まれているストアのフォルダーの設定を表示します。</span><span class="sxs-lookup"><span data-stu-id="9d73d-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d73d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9d73d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d73d-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="9d73d-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="9d73d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9d73d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d73d-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="9d73d-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="9d73d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9d73d-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d73d-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="9d73d-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="9d73d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="9d73d-112">Area:</span></span>  <br/> |<span data-ttu-id="9d73d-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="9d73d-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d73d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9d73d-114">Remarks</span></span>

<span data-ttu-id="9d73d-115">このプロパティは、 [IMAPIProp::CopyTo](imapiprop-copyto.md)操作で除外または[IMAPIProp::CopyProps](imapiprop-copyprops.md)操作に含まれることができます。</span><span class="sxs-lookup"><span data-stu-id="9d73d-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="9d73d-116">PT_OBJECT の型のプロパティとして、正常に取得できません、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドで方式では[IMAPIProp::OpenProperty](imapiprop-openproperty.md) IID_IMAPITable の識別子を持つインターフェイスを要求するその内容にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d73d-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="9d73d-117">サービス プロバイダーする必要がありますに報告して、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドが設定されているが報告したことができます (オプション)、または設定されていない場合はありません。</span><span class="sxs-lookup"><span data-stu-id="9d73d-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="9d73d-118">テーブルの内容を取得するには、クライアント アプリケーションは、 [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d73d-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="9d73d-119">詳細については、[表示されるフォルダーのテーブル](receive-folder-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d73d-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="9d73d-120">このプロパティには、メッセージ ・ ストア用の受信フォルダーのマッピングのテーブルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d73d-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="9d73d-121">このプロパティに**OpenProperty**を呼び出すことは、メッセージ ・ ストアに対して**GetReceiveFolderTable**を呼び出すことと同じです。</span><span class="sxs-lookup"><span data-stu-id="9d73d-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9d73d-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9d73d-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9d73d-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9d73d-123">Header files</span></span>

<span data-ttu-id="9d73d-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d73d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d73d-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d73d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d73d-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9d73d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9d73d-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d73d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d73d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d73d-128">See also</span></span>



[<span data-ttu-id="9d73d-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d73d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d73d-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d73d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d73d-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9d73d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d73d-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9d73d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

