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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316430"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="b731a-103">PidTagExchangeProfileSectionId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b731a-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="b731a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b731a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b731a-105">複数の Microsoft Exchange Server アカウントを使用している場合にアカウントを判別するために使用される動的に生成される GUID を含みます。</span><span class="sxs-lookup"><span data-stu-id="b731a-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b731a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b731a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b731a-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="b731a-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="b731a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b731a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b731a-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="b731a-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="b731a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b731a-110">Data type:</span></span>  <br/> |<span data-ttu-id="b731a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b731a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b731a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b731a-112">Area:</span></span>  <br/> |<span data-ttu-id="b731a-113">複数の Exchange アカウント</span><span class="sxs-lookup"><span data-stu-id="b731a-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b731a-114">解説</span><span class="sxs-lookup"><span data-stu-id="b731a-114">Remarks</span></span>

<span data-ttu-id="b731a-115">microsoft outlook 2010 および microsoft outlook 2013 は、1つの exchange アカウントではなく複数の exchange アカウントをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b731a-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="b731a-116">複数の Exchange アカウントに対応するために、MAPI プロファイルレイアウトが変更されました。</span><span class="sxs-lookup"><span data-stu-id="b731a-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="b731a-117">Microsoft Office Outlook 2007 以前では、プロファイルには、サーバー名、ユーザー名、オフラインフォルダーファイル (.ost) などの Exchange 設定専用の固定プロファイルセクションが含まれていました。</span><span class="sxs-lookup"><span data-stu-id="b731a-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="b731a-118">位置.</span><span class="sxs-lookup"><span data-stu-id="b731a-118">location.</span></span> <span data-ttu-id="b731a-119">これらの設定は、一意の識別子で**pbGlobalProfileSectionGuid**プロパティを使用して識別されました。</span><span class="sxs-lookup"><span data-stu-id="b731a-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="b731a-120">exchange の設定に使用されるセクションは、「exchange グローバルプロファイル」セクションと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b731a-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> 
  
<span data-ttu-id="b731a-121">固定プロファイルセクションの場所は、複数の Exchange アカウントに対応するのに十分ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="b731a-121">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="b731a-122">代わりに、プロファイル内の Exchange アカウントごとに、そのアカウントの設定専用のセクションが存在します。</span><span class="sxs-lookup"><span data-stu-id="b731a-122">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="b731a-123">Exchange の設定に使用される新しいセクションは、一意の識別子**emsmdbUID**によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="b731a-123">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="b731a-124">Exchange アカウントの [メッセージサービスプロファイル] セクションでは、アカウントの作成時に動的に生成される GUID を含むプロパティを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="b731a-124">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="b731a-125">この GUID は、 **PidTagExchangeProfileSectionId**プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="b731a-125">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="b731a-126">メッセージストアとアドレス帳コンテナーは、どの Exchange アカウントが属しているかを判断するためのプロパティを公開します。</span><span class="sxs-lookup"><span data-stu-id="b731a-126">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="b731a-127">メッセージサービステーブルでアクセスできるようになると、各 Exchange サービスはこのプロパティを公開します。</span><span class="sxs-lookup"><span data-stu-id="b731a-127">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="b731a-128">このプロパティは、次のいずれかのインターフェイスに対してクエリを実行した後に、 **PidTagExchangeProfileSectionId**上の[imapiprop:: GetProps](imapiprop-getprops.md)への呼び出しによって取得できます。</span><span class="sxs-lookup"><span data-stu-id="b731a-128">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="b731a-129">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b731a-129">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="b731a-130">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b731a-130">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="b731a-131">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b731a-131">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="b731a-132">オブジェクトが Exchange に関連付けられていない場合、呼び出しは**MAPI_E_NOT_FOUND**を返します。</span><span class="sxs-lookup"><span data-stu-id="b731a-132">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="b731a-133">アドレス帳を表示するときに、 **PidTagExchangeProfileSectionId**のコンテナーを制限することができます。</span><span class="sxs-lookup"><span data-stu-id="b731a-133">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="b731a-134">コンテナーを開いた後、そのコンテナーから**emsmdbUID**を照会することができます。</span><span class="sxs-lookup"><span data-stu-id="b731a-134">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="b731a-135">また、受信者が Exchange アドレス帳から選択されている場合は、受信者の**PidTagExchangeProfileSectionId**もプロパティの一覧に表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b731a-135">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b731a-136">コードサンプルと関数ヘッダー全体で、この GUID は**emsmdbUID**と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b731a-136">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="b731a-137">exchange アカウントの1つは、従来の exchange アカウントとしてマークされています。</span><span class="sxs-lookup"><span data-stu-id="b731a-137">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="b731a-138">通常、これはプロファイルに最初に追加されるアカウントです。</span><span class="sxs-lookup"><span data-stu-id="b731a-138">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="b731a-139">open **pbGlobalProfileSectionGuid**へのすべての呼び出しは、従来のアカウントの Exchange グローバルセクションにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="b731a-139">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="b731a-140">従来の exchange アカウントではないオブジェクトモデル呼び出しは、従来の exchange アカウントとも対話します。</span><span class="sxs-lookup"><span data-stu-id="b731a-140">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="b731a-141">従来の Exchange サービスには、 **PR_EMSMDB_LEGACY** (0x3D18000B) というプロパティがあり、メッセージサービステーブルでは**true**に設定されています。</span><span class="sxs-lookup"><span data-stu-id="b731a-141">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="b731a-142">従来の**emsmdbUID**も、プロファイルの Outlook グローバルプロファイルセクションに**PidTagExchangeProfileSectionId**としてスタンプされます。</span><span class="sxs-lookup"><span data-stu-id="b731a-142">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="b731a-143">複数の Exchange アカウントをサポートするように記述されたコードは、コードが対話するアカウントに応じて正しい**emsmdbUID**を取得する必要があるため、従来の**emsmdbUID**を取得する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b731a-143">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b731a-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="b731a-144">See also</span></span>



[<span data-ttu-id="b731a-145">複数の Exchange アカウントの使用</span><span class="sxs-lookup"><span data-stu-id="b731a-145">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


<span data-ttu-id="b731a-146">[[�O���[�o�� �v���t�@�C��] �Z�N�V������J�����@](https://support.microsoft.com/kb/188482)</span><span class="sxs-lookup"><span data-stu-id="b731a-146">[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)</span></span>

