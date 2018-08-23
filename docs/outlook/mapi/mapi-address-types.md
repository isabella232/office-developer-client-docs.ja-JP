---
title: MAPI アドレスの種類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 20eb429b2574f67e8b28ae96eeb96f42840123d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801312"
---
# <a name="mapi-address-types"></a><span data-ttu-id="331a6-103">MAPI アドレスの種類</span><span class="sxs-lookup"><span data-stu-id="331a6-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="331a6-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="331a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="331a6-105">メッセージングのすべてのユーザーは、アドレスの種類、 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) のプロパティに格納されているユーザーのアドレスの形式を記述する文字の文字列に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="331a6-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="331a6-106">アドレスの種類は、アドレスの形式にマップします。</span><span class="sxs-lookup"><span data-stu-id="331a6-106">Address types map to address formats.</span></span> <span data-ttu-id="331a6-107">受信者のアドレスの種類を見ると、により、クライアント アプリケーションは、受信者に適切なアドレスの書式を設定する方法を決定できます。</span><span class="sxs-lookup"><span data-stu-id="331a6-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="331a6-108">などの`SMTP`のアドレスの種類は、標準的なインターネット アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="331a6-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="331a6-109">`EX`のアドレスの種類は、Exchange Server のアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="331a6-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="331a6-110">すべてのアドレス帳のエントリには、有効なアドレスの種類が必要です。</span><span class="sxs-lookup"><span data-stu-id="331a6-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="331a6-111">クライアントでは、ユーザーのカスタム受信者のアドレス帳プロバイダーでサポートされていない型を作成するときに、アドレスの種類を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="331a6-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="331a6-112">、それらをサポートしているエントリのアドレス帳プロバイダーは、有効なアドレスの種類を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="331a6-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="331a6-113">MAPI のみ 1 つのアドレスの種類を定義する: MAPIPDL は、個人用配布リストを意味します。</span><span class="sxs-lookup"><span data-stu-id="331a6-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="331a6-114">セッションのすべてのトランスポート プロバイダーによってサポートされているアドレスの種類の一覧を取得するには、クライアント アプリケーションは、 **IMAPISession::EnumAdrTypes**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="331a6-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="331a6-115">詳細については、 [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="331a6-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

