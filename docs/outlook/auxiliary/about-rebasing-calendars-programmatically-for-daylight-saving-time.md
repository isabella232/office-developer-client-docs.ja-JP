---
title: 夏時間に合わせてプログラムにより予定表を調整することについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: このトピックでは、春と秋の間の期間を DST 期間と呼びます。
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316955"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a><span data-ttu-id="266c1-103">夏時間に合わせてプログラムにより予定表を調整することについて</span><span class="sxs-lookup"><span data-stu-id="266c1-103">About rebasing calendars programmatically for Daylight Saving Time</span></span>

<span data-ttu-id="266c1-104">多くの国では、夜の夏時間を延長することで夏時間 (DST) を守っています。</span><span class="sxs-lookup"><span data-stu-id="266c1-104">Many countries observe daylight saving time (DST) by advancing clocks so that evenings have longer daylight.</span></span> <span data-ttu-id="266c1-105">これは、通常、スプリングを1時間に設定してから、秋に時計を1時間後に設定することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="266c1-105">This is typically done by setting the clock an hour ahead in the spring, and setting the clock an hour back in the fall.</span></span> <span data-ttu-id="266c1-106">このトピックでは、春と秋の間の期間を DST 期間と呼びます。</span><span class="sxs-lookup"><span data-stu-id="266c1-106">In this topic, this period between the spring and fall is referred to as the DST period.</span></span> <span data-ttu-id="266c1-107">ほとんどの国には、DST の開始時と終了時に固有の規制があります。</span><span class="sxs-lookup"><span data-stu-id="266c1-107">Most countries have their own regulations for when DST starts and ends.</span></span> <span data-ttu-id="266c1-108">dst の期間の日付は年単位で変更され、ユーザーは dst 規則が変更されるたびに Microsoft Outlook の予定表を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266c1-108">The dates of the DST period can change from year to year, and users must update their Microsoft Outlook calendar every time that the DST regulations change.</span></span> 
  
<span data-ttu-id="266c1-109">windows Vista 以降のバージョンの windows を使用している場合、または windows 自動更新が有効になっている場合は、DST の変更による影響を受けない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="266c1-109">If you use a version of Windows that is Windows Vista or later, or have Windows automatic update turned on, you may not be affected by the change in DST.</span></span> <span data-ttu-id="266c1-110">それ以外の場合は、Windows 用の DST 更新プログラムをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="266c1-110">Otherwise, you should install DST updates for Windows.</span></span> <span data-ttu-id="266c1-111">更新プログラムが自動的にインストールされるのか、IT 部門が代行するのか、または自宅ユーザーであるかに関係なく、dst 期間中に発生する既存の予定の中には、Windows の dst 更新プログラムのインストール後に誤った時刻が表示される場合があります。.</span><span class="sxs-lookup"><span data-stu-id="266c1-111">Regardless of whether the updates are installed automatically, on your behalf by an IT department, or by yourself as a home user, some existing appointments that occur during the DST period might display incorrect times after the DST updates for Windows are installed.</span></span> <span data-ttu-id="266c1-112">これは、定期的な予定と単一インスタンスの予定の両方に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="266c1-112">This is true for both recurring and single-instance appointments.</span></span> <span data-ttu-id="266c1-113">これらの予定を更新して、outlook、outlook Web App、およびコラボレーションデータオブジェクト (CDO) に基づくアプリケーションで、これらを正しく表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266c1-113">You must update these appointments to display them correctly in Outlook, in Outlook Web App, and in applications that are based on Collaboration Data Objects (CDO).</span></span> <span data-ttu-id="266c1-114">DST のために予定表を再配置するという理由で、正しく表示されていない予定を予定表に更新します。</span><span class="sxs-lookup"><span data-stu-id="266c1-114">Updating incorrectly displayed appointments on calendars because of DST is known as rebasing calendars.</span></span>
  
<span data-ttu-id="266c1-115">Outlook には、ユーザーおよび Exchange Server 用のツールが用意されており、管理者は予定表を再配置することができます。</span><span class="sxs-lookup"><span data-stu-id="266c1-115">Outlook provides tools for users and Exchange Server provides tools for administrators to rebase calendars.</span></span> <span data-ttu-id="266c1-116">outlook では、outlook ユーザー用のタイムゾーンデータ更新ツールが提供されています。</span><span class="sxs-lookup"><span data-stu-id="266c1-116">Outlook provides the Time Zone Data Update Tool for Outlook users.</span></span> <span data-ttu-id="266c1-117">このツールを使用すると、ユーザーは自分の予定表を更新できます。</span><span class="sxs-lookup"><span data-stu-id="266c1-117">With this tool, users can update their own calendars.</span></span> <span data-ttu-id="266c1-118">exchange Server には、管理者が exchange 予定表更新ツールを提供しており、outlook ツールをすべてのユーザーに幅広く展開し、各ユーザーが outlook ツールを正しく実行していることを確認することによって、問題が発生しないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="266c1-118">Exchange Server provides the Exchange Calendar Update Tool that helps administrators to avoid difficulties that result from deploying the Outlook tool widely to all users and to make sure that each user runs the Outlook tool correctly.</span></span>
  
<span data-ttu-id="266c1-119">タイムゾーンデータ更新ツールまたは管理者が Exchange 予定表更新ツールを実行するためにユーザーに依存するだけでなく、サードパーティ製の MAPI クライアントソフトウェア開発者は dll、tzmovelib.h をダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="266c1-119">In addition to relying on users to run the Time Zone Data Update Tool or administrators to run the Exchange Calendar Update Tool, third-party MAPI client software developers can download a DLL, Tzmovelib.dll.</span></span> <span data-ttu-id="266c1-120">このアセンブリを使用すると、開発者は Outlook と Exchange Server が予定表の再配置ツールで使用するのと同じ api を使用できます。</span><span class="sxs-lookup"><span data-stu-id="266c1-120">By using this assembly, developers can use the same APIs that Outlook and Exchange Server use in their calendar rebasing tools.</span></span> 

<span data-ttu-id="266c1-121">次のリストは、カレンダーの再配置 api を示しています。</span><span class="sxs-lookup"><span data-stu-id="266c1-121">The following list shows the calendar rebasing APIs:</span></span>
  
- [<span data-ttu-id="266c1-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="266c1-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
    
- [<span data-ttu-id="266c1-123">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="266c1-123">IOlkApptRebaser</span></span>](iolkapptrebaser.md)
    
- [<span data-ttu-id="266c1-124">IOlkApptRebaser::BeginEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="266c1-124">IOlkApptRebaser::BeginEnumerateAppointments</span></span>](iolkapptrebaser-beginenumerateappointments.md)
    
- [<span data-ttu-id="266c1-125">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="266c1-125">IOlkApptRebaser::BeginRebaseAppointments</span></span>](iolkapptrebaser-beginrebaseappointments.md)
    
- [<span data-ttu-id="266c1-126">IOlkApptRebaser::EndEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="266c1-126">IOlkApptRebaser::EndEnumerateAppointments</span></span>](iolkapptrebaser-endenumerateappointments.md)
    
- [<span data-ttu-id="266c1-127">IOlkApptRebaser::EndRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="266c1-127">IOlkApptRebaser::EndRebaseAppointments</span></span>](iolkapptrebaser-endrebaseappointments.md)
    
- [<span data-ttu-id="266c1-128">PidLidAppointmentTimeZoneDefinitionEndDisplay</span><span class="sxs-lookup"><span data-stu-id="266c1-128">PidLidAppointmentTimeZoneDefinitionEndDisplay</span></span>](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [<span data-ttu-id="266c1-129">PidLidAppointmentTimeZoneDefinitionRecur</span><span class="sxs-lookup"><span data-stu-id="266c1-129">PidLidAppointmentTimeZoneDefinitionRecur</span></span>](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [<span data-ttu-id="266c1-130">PidLidAppointmentTimeZoneDefinitionStartDisplay</span><span class="sxs-lookup"><span data-stu-id="266c1-130">PidLidAppointmentTimeZoneDefinitionStartDisplay</span></span>](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [<span data-ttu-id="266c1-131">PidLidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="266c1-131">PidLidTimeZoneStruct</span></span>](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [<span data-ttu-id="266c1-132">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="266c1-132">RebaseTaskComplete</span></span>](rebasetaskcomplete.md)
    
- [<span data-ttu-id="266c1-133">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="266c1-133">RebaseTaskProgress</span></span>](rebasetaskprogress.md)
    
- [<span data-ttu-id="266c1-134">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="266c1-134">TZDEFINITION</span></span>](tzdefinition.md)
    
- [<span data-ttu-id="266c1-135">TZREG</span><span class="sxs-lookup"><span data-stu-id="266c1-135">TZREG</span></span>](tzreg.md)
    
- [<span data-ttu-id="266c1-136">TZRULE</span><span class="sxs-lookup"><span data-stu-id="266c1-136">TZRULE</span></span>](tzrule.md)
    
<span data-ttu-id="266c1-137">予定表の再配置 api を使用して予定の再配置ツールを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="266c1-137">To write an appointment rebasing tool by using the calendar rebasing APIs, you can use the following procedure:</span></span>
  
1. <span data-ttu-id="266c1-138">**IOlkApptRebaser:: BeginEnumerateAppointments**と**IOlkApptRebaser:: EndEnumerateAppointments**を使用して、再配置する候補の予定を検索します。</span><span class="sxs-lookup"><span data-stu-id="266c1-138">Use **IOlkApptRebaser::BeginEnumerateAppointments** and **IOlkApptRebaser::EndEnumerateAppointments** to find appointments that are candidates for rebasing.</span></span> <span data-ttu-id="266c1-139">必要に応じて、再配置する予定を決定するための情報をユーザーに提示します。</span><span class="sxs-lookup"><span data-stu-id="266c1-139">If necessary, present information to enable the user to decide which appointments to rebase.</span></span> <span data-ttu-id="266c1-140">または、MAPI または Outlook オブジェクトモデルを使用して、 **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay**を解析することにより、予定の時刻と定期的な情報を調べます。プロパティと**PidLidAppointmentTimeZoneDefinitionRecur**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="266c1-140">Alternatively, use MAPI or the Outlook Object Model to examine the time and recurrence information for an appointment by parsing the **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay**, and **PidLidAppointmentTimeZoneDefinitionRecur** properties.</span></span> 
    
2. <span data-ttu-id="266c1-141">**hrcreateapptrebaser**、 **IOlkApptRebaser:: beginrebaseappointments**、および**IOlkApptRebaser:: endrebaseappointments**を使用して、予定を再配置します。</span><span class="sxs-lookup"><span data-stu-id="266c1-141">Use **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments**, and **IOlkApptRebaser::EndRebaseAppointments** to rebase the appointment.</span></span> 
    
<span data-ttu-id="266c1-142">、tzmovelib.h アセンブリを入手するには、OutlookTimeZoneMoveLibRedist 再頒布可能パッケージと、tzmovelib.h ヘッダーファイルを Outlook にダウンロードします。 [2010: 補助参照再配布可能なインストーラーと、予定表を再配置するためのヘッダーファイル](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).</span><span class="sxs-lookup"><span data-stu-id="266c1-142">To obtain the Tzmovelib.dll assembly, download the OutlookTimeZoneMoveLibRedist.exe redistributable installer and the Tzmovelib.h header file at [Outlook 2010: Auxiliary Reference Redistributable Installer and Header File for Rebasing Calendars](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).</span></span> <span data-ttu-id="266c1-143">このダウンロードは、outlook 2010 以降のバージョンの outlook で使用できます。</span><span class="sxs-lookup"><span data-stu-id="266c1-143">This download works for Outlook 2010 and later versions of Outlook.</span></span> <span data-ttu-id="266c1-144">OutlookTimeZoneMoveLibRedist は、、tzmovelib.h アセンブリファイルを C:\Program Files\MsExTmz. にインストールします。</span><span class="sxs-lookup"><span data-stu-id="266c1-144">OutlookTimeZoneMoveLibRedist.exe installs the Tzmovelib.dll assembly file in C:\Program Files\MsExTmz.</span></span> <span data-ttu-id="266c1-145">サードパーティ製の予定表の再配置アプリケーションは、インストーラ OutlookTimeZoneMoveLibRedist のみを再配布することができ、アセンブリ、、tzmovelib.h、またはその他の抽出されたコンポーネントをインストーラーとは別に再配布することはできません。</span><span class="sxs-lookup"><span data-stu-id="266c1-145">Note that third-party calendar rebasing applications can redistribute only the installer, OutlookTimeZoneMoveLibRedist.exe, and must not redistribute the assembly, Tzmovelib.dll, or any other extracted components separately from the installer.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="266c1-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="266c1-146">See also</span></span>

- [<span data-ttu-id="266c1-147">バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて</span><span class="sxs-lookup"><span data-stu-id="266c1-147">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [<span data-ttu-id="266c1-148">バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る</span><span class="sxs-lookup"><span data-stu-id="266c1-148">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="266c1-149">バイナリ プロパティからのストリームを解析し、TZREG 構造体を読み取る</span><span class="sxs-lookup"><span data-stu-id="266c1-149">Parse a stream from a binary property to read the TZREG structure</span></span>](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [<span data-ttu-id="266c1-150">予定からタイム ゾーンのプロパティを読み取る</span><span class="sxs-lookup"><span data-stu-id="266c1-150">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)
- [<span data-ttu-id="266c1-151">夏時間のヘルプとサポートセンター</span><span class="sxs-lookup"><span data-stu-id="266c1-151">Daylight Saving Time Help and Support Center</span></span>](https://support.microsoft.com/gp/cp_dst)
- [<span data-ttu-id="266c1-152">Exchange 予定表更新ツールを使用して夏時間に対処する方法</span><span class="sxs-lookup"><span data-stu-id="266c1-152">How to address daylight saving time by using the Exchange Calendar Update Tool</span></span>](https://support.microsoft.com/kb/941018)
- <span data-ttu-id="266c1-153">[[方法] Microsoft Office Outlook 用タイムゾーンデータ更新ツールを使用してタイムゾーンの変更に対処する](https://support.microsoft.com/kb/931667)</span><span class="sxs-lookup"><span data-stu-id="266c1-153">[How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667)</span></span>

