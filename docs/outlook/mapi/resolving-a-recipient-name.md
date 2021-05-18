---
title: 受信者名の解決
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405867"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="6e77a-103">受信者名の解決</span><span class="sxs-lookup"><span data-stu-id="6e77a-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="6e77a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e77a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e77a-105">メッセージがアドレス指定された場合、受信者リストは、各受信者に関連するプロパティで構築されます。</span><span class="sxs-lookup"><span data-stu-id="6e77a-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="6e77a-106">メッセージが送信される時には、それらのプロパティの 1 つが受信者の長期エントリ識別子である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e77a-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="6e77a-107">各受信者に **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが含まれるか確認するには [、IAddrBook::ResolveName](iaddrbook-resolvename.md)の呼び出しで _lpAdrList_ パラメーターの内容の受信者リストを説明する [ADRLIST](adrlist.md)構造を渡します。</span><span class="sxs-lookup"><span data-stu-id="6e77a-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="6e77a-108">**ResolveName** は、対応する [ADRENTRY](adrentry.md)構造体の **SPropValue** 配列にエントリ識別子が存在することで示されている、既に解決されている **ADRLIST** 構造体のエントリを無視して処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="6e77a-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="6e77a-109">次に **、ResolveName は** 2 種類の受信者に 1 回のエントリ識別子を自動的に割り当てる。</span><span class="sxs-lookup"><span data-stu-id="6e77a-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="6e77a-110">アドレスがインターネット アドレスとして書式設定されている受信者</span><span class="sxs-lookup"><span data-stu-id="6e77a-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="6e77a-111">次のように書式設定されたアドレスを持つ受信者。</span><span class="sxs-lookup"><span data-stu-id="6e77a-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="6e77a-112">残りのすべてのエントリについて **、ResolveName** はアドレス帳を検索して、表示名と完全に一致します。</span><span class="sxs-lookup"><span data-stu-id="6e77a-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="6e77a-113">**ResolveName** は **、PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティを使用して、検索するコンテナーのセットと検索順序を決定します。</span><span class="sxs-lookup"><span data-stu-id="6e77a-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="6e77a-114">MAPI は、 [すべてのコンテナーの IABContainer::ResolveNames](iabcontainer-resolvenames.md) メソッドを呼び出して、すべての名前を解決します。</span><span class="sxs-lookup"><span data-stu-id="6e77a-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="6e77a-115">一部のコンテナーは **ResolveNames** をサポートしないので、コンテナーが MAPI_E_NO_SUPPORT を返す場合、MAPI はコンテンツ テーブルに対して **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティの制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="6e77a-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="6e77a-116">この制限付き名前解決をサポートするには、すべてのアドレス帳コンテナーが必要です。</span><span class="sxs-lookup"><span data-stu-id="6e77a-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="6e77a-117">すべての名前が解決された後、それ以上コンテナー呼び出しは行なされません。</span><span class="sxs-lookup"><span data-stu-id="6e77a-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="6e77a-118">すべてのコンテナーが呼び出されたが、あいまいな名前または未解決の名前が残っている場合、MAPI は、可能であれば、残りの名前を解決するようにユーザーに求めるダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="6e77a-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="6e77a-119">この **PR_ANR** は、ADRLIST 構造の表示 **名** PR_ANRプロパティの値 **と一致** します。</span><span class="sxs-lookup"><span data-stu-id="6e77a-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="6e77a-120">**PR_ANR** プロパティ制限を使用してコンテナーのコンテンツ テーブルのビューを制限すると、アドレス帳プロバイダーは"最適な推測" 型の検索を実行し、プロバイダーに意味のあるプロパティと一致します。</span><span class="sxs-lookup"><span data-stu-id="6e77a-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="6e77a-121">たとえば、あるアドレス帳プロバイダーは、受信者リスト内の名前を **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) と常に一致し、もう 1 つは管理者がプロパティを選択できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6e77a-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="6e77a-122">**アドレス帳コンテナー PR_ANRのコンテンツ テーブルのプロパティ制限を設定するには**</span><span class="sxs-lookup"><span data-stu-id="6e77a-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="6e77a-123">次の [コードに示すように、SRestriction](srestriction.md) 構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="6e77a-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="6e77a-124">コンテンツ テーブルの [IMAPITable::Restrict](imapitable-restrict.md) メソッドを呼び出し **、sRestriction** 構造体を  _lpRestriction パラメーターとして渡_ します。</span><span class="sxs-lookup"><span data-stu-id="6e77a-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

