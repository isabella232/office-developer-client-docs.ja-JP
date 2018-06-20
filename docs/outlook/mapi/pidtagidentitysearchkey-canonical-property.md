---
title: PidTagIdentitySearchKey の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 28c269db15d0c0a81950a61ee9e6629ad067b789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802826"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="29260-103">PidTagIdentitySearchKey の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="29260-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="29260-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="29260-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="29260-105">メッセージング システム内で定義されているように、サービス プロバイダーの id の検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="29260-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29260-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="29260-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29260-107">PR_IDENTITY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="29260-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="29260-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="29260-108">Identifier:</span></span>  <br/> |<span data-ttu-id="29260-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="29260-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="29260-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="29260-110">Data type:</span></span>  <br/> |<span data-ttu-id="29260-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="29260-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="29260-112">領域:</span><span class="sxs-lookup"><span data-stu-id="29260-112">Area:</span></span>  <br/> |<span data-ttu-id="29260-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="29260-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29260-114">備考</span><span class="sxs-lookup"><span data-stu-id="29260-114">Remarks</span></span>

<span data-ttu-id="29260-115">状態テーブル内の列としてのみですが、任意のオブジェクトのプロパティとしては、このプロパティは表示されません。</span><span class="sxs-lookup"><span data-stu-id="29260-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="29260-116">状態テーブルの行を公開するサービス ・ プロバイダーの id の一部であります。</span><span class="sxs-lookup"><span data-stu-id="29260-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="29260-117">プロバイダーの識別情報は通常、サーバー上のアカウントを参照が、プロバイダーは、メッセージング システム内で定義された表現を参照できます。</span><span class="sxs-lookup"><span data-stu-id="29260-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="29260-118">Id プロパティのいずれかを使用する際、サービス プロバイダーは、それらのすべてを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29260-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="29260-119">同じメッセージ サービスに属しているプロバイダーには、id プロパティに同じ値を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29260-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="29260-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="29260-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="29260-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="29260-121">Header files</span></span>

<span data-ttu-id="29260-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29260-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="29260-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="29260-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="29260-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="29260-124">Mapitags.h</span></span>
  
> <span data-ttu-id="29260-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="29260-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29260-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="29260-126">See also</span></span>



[<span data-ttu-id="29260-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="29260-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="29260-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="29260-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29260-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="29260-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29260-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="29260-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29260-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="29260-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

