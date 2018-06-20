---
title: 空き/予約済み API について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: 空き/予約済み API では、指定の時間範囲内の指定したユーザー アカウントの空き時間情報のステータス情報を提供するメール プロバイダーを使用します。
ms.openlocfilehash: 8b1559173297fbde9930b6f8f7fbc74f176273da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799300"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="44544-103">空き/予約済み API について</span><span class="sxs-lookup"><span data-stu-id="44544-103">About the Free/Busy API</span></span>

<span data-ttu-id="44544-104">空き/予約済み API では、指定の時間範囲内の指定したユーザー アカウントの空き時間情報のステータス情報を提供するメール プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="44544-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="44544-105">ユーザーの予定表で時間帯の空き時間情報のステータスは、次のいずれか: 不在時の使用中、仮承諾、または無料です。</span><span class="sxs-lookup"><span data-stu-id="44544-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="44544-106">空き/予約済みのプロバイダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="44544-106">Create a free/busy provider</span></span>

<span data-ttu-id="44544-107">メール ユーザーに空き時間情報を提供するには、メール プロバイダーは空き/予約済みのプロバイダーを作成し、Outlook に登録します。</span><span class="sxs-lookup"><span data-stu-id="44544-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="44544-108">空き/予約済みのプロバイダーは、次のインタ フェースを実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="44544-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="44544-109">これらのインターフェイスのメンバーの多くがサポートされておらず、指定した戻り値を返す必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="44544-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="44544-110">具体的には、空き/予約済み API は空き時間情報およびアカウントへのアクセスを委任への書き込みアクセスをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="44544-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="44544-111">[IFreeBusySupport](ifreebusysupport.md) -このインターフェイスは、指定したユーザーの空き時間情報データにアクセスするインターフェイスの仕様をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="44544-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="44544-112">[FBUser](fbuser.md)を使用してユーザーを識別します。</span><span class="sxs-lookup"><span data-stu-id="44544-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="44544-113">[IFreeBusyData](ifreebusydata.md) -このインターフェイスを取得しユーザーが指定した時間範囲を設定し、この時間の範囲内のデータのブロックの空き時間情報を列挙するためのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="44544-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="44544-114">相対時間を使用して取得し、この時間範囲を設定します。</span><span class="sxs-lookup"><span data-stu-id="44544-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="44544-115">詳細については、[空き時間情報データにアクセスするのには相対的な時間の使用](how-to-use-relative-time-to-access-free-busy-data.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44544-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="44544-116">[IEnumFBBlock](ienumfbblock.md) -このインターフェイスにアクセスして、時間の範囲内でのユーザーのデータのブロックの空き時間情報を列挙をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="44544-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="44544-117">列挙体には、( [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)で指定された) 時間の範囲内で、ユーザーの予定表で時間の期間の空き時間情報のステータスを示す空き時間情報のブロックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="44544-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="44544-118">予定および会議出席依頼などの予定表のアイテムは、列挙体のブロックを形成します。</span><span class="sxs-lookup"><span data-stu-id="44544-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="44544-119">カレンダーに互いに隣接しているし、同じ空き時間情報のステータスを持つアイテムは、1 つのブロックを 1 つのフォームに結合されます。</span><span class="sxs-lookup"><span data-stu-id="44544-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="44544-120">カレンダー上の時間の無料期間もブロックを形成します。</span><span class="sxs-lookup"><span data-stu-id="44544-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="44544-121">したがって、列挙型の連続する 2 つのブロックがありません。 には、同じ空き時間情報のステータスがあります。</span><span class="sxs-lookup"><span data-stu-id="44544-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="44544-122">これらのブロックは、時に重複しません。</span><span class="sxs-lookup"><span data-stu-id="44544-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="44544-123">これらの項目の優先順位に基づいて列挙体の空き/予約済みブロックの重複を形成する結合 Outlook の予定表に重複する項目がある場合は、: 不在時の予定あり、仮の予定です。</span><span class="sxs-lookup"><span data-stu-id="44544-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="44544-124">Outlook で空き時間情報のプロバイダーを登録するにメール プロバイダーは、次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="44544-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="44544-125">COM、 **IFreeBusySupport**のプロバイダーの実装にアクセスできるようにするための CLSID を提供することで、空き/予約済みのプロバイダーを登録します。</span><span class="sxs-lookup"><span data-stu-id="44544-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="44544-126">自動的に次のキーを設定することによって、空き/予約済みのプロバイダーの存在を (位置`<xx.x>`Outlook のバージョンを表します)、システム レジストリに。</span><span class="sxs-lookup"><span data-stu-id="44544-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="44544-127">などのトランスポート プロバイダーが SMTP である場合は、Microsoft Outlook 2010 では、プロバイダーを登録するのには次のキーに設定次の表のデータ。</span><span class="sxs-lookup"><span data-stu-id="44544-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="44544-128">名前</span><span class="sxs-lookup"><span data-stu-id="44544-128">Name</span></span> |<span data-ttu-id="44544-129">種類</span><span class="sxs-lookup"><span data-stu-id="44544-129">Type</span></span> |<span data-ttu-id="44544-130">値</span><span class="sxs-lookup"><span data-stu-id="44544-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="44544-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="44544-131">SMTP</span></span>  |<span data-ttu-id="44544-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="44544-132">REG_SZ</span></span>  |<span data-ttu-id="44544-133">{CLSID} IFreeBusySupport のそれぞれの実装について</span><span class="sxs-lookup"><span data-stu-id="44544-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="44544-134">このシナリオでは、Outlook の COM クラスを再作成して使用して SMTP メール ユーザーの空き時間情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="44544-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="44544-135">SMTP 以外のアドレス エントリの種類を使用しているアドレス帳とトランスポート プロバイダーをサポートするためには、それに応じて*名前*を変更します。</span><span class="sxs-lookup"><span data-stu-id="44544-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="44544-136">かどうかのレジストリ設定、インストール時にプロバイダーの空き時間情報をチェック、同じアドレスのエントリの種類が既に存在します。</span><span class="sxs-lookup"><span data-stu-id="44544-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="44544-137">場合は、空き/予約済みのプロバイダーはそのアドレスのエントリの種類の現在のプロバイダーを上書きし、そのプロバイダーのアンインストール時に復元ください。</span><span class="sxs-lookup"><span data-stu-id="44544-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="44544-138">ただし、ユーザーが同じアドレスのエントリの種類の 1 つ以上の空き/予約済みのプロバイダーをインストールしている場合、ユーザーする必要がありますアンインストールこれらのプロバイダーのインストールと逆の順序で (つまり、常にアンインストール、最新のプロバイダー)。</span><span class="sxs-lookup"><span data-stu-id="44544-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="44544-139">それ以外の場合、レジストリは、既にアンインストールされているプロバイダーにポイントがあります。</span><span class="sxs-lookup"><span data-stu-id="44544-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="44544-140">API コンポーネント</span><span class="sxs-lookup"><span data-stu-id="44544-140">API components</span></span>

<span data-ttu-id="44544-141">空き/予約済みの API には、次のコンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="44544-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="44544-142">定義</span><span class="sxs-lookup"><span data-stu-id="44544-142">Definitions</span></span>

- [<span data-ttu-id="44544-143">定数 (空き時間情報の API)</span><span class="sxs-lookup"><span data-stu-id="44544-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="44544-144">データ型</span><span class="sxs-lookup"><span data-stu-id="44544-144">Data types</span></span>

- [<span data-ttu-id="44544-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="44544-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="44544-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="44544-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="44544-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="44544-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="44544-148">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="44544-148">Interfaces</span></span>

- [<span data-ttu-id="44544-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="44544-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="44544-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="44544-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="44544-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="44544-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

