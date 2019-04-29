---
title: MAPI アドレスの種類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b0ff4ecff7a6e834f1e017adc11244657896db03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405437"
---
# <a name="mapi-address-types"></a><span data-ttu-id="43b99-103">MAPI アドレスの種類</span><span class="sxs-lookup"><span data-stu-id="43b99-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="43b99-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43b99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43b99-105">すべてのメッセージングユーザーは、 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティに格納されているユーザーのアドレスの形式を示す文字列であるアドレスの種類に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="43b99-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="43b99-106">アドレスの種類は、アドレス形式にマップされます。</span><span class="sxs-lookup"><span data-stu-id="43b99-106">Address types map to address formats.</span></span> <span data-ttu-id="43b99-107">つまり、受信者のアドレスの種類を調べることで、クライアントアプリケーションは受信者に適したアドレスを書式設定する方法を判断できます。</span><span class="sxs-lookup"><span data-stu-id="43b99-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="43b99-108">たとえば、アドレスの`SMTP`種類は標準のインターネットアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="43b99-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="43b99-109">そして、アドレス`EX`の種類は、Exchange サーバーのアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="43b99-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="43b99-110">すべてのアドレス帳エントリには、有効なアドレスの種類を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43b99-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="43b99-111">クライアントは、アドレス帳プロバイダーによってサポートされていない種類のカスタム受信者を作成するときに、ユーザーにアドレスの種類を指定するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="43b99-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="43b99-112">サポートされているエントリについては、アドレス帳プロバイダーが有効なアドレスの種類を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43b99-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="43b99-113">MAPI では、個人用配布リストを表すアドレスの種類として、mapipdl が1つだけ定義されています。</span><span class="sxs-lookup"><span data-stu-id="43b99-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="43b99-114">セッション内のすべてのトランスポートプロバイダーでサポートされているアドレスの種類の一覧を取得するために、クライアントアプリケーションは**imapisession:: enumadrtypes**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="43b99-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="43b99-115">詳細については、「 [imapisession:: enumadrtypes](imapisession-enumadrtypes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43b99-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

