---
title: 空き時間情報 API について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: 空き時間情報 API を使用すると、指定したユーザーアカウントに対して、指定した時間範囲内に、メールプロバイダーが空き時間情報の状態情報を提供できます。
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317011"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="2bbaf-103">空き時間情報 API について</span><span class="sxs-lookup"><span data-stu-id="2bbaf-103">About the Free/Busy API</span></span>

<span data-ttu-id="2bbaf-104">空き時間情報 API を使用すると、指定したユーザーアカウントに対して、指定した時間範囲内に、メールプロバイダーが空き時間情報の状態情報を提供できます。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="2bbaf-105">ユーザーの予定表の時間ブロックの空き時間情報は、不在時、取り込み中、仮承諾、または無料のいずれかの状態になります。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="2bbaf-106">空き時間情報プロバイダーを作成する</span><span class="sxs-lookup"><span data-stu-id="2bbaf-106">Create a free/busy provider</span></span>

<span data-ttu-id="2bbaf-107">メールユーザーに空き時間情報を提供するために、メールプロバイダーは空き時間情報プロバイダーを作成し、それを Outlook に登録します。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="2bbaf-108">空き時間情報プロバイダーは、次のインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="2bbaf-109">これらのインターフェイスのメンバーの数はサポートされておらず、指定された戻り値を返す必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="2bbaf-110">特に、空き時間情報 API は、空き時間情報への書き込みアクセス、およびアカウントへの代理人アクセスをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="2bbaf-111">[IFreeBusySupport](ifreebusysupport.md) —このインターフェイスは、指定されたユーザーの空き時間情報データにアクセスするインターフェイスの指定をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="2bbaf-112">[fbuser](fbuser.md)を使用してユーザーを識別します。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="2bbaf-113">[IFreeBusyData](ifreebusydata.md) —このインターフェイスは、指定されたユーザーの時間範囲を取得および設定し、この時間範囲内のデータの空き時間情報ブロックを列挙するためのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="2bbaf-114">この時間範囲を取得して設定するには、相対時間を使用します。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="2bbaf-115">詳細については、「[相対時間を使用して空き時間情報データにアクセスする](how-to-use-relative-time-to-access-free-busy-data.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="2bbaf-116">[IEnumFBBlock](ienumfbblock.md) —このインターフェイスは、時間範囲内のユーザーのデータの空き時間情報ブロックへのアクセスと列挙をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="2bbaf-117">列挙体には、時間範囲 ( [IFreeBusyData:: enumblocks](ifreebusydata-enumblocks.md)で指定されます) 内のユーザーの予定表の空き時間状態を示す空き時間情報ブロックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="2bbaf-118">予定や会議出席依頼などの予定表のアイテムには、列挙のフォームブロックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="2bbaf-119">予定表で相互に隣接していて、空き時間情報の状態が同じであるアイテムは、1つのブロックを形成するために結合されます。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="2bbaf-120">予定表の空き時間もブロックを形成します。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="2bbaf-121">そのため、列挙内の2つの連続するブロックの空き時間状態は同じではありません。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="2bbaf-122">これらのブロックは時間内に重なりません。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="2bbaf-123">予定表に重複するアイテムがある場合、Outlook はこれらのアイテムを結合して、この優先順位 (不在、取り込み中、仮承諾) に基づいて列挙で重複しない空き時間ブロックを形成します。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="2bbaf-124">空き時間情報プロバイダーを Outlook に登録するには、メールプロバイダーは次の操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="2bbaf-125">プロバイダーの**IFreeBusySupport**の実装へのアクセスを許可する CLSID を提供して、空き時間情報プロバイダーを COM に登録します。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="2bbaf-126">システムレジストリ内の次のキー (outlook のバージョンを表す場所`<xx.x>` ) を設定して、空き時間情報プロバイダーが存在することを Outlook に認識させます。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="2bbaf-127">たとえば、トランスポートプロバイダーが SMTP の場合、プロバイダーを Microsoft Outlook 2010 に登録するには、次のキーを次の表のデータに設定します。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="2bbaf-128">名前</span><span class="sxs-lookup"><span data-stu-id="2bbaf-128">Name</span></span> |<span data-ttu-id="2bbaf-129">型</span><span class="sxs-lookup"><span data-stu-id="2bbaf-129">Type</span></span> |<span data-ttu-id="2bbaf-130">値</span><span class="sxs-lookup"><span data-stu-id="2bbaf-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="2bbaf-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="2bbaf-131">SMTP</span></span>  |<span data-ttu-id="2bbaf-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2bbaf-132">REG_SZ</span></span>  |<span data-ttu-id="2bbaf-133">{IFreeBusySupport の各実装の CLSID</span><span class="sxs-lookup"><span data-stu-id="2bbaf-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="2bbaf-134">このシナリオでは、Outlook は COM クラスを共同作成し、それを使用して任意の SMTP メールユーザーの空き時間情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="2bbaf-135">SMTP 以外のアドレスエントリの種類を使用するアドレス帳とトランスポートプロバイダーをサポートするには、その*名前*を適宜変更します。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2bbaf-136">インストール時に、空き時間情報プロバイダーは、同じアドレスエントリの種類のレジストリ設定が既に存在するかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="2bbaf-137">その場合は、そのアドレスエントリの種類について現在のプロバイダーを空き時間情報プロバイダーが上書きし、アンインストール時にそのプロバイダーに復元する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="2bbaf-138">ただし、ユーザーが同じアドレスエントリの種類に対して複数の空き時間情報プロバイダーをインストールしている場合は、これらのプロバイダーをインストールとは逆の順序でアンインストールする必要があります (つまり、常に最新のプロバイダーをアンインストールする必要があります)。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="2bbaf-139">それ以外の場合は、既にアンインストールされているプロバイダーをレジストリが参照している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="2bbaf-140">API コンポーネント</span><span class="sxs-lookup"><span data-stu-id="2bbaf-140">API components</span></span>

<span data-ttu-id="2bbaf-141">空き時間情報 API には、次のコンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2bbaf-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="2bbaf-142">定義</span><span class="sxs-lookup"><span data-stu-id="2bbaf-142">Definitions</span></span>

- [<span data-ttu-id="2bbaf-143">定数 (空き時間情報 API)</span><span class="sxs-lookup"><span data-stu-id="2bbaf-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="2bbaf-144">データ型</span><span class="sxs-lookup"><span data-stu-id="2bbaf-144">Data types</span></span>

- [<span data-ttu-id="2bbaf-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="2bbaf-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="2bbaf-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="2bbaf-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="2bbaf-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="2bbaf-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="2bbaf-148">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="2bbaf-148">Interfaces</span></span>

- [<span data-ttu-id="2bbaf-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="2bbaf-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="2bbaf-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="2bbaf-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="2bbaf-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="2bbaf-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

