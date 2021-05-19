---
title: トランスポートの順序の設定
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
# <a name="setting-transport-order"></a><span data-ttu-id="39cbf-103">トランスポートの順序の設定</span><span class="sxs-lookup"><span data-stu-id="39cbf-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="39cbf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39cbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39cbf-105">MAPI スプーラーは、トランスポート プロバイダーが処理できると宣言するアドレスの種類と識別子に基づいて、送信メッセージの責任を割り当てします。</span><span class="sxs-lookup"><span data-stu-id="39cbf-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="39cbf-106">トランスポート プロバイダーは、MAPI がログオン直後に [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出す場合に **、MAPIUID** 構造に格納されているサポートされているアドレスの種類と識別子の一覧を公開します。</span><span class="sxs-lookup"><span data-stu-id="39cbf-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="39cbf-107">受信者のアドレスの種類は、プロパティ ([PidTagAddressType](pidtagaddresstype-canonical-property.md) **)** PR_ADDRTYPEに格納されます。</span><span class="sxs-lookup"><span data-stu-id="39cbf-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="39cbf-108">アドレスの種類に登録すると、トランスポート プロバイダーは、登録されているアドレスの種類に設定された PR_ADDRTYPE プロパティを使用して **受信者** に配信できる MAPI を示します。</span><span class="sxs-lookup"><span data-stu-id="39cbf-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="39cbf-109">同様に **、MAPIUID** を登録すると、トランスポート プロバイダーは、登録済みの **MAPIUID** を持つエントリ識別子によって表される受信者に配信できます。</span><span class="sxs-lookup"><span data-stu-id="39cbf-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="39cbf-110">ほとんどのトランスポート プロバイダーは、1 つ以上のアドレスの種類に登録します。 **MAPIUID による登録が少ない**。</span><span class="sxs-lookup"><span data-stu-id="39cbf-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="39cbf-111">アドレス帳プロバイダーと緊密に結合され、そのエントリ識別子の形式を理解しているトランスポート プロバイダーは **、MAPIUID** によってメッセージを処理するために登録でき、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="39cbf-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="39cbf-112">これらの緊密に結合されたトランスポート プロバイダーは **、IMAPISupport::OpenEntry** 呼び出しで開かなくても、受信者の電子メール アドレスなどの必要な情報をエントリ識別子から抽出できます。</span><span class="sxs-lookup"><span data-stu-id="39cbf-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="39cbf-113">MAPI は、複数のトランスポート プロバイダーが同じアドレスの種類または MAPIUID に登録されている場合に使用されるトランスポート プロバイダーの **注文を維持します**。</span><span class="sxs-lookup"><span data-stu-id="39cbf-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="39cbf-114">この順序をオーバーライドするには [、IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)を呼び出し _、lpUIDList_ パラメーターが指すすべてのアクティブなトランスポート プロバイダーの **MAPIUID** の順序付きリストを渡します。</span><span class="sxs-lookup"><span data-stu-id="39cbf-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID** s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="39cbf-115">アクティブなトランスポート プロバイダーの 1 つで処理できるすべてのアドレスの種類の一覧を取得するには [、IMAPISession::EnumAdrTypes を呼び出します](imapisession-enumadrtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="39cbf-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="39cbf-116">**EnumAdrTypes** は、現在のセッションでアクティブなトランスポート プロバイダーがサポートするアドレスの種類を表す文字列の配列を返します。</span><span class="sxs-lookup"><span data-stu-id="39cbf-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

