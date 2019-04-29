---
title: NDR の受信の集中管理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: af2531076755d1e183409f50fe1a0c97d28063f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405857"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="3d6a9-103">NDR の受信の集中管理</span><span class="sxs-lookup"><span data-stu-id="3d6a9-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="3d6a9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d6a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d6a9-105">**クライアントの複数のインスタンスが同時に実行されている場合に、配信不能レポート (ndr) を集中管理する場所に配信するには**</span><span class="sxs-lookup"><span data-stu-id="3d6a9-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="3d6a9-106">**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))、 **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md))、および**PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) を受信するアカウントの適切な値に設定します。レポート。</span><span class="sxs-lookup"><span data-stu-id="3d6a9-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="3d6a9-107">必要に応じて、 [IAddrBook:: createoneoff](iaddrbook-createoneoff.md)を呼び出して、エントリ id を作成します。</span><span class="sxs-lookup"><span data-stu-id="3d6a9-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="3d6a9-108">レポートに対して要求したアカウントを無視するメッセージングシステムがあり、発信者に送信されることを理解します。</span><span class="sxs-lookup"><span data-stu-id="3d6a9-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="3d6a9-109">次の方法でレポートを移動する必要がある管理者に与える影響を軽減します。</span><span class="sxs-lookup"><span data-stu-id="3d6a9-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="3d6a9-110">元のメッセージに、IPM などの別のメッセージクラスを付与します。MSNNews。</span><span class="sxs-lookup"><span data-stu-id="3d6a9-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="3d6a9-111">MSNNews を使用して受信メッセージを検索し、送信者が報告する予定のアカウントに転送します。</span><span class="sxs-lookup"><span data-stu-id="3d6a9-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="3d6a9-112">同時に、配信不能レポートアカウントを無視する電子メールをメッセージングシステムに送信して、 **PR_REPORT_ENTRYID**プロパティを優先させる必要があることを伝えます。</span><span class="sxs-lookup"><span data-stu-id="3d6a9-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="3d6a9-113">**PR_REPORT_ENTRYID**を優先しないほとんどのメッセージングシステムでは、MAPI メッセージクラスの規則は適用されません。</span><span class="sxs-lookup"><span data-stu-id="3d6a9-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="3d6a9-114">そのため、メモのような内容が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d6a9-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="3d6a9-115">これは、入力が変数になるため、これを処理するのはやや困難です。</span><span class="sxs-lookup"><span data-stu-id="3d6a9-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="3d6a9-116">件名を参照して、"配信不能" または元の件名から何らかの単語があることを意味しているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="3d6a9-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="3d6a9-117">これらのリストを時間の経過とともに調整できるようにしておきます。</span><span class="sxs-lookup"><span data-stu-id="3d6a9-117">Be prepared to tune these lists over time.</span></span> 
    

