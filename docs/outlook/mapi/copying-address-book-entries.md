---
title: アドレス帳エントリのコピー
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eca0c9f63a4efaaa7f9fd066cf5dce451b8f6175
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565887"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="9e2b6-103">アドレス帳エントリのコピー</span><span class="sxs-lookup"><span data-stu-id="9e2b6-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="9e2b6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e2b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e2b6-105">コンテナーの[IABContainer::CopyEntries](iabcontainer-copyentries.md)メソッドが呼び出されますから、同じ 1 つまたは複数の受信者このコンテナーにコピーするか、別のコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="9e2b6-106">**CopyEntries**は、4 つの入力パラメーターを持つ: コピーする受信者を表すエントリの識別子、進行状況インジケーター、進行中のオブジェクト ポインター、およびフラグの値のウィンドウ ハンドルの配列。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="9e2b6-107">プロバイダーは、AB_NO_DIALOG フラグが設定されていないと、オブジェクトを使用して、進行状況、 _lpProgress_パラメーターからが NULL でない場合、進行状況を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="9e2b6-108">_LpProgress_が NULL の場合は、MAPI 処理中のオブジェクトを使用して[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="9e2b6-109">進行状況を表示する方法についての詳細については、[進行状況のインジケーターを表示する](mapi-progress-indicators.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="9e2b6-110">以外に、進行状況インジケーターを非表示にする AB_NO_DIALOG は、他の 2 つのフラグの 1 つも設定型の重複するエントリのチェックを要求する: CREATE_CHECK_DUP_LOOSE または CREATE_CHECK_DUP_STRICT です。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="9e2b6-111">CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT のフラグは無視して、プロバイダーが重複したエントリを決定する方法についての提案のみです。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="9e2b6-112">MAPI は、プロバイダーが次のようにこれらのフラグのサポートを実装することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="9e2b6-113">**重複するエントリのフラグ**</span><span class="sxs-lookup"><span data-stu-id="9e2b6-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="9e2b6-114">**推奨される実装**</span><span class="sxs-lookup"><span data-stu-id="9e2b6-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9e2b6-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="9e2b6-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="9e2b6-116">コンテナー内のエントリの表示名を作成するエントリの表示名が一致したかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="9e2b6-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="9e2b6-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="9e2b6-118">表示名と検索キーの両方を作成するエントリのコンテナーのエントリの表示名と検索キーに一致するかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="9e2b6-119">最後のフラグでは、CREATE_REPLACE は、新しいエントリは、プロバイダーが作成されるエントリがコンテナー内のエントリの重複を決定する場合は既存の 1 つを置き換える必要がありますを示します。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="9e2b6-120">プロバイダーが個人用アドレス帳の場合は、コピー操作を行うたびに、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="9e2b6-121">コピーの受信者の詳細表示のテーブルを含む、受信者ではなく呼び出し元のコンテナーに表示を作成するの詳細を表示するのには、コンテナーが有効にします。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="9e2b6-122">**IABContainer::CopyEntries を実装するには**</span><span class="sxs-lookup"><span data-stu-id="9e2b6-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="9e2b6-123">_LpEntries_パラメーターでは、各エントリ id は、プロバイダーを処理し、されていない場合は失敗し、MAPI_E_INVALID_ENTRYID を返す形式で、かどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="9e2b6-124">場合は、エントリ id は、メッセージングのユーザー、配布リスト、または、プロバイダーを処理するためのコンテナーを表します。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="9e2b6-125">開くには、対応する受信者の[IMAPISupport::OpenEntry](imapisupport-openentry.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="9e2b6-126">受信者コンテナーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="9e2b6-127">場合はエントリの識別子は、外部の受信者を表しています。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="9e2b6-128">新しい受信者を作成するのには、コンテナーの[IABContainer::CreateEntry](iabcontainer-createentry.md)のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="9e2b6-129">新しい受信者には、初期のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="9e2b6-130">保存するための新しいオブジェクトの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="9e2b6-131">新しい受信者を反映するためにコンテナーの内容のテーブルを更新します。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="9e2b6-132">登録済みクライアントにテーブルの通知を送信する[IMAPISupport::Notify](imapisupport-notify.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9e2b6-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

