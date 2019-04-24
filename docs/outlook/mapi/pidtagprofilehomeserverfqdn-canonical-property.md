---
title: PidTagProfileHomeServerFQDN 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341595"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="40333-103">PidTagProfileHomeServerFQDN 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="40333-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="40333-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40333-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40333-105">プロファイル構成の Kerberos 認証を有効にします。</span><span class="sxs-lookup"><span data-stu-id="40333-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="40333-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="40333-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40333-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="40333-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="40333-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="40333-108">Identifier:</span></span>  <br/> |<span data-ttu-id="40333-109">0x662a001f</span><span class="sxs-lookup"><span data-stu-id="40333-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="40333-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="40333-110">Data type:</span></span>  <br/> |<span data-ttu-id="40333-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40333-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="40333-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="40333-112">Area:</span></span>  <br/> |<span data-ttu-id="40333-113">MAPI プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="40333-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40333-114">解説</span><span class="sxs-lookup"><span data-stu-id="40333-114">Remarks</span></span>

<span data-ttu-id="40333-115">このプロパティをユーザーのディレクトリサーバーのドメイン名に設定すると、ドメインコントローラー (DC) への直接接続が許可されます。これは、Microsoft Exchange server 2007 に対して Kerberos 認証を使用するように構成されているプロファイルに必要です。以前のバージョンでは、 **PR_PROFILE_AUTH_PACKAGE**で**RPC_C_AUTHN_GSS_KERBEROS**を設定します。</span><span class="sxs-lookup"><span data-stu-id="40333-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="40333-116">Microsoft exchange server 2010 および exchange server 2013 は、クライアントアクセスサーバーに対して行われたアドレス帳呼び出しを、exchange server 2007 および以前のバージョンで処理する方法とは異なる方法で処理します。</span><span class="sxs-lookup"><span data-stu-id="40333-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="40333-117">DSProxy プロセスは使用されなくなったため、Kerberos 認証が成功する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="40333-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="40333-118">ただし、クライアントは依然として DC ではなく Exchange サーバーと通信していますが、これは望ましくない場合があります。 **PR_PROFILE_HOME_SERVER_FQDN**を設定すると、これを回避できます。</span><span class="sxs-lookup"><span data-stu-id="40333-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="40333-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="40333-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40333-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="40333-120">Protocol specifications</span></span>

<span data-ttu-id="40333-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40333-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40333-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="40333-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="40333-123">[[OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40333-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40333-124">コアメッセージストアオブジェクトに対する許容される操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="40333-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40333-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="40333-125">Header files</span></span>

<span data-ttu-id="40333-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40333-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="40333-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="40333-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="40333-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="40333-128">Mapitags.h</span></span>
  
> <span data-ttu-id="40333-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="40333-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40333-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="40333-130">See also</span></span>



[<span data-ttu-id="40333-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="40333-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40333-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="40333-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40333-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="40333-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40333-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="40333-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

