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
# <a name="mapi-address-types"></a><span data-ttu-id="440f4-103">MAPI アドレスの種類</span><span class="sxs-lookup"><span data-stu-id="440f4-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="440f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="440f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="440f4-105">すべてのメッセージング ユーザーは、PR_ADDRTYPE **(** [PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティに格納されているユーザーのアドレスの形式を表す文字列であるアドレスの種類に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="440f4-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="440f4-106">アドレスの種類は、アドレス形式にマップされます。</span><span class="sxs-lookup"><span data-stu-id="440f4-106">Address types map to address formats.</span></span> <span data-ttu-id="440f4-107">つまり、受信者のアドレスの種類を確認することで、クライアント アプリケーションは、受信者に適したアドレスを書式設定する方法を決定できます。</span><span class="sxs-lookup"><span data-stu-id="440f4-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="440f4-108">たとえば、アドレスの  `SMTP` 種類は、標準のインターネット アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="440f4-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="440f4-109">また、アドレス `EX` の種類は、アドレスのExchange Serverします。</span><span class="sxs-lookup"><span data-stu-id="440f4-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="440f4-110">すべてのアドレス帳エントリには、有効なアドレスの種類が必要です。</span><span class="sxs-lookup"><span data-stu-id="440f4-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="440f4-111">クライアントは、アドレス帳プロバイダーでサポートされていない種類のカスタム受信者を作成するときに、ユーザーにアドレスの種類を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="440f4-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="440f4-112">サポートするエントリについては、有効なアドレスの種類を指定するためにアドレス帳プロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="440f4-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="440f4-113">MAPI では、個人配布リストを表す MAPIPDL という 1 つのアドレスの種類のみを定義します。</span><span class="sxs-lookup"><span data-stu-id="440f4-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="440f4-114">セッション内のすべてのトランスポート プロバイダーでサポートされているアドレスの種類の一覧を取得するには、クライアント アプリケーションは **IMAPISession::EnumAdrTypes** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="440f4-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="440f4-115">詳細については [、「IMAPISession::EnumAdrTypes」を参照してください](imapisession-enumadrtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="440f4-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

