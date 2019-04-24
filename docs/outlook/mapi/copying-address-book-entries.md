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
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333069"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="f1c1c-103">アドレス帳エントリのコピー</span><span class="sxs-lookup"><span data-stu-id="f1c1c-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="f1c1c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1c1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1c1c-105">同じまたは別のコンテナーの1人または複数の受信者がこのコンテナーにコピーされると、コンテナーの[IABContainer:: copyentries](iabcontainer-copyentries.md)メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="f1c1c-106">**copyentries**には4つの入力パラメーターがあります。コピーされる受信者を表すエントリ識別子の配列、進行状況インジケーターのウィンドウハンドル、進行状況オブジェクトポインター、およびフラグ値があります。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="f1c1c-107">AB_NO_DIALOG フラグが設定されていない場合はプロバイダーに進行状況が表示され、NULL でない場合は_lpprogress_パラメーターから progress オブジェクトを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="f1c1c-108">_lpprogress_が NULL の場合は、MAPI progress オブジェクトを使用するために、 [imapisupport::D oprogress dialog](imapisupport-doprogressdialog.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="f1c1c-109">進捗状況の表示の詳細については、「[進行状況インジケーターの表示](mapi-progress-indicators.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="f1c1c-110">進行状況インジケーターを表示しないように AB_NO_DIALOG に加えて、他の2つのフラグのいずれかを設定して、重複するエントリチェックの種類を要求することができます: CREATE_CHECK_DUP_LOOSE または CREATE_CHECK_DUP_STRICT。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="f1c1c-111">CREATE_CHECK_DUP_LOOSE および CREATE_CHECK_DUP_STRICT フラグは、プロバイダーが重複エントリを決定し、無視できるようにするための推奨事項に過ぎません。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="f1c1c-112">MAPI では、次のように、これらのフラグのサポートを実装することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="f1c1c-113">**重複するエントリフラグ**</span><span class="sxs-lookup"><span data-stu-id="f1c1c-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="f1c1c-114">**推奨される実装**</span><span class="sxs-lookup"><span data-stu-id="f1c1c-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f1c1c-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="f1c1c-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="f1c1c-116">作成するエントリの表示名が、コンテナー内に既にあるエントリの表示名と一致しているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="f1c1c-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="f1c1c-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="f1c1c-118">作成するエントリの表示名と検索キーの両方が、コンテナーエントリの表示名と検索キーと一致するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="f1c1c-119">最後のフラグ CREATE_REPLACE は、作成するエントリがコンテナー内に既に存在するエントリと重複しているとプロバイダーが判断した場合に、新しいエントリが既存のエントリを置き換える必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="f1c1c-120">プロバイダーが個人用アドレス帳の場合は、すべてのコピー操作に**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="f1c1c-121">コピーされた受信者の詳細表示テーブルを含めると、表示を作成する元のコンテナーを呼び出すことなく、受信者の詳細をコンテナーで表示できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="f1c1c-122">**IABContainer:: copyentries を実装するには**</span><span class="sxs-lookup"><span data-stu-id="f1c1c-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="f1c1c-123">_lpentries_パラメーターの各エントリ識別子が、プロバイダーが処理し、失敗した場合は、MAPI_E_INVALID_ENTRYID を返すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="f1c1c-124">エントリ識別子が、プロバイダーが処理するメッセージングユーザー、配布リスト、またはコンテナーを表している場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="f1c1c-125">[imapisupport:: openentry](imapisupport-openentry.md)メソッドを呼び出して、対応する受信者を開きます。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="f1c1c-126">受信者をコンテナーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="f1c1c-127">エントリ識別子が外部の受信者を表す場合:</span><span class="sxs-lookup"><span data-stu-id="f1c1c-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="f1c1c-128">コンテナーの[IABContainer:: createentry](iabcontainer-createentry.md)メソッドを呼び出して、新しい受信者を作成します。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="f1c1c-129">新しい受信者の初期プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="f1c1c-130">新しいオブジェクトの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して保存します。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="f1c1c-131">コンテナーの contents テーブルを更新して、新しい受信者を反映させます。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="f1c1c-132">Call [imapisupport::](imapisupport-notify.md)登録済みクライアントにテーブル通知を送信するよう通知します。</span><span class="sxs-lookup"><span data-stu-id="f1c1c-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

