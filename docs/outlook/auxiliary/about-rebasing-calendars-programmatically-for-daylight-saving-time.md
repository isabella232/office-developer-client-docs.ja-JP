---
title: 夏時間に合わせてプログラムにより予定表を調整することについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: このトピックでは、春と秋の間には、この期間を DST の期間と呼びます。
ms.openlocfilehash: 4787b2143b3f5d1f0400524f0da82e19e2cbed8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799295"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a><span data-ttu-id="0c5b4-103">夏時間に合わせてプログラムにより予定表を調整することについて</span><span class="sxs-lookup"><span data-stu-id="0c5b4-103">About rebasing calendars programmatically for Daylight Saving Time</span></span>

<span data-ttu-id="0c5b4-104">多くの国では、夜が長くなります (夏時間) できるように、時計を進めることで夏時間 (DST) を観察します。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-104">Many countries observe daylight saving time (DST) by advancing clocks so that evenings have longer daylight.</span></span> <span data-ttu-id="0c5b4-105">、春に今後 1 時間時計を設定することによってこれは、通常、秋の 1 時間にバックアップの時計の設定。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-105">This is typically done by setting the clock an hour ahead in the spring, and setting the clock an hour back in the fall.</span></span> <span data-ttu-id="0c5b4-106">このトピックでは、春と秋の間には、この期間を DST の期間と呼びます。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-106">In this topic, this period between the spring and fall is referred to as the DST period.</span></span> <span data-ttu-id="0c5b4-107">ほとんどの国では、DST の開始時と終了時の独自の規制があります。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-107">Most countries have their own regulations for when DST starts and ends.</span></span> <span data-ttu-id="0c5b4-108">DST の期間の日付から 1 年に 1 年を変更できます、ユーザーする必要があります更新、Microsoft Outlook の予定表毎回 DST 規則を変更することです。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-108">The dates of the DST period can change from year to year, and users must update their Microsoft Outlook calendar every time that the DST regulations change.</span></span> 
  
<span data-ttu-id="0c5b4-109">Windows Vista は、Windows のバージョンを使用するかどうかまたは後で、Windows の自動更新が有効になっていることもすることがありますいない影響を受ける DST の変更。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-109">If you use a version of Windows that is Windows Vista or later, or have Windows automatic update turned on, you may not be affected by the change in DST.</span></span> <span data-ttu-id="0c5b4-110">それ以外の場合、Windows の DST 更新プログラムをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-110">Otherwise, you should install DST updates for Windows.</span></span> <span data-ttu-id="0c5b4-111">DST の期間中に発生するいくつかの既存の予定かどうか、更新プログラムはお客様に代わって、IT 部門では、または自分でホーム ユーザーは、自動的にインストールに関係なく Windows の DST 更新プログラムをインストールした後に誤った時刻を表示可能性があります。.</span><span class="sxs-lookup"><span data-stu-id="0c5b4-111">Regardless of whether the updates are installed automatically, on your behalf by an IT department, or by yourself as a home user, some existing appointments that occur during the DST period might display incorrect times after the DST updates for Windows are installed.</span></span> <span data-ttu-id="0c5b4-112">これは、定期的な予定と単独の予定の場合は true。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-112">This is true for both recurring and single-instance appointments.</span></span> <span data-ttu-id="0c5b4-113">Outlook、Outlook Web App では、およびコラボレーション データ オブジェクト (CDO) をベースとするアプリケーションで正しく表示するのにはこれらの予定を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-113">You must update these appointments to display them correctly in Outlook, in Outlook Web App, and in applications that are based on Collaboration Data Objects (CDO).</span></span> <span data-ttu-id="0c5b4-114">DST のために、カレンダーが正しく表示されている予定を更新すると、予定表を再配置と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-114">Updating incorrectly displayed appointments on calendars because of DST is known as rebasing calendars.</span></span>
  
<span data-ttu-id="0c5b4-115">Outlook には、ユーザー用のツールが用意されていて、Exchange Server には、カレンダーを再設定する管理者用のツールが用意されています。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-115">Outlook provides tools for users and Exchange Server provides tools for administrators to rebase calendars.</span></span> <span data-ttu-id="0c5b4-116">Outlook は、Outlook ユーザーのタイム ゾーン データ更新ツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-116">Outlook provides the Time Zone Data Update Tool for Outlook users.</span></span> <span data-ttu-id="0c5b4-117">このツールでは、ユーザーが独自のカレンダーを更新できます。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-117">With this tool, users can update their own calendars.</span></span> <span data-ttu-id="0c5b4-118">Exchange Server には、管理者が Outlook ツールをすべてのユーザーに広く展開するために発生する問題を回避し、各ユーザーが Outlook ツールを正しく実行するかどうかを確認するのには Exchange 予定表更新ツールが用意されています。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-118">Exchange Server provides the Exchange Calendar Update Tool that helps administrators to avoid difficulties that result from deploying the Outlook tool widely to all users and to make sure that each user runs the Outlook tool correctly.</span></span>
  
<span data-ttu-id="0c5b4-119">タイム ゾーン データ更新ツールを実行するユーザーまたは管理者は、Exchange 予定表更新ツールの実行に依存している、だけでなくサードパーティの MAPI クライアントのソフトウェア開発者は、DLL、Tzmovelib.dll をダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-119">In addition to relying on users to run the Time Zone Data Update Tool or administrators to run the Exchange Calendar Update Tool, third-party MAPI client software developers can download a DLL, Tzmovelib.dll.</span></span> <span data-ttu-id="0c5b4-120">このアセンブリを使用すると、開発者は、Outlook と Exchange Server を使用してツールを再配置の予定表に共通の Api を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-120">By using this assembly, developers can use the same APIs that Outlook and Exchange Server use in their calendar rebasing tools.</span></span> 

<span data-ttu-id="0c5b4-121">Api を再配置する予定表を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-121">The following list shows the calendar rebasing APIs:</span></span>
  
- [<span data-ttu-id="0c5b4-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="0c5b4-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
    
- [<span data-ttu-id="0c5b4-123">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="0c5b4-123">IOlkApptRebaser</span></span>](iolkapptrebaser.md)
    
- [<span data-ttu-id="0c5b4-124">IOlkApptRebaser::BeginEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="0c5b4-124">IOlkApptRebaser::BeginEnumerateAppointments</span></span>](iolkapptrebaser-beginenumerateappointments.md)
    
- [<span data-ttu-id="0c5b4-125">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="0c5b4-125">IOlkApptRebaser::BeginRebaseAppointments</span></span>](iolkapptrebaser-beginrebaseappointments.md)
    
- [<span data-ttu-id="0c5b4-126">IOlkApptRebaser::EndEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="0c5b4-126">IOlkApptRebaser::EndEnumerateAppointments</span></span>](iolkapptrebaser-endenumerateappointments.md)
    
- [<span data-ttu-id="0c5b4-127">IOlkApptRebaser::EndRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="0c5b4-127">IOlkApptRebaser::EndRebaseAppointments</span></span>](iolkapptrebaser-endrebaseappointments.md)
    
- [<span data-ttu-id="0c5b4-128">PidLidAppointmentTimeZoneDefinitionEndDisplay</span><span class="sxs-lookup"><span data-stu-id="0c5b4-128">PidLidAppointmentTimeZoneDefinitionEndDisplay</span></span>](http://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [<span data-ttu-id="0c5b4-129">PidLidAppointmentTimeZoneDefinitionRecur</span><span class="sxs-lookup"><span data-stu-id="0c5b4-129">PidLidAppointmentTimeZoneDefinitionRecur</span></span>](http://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [<span data-ttu-id="0c5b4-130">PidLidAppointmentTimeZoneDefinitionStartDisplay</span><span class="sxs-lookup"><span data-stu-id="0c5b4-130">PidLidAppointmentTimeZoneDefinitionStartDisplay</span></span>](http://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [<span data-ttu-id="0c5b4-131">PidLidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="0c5b4-131">PidLidTimeZoneStruct</span></span>](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [<span data-ttu-id="0c5b4-132">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="0c5b4-132">RebaseTaskComplete</span></span>](rebasetaskcomplete.md)
    
- [<span data-ttu-id="0c5b4-133">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="0c5b4-133">RebaseTaskProgress</span></span>](rebasetaskprogress.md)
    
- [<span data-ttu-id="0c5b4-134">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="0c5b4-134">TZDEFINITION</span></span>](tzdefinition.md)
    
- [<span data-ttu-id="0c5b4-135">TZREG</span><span class="sxs-lookup"><span data-stu-id="0c5b4-135">TZREG</span></span>](tzreg.md)
    
- [<span data-ttu-id="0c5b4-136">TZRULE</span><span class="sxs-lookup"><span data-stu-id="0c5b4-136">TZRULE</span></span>](tzrule.md)
    
<span data-ttu-id="0c5b4-137">Api を再配置する予定表を使用して予定の再配置ツールを作成するには、次の手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-137">To write an appointment rebasing tool by using the calendar rebasing APIs, you can use the following procedure:</span></span>
  
1. <span data-ttu-id="0c5b4-138">候補を再配置するため、予定を検索するのにには、 **IOlkApptRebaser::BeginEnumerateAppointments**と**IOlkApptRebaser::EndEnumerateAppointments**を使用します。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-138">Use **IOlkApptRebaser::BeginEnumerateAppointments** and **IOlkApptRebaser::EndEnumerateAppointments** to find appointments that are candidates for rebasing.</span></span> <span data-ttu-id="0c5b4-139">必要に応じて、再配置するには、対象となる予定を決定するユーザーを有効にする情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-139">If necessary, present information to enable the user to decide which appointments to rebase.</span></span> <span data-ttu-id="0c5b4-140">また、MAPI または Outlook オブジェクト モデルを使用して、 **PidLidAppointmentTimeZoneDefinitionStartDisplay**、 **PidLidAppointmentTimeZoneDefinitionEndDisplay**を解析することによって、予定の時間と定期的なアイテムの情報を確認するには**PidLidAppointmentTimeZoneDefinitionRecur**のプロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-140">Alternatively, use MAPI or the Outlook Object Model to examine the time and recurrence information for an appointment by parsing the **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay**, and **PidLidAppointmentTimeZoneDefinitionRecur** properties.</span></span> 
    
2. <span data-ttu-id="0c5b4-141">予定を再配置するのにには、 **HrCreateApptRebaser**、 **IOlkApptRebaser::BeginRebaseAppointments**、および**IOlkApptRebaser::EndRebaseAppointments**を使用します。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-141">Use **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments**, and **IOlkApptRebaser::EndRebaseAppointments** to rebase the appointment.</span></span> 
    
<span data-ttu-id="0c5b4-142">Tzmovelib.dll アセンブリを取得するには、「OutlookTimeZoneMoveLibRedist.exe の再頒布可能なインストーラーと、Tzmovelib.h ヘッダー ファイルでの使用」をダウンロードしていますください。 [Outlook 2010: 補助型の参照の再頒布可能なインストーラーと再配置の予定表のヘッダー ファイル](http://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).</span><span class="sxs-lookup"><span data-stu-id="0c5b4-142">To obtain the Tzmovelib.dll assembly, download the OutlookTimeZoneMoveLibRedist.exe redistributable installer and the Tzmovelib.h header file at [Outlook 2010: Auxiliary Reference Redistributable Installer and Header File for Rebasing Calendars](http://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).</span></span> <span data-ttu-id="0c5b4-143">このダウンロードは、Outlook 2010 およびそれ以降のバージョンの Outlook の動作します。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-143">This download works for Outlook 2010 and later versions of Outlook.</span></span> <span data-ttu-id="0c5b4-144">OutlookTimeZoneMoveLibRedist.exe は、C:\Program Files\MsExTmz で Tzmovelib.dll のアセンブリ ファイルをインストールします。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-144">OutlookTimeZoneMoveLibRedist.exe installs the Tzmovelib.dll assembly file in C:\Program Files\MsExTmz.</span></span> <span data-ttu-id="0c5b4-145">そのサードパーティ製のカレンダー アプリケーションを再配置は、OutlookTimeZoneMoveLibRedist.exe、インストーラーのみを再配布でき、アセンブリ、Tzmovelib.dll、またはインストーラーから個別に抽出されたその他のコンポーネントを再配布する必要があります注意してください。</span><span class="sxs-lookup"><span data-stu-id="0c5b4-145">Note that third-party calendar rebasing applications can redistribute only the installer, OutlookTimeZoneMoveLibRedist.exe, and must not redistribute the assembly, Tzmovelib.dll, or any other extracted components separately from the installer.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0c5b4-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c5b4-146">See also</span></span>

- [<span data-ttu-id="0c5b4-147">バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて</span><span class="sxs-lookup"><span data-stu-id="0c5b4-147">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [<span data-ttu-id="0c5b4-148">バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る</span><span class="sxs-lookup"><span data-stu-id="0c5b4-148">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="0c5b4-149">バイナリ プロパティからのストリームを解析し、TZREG 構造体を読み取る</span><span class="sxs-lookup"><span data-stu-id="0c5b4-149">Parse a stream from a binary property to read the TZREG structure</span></span>](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [<span data-ttu-id="0c5b4-150">予定からタイム ゾーンのプロパティを読み取る</span><span class="sxs-lookup"><span data-stu-id="0c5b4-150">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)
- [<span data-ttu-id="0c5b4-151">夏時間のヘルプとサポート センター</span><span class="sxs-lookup"><span data-stu-id="0c5b4-151">Daylight Saving Time Help and Support Center</span></span>](http://support.microsoft.com/gp/cp_dst)
- [<span data-ttu-id="0c5b4-152">Exchange 予定表更新ツールを使用して夏時間に対応する方法</span><span class="sxs-lookup"><span data-stu-id="0c5b4-152">How to address daylight saving time by using the Exchange Calendar Update Tool</span></span>](http://support.microsoft.com/kb/941018)
- [<span data-ttu-id="0c5b4-153">Microsoft Office Outlook 用タイム ゾーン データ更新ツールを使用してタイム ゾーンの変更に対処する方法</span><span class="sxs-lookup"><span data-stu-id="0c5b4-153">How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook</span></span>](http://support.microsoft.com/kb/931667)

