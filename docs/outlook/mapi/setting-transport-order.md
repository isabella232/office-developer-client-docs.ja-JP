---
title: トランスポート順序の設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433599"
---
# <a name="setting-transport-order"></a><span data-ttu-id="bc4e8-103">トランスポート順序の設定</span><span class="sxs-lookup"><span data-stu-id="bc4e8-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="bc4e8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc4e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc4e8-105">MAPI スプーラーは、トランスポートプロバイダーが処理できる、アドレスの種類と識別子に基づいて、送信メッセージの責任を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="bc4e8-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="bc4e8-106">トランスポートプロバイダーは、 **MAPIUID**構造に格納されているサポートされているアドレスの種類と識別子の一覧を発行します。これは、MAPI が[IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドをログオンした直後に呼び出したときに行います。</span><span class="sxs-lookup"><span data-stu-id="bc4e8-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="bc4e8-107">受信者のアドレスの種類は、その**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="bc4e8-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="bc4e8-108">アドレスの種類を登録すると、トランスポートプロバイダーは、 **PR_ADDRTYPE**プロパティが登録されているアドレスの種類に設定された受信者に配信できる MAPI に示されます。</span><span class="sxs-lookup"><span data-stu-id="bc4e8-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="bc4e8-109">同様に、 **MAPIUID**の登録は、トランスポートプロバイダーが登録済みの**MAPIUID**を持つエントリ id で表される受信者に配信できることを示します。</span><span class="sxs-lookup"><span data-stu-id="bc4e8-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="bc4e8-110">ほとんどのトランスポートプロバイダーは、1つまたは複数のアドレスの種類に対して登録します。**MAPIUID**による登録はほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="bc4e8-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="bc4e8-111">アドレス帳プロバイダーと密接に結合され、そのエントリ識別子形式を理解しているトランスポートプロバイダーは、 **MAPIUID**によってメッセージを処理するように登録できます。これにより、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="bc4e8-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="bc4e8-112">これらの密結合トランスポートプロバイダーは、受信者の電子メールアドレスやその他の必要な情報を**imapisupport:: openentry**呼び出しを使用して開くことなく、エントリ識別子から抽出できます。</span><span class="sxs-lookup"><span data-stu-id="bc4e8-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="bc4e8-113">MAPI は、複数のトランスポートプロバイダーが同じアドレスの種類または**MAPIUID**に登録されている場合に使用されるトランスポートプロバイダーの順序を保持します。</span><span class="sxs-lookup"><span data-stu-id="bc4e8-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="bc4e8-114">この順序を上書きするには、 [IMsgServiceAdmin:: msgservicetransportorder](imsgserviceadmin-msgservicetransportorder.md)を呼び出し、 _lpuidlist_パラメーターで示されているすべてのアクティブなトランスポートプロバイダーの**MAPIUID**s の順序付きリストを渡します。</span><span class="sxs-lookup"><span data-stu-id="bc4e8-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID**s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="bc4e8-115">アクティブなトランスポートプロバイダーのいずれかによって処理可能なすべてのアドレスの種類の一覧を取得するには、 [imapisession:: enumadrtypes](imapisession-enumadrtypes.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bc4e8-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="bc4e8-116">**enumadrtypes**は、現在のセッションでアクティブなトランスポートプロバイダーによってサポートされているアドレスの種類を表す文字列の配列を返します。</span><span class="sxs-lookup"><span data-stu-id="bc4e8-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

