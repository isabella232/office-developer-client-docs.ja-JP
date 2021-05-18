---
title: 外部補助Outlookへようこそ
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: Outlook補助リファレンスには、4 組の API、コード サンプル、および再頒布可能なインストーラーの概念的なコンテンツとリファレンス ドキュメントが含まれています。開発者は Outlook と拡張して統合できます。 この参照の API は、Outlookモデルの外部で、機能拡張Outlook公開されます。
ms.openlocfilehash: 445d35c12e4c8984d47adcef3ecf50ebd881875b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328984"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a><span data-ttu-id="4737d-104">外部補助Outlookへようこそ</span><span class="sxs-lookup"><span data-stu-id="4737d-104">Welcome to the Outlook Auxiliary Reference</span></span>

<span data-ttu-id="4737d-105">Outlook補助リファレンスには、4 組の API、コード サンプル、および再頒布可能なインストーラーの概念的なコンテンツとリファレンス ドキュメントが含まれています。開発者は Outlook と拡張して統合できます。</span><span class="sxs-lookup"><span data-stu-id="4737d-105">The Outlook Auxiliary Reference contains conceptual content and reference documentation for four sets of APIs, code samples, and a redistributable installer that allow developers to extend and integrate with Outlook.</span></span> <span data-ttu-id="4737d-106">この参照の API は、Outlookモデルの外部で、機能拡張Outlook公開されます。</span><span class="sxs-lookup"><span data-stu-id="4737d-106">APIs in this reference are exposed by Outlook for extensibility, outside of the Outlook object model.</span></span> 
  
<span data-ttu-id="4737d-107">Outlook のソリューションを開発するのが初めての場合は、「[Outlook 用のソリューションを開発するための API またはテクノロジの選択](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md)」を参照し、必要に応じて適切な API とテクノロジを特定します。</span><span class="sxs-lookup"><span data-stu-id="4737d-107">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="4737d-108">オブジェクト モデルの詳細についてはOutlook VBA リファレンスOutlook[参照してください](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4737d-108">For specific information about the Outlook object model, see the [Outlook VBA reference](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx).</span></span> 

<span data-ttu-id="4737d-109">ユーザーがサポートするメッセージング API (MAPI) の詳細についてはOutlook MAPI リファレンスOutlook[参照してください](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4737d-109">For specific information about Messaging API (MAPI) supported by Outlook, see the [Outlook MAPI Reference](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx).</span></span>

## <a name="conceptual"></a><span data-ttu-id="4737d-110">概念</span><span class="sxs-lookup"><span data-stu-id="4737d-110">Conceptual</span></span> 

<span data-ttu-id="4737d-111">概念的な議論には、次のテーマが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4737d-111">The conceptual discussion includes the following subjects:</span></span>
  
- [<span data-ttu-id="4737d-112">スパム対策の設定について</span><span class="sxs-lookup"><span data-stu-id="4737d-112">About anti-spam settings</span></span>](about-anti-spam-settings.md)
    
- [<span data-ttu-id="4737d-113">POP3 アカウントのメッセージ ダウンロードの管理</span><span class="sxs-lookup"><span data-stu-id="4737d-113">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)
    
- [<span data-ttu-id="4737d-114">POP3 アカウントのメッセージのダウンロードの履歴を検索します。</span><span class="sxs-lookup"><span data-stu-id="4737d-114">Locating the message download history for a POP3 account</span></span>](locating-the-message-download-history-for-a-pop3-account.md)
    
- [<span data-ttu-id="4737d-115">POP3 アカウントのメッセージのダウンロードの履歴の解析</span><span class="sxs-lookup"><span data-stu-id="4737d-115">Parsing the message download history for a POP3 account</span></span>](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [<span data-ttu-id="4737d-116">ユーザー設定アイテム タイプの競合解決について</span><span class="sxs-lookup"><span data-stu-id="4737d-116">About conflict resolution for custom item types</span></span>](about-conflict-resolution-for-custom-item-types.md)
    
- [<span data-ttu-id="4737d-117">オフライン アドレス帳の最終更新時刻について</span><span class="sxs-lookup"><span data-stu-id="4737d-117">About the last update time of an Offline Address Book</span></span>](about-the-last-update-time-of-an-offline-address-book.md)
    
- [<span data-ttu-id="4737d-118">自動構成のための新しいドメインの登録について</span><span class="sxs-lookup"><span data-stu-id="4737d-118">About registering a new domain for automatic configuration</span></span>](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [<span data-ttu-id="4737d-119">情報更新および完全な更新としての会議出席依頼について</span><span class="sxs-lookup"><span data-stu-id="4737d-119">About meeting requests as informational updates and full updates</span></span>](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- <span data-ttu-id="4737d-120">[夏時間](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)に合わせてカレンダーをプログラムで再調整する方法について (Outlook 2010 以降、以前のバージョンの Outlook でも動作するサードパーティの予定表の再分散ツール用の再配布可能なインストーラーもあります。</span><span class="sxs-lookup"><span data-stu-id="4737d-120">[About rebasing calendars programmatically for Daylight Saving Time](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) (There is also a redistributable installer for third-party calendar rebasing tools, which works for previous versions of Outlook as well, since Outlook 2010.</span></span> <span data-ttu-id="4737d-121">インストーラーをダウンロードするには[、「Outlook 2010:](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)補助参照再頒布可能インストーラーと予定表の再分散用ヘッダー ファイル」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4737d-121">To download the installer, see [Outlook 2010: Auxiliary Reference Redistributable Installer and Header File for Rebasing Calendars](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).)</span></span>
    
- [<span data-ttu-id="4737d-122">バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて</span><span class="sxs-lookup"><span data-stu-id="4737d-122">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a><span data-ttu-id="4737d-123">参照</span><span class="sxs-lookup"><span data-stu-id="4737d-123">Reference</span></span>

<span data-ttu-id="4737d-124">参照コンテンツには、次の内容が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4737d-124">The reference content includes the following:</span></span>
  
- <span data-ttu-id="4737d-125">この[API は、Outlook](about-apis-exported-by-outlook.md)に実装され、パブリックに使用するために公開されている関数とデータ構造を含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="4737d-125">The [APIs Exported by Outlook](about-apis-exported-by-outlook.md) include functions and data structures that were originally implemented for internal use and are now exposed for public use.</span></span> 
    
- <span data-ttu-id="4737d-126">アカウント [管理 API は、](about-the-account-management-api.md) ユーザー アカウント情報へのアクセスとアカウント変更の通知を提供します。</span><span class="sxs-lookup"><span data-stu-id="4737d-126">The [Account Management API](about-the-account-management-api.md) provides access to user account information and notifications of account changes.</span></span> 
    
- <span data-ttu-id="4737d-127">データ[低下層 API](about-the-data-degradation-layer-api.md)は、オブジェクトのネイティブ文字形式Outlook優先文字形式でアイテムにアクセスするクライアントをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4737d-127">The [Data Degradation Layer API](about-the-data-degradation-layer-api.md) supports clients that access an Outlook item in a preferred character format rather than the object's native character format.</span></span> 
    
- <span data-ttu-id="4737d-128">空 [き時間情報 API は](about-the-free-busy-api.md) 、特定の時間範囲内の特定のユーザー アカウントに関する空き時間情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="4737d-128">The [Free/Busy API](about-the-free-busy-api.md) provides free/busy status information about specific user accounts within a specific time range.</span></span> 

## <a name="sample-tasks"></a><span data-ttu-id="4737d-129">サンプル タスク</span><span class="sxs-lookup"><span data-stu-id="4737d-129">Sample tasks</span></span>

<span data-ttu-id="4737d-130">「補助リファレンス」のサンプルのOutlookを次に示します。</span><span class="sxs-lookup"><span data-stu-id="4737d-130">Sample how-to tasks in the Outlook Auxiliary Reference include the following:</span></span>
    
- [<span data-ttu-id="4737d-131">Outlook アイテムが変更されたが保存されていないかどうかを確認する (Outlook の補助リファレンス)</span><span class="sxs-lookup"><span data-stu-id="4737d-131">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [<span data-ttu-id="4737d-132">バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る</span><span class="sxs-lookup"><span data-stu-id="4737d-132">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [<span data-ttu-id="4737d-133">バイナリ プロパティからのストリームを解析し、TZREG 構造体を読み取る</span><span class="sxs-lookup"><span data-stu-id="4737d-133">Parse a stream from a binary property to read the TZREG structure</span></span>](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [<span data-ttu-id="4737d-134">予定からタイム ゾーンのプロパティを読み取る</span><span class="sxs-lookup"><span data-stu-id="4737d-134">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [<span data-ttu-id="4737d-135">Outlook (Outlook の補助リファレンス) で、連絡先の画像を表示するかどうかを指定</span><span class="sxs-lookup"><span data-stu-id="4737d-135">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [<span data-ttu-id="4737d-136">空き時間情報データにアクセスするのに相対時間を使用する</span><span class="sxs-lookup"><span data-stu-id="4737d-136">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
    
<span data-ttu-id="4737d-137">各 API の参照には、追加の機能を使用するために開発者が実装する必要がある定数、型定義、およびインターフェイスが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="4737d-137">The reference for each API lists the constants, type definitions, and interfaces that a developer must implement to use the additional functionality.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4737d-138">開発者は、この参照に記載されている API のみを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4737d-138">Developers must implement these APIs only as documented in this reference.</span></span> <span data-ttu-id="4737d-139">特定のインターフェイス メンバーとメソッド パラメーターは、Outlook の内部使用のために予約され、予告なしに変更される可能性があるため、プレースホルダーとして名前が付けされます。</span><span class="sxs-lookup"><span data-stu-id="4737d-139">Certain interface members and method parameters are named as placeholders because they are reserved for the internal use of Outlook and are subject to change without notice.</span></span> 
  

