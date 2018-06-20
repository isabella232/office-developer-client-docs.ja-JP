---
title: PidLidInternetAccountName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountName
api_type:
- COM
ms.assetid: 29bedadf-903d-419d-804d-dc8bd92b745d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6705b121c58e0ff14726f835c779237cb35c32a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802003"
---
# <a name="pidlidinternetaccountname-canonical-property"></a><span data-ttu-id="70257-103">PidLidInternetAccountName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="70257-103">PidLidInternetAccountName Canonical Property</span></span>

  
  
<span data-ttu-id="70257-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="70257-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="70257-105">電子メール メッセージを送信するユーザーに表示されている電子メール アカウント名を指定します。</span><span class="sxs-lookup"><span data-stu-id="70257-105">Specifies the user-visible email account name through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70257-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="70257-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70257-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="70257-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="70257-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="70257-108">Property set:</span></span>  <br/> |<span data-ttu-id="70257-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="70257-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="70257-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="70257-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="70257-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="70257-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="70257-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="70257-112">Data type:</span></span>  <br/> |<span data-ttu-id="70257-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70257-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="70257-114">領域:</span><span class="sxs-lookup"><span data-stu-id="70257-114">Area:</span></span>  <br/> |<span data-ttu-id="70257-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="70257-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70257-116">備考</span><span class="sxs-lookup"><span data-stu-id="70257-116">Remarks</span></span>

<span data-ttu-id="70257-117">この文字列の形式は、実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="70257-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="70257-118">このプロパティは、メールを送信するサーバーを決定するのには、クライアントで使用できますが、オプションし、値は、サーバーに意味を持ちません。</span><span class="sxs-lookup"><span data-stu-id="70257-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="70257-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="70257-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="70257-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="70257-120">Protocol specifications</span></span>

<span data-ttu-id="70257-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70257-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70257-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="70257-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="70257-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70257-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70257-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="70257-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="70257-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="70257-125">Header files</span></span>

<span data-ttu-id="70257-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70257-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="70257-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="70257-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70257-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="70257-128">See also</span></span>



[<span data-ttu-id="70257-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="70257-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70257-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="70257-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70257-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="70257-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70257-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="70257-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

