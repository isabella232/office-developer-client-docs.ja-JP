---
title: アドレス帳エントリのコピー
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418744"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="81bd8-103">アドレス帳エントリのコピー</span><span class="sxs-lookup"><span data-stu-id="81bd8-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="81bd8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81bd8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81bd8-105">コンテナーの [IABContainer::CopyEntries](iabcontainer-copyentries.md) メソッドは、同じコンテナーまたは別のコンテナーから 1 つ以上の受信者をこのコンテナーにコピーするときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="81bd8-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="81bd8-106">**CopyEntries** には、コピーする受信者を表すエントリ識別子の配列、進行状況インジケーターのウィンドウ ハンドル、進行状況オブジェクト ポインター、フラグ値の 4 つの入力パラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="81bd8-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="81bd8-107">プロバイダーは、AB_NO_DIALOG フラグが設定されていない場合は進行状況を表示し、null 以外の場合は  _lpProgress_ パラメーターの progress オブジェクトを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81bd8-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="81bd8-108">_lpProgress が_ NULL の場合は [、IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md)を呼び出して MAPI 進行状況オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="81bd8-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="81bd8-109">進行状況の表示の詳細については、「進行状況インジケーターの [表示」を参照してください](mapi-progress-indicators.md)。</span><span class="sxs-lookup"><span data-stu-id="81bd8-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="81bd8-110">進行状況インジケーターをAB_NO_DIALOGに加えて、他の 2 つのフラグの 1 つを設定して、重複するエントリチェックの種類 (CREATE_CHECK_DUP_LOOSE または CREATE_CHECK_DUP_STRICT) を要求できます。</span><span class="sxs-lookup"><span data-stu-id="81bd8-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="81bd8-111">このCREATE_CHECK_DUP_LOOSEフラグCREATE_CHECK_DUP_STRICTは、プロバイダーが重複するエントリを決定する方法についてのみ提案され、無視できます。</span><span class="sxs-lookup"><span data-stu-id="81bd8-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="81bd8-112">MAPI は、プロバイダーが次のようにこれらのフラグのサポートを実装するように提案します。</span><span class="sxs-lookup"><span data-stu-id="81bd8-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="81bd8-113">**重複するエントリ フラグ**</span><span class="sxs-lookup"><span data-stu-id="81bd8-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="81bd8-114">**推奨される実装**</span><span class="sxs-lookup"><span data-stu-id="81bd8-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81bd8-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="81bd8-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="81bd8-116">作成するエントリの表示名が、コンテナー内の既にエントリの表示名と一致していないか確認します。</span><span class="sxs-lookup"><span data-stu-id="81bd8-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="81bd8-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="81bd8-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="81bd8-118">作成するエントリの表示名と検索キーの両方が、コンテナー エントリの表示名と検索キーと一致しないか確認します。</span><span class="sxs-lookup"><span data-stu-id="81bd8-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="81bd8-119">最後のフラグ CREATE_REPLACE は、プロバイダーが作成するエントリがコンテナー内の既にエントリと重複すると判断した場合、新しいエントリが既存のエントリを置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="81bd8-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="81bd8-120">プロバイダーが個人用アドレス帳の場合は、すべてのコピー **操作** に PR_DETAILS_TABLE ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="81bd8-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="81bd8-121">コピーされた受信者の詳細表示テーブルを含め、元のコンテナーを呼び出して表示を作成するのではなく、コンテナーで受信者の詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="81bd8-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="81bd8-122">**IABContainer を実装するには::CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="81bd8-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="81bd8-123">_lpEntries_ パラメーター内の各エントリ識別子が、プロバイダーが処理する形式かどうかを確認し、処理しない場合は失敗し、MAPI_E_INVALID_ENTRYID。</span><span class="sxs-lookup"><span data-stu-id="81bd8-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="81bd8-124">エントリ識別子が、プロバイダーが処理するメッセージング ユーザー、配布リスト、またはコンテナーを表す場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="81bd8-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="81bd8-125">[IMAPISupport::OpenEntry](imapisupport-openentry.md)メソッドを呼び出して、対応する受信者を開きます。</span><span class="sxs-lookup"><span data-stu-id="81bd8-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="81bd8-126">受信者をコンテナーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="81bd8-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="81bd8-127">エントリ識別子が外部受信者を表す場合:</span><span class="sxs-lookup"><span data-stu-id="81bd8-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="81bd8-128">コンテナーの [IABContainer::CreateEntry](iabcontainer-createentry.md) メソッドを呼び出して、新しい受信者を作成します。</span><span class="sxs-lookup"><span data-stu-id="81bd8-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="81bd8-129">新しい受信者に初期プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="81bd8-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="81bd8-130">新しいオブジェクトの [IMAPIProp::SaveChanges メソッドを呼](imapiprop-savechanges.md) び出して保存します。</span><span class="sxs-lookup"><span data-stu-id="81bd8-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="81bd8-131">コンテナーのコンテンツ テーブルを更新して、新しい受信者を反映します。</span><span class="sxs-lookup"><span data-stu-id="81bd8-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="81bd8-132">[IMAPISupport::Notify](imapisupport-notify.md)を呼び出して、登録済みのクライアントにテーブル通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="81bd8-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

