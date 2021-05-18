---
title: PidTagExchangeProfileSectionId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316430"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="acf0b-103">PidTagExchangeProfileSectionId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="acf0b-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="acf0b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acf0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acf0b-105">複数のアカウントを使用する場合にアカウントを決定するために使用される動的に生成された GUID Microsoft Exchange Serverします。</span><span class="sxs-lookup"><span data-stu-id="acf0b-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="acf0b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="acf0b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="acf0b-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="acf0b-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="acf0b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="acf0b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="acf0b-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="acf0b-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="acf0b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="acf0b-110">Data type:</span></span>  <br/> |<span data-ttu-id="acf0b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="acf0b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="acf0b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="acf0b-112">Area:</span></span>  <br/> |<span data-ttu-id="acf0b-113">複数の Exchange アカウント</span><span class="sxs-lookup"><span data-stu-id="acf0b-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acf0b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="acf0b-114">Remarks</span></span>

<span data-ttu-id="acf0b-115">Microsoft Outlook 2010とMicrosoft Outlook 2013 1 つのアカウントではなくExchange複数のアカウントをExchangeできます。</span><span class="sxs-lookup"><span data-stu-id="acf0b-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="acf0b-116">複数のアカウントにExchange、MAPI プロファイル のレイアウトが変更されました。</span><span class="sxs-lookup"><span data-stu-id="acf0b-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="acf0b-117">2007 Microsoft Office Outlook以前では、プロファイルには、サーバー名、ユーザー名、オフライン フォルダー ファイル (.ost) などの Exchange 設定専用の固定プロファイル セクションが含まれるがありました。</span><span class="sxs-lookup"><span data-stu-id="acf0b-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="acf0b-118">場所。</span><span class="sxs-lookup"><span data-stu-id="acf0b-118">location.</span></span> <span data-ttu-id="acf0b-119">これらの設定は、一意の識別子 **pbGlobalProfileSectionGuid** プロパティを使用して識別されました。</span><span class="sxs-lookup"><span data-stu-id="acf0b-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="acf0b-120">この設定に使用Exchangeセクションは、[グローバル プロファイル] セクションExchange呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="acf0b-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> 
  
<span data-ttu-id="acf0b-121">固定プロファイル セクションの場所では、複数のアカウントに対応Exchangeなくなりました。</span><span class="sxs-lookup"><span data-stu-id="acf0b-121">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="acf0b-122">代わりに、プロファイルExchangeアカウントごとに、そのアカウントの設定専用のセクションが存在します。</span><span class="sxs-lookup"><span data-stu-id="acf0b-122">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="acf0b-123">ユーザー設定に使用される新Exchangeは、一意の識別子 **emsmdbUID によって識別されます**。</span><span class="sxs-lookup"><span data-stu-id="acf0b-123">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="acf0b-124">Exchange アカウントの [メッセージ サービス プロファイル] セクションで、アカウントの作成時に動的に生成される GUID を含むプロパティを検索できます。</span><span class="sxs-lookup"><span data-stu-id="acf0b-124">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="acf0b-125">この GUID は **、PidTagExchangeProfileSectionId プロパティに格納** されます。</span><span class="sxs-lookup"><span data-stu-id="acf0b-125">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="acf0b-126">メッセージ ストアとアドレス帳コンテナーは、どのアカウントに属Exchangeプロパティを公開します。</span><span class="sxs-lookup"><span data-stu-id="acf0b-126">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="acf0b-127">メッセージ サービス テーブルでアクセス可能で、各サービスExchangeこのプロパティを公開します。</span><span class="sxs-lookup"><span data-stu-id="acf0b-127">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="acf0b-128">次のインターフェイスのクエリを実行した後 **、PidTagExchangeProfileSectionId** の [IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出して、このプロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="acf0b-128">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="acf0b-129">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="acf0b-129">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="acf0b-130">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="acf0b-130">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="acf0b-131">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="acf0b-131">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="acf0b-132">オブジェクトがオブジェクトに関連付Exchange場合、呼び出しは次 **MAPI_E_NOT_FOUND。**</span><span class="sxs-lookup"><span data-stu-id="acf0b-132">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="acf0b-133">アドレス帳を表示するときに **、PidTagExchangeProfileSectionId** のコンテナーを制限できます。</span><span class="sxs-lookup"><span data-stu-id="acf0b-133">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="acf0b-134">コンテナーを開いた後、そのコンテナーから **emsmdbUID を** 照会できます。</span><span class="sxs-lookup"><span data-stu-id="acf0b-134">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="acf0b-135">また、受信者が Exchange アドレス帳から選択された場合、受信者はプロパティの一覧に **PidTagExchangeProfileSectionId** を持っています。</span><span class="sxs-lookup"><span data-stu-id="acf0b-135">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="acf0b-136">コード サンプルと関数ヘッダー全体で、この GUID は **emsmdbUID と呼ばれる。**</span><span class="sxs-lookup"><span data-stu-id="acf0b-136">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="acf0b-137">既存のアカウントの 1 Exchangeは、従来のアカウントとしてExchangeされます。</span><span class="sxs-lookup"><span data-stu-id="acf0b-137">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="acf0b-138">通常、プロファイルに追加された最初のアカウントです。</span><span class="sxs-lookup"><span data-stu-id="acf0b-138">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="acf0b-139">**pbGlobalProfileSectionGuid** を開くすべての呼び出しは、従来のアカウントExchangeグローバル セクションにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="acf0b-139">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="acf0b-140">従来以外のユーザー アカウントとやり取りするオブジェクト モデルExchange、従来のユーザー アカウントExchangeします。</span><span class="sxs-lookup"><span data-stu-id="acf0b-140">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="acf0b-141">レガシ Exchangeサービスには、PR_EMSMDB_LEGACY **(0x3D18000B)** というプロパティが設定されています。これは、メッセージ サービス テーブルで **true** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="acf0b-141">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="acf0b-142">従来の **emsmdbUID** は、プロファイルの Outlook グローバル プロファイル セクションにも **PidTagExchangeProfileSectionId としてスタンプされます**。</span><span class="sxs-lookup"><span data-stu-id="acf0b-142">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="acf0b-143">複数の Exchange アカウントをサポートするために記述されたコードは、コードが操作しているアカウントに応じて、正しい **emsmdbUID** を取得する必要がありますので、従来の **emsmdbUID** を取得する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="acf0b-143">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="acf0b-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="acf0b-144">See also</span></span>



[<span data-ttu-id="acf0b-145">複数のアカウントExchange使用する</span><span class="sxs-lookup"><span data-stu-id="acf0b-145">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


<span data-ttu-id="acf0b-146">[[�O���[�o�� �v���t�@�C��] �Z�N�V������J�����@](https://support.microsoft.com/kb/188482)</span><span class="sxs-lookup"><span data-stu-id="acf0b-146">[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)</span></span>

