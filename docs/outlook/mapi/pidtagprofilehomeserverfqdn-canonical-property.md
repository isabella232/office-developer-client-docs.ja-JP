---
title: PidTagProfileHomeServerFQDN の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 398ff2fd4bab49c8279e198e3efa416c53abda7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803189"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="6f7c7-103">PidTagProfileHomeServerFQDN の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6f7c7-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="6f7c7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f7c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f7c7-105">プロファイル構成の Kerberos 認証を有効にします。</span><span class="sxs-lookup"><span data-stu-id="6f7c7-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="6f7c7-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="6f7c7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f7c7-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="6f7c7-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="6f7c7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6f7c7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f7c7-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="6f7c7-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="6f7c7-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="6f7c7-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f7c7-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6f7c7-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6f7c7-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6f7c7-112">Area:</span></span>  <br/> |<span data-ttu-id="6f7c7-113">MAPI プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="6f7c7-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f7c7-114">備考</span><span class="sxs-lookup"><span data-stu-id="6f7c7-114">Remarks</span></span>

<span data-ttu-id="6f7c7-115">により直接接続するドメイン コント ローラー (DC)、Microsoft Exchange Server 2007 に対して Kerberos 認証を使用するように構成されたプロファイルに必要なユーザーのディレクトリ サーバーのドメイン名にこのプロパティを設定し、以前のバージョンで**PR_PROFILE_AUTH_PACKAGE**で**RPC_C_AUTHN_GSS_KERBEROS**を設定します。</span><span class="sxs-lookup"><span data-stu-id="6f7c7-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6f7c7-116">Microsoft Exchange Server 2010 と Exchange Server 2013 は、アドレス帳からの呼び出しをクライアント アクセス サーバーとは異なるで Exchange Server 2007 と以前のバージョンを処理する方法を処理します。</span><span class="sxs-lookup"><span data-stu-id="6f7c7-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="6f7c7-117">DSProxy プロセスは使用されませんので、Kerberos 認証が成功することがあります。</span><span class="sxs-lookup"><span data-stu-id="6f7c7-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="6f7c7-118">ただし、クライアントがあると通信できている Exchange サーバーの代わりに直接、DC では、適さない場合があります: 設定**PR_PROFILE_HOME_SERVER_FQDN**がこれを回避できます。</span><span class="sxs-lookup"><span data-stu-id="6f7c7-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6f7c7-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6f7c7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f7c7-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6f7c7-120">Protocol specifications</span></span>

<span data-ttu-id="6f7c7-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f7c7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f7c7-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6f7c7-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6f7c7-123">[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f7c7-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f7c7-124">コア メッセージのストア オブジェクトの許可された操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6f7c7-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f7c7-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6f7c7-125">Header files</span></span>

<span data-ttu-id="6f7c7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f7c7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f7c7-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6f7c7-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f7c7-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f7c7-128">Mapitags.h</span></span>
  
> <span data-ttu-id="6f7c7-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f7c7-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f7c7-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f7c7-130">See also</span></span>



[<span data-ttu-id="6f7c7-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6f7c7-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f7c7-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6f7c7-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f7c7-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="6f7c7-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f7c7-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="6f7c7-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

