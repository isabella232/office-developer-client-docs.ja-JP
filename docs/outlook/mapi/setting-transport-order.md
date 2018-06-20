---
title: トランスポート オーダを設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 71d7ebf2bc8c7bbf3b5ee6ce60959fdeee79abe3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803895"
---
# <a name="setting-transport-order"></a><span data-ttu-id="61a91-103">トランスポート オーダを設定</span><span class="sxs-lookup"><span data-stu-id="61a91-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="61a91-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61a91-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61a91-105">MAPI スプーラーに送信メッセージを処理できるトランスポート プロバイダーを宣言するための識別子とアドレスの種類に基づく責任が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="61a91-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="61a91-106">トランスポート プロバイダーがサポートされているアドレスの種類と識別子のリストを発行する- **MAPIUID**構造体に格納されている: MAPI がログオンの直後に、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すとします。</span><span class="sxs-lookup"><span data-stu-id="61a91-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="61a91-107">受信者のアドレスの種類は、 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="61a91-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="61a91-108">アドレスの種類を登録することを示します MAPI トランスポート プロバイダーは、登録されているアドレスの種類を設定、 **PR_ADDRTYPE**プロパティを使用して受信者に配信できること。</span><span class="sxs-lookup"><span data-stu-id="61a91-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="61a91-109">同様にの**MAPIUID**に登録するには、トランスポート プロバイダーが登録されている**MAPIUID**のエントリの識別子によって表される受信者に提供できることを示します。</span><span class="sxs-lookup"><span data-stu-id="61a91-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="61a91-110">ほとんどのトランスポート プロバイダーの登録の 1 つまたは複数のアドレスの種類です。数は、 **MAPIUID**で登録します。</span><span class="sxs-lookup"><span data-stu-id="61a91-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="61a91-111">アドレス帳プロバイダーと密に結合し、そのエントリの識別子の形式を理解するためのトランスポート プロバイダーは、 **MAPIUID**、それによってパフォーマンスの向上によってメッセージを処理するために登録できます。</span><span class="sxs-lookup"><span data-stu-id="61a91-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="61a91-112">このような密結合のトランスポート プロバイダーから抽出できます、受信者の電子メール アドレスおよびその他の必要な情報のエントリ id、 **IMAPISupport::OpenEntry**の呼び出しを使用してそれを開くことがなく。</span><span class="sxs-lookup"><span data-stu-id="61a91-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="61a91-113">MAPI は、トランスポート プロバイダーは、複数のトランスポート プロバイダーは、同じアドレスの種類または**MAPIUID**に登録しているときに使用される順序が維持されます。</span><span class="sxs-lookup"><span data-stu-id="61a91-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="61a91-114">[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)を呼び出すことによって、この順序を上書きすることができ、 _lpUIDList_パラメーターで指定されたすべてのアクティブなトランスポート プロバイダーの**MAPIUID**s の順序付きリストを渡すことです。。</span><span class="sxs-lookup"><span data-stu-id="61a91-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID**s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="61a91-115">アクティブなトランスポート プロバイダーの 1 つで処理可能なアドレスの種類のすべての一覧を取得するには、 [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="61a91-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="61a91-116">**EnumAdrTypes**は、現在のセッションでアクティブになっているトランスポート プロバイダーによってサポートされているアドレスの種類を説明する文字列の配列を返します。</span><span class="sxs-lookup"><span data-stu-id="61a91-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

