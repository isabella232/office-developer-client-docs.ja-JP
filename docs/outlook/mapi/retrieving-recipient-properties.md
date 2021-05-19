---
title: 受信者のプロパティの取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 38063cebe70b153decce6713ac5fc31d6916dbf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426675"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="9de56-103">受信者のプロパティの取得</span><span class="sxs-lookup"><span data-stu-id="9de56-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="9de56-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9de56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="9de56-105">アドレス帳エントリの 1 つ以上のプロパティにアクセスするには</span><span class="sxs-lookup"><span data-stu-id="9de56-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="9de56-106">対象のアドレス帳エントリごとに [、IAddrBook::OpenEntry](iaddrbook-openentry.md)を呼び出し、ターゲット メッセージング ユーザーまたは配布リストのエントリ識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="9de56-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="9de56-107">次に、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="9de56-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="9de56-108">メッセージング ユーザーまたは配布リストの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを、取得する 1 つ以上のプロパティの一覧で、関心のあるアドレス帳エントリごとに呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9de56-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="9de56-109">[IAddrBook::P repareRecips](iaddrbook-preparerecips.md)を呼び出し、必要なすべてのアドレス帳エントリのすべてのプロパティを保持する[ADRLIST](adrlist.md)構造体を渡します。</span><span class="sxs-lookup"><span data-stu-id="9de56-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="9de56-110">**PrepareRecips** を呼び出す 1 つの呼び出しは、複数のアドレス帳エントリの情報を返す可能性があるから、複数の受信者に関心がある場合に、この方法が望ましい戦略です。</span><span class="sxs-lookup"><span data-stu-id="9de56-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

