---
title: PidTagProfileHomeServerFQDN 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341595"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="ebafb-103">PidTagProfileHomeServerFQDN 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ebafb-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="ebafb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebafb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebafb-105">プロファイル構成の Kerberos 認証を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ebafb-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="ebafb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ebafb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ebafb-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="ebafb-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="ebafb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ebafb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ebafb-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="ebafb-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="ebafb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ebafb-110">Data type:</span></span>  <br/> |<span data-ttu-id="ebafb-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ebafb-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ebafb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ebafb-112">Area:</span></span>  <br/> |<span data-ttu-id="ebafb-113">MAPI プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="ebafb-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebafb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ebafb-114">Remarks</span></span>

<span data-ttu-id="ebafb-115">このプロパティをユーザーのディレクトリ サーバーのドメイン名に設定すると、PR_PROFILE_AUTH_PACKAGE で **RPC_C_AUTHN_GSS_KERBEROS** を設定することにより、Microsoft Exchange Server 2007 以前のバージョンに対して Kerberos 認証を使用するように構成されているプロファイルに必要なドメイン コントローラー (DC) に直接接続できます。 </span><span class="sxs-lookup"><span data-stu-id="ebafb-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ebafb-116">Microsoft Exchange Server 2010 および Exchange Server 2013 は、クライアント アクセス サーバーに対して行われたアドレス帳の呼び出しを、Exchange Server 2007 以前のバージョンで処理する方法とは異なる方法で処理します。</span><span class="sxs-lookup"><span data-stu-id="ebafb-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="ebafb-117">DSProxy プロセスは使用されなくなったので、Kerberos 認証が成功する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ebafb-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="ebafb-118">ただし、クライアントは DC と直接通信するのではなく、Exchange サーバーと通信します。これは望PR_PROFILE_HOME_SERVER_FQDNしません。 </span><span class="sxs-lookup"><span data-stu-id="ebafb-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ebafb-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ebafb-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ebafb-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ebafb-120">Protocol specifications</span></span>

<span data-ttu-id="ebafb-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebafb-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebafb-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="ebafb-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ebafb-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebafb-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebafb-124">コア メッセージ ストア オブジェクトに対して許容される操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ebafb-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ebafb-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ebafb-125">Header files</span></span>

<span data-ttu-id="ebafb-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ebafb-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ebafb-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ebafb-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="ebafb-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ebafb-128">Mapitags.h</span></span>
  
> <span data-ttu-id="ebafb-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ebafb-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ebafb-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="ebafb-130">See also</span></span>



[<span data-ttu-id="ebafb-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ebafb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ebafb-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ebafb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ebafb-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ebafb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ebafb-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ebafb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

