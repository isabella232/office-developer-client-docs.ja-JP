---
title: GetProps および SetProps によるプロパティの取得と設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299399"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="04131-103">GetProps および SetProps によるプロパティの取得と設定</span><span class="sxs-lookup"><span data-stu-id="04131-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="04131-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04131-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04131-105">可能な限り、 [imapiprop:: GetProps](imapiprop-getprops.md)および[imapiprop:: setprops](imapiprop-setprops.md)メソッドを使用して、プロパティを取得または変更してみてください。</span><span class="sxs-lookup"><span data-stu-id="04131-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="04131-106">作業しているプロパティが非常に大きい場合以外は、これらのメソッドが適切である必要があります。</span><span class="sxs-lookup"><span data-stu-id="04131-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="04131-107">もう1つの方法として、 [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスを使用してストリームの読み取りまたは書き込みを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="04131-107">The other alternative is to read from or write to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="04131-108">ストリームは非常に大きなプロパティを正常に処理できますが、COM ライブラリを必要とするため、リソースがより高速に処理されます。</span><span class="sxs-lookup"><span data-stu-id="04131-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="04131-109">**IStream**インターフェイスは、 **imapiprop:: GetProps**または**imapiprop:: setprops**の呼び出しが失敗した後にのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="04131-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

