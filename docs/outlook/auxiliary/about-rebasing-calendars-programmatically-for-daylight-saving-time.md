---
title: 夏時間に合わせてプログラムにより予定表を調整することについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: このトピックでは、春と秋の間のこの期間を DST 期間と呼ばれます。
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316955"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a><span data-ttu-id="19e04-103">夏時間に合わせてプログラムにより予定表を調整することについて</span><span class="sxs-lookup"><span data-stu-id="19e04-103">About rebasing calendars programmatically for Daylight Saving Time</span></span>

<span data-ttu-id="19e04-104">多くの国では、夜間の夏時間が長くなるので、クロックを進めることによって夏時間 (DST) が観測されます。</span><span class="sxs-lookup"><span data-stu-id="19e04-104">Many countries observe daylight saving time (DST) by advancing clocks so that evenings have longer daylight.</span></span> <span data-ttu-id="19e04-105">これは通常、春に 1 時間先に時計を設定し、秋に 1 時間戻して設定することで行われます。</span><span class="sxs-lookup"><span data-stu-id="19e04-105">This is typically done by setting the clock an hour ahead in the spring, and setting the clock an hour back in the fall.</span></span> <span data-ttu-id="19e04-106">このトピックでは、春と秋の間のこの期間を DST 期間と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="19e04-106">In this topic, this period between the spring and fall is referred to as the DST period.</span></span> <span data-ttu-id="19e04-107">ほとんどの国では、DST の開始および終了に関する独自の規制があります。</span><span class="sxs-lookup"><span data-stu-id="19e04-107">Most countries have their own regulations for when DST starts and ends.</span></span> <span data-ttu-id="19e04-108">DST 期間の日付は年ごとに変更される可能性があります。また、ユーザーは DST 規制が変更される度に Microsoft Outlookカレンダーを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19e04-108">The dates of the DST period can change from year to year, and users must update their Microsoft Outlook calendar every time that the DST regulations change.</span></span> 
  
<span data-ttu-id="19e04-109">Vista 以降のバージョンの Windows を使用Windows、または Windows 自動更新を有効にしている場合は、DST の変更の影響を受けない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="19e04-109">If you use a version of Windows that is Windows Vista or later, or have Windows automatic update turned on, you may not be affected by the change in DST.</span></span> <span data-ttu-id="19e04-110">それ以外の場合は、DST 更新プログラムをインストールする必要Windows。</span><span class="sxs-lookup"><span data-stu-id="19e04-110">Otherwise, you should install DST updates for Windows.</span></span> <span data-ttu-id="19e04-111">更新プログラムが自動的にインストールされるか、IT 部門によって、またはホーム ユーザーとして自動的にインストールされるかに関係なく、DST 期間中に発生する一部の既存の予定は、Windows の DST 更新プログラムがインストールされた後に正しく表示されません。</span><span class="sxs-lookup"><span data-stu-id="19e04-111">Regardless of whether the updates are installed automatically, on your behalf by an IT department, or by yourself as a home user, some existing appointments that occur during the DST period might display incorrect times after the DST updates for Windows are installed.</span></span> <span data-ttu-id="19e04-112">これは、定期的な予定と単一インスタンスの予定の両方に当てはまる。</span><span class="sxs-lookup"><span data-stu-id="19e04-112">This is true for both recurring and single-instance appointments.</span></span> <span data-ttu-id="19e04-113">これらの予定を更新して、Outlook、Outlook Web App、およびコラボレーション データ オブジェクト (CDO) に基づくアプリケーションで正しく表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19e04-113">You must update these appointments to display them correctly in Outlook, in Outlook Web App, and in applications that are based on Collaboration Data Objects (CDO).</span></span> <span data-ttu-id="19e04-114">DST が理由で予定表に正しく表示されていない予定を更新すると、予定表の再予約と呼ばれることがあります。</span><span class="sxs-lookup"><span data-stu-id="19e04-114">Updating incorrectly displayed appointments on calendars because of DST is known as rebasing calendars.</span></span>
  
<span data-ttu-id="19e04-115">Outlookユーザーと管理者向けツールExchange Server、管理者が予定表を再ベースするためのツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="19e04-115">Outlook provides tools for users and Exchange Server provides tools for administrators to rebase calendars.</span></span> <span data-ttu-id="19e04-116">Outlookユーザー向けタイム ゾーン データ更新ツールOutlook提供します。</span><span class="sxs-lookup"><span data-stu-id="19e04-116">Outlook provides the Time Zone Data Update Tool for Outlook users.</span></span> <span data-ttu-id="19e04-117">このツールを使用すると、ユーザーは自分の予定表を更新できます。</span><span class="sxs-lookup"><span data-stu-id="19e04-117">With this tool, users can update their own calendars.</span></span> <span data-ttu-id="19e04-118">Exchange Server Exchange カレンダー更新ツールは、管理者が Outlook ツールをすべてのユーザーに広く展開し、各ユーザーが Outlook ツールを正しく実行することで生じにくい問題を回避するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="19e04-118">Exchange Server provides the Exchange Calendar Update Tool that helps administrators to avoid difficulties that result from deploying the Outlook tool widely to all users and to make sure that each user runs the Outlook tool correctly.</span></span>
  
<span data-ttu-id="19e04-119">ユーザーがタイム ゾーン データ更新ツールを実行するか、管理者が Exchange 予定表更新ツールを実行するだけでなく、サードパーティの MAPI クライアント ソフトウェア開発者は DLL、Tzmovelib.dll をダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="19e04-119">In addition to relying on users to run the Time Zone Data Update Tool or administrators to run the Exchange Calendar Update Tool, third-party MAPI client software developers can download a DLL, Tzmovelib.dll.</span></span> <span data-ttu-id="19e04-120">このアセンブリを使用すると、開発者はカレンダーの再OutlookツールExchange Server同じ API を使用できます。</span><span class="sxs-lookup"><span data-stu-id="19e04-120">By using this assembly, developers can use the same APIs that Outlook and Exchange Server use in their calendar rebasing tools.</span></span> 

<span data-ttu-id="19e04-121">次の一覧は、予定表の再バーズ API を示しています。</span><span class="sxs-lookup"><span data-stu-id="19e04-121">The following list shows the calendar rebasing APIs:</span></span>
  
- [<span data-ttu-id="19e04-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="19e04-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
    
- [<span data-ttu-id="19e04-123">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="19e04-123">IOlkApptRebaser</span></span>](iolkapptrebaser.md)
    
- [<span data-ttu-id="19e04-124">IOlkApptRebaser::BeginEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="19e04-124">IOlkApptRebaser::BeginEnumerateAppointments</span></span>](iolkapptrebaser-beginenumerateappointments.md)
    
- [<span data-ttu-id="19e04-125">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="19e04-125">IOlkApptRebaser::BeginRebaseAppointments</span></span>](iolkapptrebaser-beginrebaseappointments.md)
    
- [<span data-ttu-id="19e04-126">IOlkApptRebaser::EndEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="19e04-126">IOlkApptRebaser::EndEnumerateAppointments</span></span>](iolkapptrebaser-endenumerateappointments.md)
    
- [<span data-ttu-id="19e04-127">IOlkApptRebaser::EndRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="19e04-127">IOlkApptRebaser::EndRebaseAppointments</span></span>](iolkapptrebaser-endrebaseappointments.md)
    
- [<span data-ttu-id="19e04-128">PidLidAppointmentTimeZoneDefinitionEndDisplay</span><span class="sxs-lookup"><span data-stu-id="19e04-128">PidLidAppointmentTimeZoneDefinitionEndDisplay</span></span>](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [<span data-ttu-id="19e04-129">PidLidAppointmentTimeZoneDefinitionRecur</span><span class="sxs-lookup"><span data-stu-id="19e04-129">PidLidAppointmentTimeZoneDefinitionRecur</span></span>](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [<span data-ttu-id="19e04-130">PidLidAppointmentTimeZoneDefinitionStartDisplay</span><span class="sxs-lookup"><span data-stu-id="19e04-130">PidLidAppointmentTimeZoneDefinitionStartDisplay</span></span>](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [<span data-ttu-id="19e04-131">PidLidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="19e04-131">PidLidTimeZoneStruct</span></span>](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [<span data-ttu-id="19e04-132">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="19e04-132">RebaseTaskComplete</span></span>](rebasetaskcomplete.md)
    
- [<span data-ttu-id="19e04-133">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="19e04-133">RebaseTaskProgress</span></span>](rebasetaskprogress.md)
    
- [<span data-ttu-id="19e04-134">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="19e04-134">TZDEFINITION</span></span>](tzdefinition.md)
    
- [<span data-ttu-id="19e04-135">TZREG</span><span class="sxs-lookup"><span data-stu-id="19e04-135">TZREG</span></span>](tzreg.md)
    
- [<span data-ttu-id="19e04-136">TZRULE</span><span class="sxs-lookup"><span data-stu-id="19e04-136">TZRULE</span></span>](tzrule.md)
    
<span data-ttu-id="19e04-137">予定表の再バーズ API を使用して予定の再処理ツールを作成するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="19e04-137">To write an appointment rebasing tool by using the calendar rebasing APIs, you can use the following procedure:</span></span>
  
1. <span data-ttu-id="19e04-138">**IOlkApptRebaser::BeginEnumerateAppointments** および **IOlkApptRebaser::EndEnumerateAppointments** を使用して、リベースの候補である予定を検索します。</span><span class="sxs-lookup"><span data-stu-id="19e04-138">Use **IOlkApptRebaser::BeginEnumerateAppointments** and **IOlkApptRebaser::EndEnumerateAppointments** to find appointments that are candidates for rebasing.</span></span> <span data-ttu-id="19e04-139">必要に応じて、ユーザーがリベースする予定を決定できる情報を提示します。</span><span class="sxs-lookup"><span data-stu-id="19e04-139">If necessary, present information to enable the user to decide which appointments to rebase.</span></span> <span data-ttu-id="19e04-140">または、MAPI または Outlook オブジェクト モデルを使用して **、PidLidAppointmentTimeZoneDefinitionStartDisplay、PidLidAppointmentTimeZoneDefinitionEndDisplay、\*\*\*\*および PidLidAppointmentTimeZoneDefinitionRecur** プロパティを解析して、予定の時間と繰り返し情報を調べてください。 </span><span class="sxs-lookup"><span data-stu-id="19e04-140">Alternatively, use MAPI or the Outlook Object Model to examine the time and recurrence information for an appointment by parsing the **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay**, and **PidLidAppointmentTimeZoneDefinitionRecur** properties.</span></span> 
    
2. <span data-ttu-id="19e04-141">予定を再ベース化するには **、HrCreateApptRebaser** **、IOlkApptRebaser::BeginRebaseAppointments、\*\*\*\*および IOlkApptRebaser::EndRebaseAppointments** を使用します。</span><span class="sxs-lookup"><span data-stu-id="19e04-141">Use **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments**, and **IOlkApptRebaser::EndRebaseAppointments** to rebase the appointment.</span></span> 
    
<span data-ttu-id="19e04-142">Tzmovelib.dll アセンブリを取得するには、Outlook [2010](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)の OutlookTimeZoneMoveLibRedist.exe 再頒布可能インストーラーと Tzmovelib.h ヘッダー ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="19e04-142">To obtain the Tzmovelib.dll assembly, download the OutlookTimeZoneMoveLibRedist.exe redistributable installer and the Tzmovelib.h header file at [Outlook 2010: Auxiliary Reference Redistributable Installer and Header File for Rebasing Calendars](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).</span></span> <span data-ttu-id="19e04-143">このダウンロードは、2010 Outlook以降のバージョンのバージョンでOutlook。</span><span class="sxs-lookup"><span data-stu-id="19e04-143">This download works for Outlook 2010 and later versions of Outlook.</span></span> <span data-ttu-id="19e04-144">OutlookTimeZoneMoveLibRedist.exe C:\Program Files\MsExTmz にTzmovelib.dllアセンブリ ファイルをインストールします。</span><span class="sxs-lookup"><span data-stu-id="19e04-144">OutlookTimeZoneMoveLibRedist.exe installs the Tzmovelib.dll assembly file in C:\Program Files\MsExTmz.</span></span> <span data-ttu-id="19e04-145">サード パーティ製の予定表の再分散アプリケーションでは、インストーラー 、OutlookTimeZoneMoveLibRedist.exe のみを再配布できます。また、アセンブリ、Tzmovelib.dll、または他の抽出されたコンポーネントをインストーラーとは別に再配布する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19e04-145">Note that third-party calendar rebasing applications can redistribute only the installer, OutlookTimeZoneMoveLibRedist.exe, and must not redistribute the assembly, Tzmovelib.dll, or any other extracted components separately from the installer.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19e04-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="19e04-146">See also</span></span>

- [<span data-ttu-id="19e04-147">バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて</span><span class="sxs-lookup"><span data-stu-id="19e04-147">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [<span data-ttu-id="19e04-148">バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る</span><span class="sxs-lookup"><span data-stu-id="19e04-148">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="19e04-149">バイナリ プロパティからのストリームを解析し、TZREG 構造体を読み取る</span><span class="sxs-lookup"><span data-stu-id="19e04-149">Parse a stream from a binary property to read the TZREG structure</span></span>](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [<span data-ttu-id="19e04-150">予定からタイム ゾーンのプロパティを読み取る</span><span class="sxs-lookup"><span data-stu-id="19e04-150">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)
- [<span data-ttu-id="19e04-151">夏時間のヘルプとサポート センター</span><span class="sxs-lookup"><span data-stu-id="19e04-151">Daylight Saving Time Help and Support Center</span></span>](https://support.microsoft.com/gp/cp_dst)
- [<span data-ttu-id="19e04-152">カレンダー更新ツールを使用して夏時間に対処Exchange方法</span><span class="sxs-lookup"><span data-stu-id="19e04-152">How to address daylight saving time by using the Exchange Calendar Update Tool</span></span>](https://support.microsoft.com/kb/941018)
- [<span data-ttu-id="19e04-153">タイム ゾーン データ更新ツールを使用してタイム ゾーンの変更に対処するMicrosoft Office Outlook</span><span class="sxs-lookup"><span data-stu-id="19e04-153">How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook</span></span>](https://support.microsoft.com/kb/931667)

