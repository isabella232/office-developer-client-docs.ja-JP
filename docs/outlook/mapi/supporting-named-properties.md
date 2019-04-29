---
title: 名前付きプロパティのサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 27625e913f06e858295351ed62de840ae7789915
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434327"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="f6917-103">名前付きプロパティのサポート</span><span class="sxs-lookup"><span data-stu-id="f6917-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="f6917-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6917-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6917-105">[imapiprop: IUnknown](imapipropiunknown.md)インターフェイスを実装するオブジェクトは、名前付きプロパティをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="f6917-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="f6917-106">名前付きプロパティのサポートは、次の場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="f6917-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="f6917-107">他のプロバイダーからのエントリをコンテナーにコピーできるアドレス帳プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="f6917-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="f6917-108">任意のメッセージの種類を作成するために使用できるメッセージストアプロバイダー。</span><span class="sxs-lookup"><span data-stu-id="f6917-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="f6917-109">名前付きプロパティのサポートは、他のすべてのサービスプロバイダーでは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="f6917-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="f6917-110">名前付きプロパティをサポートするサービスプロバイダーは、 [imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)および[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドに名前から識別子へのマッピングを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6917-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="f6917-111">クライアントは**GetNamesFromIDs**を呼び出して、1つ以上の名前の識別子を作成または取得するために、0x8000 を超える範囲および**getidsfromnames**内の1つ以上のプロパティ識別子に対応する名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f6917-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="f6917-112">名前付きプロパティをサポートしていないサービスプロバイダーは次のようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6917-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="f6917-113">失敗した[imapiprop:: setprops](imapiprop-setprops.md)を使用して、id 0x8000 以上のプロパティを設定します。この値は、 [spropproblem](spropproblem.md)の配列の MAPI_E_UNEXPECTED_ID を返します。</span><span class="sxs-lookup"><span data-stu-id="f6917-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="f6917-114">[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)および[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドから MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="f6917-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    

