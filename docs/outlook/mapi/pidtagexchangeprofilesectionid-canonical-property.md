---
title: PidTagExchangeProfileSectionId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 37a318df01101487fe0e8970251201c2515d1e8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802722"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="96405-103">PidTagExchangeProfileSectionId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="96405-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="96405-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96405-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96405-105">複数の Microsoft Exchange Server アカウントを使用している場合は、アカウントを決定するために動的に生成された GUID が含まれています。</span><span class="sxs-lookup"><span data-stu-id="96405-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96405-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="96405-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96405-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="96405-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="96405-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="96405-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96405-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="96405-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="96405-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="96405-110">Data type:</span></span>  <br/> |<span data-ttu-id="96405-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="96405-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="96405-112">領域:</span><span class="sxs-lookup"><span data-stu-id="96405-112">Area:</span></span>  <br/> |<span data-ttu-id="96405-113">複数の Exchange アカウント</span><span class="sxs-lookup"><span data-stu-id="96405-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96405-114">備考</span><span class="sxs-lookup"><span data-stu-id="96405-114">Remarks</span></span>

<span data-ttu-id="96405-115">Microsoft Outlook 2010 と Microsoft Outlook 2013 は、1 つ 1 つの Exchange アカウントではなく、複数の Exchange アカウントをサポートします。</span><span class="sxs-lookup"><span data-stu-id="96405-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="96405-116">複数の Exchange アカウントに対応するため、MAPI プロファイルのレイアウトが変更されました。</span><span class="sxs-lookup"><span data-stu-id="96405-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="96405-117">Microsoft Office Outlook 2007 と以前のバージョンでは、プロファイルには、サーバー名、ユーザー名、およびオフライン フォルダー ファイル (.ost) などの Exchange の設定には専用の固定プロファイル セクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="96405-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="96405-118">場所です。</span><span class="sxs-lookup"><span data-stu-id="96405-118">location.</span></span> <span data-ttu-id="96405-119">**PbGlobalProfileSectionGuid**プロパティの一意の識別子を使用してこれらの設定が確認されました。</span><span class="sxs-lookup"><span data-stu-id="96405-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="96405-120">交換の設定に使用されるセクションは、Exchange のグローバル プロファイル セクションと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="96405-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> <span data-ttu-id="96405-121">Outlook 2007 で Exchange のグローバル プロファイルの詳細については、[グローバル プロファイル セクションを開く方法](http://support.microsoft.com/kb/188482)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96405-121">For more information about the Exchange Global Profile in Outlook 2007, see [How To Open the Global Profile Section](http://support.microsoft.com/kb/188482).</span></span>
  
<span data-ttu-id="96405-122">固定プロファイル セクションの場所は、複数の Exchange アカウントに対応するために十分ではありません。</span><span class="sxs-lookup"><span data-stu-id="96405-122">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="96405-123">代わりに、プロファイルに Exchange アカウントごとのセクションが存在し、そのアカウントの設定は、専用です。</span><span class="sxs-lookup"><span data-stu-id="96405-123">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="96405-124">交換の設定に使用される新しいセクションは、 **emsmdbUID**の一意の識別子によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="96405-124">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="96405-125">メッセージにサービス プロファイルの Exchange アカウント、アカウントの作成時に動的に生成される GUID を格納するプロパティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="96405-125">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="96405-126">この GUID は、 **PidTagExchangeProfileSectionId**プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="96405-126">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="96405-127">メッセージ ストアやアドレス帳コンテナーに属している Exchange アカウントを決定するプロパティを公開します。</span><span class="sxs-lookup"><span data-stu-id="96405-127">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="96405-128">メッセージ サービス テーブルにアクセスできるように、各 Exchange サービスは、このプロパティを公開します。</span><span class="sxs-lookup"><span data-stu-id="96405-128">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="96405-129">次のインターフェイスのいずれかのクエリを実行した後、 **PidTagExchangeProfileSectionId**で[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出すことによってこのプロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="96405-129">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="96405-130">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="96405-130">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="96405-131">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="96405-131">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="96405-132">これにより: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="96405-132">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="96405-133">オブジェクトが Exchange に関連しては、呼び出しは**MAPI_E_NOT_FOUND**を返します。</span><span class="sxs-lookup"><span data-stu-id="96405-133">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="96405-134">アドレス帳を表示するときに、 **PidTagExchangeProfileSectionId**にあるコンテナーを制限できます。</span><span class="sxs-lookup"><span data-stu-id="96405-134">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="96405-135">開かれているコンテナーを作成したら、そこから**emsmdbUID**を照会できます。</span><span class="sxs-lookup"><span data-stu-id="96405-135">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="96405-136">注目に値します受信者を Exchange アドレス帳から選択した場合、受信者もいる**PidTagExchangeProfileSectionId**プロパティの一覧にします。</span><span class="sxs-lookup"><span data-stu-id="96405-136">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="96405-137">コード サンプルおよび関数のヘッダーでは、全体では、この GUID は**emsmdbUID**と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="96405-137">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="96405-138">Exchange アカウントの 1 つは、従来の Exchange アカウントとしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="96405-138">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="96405-139">通常、最初のアカウントをプロファイルに追加されることです。</span><span class="sxs-lookup"><span data-stu-id="96405-139">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="96405-140">開くには**pbGlobalProfileSectionGuid**のすべての呼び出しは、従来のアカウントの Exchange のグローバル セクションにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="96405-140">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="96405-141">非レガシ Exchange アカウントを使用してデータをやり取りするオブジェクト モデルの呼び出しは、従来の Exchange アカウントを使用しても操作できます。</span><span class="sxs-lookup"><span data-stu-id="96405-141">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="96405-142">従来の Exchange サービスには、 **PR_EMSMDB_LEGACY** (0x3D18000B)、 **true**メッセージ サービス テーブルに設定されているプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="96405-142">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="96405-143">従来の**emsmdbUID**は**PidTagExchangeProfileSectionId**としてプロファイルの Outlook のグローバル プロファイル セクションでも記録されます。</span><span class="sxs-lookup"><span data-stu-id="96405-143">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="96405-144">複数の Exchange アカウントをサポートするために記述されたコードは、正しい**emsmdbUID**コードとの対話は、パスワードを取得する必要がありますので、従来の**emsmdbUID**を取得する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="96405-144">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="96405-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="96405-145">See also</span></span>



[<span data-ttu-id="96405-146">複数の Exchange アカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="96405-146">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


<span data-ttu-id="96405-147">[[�O���[�o�� �v���t�@�C��] �Z�N�V������J�����@](http://support.microsoft.com/kb/188482)</span><span class="sxs-lookup"><span data-stu-id="96405-147">[How To Open the Global Profile Section](http://support.microsoft.com/kb/188482)</span></span>

