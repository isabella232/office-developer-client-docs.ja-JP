---
title: 空き時間情報 API について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: 空き時間情報 API を使用すると、メール プロバイダーは指定した時間範囲内で指定したユーザー アカウントの空き時間情報を提供できます。
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433760"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="99eb7-103">空き時間情報 API について</span><span class="sxs-lookup"><span data-stu-id="99eb7-103">About the Free/Busy API</span></span>

<span data-ttu-id="99eb7-104">空き時間情報 API を使用すると、メール プロバイダーは指定した時間範囲内で指定したユーザー アカウントの空き時間情報を提供できます。</span><span class="sxs-lookup"><span data-stu-id="99eb7-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="99eb7-105">ユーザーの予定表の時間のブロックの空き時間情報の状態は、次の 1 つになります。</span><span class="sxs-lookup"><span data-stu-id="99eb7-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="99eb7-106">空き時間情報プロバイダーを作成する</span><span class="sxs-lookup"><span data-stu-id="99eb7-106">Create a free/busy provider</span></span>

<span data-ttu-id="99eb7-107">メール ユーザーに空き時間情報を提供するために、メール プロバイダーは空き時間情報プロバイダーを作成し、空き時間情報に登録Outlook。</span><span class="sxs-lookup"><span data-stu-id="99eb7-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="99eb7-108">空き時間情報プロバイダーは、次のインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99eb7-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="99eb7-109">これらのインターフェイスのメンバーの数はサポートされていないので、指定した戻り値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="99eb7-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="99eb7-110">特に、空き時間情報 API では、空き時間情報への書き込みアクセスとアカウントへのアクセスの委任はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="99eb7-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="99eb7-111">[IFreeBusySupport](ifreebusysupport.md) —このインターフェイスは、指定されたユーザーの空き時間情報データにアクセスするインターフェイスの仕様をサポートします。</span><span class="sxs-lookup"><span data-stu-id="99eb7-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="99eb7-112">FBUser [を使用して](fbuser.md) ユーザーを識別します。</span><span class="sxs-lookup"><span data-stu-id="99eb7-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="99eb7-113">[IFreeBusyData](ifreebusydata.md) —このインターフェイスは、特定のユーザーの時間範囲を取得および設定し、この時間範囲内のデータの空き時間情報ブロックを列挙するためのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="99eb7-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="99eb7-114">相対時間を使用して、この時間範囲を取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="99eb7-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="99eb7-115">詳細については、「相対時間を [使用して空き時間情報にアクセスする」を参照してください](how-to-use-relative-time-to-access-free-busy-data.md)。</span><span class="sxs-lookup"><span data-stu-id="99eb7-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="99eb7-116">[IEnumFBBlock](ienumfbblock.md) —このインターフェイスは、時間範囲内のユーザーのデータの空き時間情報ブロックへのアクセスと列挙をサポートします。</span><span class="sxs-lookup"><span data-stu-id="99eb7-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="99eb7-117">列挙には、ユーザーの予定表の時間の空き時間状態を示す空き時間情報ブロックが含まれています [(IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)で指定)。</span><span class="sxs-lookup"><span data-stu-id="99eb7-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="99eb7-118">予定表のアイテム (予定や会議出席依頼など) は、列挙のフォーム ブロックです。</span><span class="sxs-lookup"><span data-stu-id="99eb7-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="99eb7-119">予定表で隣接し、同じ空き時間情報の状態を持つアイテムは、1 つのブロックを形成するために結合されます。</span><span class="sxs-lookup"><span data-stu-id="99eb7-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="99eb7-120">予定表の空き時間もブロックを形成します。</span><span class="sxs-lookup"><span data-stu-id="99eb7-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="99eb7-121">したがって、列挙の 2 つの連続するブロックの空き時間情報の状態は同じではありません。</span><span class="sxs-lookup"><span data-stu-id="99eb7-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="99eb7-122">これらのブロックは時間内に重複しません。</span><span class="sxs-lookup"><span data-stu-id="99eb7-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="99eb7-123">予定表に重複するアイテムがある場合、Outlook は、これらのアイテムを結合して、次の優先順位 (アウトオブオフィス、ビジー、暫定的) に基づいて、列挙内の重複しない空き時間情報ブロックを形成します。</span><span class="sxs-lookup"><span data-stu-id="99eb7-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="99eb7-124">空き時間情報プロバイダーを Outlook、メール プロバイダーは次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="99eb7-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="99eb7-125">空き時間情報プロバイダーを COM に登録し、プロバイダーの **IFreeBusySupport** の実装にアクセスできる CLSID を提供します。</span><span class="sxs-lookup"><span data-stu-id="99eb7-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="99eb7-126">システム Outlookに次のキー (バージョンの Outlook を表す) を設定して、空き時間情報プロバイダーが存在することを確認 `<xx.x>` します。</span><span class="sxs-lookup"><span data-stu-id="99eb7-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="99eb7-127">たとえば、トランスポート プロバイダーが SMTP の場合、プロバイダーを Microsoft Outlook 2010 に登録するには、次の表のデータに次のキーを設定します。</span><span class="sxs-lookup"><span data-stu-id="99eb7-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="99eb7-128">名前</span><span class="sxs-lookup"><span data-stu-id="99eb7-128">Name</span></span> |<span data-ttu-id="99eb7-129">型</span><span class="sxs-lookup"><span data-stu-id="99eb7-129">Type</span></span> |<span data-ttu-id="99eb7-130">値</span><span class="sxs-lookup"><span data-stu-id="99eb7-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="99eb7-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="99eb7-131">SMTP</span></span>  |<span data-ttu-id="99eb7-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="99eb7-132">REG_SZ</span></span>  |<span data-ttu-id="99eb7-133">{IFreeBusySupport の各実装の CLSID}</span><span class="sxs-lookup"><span data-stu-id="99eb7-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="99eb7-134">このシナリオでは、Outlook COM クラスを共同作成し、それを使用して SMTP メール ユーザーの空き時間情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="99eb7-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="99eb7-135">SMTP 以外のアドレス入力タイプを使用するアドレス帳とトランスポート プロバイダーをサポートするには、名前を変更  *します* 。</span><span class="sxs-lookup"><span data-stu-id="99eb7-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="99eb7-136">インストール中に、空き時間情報プロバイダーは、同じアドレス エントリの種類のレジストリ設定が既に存在するかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99eb7-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="99eb7-137">その場合、空き時間情報プロバイダーは、そのアドレス エントリの種類の現在のプロバイダーを上書きし、アンインストール時にそのプロバイダーに復元する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99eb7-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="99eb7-138">ただし、ユーザーが同じアドレス エントリの種類に対して複数の空き時間情報プロバイダーをインストールしている場合、ユーザーはこれらのプロバイダーをインストールと逆の順序でアンインストールする必要があります (つまり、常に最新のプロバイダーをアンインストールしてください)。</span><span class="sxs-lookup"><span data-stu-id="99eb7-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="99eb7-139">それ以外の場合、レジストリは既にアンインストールされているプロバイダーを指している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="99eb7-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="99eb7-140">API コンポーネント</span><span class="sxs-lookup"><span data-stu-id="99eb7-140">API components</span></span>

<span data-ttu-id="99eb7-141">空き時間情報 API には、次のコンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="99eb7-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="99eb7-142">定義</span><span class="sxs-lookup"><span data-stu-id="99eb7-142">Definitions</span></span>

- [<span data-ttu-id="99eb7-143">定数 (空き時間情報 API)</span><span class="sxs-lookup"><span data-stu-id="99eb7-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="99eb7-144">データ型</span><span class="sxs-lookup"><span data-stu-id="99eb7-144">Data types</span></span>

- [<span data-ttu-id="99eb7-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="99eb7-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="99eb7-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="99eb7-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="99eb7-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="99eb7-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="99eb7-148">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="99eb7-148">Interfaces</span></span>

- [<span data-ttu-id="99eb7-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="99eb7-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="99eb7-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="99eb7-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="99eb7-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="99eb7-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

