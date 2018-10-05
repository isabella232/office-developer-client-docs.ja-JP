---
title: GetProps と SetProps プロパティの設定を取得および
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395008"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="b9eb2-103">GetProps と SetProps プロパティの設定を取得および</span><span class="sxs-lookup"><span data-stu-id="b9eb2-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="b9eb2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9eb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9eb2-105">、可能な限りしようとするを取得または[IMAPIProp::GetProps](imapiprop-getprops.md)および[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを使用してプロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="b9eb2-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="b9eb2-106">プロパティを使用しているが非常に大きい場合を除き、これらのメソッドが適切な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9eb2-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="b9eb2-107">その他の場合は読み取りまたは[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスを使用してストリームに書き込みします。</span><span class="sxs-lookup"><span data-stu-id="b9eb2-107">The other alternative is to read from or write to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="b9eb2-108">ストリームでは、非常に大規模なプロパティを正常に処理できますが、リソースを大きく消費 COM ライブラリが必要なためです。</span><span class="sxs-lookup"><span data-stu-id="b9eb2-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="b9eb2-109">**IMAPIProp::GetProps**または**IMAPIProp::SetProps**呼び出しが失敗した後にのみ、 **IStream**インターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="b9eb2-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

