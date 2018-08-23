---
title: 受信者のプロパティを取得します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a48c6a8e043062bc6b48e09934fded1dccb507b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585438"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="3d714-103">受信者のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d714-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="3d714-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d714-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="3d714-105">アドレス帳エントリの 1 つまたは複数のプロパティにアクセスするのには</span><span class="sxs-lookup"><span data-stu-id="3d714-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="3d714-106">目的のアドレス帳エントリごとに、[アドレス帳コンテナー](iaddrbook-openentry.md)ターゲットのユーザーまたは配布リストをメッセージのエントリ id を渡すことを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d714-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="3d714-107">次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="3d714-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="3d714-108">取得する 1 つまたは複数のプロパティの一覧で、目的の各アドレス帳エントリには、メッセージングのユーザーまたは配布リストの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d714-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="3d714-109">[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)、すべての目的のアドレス帳のエントリのすべてのプロパティを保持する[ADRLIST](adrlist.md)構造体を渡すことを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d714-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="3d714-110">**PrepareRecips** 1 回の呼び出しは、について、複数のアドレス帳のエントリを返すことができます、ためには、複数の受信者に興味があるとき、という方針です。</span><span class="sxs-lookup"><span data-stu-id="3d714-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

