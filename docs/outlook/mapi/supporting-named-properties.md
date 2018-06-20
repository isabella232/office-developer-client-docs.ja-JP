---
title: 名前付きプロパティをサポートしています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 983cbaf4d3523bf1e5370e5ad3119ab8c1490f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804048"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="fc11a-103">名前付きプロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="fc11a-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="fc11a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc11a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc11a-105">実装する任意のオブジェクト、 [IMAPIProp: IUnknown](imapipropiunknown.md)インターフェイスは、名前付きプロパティをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="fc11a-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="fc11a-106">名前付きプロパティのサポートに必要です。</span><span class="sxs-lookup"><span data-stu-id="fc11a-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="fc11a-107">アドレス帳プロバイダーのコンテナーにコピーするには、他のプロバイダーからのエントリを許可します。</span><span class="sxs-lookup"><span data-stu-id="fc11a-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="fc11a-108">メッセージは、任意のメッセージの種類を作成するのに使用できるプロバイダーを格納します。</span><span class="sxs-lookup"><span data-stu-id="fc11a-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="fc11a-109">名前付きプロパティのサポートは、他のすべてのサービス プロバイダーのオプションです。</span><span class="sxs-lookup"><span data-stu-id="fc11a-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="fc11a-110">名前付きプロパティをサポートしているサービス プロバイダーは、 [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドと[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドの名前の識別子にマッピングを実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="fc11a-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="fc11a-111">0x8000 の上の範囲内の 1 つまたは複数のプロパティ識別子に対応する名前を取得する**GetNamesFromIDs**と**GetIDsFromNames**を作成するか、1 つまたは複数の名前の識別子を取得するのには、クライアントが呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fc11a-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="fc11a-112">名前付きプロパティをサポートしていないサービスのプロバイダーにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc11a-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="fc11a-113">[SPropProblem](spropproblem.md)配列内の MAPI_E_UNEXPECTED_ID を返すことで 0x8000 以上の識別子を持つプロパティを設定するのには[IMAPIProp::SetProps](imapiprop-setprops.md)への呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="fc11a-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="fc11a-114">[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドと[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドから MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="fc11a-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    

