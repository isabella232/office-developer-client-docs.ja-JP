---
title: IM アプリケーションと Office の統合
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: この記事では、プレゼンスの表示や連絡先カードからのインスタント メッセージの送信など、Office 2013 以降のソーシャル機能と統合するように、インスタント メッセージ (IM) クライアント アプリケーションを構成する方法について説明します。
localization_priority: Priority
ms.openlocfilehash: c0094b880bae5cac2cef4236d3ff3edcefd21678
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819295"
---
# <a name="integrating-im-applications-with-office"></a><span data-ttu-id="fec71-103">IM アプリケーションと Office の統合</span><span class="sxs-lookup"><span data-stu-id="fec71-103">Integrating IM applications with Office</span></span>

<span data-ttu-id="fec71-104">この記事では、プレゼンスの表示や連絡先カードからのインスタント メッセージの送信など、Office 2013、Office 2016、Office 2019、Office 365 のソーシャル機能と統合するように、インスタント メッセージ (IM) クライアント アプリケーションを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fec71-104">This article describes how to configure an instant message (IM) client application so that it integrates with the social features in Office 2013, including displaying presence and sending instant messages from the contact card.</span></span>
  
## <a name="introduction"></a><span data-ttu-id="fec71-105">概要</span><span class="sxs-lookup"><span data-stu-id="fec71-105">Introduction</span></span>
<span data-ttu-id="fec71-106"><a name="off15_IMIntegration_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-106"></span></span>

<span data-ttu-id="fec71-107">Office 2013 (およびそれ以降のバージョン) には、Lync 2013 や Teams を含む IM クライアント アプリケーションとの統合機能が備わっています。</span><span class="sxs-lookup"><span data-stu-id="fec71-107">Office 2013 provides rich integration with IM client applications, including Lync 2013.</span></span> <span data-ttu-id="fec71-108">この統合により、Word、Excel、PowerPoint、Outlook、Visio、Project、および OneNote の中から IM 機能を使用できるようになり、SharePoint ページでのプレゼンス統合も可能です。</span><span class="sxs-lookup"><span data-stu-id="fec71-108">This integration provides users with IM capabilities from within Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013, and OneNote 2013 as well as providing presence integration on SharePoint 2013 pages.</span></span> <span data-ttu-id="fec71-109">ユーザーは、連絡先リスト内でユーザーの写真、名前、プレゼンス状態、連絡先データを表示できます。</span><span class="sxs-lookup"><span data-stu-id="fec71-109">Users can see the photo, name, presence status, and contact data for people in their contacts list.</span></span> <span data-ttu-id="fec71-110">IM セッション、ビデオ通話、または電話による通話を連絡先カード (連絡情報と通信オプションが表示される Office の UI 要素) から直接開始することができます。</span><span class="sxs-lookup"><span data-stu-id="fec71-110">They can start an IM session, video call, or phone call directly from the contact card (the UI element in Office 2013 that surfaces contact information and communication options).</span></span> <span data-ttu-id="fec71-111">Office を使用すると、メールやドキュメントを使用しなくても、簡単に連絡先に接続できます。</span><span class="sxs-lookup"><span data-stu-id="fec71-111">Office 2013 makes it easy to stay connected to your contacts without taking you outside of your email or documents.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fec71-112">[!メモ] この記事では、コンピューターにインストールされた IM サービスと通信するアプリケーションを特に表すために、 IM クライアント アプリケーションという用語を使用します。</span><span class="sxs-lookup"><span data-stu-id="fec71-112">This article uses the term IM client application to refer specifically to the application installed on a user's computer that communicates to the IM service.</span></span> <span data-ttu-id="fec71-113">たとえば、Lync 2013 および Teams は、IM クライアント アプリケーションと見なされます。</span><span class="sxs-lookup"><span data-stu-id="fec71-113">For example, Lync 2013 and Teams are considered an IM client applications.</span></span> <span data-ttu-id="fec71-114">この記事では、IM クライアント アプリケーションが IM サービスと通信する方法や、IM サービス自体については詳しく説明しません。</span><span class="sxs-lookup"><span data-stu-id="fec71-114">This article does not provide details about how the IM client application communicates to the IM service or about the IM service itself.</span></span> 
  
<span data-ttu-id="fec71-p103">Office と通信できるように、IM のクライアント アプリケーションをカスタマイズすることができます。具体的には、Office UI 内に次の情報が表示されるように、IM のアプリケーションを変更できます。</span><span class="sxs-lookup"><span data-stu-id="fec71-p103">You can customize an IM client application so that it communicates with Office. Specifically, you can modify your IM application so that it displays the following information within the Office UI:</span></span>
  
- <span data-ttu-id="fec71-117">連絡先の写真。</span><span class="sxs-lookup"><span data-stu-id="fec71-117">Contact photo.</span></span>
    
- <span data-ttu-id="fec71-118">連絡先の名前。</span><span class="sxs-lookup"><span data-stu-id="fec71-118">Contact name.</span></span>
    
- <span data-ttu-id="fec71-119">連絡先の個人ステータスに関する注記。</span><span class="sxs-lookup"><span data-stu-id="fec71-119">Contact personal status note.</span></span>
    
- <span data-ttu-id="fec71-120">連絡先のプレゼンス ステータス。</span><span class="sxs-lookup"><span data-stu-id="fec71-120">Contact presence status.</span></span>
    
- <span data-ttu-id="fec71-121">連絡先の連絡可能性を示す文字列 (たとえば「連絡可能」や「退席中」など)。</span><span class="sxs-lookup"><span data-stu-id="fec71-121">Contact availability string (for example, "Available" or "Out of Office").</span></span>
    
- <span data-ttu-id="fec71-122">連絡先の機能を示す文字列 (たとえば、「ビデオ準備完了」など)。</span><span class="sxs-lookup"><span data-stu-id="fec71-122">Contact capability string (for example, "Video Ready").</span></span>
    
- <span data-ttu-id="fec71-123">IM のワンクリック起動。</span><span class="sxs-lookup"><span data-stu-id="fec71-123">One-click IM launch.</span></span>
    
- <span data-ttu-id="fec71-124">ビデオ通話のワンクリック起動。</span><span class="sxs-lookup"><span data-stu-id="fec71-124">One-click video call launch.</span></span>
    
- <span data-ttu-id="fec71-125">電話通話のワンクリック起動 (SIP、電話番号、ボイス メール、新規番号の呼び出しを含む)。</span><span class="sxs-lookup"><span data-stu-id="fec71-125">One-click phone call launch (including SIP, phone number, voice mail, and call new number).</span></span>
    
- <span data-ttu-id="fec71-126">連絡先の管理 (IM グループに追加)。</span><span class="sxs-lookup"><span data-stu-id="fec71-126">Contact management (add to IM group).</span></span>
    
- <span data-ttu-id="fec71-127">連絡先の場所とタイム ゾーン。</span><span class="sxs-lookup"><span data-stu-id="fec71-127">Contact location and time zone.</span></span>
    
- <span data-ttu-id="fec71-128">連絡先データ、電話番号、電子メール アドレス、役職、および会社名。</span><span class="sxs-lookup"><span data-stu-id="fec71-128">Contact data, phone number, email address, title, and company name.</span></span>
    
<span data-ttu-id="fec71-129">**図 1. Office 2013 での連絡先カード**</span><span class="sxs-lookup"><span data-stu-id="fec71-129">**Figure 1. Contact card in Office 2013**</span></span>

<span data-ttu-id="fec71-130">![Office 2013 の連絡先カード](media/ocom15_peoplecard.png "Office 2013 の連絡先カード")</span><span class="sxs-lookup"><span data-stu-id="fec71-130">![The People Card in Office 2013](media/ocom15_peoplecard.png "The People Card in Office 2013")</span></span>
  
<span data-ttu-id="fec71-p104">Office とのこの統合を有効にするために、IM のクライアント アプリケーションは、Office に接続するために提供されている一連のインターフェイスを実装する必要があります。この統合の API は、Lync / Skype for Business を含むバージョンの Office 2013 と共にインストールされる Microsoft.Office.UC.dll ファイル内にある [UCCollborationLib](https://docs.microsoft.com/previous-versions/office/communications/ff398475(v=ocs.14)) 名前空間に含まれています。 **UCCollaborationLib** 名前空間には、Office と統合するために実装する必要のあるインターフェイスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fec71-p104">To enable this integration with Office, an IM client application must implement a set of interfaces that Office provides to connect to it. The APIs for this integration are included in the [UCCollborationLib](https://docs.microsoft.com/previous-versions/office/communications/ff398475(v=ocs.14)) namespace that is contained in the Microsoft.Office.UC.dll file, which is installed with versions of Office 2013 that include Lync / Skype for Business. The **UCCollaborationLib** namespace includes the interfaces that you must implement to integrate with Office.</span></span> 
  
> [!IMPORTANT] 
> <span data-ttu-id="fec71-134">Lync 2013/Skype for Business には、必要なインターフェイスのタイプ ライブラリが埋め込まれています。</span><span class="sxs-lookup"><span data-stu-id="fec71-134">The type library for the required interfaces is embedded in Lync 2013/Skype for Business.</span></span> <span data-ttu-id="fec71-135">サード パーティ インテグレーターの場合、これは Lync 2013 と Skype for Business の両方が対象コンピューターにインストールされている場合にのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="fec71-135">For third-party integrators, this works only when both Lync 2013 and Skype for Business are installed on the target machine.</span></span> <span data-ttu-id="fec71-136">Office 標準を使用して統合している場合は、タイプ ライブラリを抽出して、対象コンピューターにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-136">If you are integrating using Office Standard, you need to extract the type library and install it on the target machine.</span></span> <span data-ttu-id="fec71-137">[Lync 2013 SDK](https://www.microsoft.com/download/details.aspx?id=36824) には、Microsoft.Office.UC.dll ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fec71-137">The [Lync 2013 SDK](https://www.microsoft.com/download/details.aspx?id=36824) includes the Microsoft.Office.UC.dll file.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="fec71-138">少数の Office 2010 アプリケーションは、同様に、次のサード パーティ IM プロバイダーのアプリケーションと統合できます: Outlook 2010、Word 2010、Excel 2010、PowerPoint 2010、および SharePoint Server 2010 (ActiveX コントロールを使用)。</span><span class="sxs-lookup"><span data-stu-id="fec71-138">A handful of Office 2010 applications can integrate similarly with a third-party IM provider application: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010, and SharePoint Server 2010 (using an ActiveX control).</span></span> <span data-ttu-id="fec71-139">Office 2013 との統合に必要な手順の多くは、Office 2010 にも同様に適用されます。</span><span class="sxs-lookup"><span data-stu-id="fec71-139">Many of the steps required for integration with Office 2013 apply to Office 2010 as well.</span></span> <span data-ttu-id="fec71-140">Office 2010 が IM プロバイダー アプリケーションと統合する方法には、いくつかの重要な相違があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-140">There are several key differences in how Office 2010 integrates with an IM provider application:</span></span> 
>  - <span data-ttu-id="fec71-141">Office 2010 には、連絡先の写真が表示されません。</span><span class="sxs-lookup"><span data-stu-id="fec71-141">Office 2010 does not display the contact's photo.</span></span> 
>  - <span data-ttu-id="fec71-142">Microsoft.Office.Uc.dll ファイルは、Office 2010 とは別にダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-142">You must download the Microsoft.Office.Uc.dll file separately from Office 2010.</span></span> <span data-ttu-id="fec71-143">[Lync 2010 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=18898) には、Office 2010 のための Microsoft.Office.UC.dll ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fec71-143">The [Lync 2010 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=18898) includes the Microsoft.Office.UC.dll file for Office 2010.</span></span> 
>  - <span data-ttu-id="fec71-144">Office アプリケーションが IM クライアント アプリケーションで [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) メソッドを呼び出すときには、文字列「14.0.0.0」が渡されます。</span><span class="sxs-lookup"><span data-stu-id="fec71-144">When the Office application calls the [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) method on the IM client application, it passes in the string "14.0.0.0".</span></span> 
>  - <span data-ttu-id="fec71-145">Office 2010 は、IM クライアント アプリケーションに接続した直後に、すべてのグループと連絡先を列挙します。</span><span class="sxs-lookup"><span data-stu-id="fec71-145">Office 2010 enumerates all groups and contacts as soon as it connects to an IM client application.</span></span> 
  
## <a name="how-office-integrates-with-an-im-client-application"></a><span data-ttu-id="fec71-146">IM クライアント アプリケーションとの Office の統合方法</span><span class="sxs-lookup"><span data-stu-id="fec71-146">How Office integrates with an IM client application</span></span>
<span data-ttu-id="fec71-147"><a name="off15_IMIntegration_How"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-147"></span></span>

<span data-ttu-id="fec71-148">Office 2013 (またはそれ以降) アプリケーションは、起動するときに、以下のプロセスによって既定の IM クライアント アプリケーションと統合します。</span><span class="sxs-lookup"><span data-stu-id="fec71-148">When an Office 2013 application starts, it goes through the following process to integrate with the default IM client application:</span></span>
  
1. <span data-ttu-id="fec71-149">レジストリをチェックして既定の IM クライアント アプリケーションを検出し、それに接続します。</span><span class="sxs-lookup"><span data-stu-id="fec71-149">It checks the registry to discover the default IM client application and then connects to it.</span></span>
    
2. <span data-ttu-id="fec71-150">IM クライアント アプリケーションでの認証を行います。</span><span class="sxs-lookup"><span data-stu-id="fec71-150">It authenticates with the IM client application.</span></span>
    
3. <span data-ttu-id="fec71-151">IM クライアント アプリケーションで公開されている特定のインターフェイスに接続します。</span><span class="sxs-lookup"><span data-stu-id="fec71-151">It connects to specific interfaces that are exposed by the IM client application.</span></span>
    
4. <span data-ttu-id="fec71-152">現在サインインしているユーザー (ローカル ユーザー) の能力を判別します。これには、ユーザーの連絡先の取得、ユーザーのプレゼンスの判別、ユーザーの IM の能力 (インスタント メッセージング、ビデオ チャット、VOIP、その他) の判別などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fec71-152">It determines the capabilities of the currently signed-in user (local user), including getting the user's contacts, determining the user's presence, and determining the user's IM capabilities (instant messaging, video chat, VOIP, and so on).</span></span>
    
5. <span data-ttu-id="fec71-153">ローカル ユーザーの連絡先のプレゼンス情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-153">It gets presence information for the local user's contacts.</span></span>
    
6. <span data-ttu-id="fec71-154">IM クライアント アプリケーションが終了するとき、Office アプリケーションは警告なしに切断します。</span><span class="sxs-lookup"><span data-stu-id="fec71-154">When the IM client application shuts down, the Office 2013 application silently disconnects.</span></span>
    
### <a name="discovering-the-im-application"></a><span data-ttu-id="fec71-155">IM アプリケーションの検出</span><span class="sxs-lookup"><span data-stu-id="fec71-155">Discovering the IM application</span></span>

<span data-ttu-id="fec71-p108">Office アプリケーションは、レジストリ内でいくつかの特定のキーとエントリを検索して、既定の IM クライアント アプリケーションを検出します。既定の IM クライアント アプリケーションが見つかった場合、それに接続しようとします。</span><span class="sxs-lookup"><span data-stu-id="fec71-p108">The Office application looks for several specific keys and entries in the registry to discover the default IM client application. If it discovers a default IM client application, it then attempts to connect to it.</span></span>
  
<span data-ttu-id="fec71-158">Office アプリケーションが、既定の IM のクライアント アプリケーションを検出するためのプロセスは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fec71-158">The process that the Office application goes through to discover the default IM client application is as follows:</span></span>
  
1. <span data-ttu-id="fec71-159">Office アプリケーションは、レジストリで HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp サブキーが設定されているかを確認し、そこにリストされているアプリケーション名を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="fec71-159">The Office application looks to see if the HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp subkey in the registry is set and reads the application name listed there.</span></span>
    
2. <span data-ttu-id="fec71-160">その後、Office アプリケーションは HKEY_CURRENT_USER\Software\IM Providers\ _アプリケーション名_\UpAndRunning を読み取り、 その値の変更を監視します。</span><span class="sxs-lookup"><span data-stu-id="fec71-160">The Office application then reads the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key and monitors the value for changes.</span></span>
    
3. <span data-ttu-id="fec71-161">次に Office アプリケーションは HKEY_LOCAL_MACHINE\Software\IM Providers\ _アプリケーション名_ レジストリ キーを読み取り、そこに格納されている ProcessName およびクラス ID (CLSID) の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-161">The Office application next reads the HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ registry key and gets the ProcessName and class ID (CLSID) values stored there.</span></span> 
    
4. <span data-ttu-id="fec71-162">IM クライアント アプリケーションは、その開始シーケンスを正常に完了し、すべてのクラスをプレゼンス統合のために正しく登録した後に、HKEY_CURRENT_USER\Software\IM Providers\ _アプリケーション名_\UpAndRunning キーを「2」に設定して、クライアント アプリケーションが実行中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="fec71-162">Once the IM client application has completed its start sequence successfully and registered all of the classes correctly for the presence integration, it sets the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key to "2", indicating that the client application is running.</span></span>
    
5. <span data-ttu-id="fec71-163">Office アプリケーションは、HKEY_CURRENT_USER\Software\IM Providers\ _アプリケーション名_\UpAndRunning キーが「2」に設定されていることを検出すると、コンピューターで実行されるプロセスの一覧を調べて IM クライアント アプリケーションのプロセス名を見つけます。</span><span class="sxs-lookup"><span data-stu-id="fec71-163">When the Office application discovers that the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key has been set to "2", it checks the list of running processes on the computer for the process name of the IM client application.</span></span>
    
6. <span data-ttu-id="fec71-164">Office アプリケーションが IM クライアント アプリケーションの使用するプロセスを検出すると、Office アプリケーションは CLSID を使用して **CoCreateInstance** を呼び出し、プロセス外 COM サーバーとして IM クライアント アプリケーションへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="fec71-164">Once the Office application finds the process that the IM client application uses, the Office application calls **CoCreateInstance** using the CLSID to establish a connection to the IM client application as an out-of-process COM server.</span></span> 
    
### <a name="authenticating-the-connection-to-the-im-application"></a><span data-ttu-id="fec71-165">IM アプリケーションへの接続の認証</span><span class="sxs-lookup"><span data-stu-id="fec71-165">Authenticating the connection to the IM application</span></span>

<span data-ttu-id="fec71-166">Office アプリケーションは、IM クライアント アプリケーションへの接続を確立した後に、以下を行います。</span><span class="sxs-lookup"><span data-stu-id="fec71-166">After the Office application establishes a connection to the IM client application, it then does the following:</span></span>
  
1. <span data-ttu-id="fec71-167">Office アプリケーションは、[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) メソッドを呼び出して、 [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) インターフェースを検索します。</span><span class="sxs-lookup"><span data-stu-id="fec71-167">The Office application calls [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to check for the [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) interface.</span></span> 
    
2. <span data-ttu-id="fec71-168">その後、Office アプリケーションは **IUCOfficeIntegration.GetAuthenticationInfo** メソッドを呼び出して、サポートされる最高の統合バージョン (たとえば、「15.0.0.0」) を渡します。</span><span class="sxs-lookup"><span data-stu-id="fec71-168">The Office application then calls the **IUCOfficeIntegration.GetAuthenticationInfo** method, passing in the highest supported integration version (for example, "15.0.0.0").</span></span> 
    
3. <span data-ttu-id="fec71-169">パラメーターとして渡された Office のバージョンを IM クライアント アプリケーションがサポートしている場合、アプリケーションは、以下のハード コーディングされた XML 文字列を呼び出し元のコードに返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-169">If the IM client application supports the version of Office passed in as a parameter, the application returns the following hard-coded XML string to the calling code:</span></span>
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > <span data-ttu-id="fec71-170">従来のものにも対応できるように、IM クライアント アプリケーションは、パラメーターとして渡された Office のバージョンをサポートしている場合、正確な値の  `<authenticationinfo>` を **GetAuthenticationInfo** への呼び出しに戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-170">For legacy reasons, the IM client application must return the exact value  `<authenticationinfo>` to the call to **GetAuthenticationInfo** if it supports the version of Office passed in as a parameter.</span></span> 
  
4. <span data-ttu-id="fec71-171">IM クライアント アプリケーションが値を返すことに失敗した場合、Office アプリケーションは、サポートされる次に高位の Office のバージョン (たとえば、「14.0.0.0」) を指定して **GetAuthenticationInfo** メソッドを再び呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fec71-171">If the IM client application fails to return a value, the Office application calls the **GetAuthenticationInfo** method again with the next highest supported version of Office (for example, "14.0.0.0").</span></span> 
    
5. <span data-ttu-id="fec71-p109">Office は、IM クライアント アプリケーションが IM とプレゼンス統合をサポートすると判断した後、必要なセットのインターフェイスに接続して初期化を完了します。(詳細については、[必要なインターフェイスへの接続](#off15_IMIntegration_HowConnect)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec71-p109">Once Office determines that the IM client application supports IM and presence integration, it connects to a required set of interfaces to finish initializing. (For more information, see [Connecting to required interfaces](#off15_IMIntegration_HowConnect).)</span></span>
    
<span data-ttu-id="fec71-174">Office アプリケーションは、上記の手順のいずれかでエラーを検出するとバックアウトして、その Office アプリケーションのセッション中にはプレゼンス統合が再実行されません。</span><span class="sxs-lookup"><span data-stu-id="fec71-174">If the Office application encounters an error on any of the steps above, it backs out and presence integration is not established again during the session of the Office application.</span></span> 
  
### <a name="connecting-to-required-interfaces"></a><span data-ttu-id="fec71-175">必要なインターフェイスへの接続</span><span class="sxs-lookup"><span data-stu-id="fec71-175">Connecting to required interfaces</span></span>
<span data-ttu-id="fec71-176"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-176"></span></span>

<span data-ttu-id="fec71-p110">IM クライアント アプリケーションへの接続を認証した後、Office アプリケーションは、IM クライアント アプリケーションが公開する必要のある必要なインターフェイスのセットに接続しようとします。Office アプリケーションは、以下を行ってこれを実行します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p110">After authenticating the connection to the IM client application, the Office application attempts to connect to a set of required interfaces that the IM client application must expose. The Office application accomplishes this by doing the following:</span></span>
  
- <span data-ttu-id="fec71-179">Office アプリケーションは、 [IUCOfficeIntegration.GetInterface](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) メソッドを呼び出し、 **oiInterfaceLyncClient** 定数を **UCCollaborationLib.OIInterface** 列挙から渡して、 [ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-179">The Office application gets an [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceLyncClient** constant from the [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> 
    
- <span data-ttu-id="fec71-180">Office アプリケーションは、 [IUCOfficeIntegration.GetInterface](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) メソッドを呼び出し、 **oiInterfaceAutomation** 定数を **OIInterface** 列挙から渡して、 **IAutomation** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-180">The Office application gets an [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceAutomation** constant from the **OIInterface** enumeration.</span></span> 
    
- <span data-ttu-id="fec71-181">Office アプリケーションは、[_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) イベント リスナーをセットアップします。</span><span class="sxs-lookup"><span data-stu-id="fec71-181">The Office application sets up the [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) event listener.</span></span> 
    
- <span data-ttu-id="fec71-182">Office アプリケーションは、[_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) イベント リスナーをセットアップします。</span><span class="sxs-lookup"><span data-stu-id="fec71-182">The Office application sets up the [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) event listener.</span></span> 
    
- <span data-ttu-id="fec71-183">Office アプリケーションは、 **ILyncClient.State** プロパティにアクセスして、IM クライアント アプリケーションからサイン イン状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-183">The Office application gets the sign-in state from the IM client application by accessing the **ILyncClient.State** property.</span></span> 
    
- <span data-ttu-id="fec71-184">Office アプリケーションは、**UCCollaborationLib.OIFeature** 列挙からフラグを戻す [IUCOfficeIntegration.GetSupportedFeatures](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) メソッドを呼び出すことにより、IM クライアント アプリケーションの機能を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-184">The Office application gets the capabilities of the IM client application by calling the **IUCOfficeIntegration.GetSupportedFeatures** method, which returns a flag from the [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> 
    
- <span data-ttu-id="fec71-185">Office アプリケーションは、 **ILyncClient.Self** プロパティにアクセスして、 [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-185">The Office application accesses the **ILyncClient.Self** property to get a reference to an [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) object.</span></span> 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a><span data-ttu-id="fec71-186">ローカル ユーザーの能力を取得する</span><span class="sxs-lookup"><span data-stu-id="fec71-186">Retrieving the capabilities of the local user</span></span>
<span data-ttu-id="fec71-187"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-187"></span></span>

<span data-ttu-id="fec71-188">Office アプリケーションは、次の手順に従ってローカル ユーザーの能力を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-188">The Office application gets the capabilities of the local user by doing the following:</span></span>
  
1. <span data-ttu-id="fec71-189">IM クライアント アプリケーションが **IClient2** インターフェイスをサポートしている場合、Office は [IClient2.PrivateContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) プロパティにアクセスして、 **IContactManager** オブジェクトを取得しようとします。</span><span class="sxs-lookup"><span data-stu-id="fec71-189">If the IM client application supports the **IClient2** interface, Office tries to get an [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) object by accessing the **IClient2.PrivateContactManager** property.</span></span> 
    
2. <span data-ttu-id="fec71-p111">IM アプリケーションが **IClient2** インターフェイスをサポートしていない場合、Office アプリケーションは **ILyncClient.ContactManager** プロパティにアクセスして、 **IContactManager** オブジェクトを取得します。IM クライアント アプリケーションは、他のいずれかの IM 機能を確立する前に、 **IContactManager** オブジェクトを正常に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-p111">If the IM application does not support the **IClient2** interface, Office application gets an **IContactManager** object by accessing the **ILyncClient.ContactManager** property. The IM client application must successfully return an **IContactManager** object before any other IM capabilities can be established.</span></span> 
    
3. <span data-ttu-id="fec71-192">Office アプリケーションは、 **ILyncClient.Uri** プロパティにアクセスしてから、 **IContactManager.GetContactByUri** を呼び出して、ローカル ユーザーに関連付けられている [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-192">The Office application accesses the **ILyncClient.Uri** property and then calls **IContactManager.GetContactByUri** to get the [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) object associated with the local user.</span></span> 
    
4. <span data-ttu-id="fec71-193">その後、Office アプリケーションは複数の呼び出しを **IContact.CanStart** に対して実行してローカル ユーザーの能力を確立し、 **ModalityTypes.ucModalityInstantMessage** と **ModalityTypes.ucModalityAudioVideo** の値を順次渡します。</span><span class="sxs-lookup"><span data-stu-id="fec71-193">The Office application then makes several calls to **IContact.CanStart** to establish the capabilities of the local user, passing in the values for **ModalityTypes.ucModalityInstantMessage** and **ModalityTypes.ucModalityAudioVideo** successively.</span></span> 
    
### <a name="retrieving-contact-presence"></a><span data-ttu-id="fec71-194">連絡先プレゼンスの取得</span><span class="sxs-lookup"><span data-stu-id="fec71-194">Retrieving contact presence</span></span>
<span data-ttu-id="fec71-195"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-195"></span></span>

<span data-ttu-id="fec71-196">Office アプリケーションは、以下を行うことにより、ローカル ユーザーを含む連絡先プレゼンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-196">The Office application gets contact presence, including the local user, by doing the following:</span></span> 
  
1. <span data-ttu-id="fec71-197">Office アプリケーションは、 **IContact.GetContactInformation** を呼び出して、連絡先からプレゼンス アイテムを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-197">The Office application calls **IContact.GetContactInformation** to get a presence item from the contact.</span></span> 
    
2. <span data-ttu-id="fec71-p112">その後、Office アプリケーションは、連絡先からのプレゼンス ステータスの変化をサブスクライブします。これは **IContactManager.CreateSubscription** を呼び出して、 [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) オブジェクトを取得します、その後、 **IContactSubscription.AddContact** を呼び出して連絡先をサブスクリプションに追加してから、 **IContactSubscription.Subscribe** を呼び出して連絡先のステータスの変更を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p112">The Office application then subscribes to presence status changes from the contact. It calls **IContactManager.CreateSubscription** to get an [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) object. It then calls **IContactSubscription.AddContact** to add the contact to the subscription and then calls **IContactSubscription.Subscribe** to get changes in the contact's status.</span></span> 
    
3. <span data-ttu-id="fec71-201">IM アプリケーションが **IContact2** をサポートしている場合、Office は **IContact2.BatchGetContactInformation2** を呼び出してプレゼンス情報を取得しようとします。</span><span class="sxs-lookup"><span data-stu-id="fec71-201">If the IM application supports **IContact2**, Office attempts to get presence information by calling **IContact2.BatchGetContactInformation2**.</span></span>
    
4. <span data-ttu-id="fec71-p113">その後、Office アプリケーションは、 **IContact.BatchGetContactInformation** を呼び出して連絡先のプレゼンス プロパティを取得します。Office アプリケーションは、 **IContact.Settings** プロパティにアクセスして、プレゼンス プロパティの 2 つ目のセットを取得できます。</span><span class="sxs-lookup"><span data-stu-id="fec71-p113">The Office application then retrieves the presence properties for the contact by calling **IContact.BatchGetContactInformation**. The Office application can get a second set of presence properties by accessing the **IContact.Settings** property.</span></span> 
    
5. <span data-ttu-id="fec71-p114">最後に、Office アプリケーションは **IContact.CustomGroups** プロパティにアクセスして、連絡先のグループ メンバーシップを取得します。これにより、連絡先の属するすべての [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) オブジェクトを含む、 [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) コレクションが返されます。</span><span class="sxs-lookup"><span data-stu-id="fec71-p114">Finally, the Office application gets the contact's group membership by accessing the **IContact.CustomGroups** property. This returns an [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) collection that includes all of the [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) objects that the contact belongs to.</span></span> 
    
### <a name="disconnecting-from-the-im-application"></a><span data-ttu-id="fec71-206">IM アプリケーションから切断する</span><span class="sxs-lookup"><span data-stu-id="fec71-206">Disconnecting from the IM application</span></span>
<span data-ttu-id="fec71-207"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-207"></span></span>

<span data-ttu-id="fec71-208">Office アプリケーションが IM アプリケーションの **OnShuttingDown** イベントを検出すると、警告なしに切断します。</span><span class="sxs-lookup"><span data-stu-id="fec71-208">When the Office 2013 application detects the **OnShuttingDown** event from the IM application, it disconnects silently.</span></span> <span data-ttu-id="fec71-209">ただし、IM アプリケーションよりも前に Office アプリケーションがシャット ダウンする場合、Office アプリケーションは接続がクリーンアップされることを保証しません。</span><span class="sxs-lookup"><span data-stu-id="fec71-209">However, if the Office application shuts down before the IM application, the Office application does not guarantee that the connection is cleaned up.</span></span> <span data-ttu-id="fec71-210">IM アプリケーションは、クライアント接続リークを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-210">The IM application must handle client connection leaks.</span></span> 
  
## <a name="setting-registry-keys-and-entries"></a><span data-ttu-id="fec71-211">レジストリ キーとエントリを設定する</span><span class="sxs-lookup"><span data-stu-id="fec71-211">Setting registry keys and entries</span></span>
<span data-ttu-id="fec71-212"><a name="off15_IMIntegration_SetRegistry"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-212"></span></span>

<span data-ttu-id="fec71-213">前述のように、IM 対応の Office アプリケーションは、レジストリ内で特定のキー、エントリ、および値を検索して、接続する IM クライアント アプリケーションを検出します。</span><span class="sxs-lookup"><span data-stu-id="fec71-213">As mentioned previously, the IM-capable Office 2013 applications look for specific keys, entries, and values in the registry to discover the IM client application to connect to.</span></span> <span data-ttu-id="fec71-214">これらのレジストリ値は、Office アプリケーションに、IM クライアント アプリケーションのオブジェクト モデルへのエントリ ポイントとして機能するクラスのプロセス名と CLSID を提供します (つまり、 **IUCOfficeIntegration** インターフェイスを実装するクラス)。</span><span class="sxs-lookup"><span data-stu-id="fec71-214">These registry values provide the Office application with the process name and CLSID of the class that acts as the entry point to the IM client application's object model (that is, the class that implements the **IUCOfficeIntegration** interface).</span></span> <span data-ttu-id="fec71-215">Office アプリケーションは、そのクラスを共同作成して、IM クライアント アプリケーションのプロセス外 COM サーバーに対するクライアントとして接続します。</span><span class="sxs-lookup"><span data-stu-id="fec71-215">The Office application co-creates that class and connects as a client to the out-of-process COM server in the IM client application.</span></span> 
  
<span data-ttu-id="fec71-216">表 1 を使用して、IM クライアント アプリケーションを Office と統合するためにレジストリに書き込む必要のあるキー、エントリ、および値を識別します。</span><span class="sxs-lookup"><span data-stu-id="fec71-216">Use Table 1 to identify the keys, entries, and values that must be written in the registry to integrate an IM client application with Office.</span></span>
  
<span data-ttu-id="fec71-217">**表 1. 既定の IM クライアント アプリケーションを設定するレジストリ キー**</span><span class="sxs-lookup"><span data-stu-id="fec71-217">**Table 1. Registry keys for setting the default IM client application**</span></span>

|<span data-ttu-id="fec71-218">**キー**</span><span class="sxs-lookup"><span data-stu-id="fec71-218">**Key**</span></span>|<span data-ttu-id="fec71-219">**エントリ**</span><span class="sxs-lookup"><span data-stu-id="fec71-219">**Entry**</span></span>|<span data-ttu-id="fec71-220">**型**</span><span class="sxs-lookup"><span data-stu-id="fec71-220">**Type**</span></span>|<span data-ttu-id="fec71-221">**値**</span><span class="sxs-lookup"><span data-stu-id="fec71-221">**Value**</span></span>|<span data-ttu-id="fec71-222">**例**</span><span class="sxs-lookup"><span data-stu-id="fec71-222">**Example**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fec71-223">HKEY_LOCAL_MACHINE\Software\IM Providers\\<アプリケーション名\></span><span class="sxs-lookup"><span data-stu-id="fec71-223">HKEY_LOCAL_MACHINE\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="fec71-224">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fec71-224">FriendlyName</span></span>  <br/> |<span data-ttu-id="fec71-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="fec71-225">REG_SZ</span></span>  <br/> |<span data-ttu-id="fec71-226">サード パーティ製の IM クライアント アプリケーションの名前。</span><span class="sxs-lookup"><span data-stu-id="fec71-226">The name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="fec71-227">Litware IM 2012</span><span class="sxs-lookup"><span data-stu-id="fec71-227">Litware IM 2012</span></span>  <br/> |
||<span data-ttu-id="fec71-228">ProcessName</span><span class="sxs-lookup"><span data-stu-id="fec71-228">ProcessName</span></span>  <br/> |<span data-ttu-id="fec71-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="fec71-229">REG_SZ</span></span>  <br/> |<span data-ttu-id="fec71-230">サード パーティ製の IM クライアント アプリケーションのプロセス名。</span><span class="sxs-lookup"><span data-stu-id="fec71-230">The process name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="fec71-231">litware.exe</span><span class="sxs-lookup"><span data-stu-id="fec71-231">litware.exe</span></span>  <br/> |
||<span data-ttu-id="fec71-232">GUID</span><span class="sxs-lookup"><span data-stu-id="fec71-232">GUID</span></span>  <br/> |<span data-ttu-id="fec71-233">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="fec71-233">REG_SZ</span></span>  <br/> |<span data-ttu-id="fec71-234">ルートのクラス ID (CLSID)、 IM アプリケーションでの共同作成可能なクラス ( **IUCOfficeIntegration** インターフェイスを実装するクラス)。</span><span class="sxs-lookup"><span data-stu-id="fec71-234">A class ID (CLSID) for the root, cocreatable class in the IM application (the class that implements the **IUCOfficeIntegration** interface).</span></span>  <br/> |<span data-ttu-id="fec71-235">(A GUID)</span><span class="sxs-lookup"><span data-stu-id="fec71-235">(A GUID)</span></span>  <br/> |
|<span data-ttu-id="fec71-236">HKEY_CURRENT_USER\Software\IM Providers</span><span class="sxs-lookup"><span data-stu-id="fec71-236">HKEY_CURRENT_USER\Software\IM Providers</span></span>  <br/> |<span data-ttu-id="fec71-237">DefaultIMApp</span><span class="sxs-lookup"><span data-stu-id="fec71-237">DefaultIMApp</span></span>  <br/> |<span data-ttu-id="fec71-238">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="fec71-238">REG_SZ</span></span>  <br/> |<span data-ttu-id="fec71-p117">IM クライアント アプリケーションの名前。これは、HKEY_LOCAL_MACHINE の最上位レベルのレジストリ キー (ハイブ) と同じ名前でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="fec71-p117">The name of the IM client application. This must be the same as the name at the top-level registry key (hive) in the HKEY_LOCAL_MACHINE.</span></span>  <br/> |<span data-ttu-id="fec71-241">Litware</span><span class="sxs-lookup"><span data-stu-id="fec71-241">Litware</span></span>  <br/> |
|<span data-ttu-id="fec71-242">HKEY_CURRENT_USER\Software\IM Providers\\<アプリケーション名\></span><span class="sxs-lookup"><span data-stu-id="fec71-242">HKEY_CURRENT_USER\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="fec71-243">UpAndRunning</span><span class="sxs-lookup"><span data-stu-id="fec71-243">UpAndRunning</span></span>  <br/> |<span data-ttu-id="fec71-244">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="fec71-244">REG_DWORD</span></span>  <br/> | <span data-ttu-id="fec71-245">0 ～ 2 の整数値。</span><span class="sxs-lookup"><span data-stu-id="fec71-245">An integer value between 0 and 2:</span></span>  <br/>  <span data-ttu-id="fec71-246">0—実行していない</span><span class="sxs-lookup"><span data-stu-id="fec71-246">0—Not running</span></span>  <br/>  <span data-ttu-id="fec71-247">1—開始中</span><span class="sxs-lookup"><span data-stu-id="fec71-247">1—Starting</span></span>  <br/>  <span data-ttu-id="fec71-248">2—実行中</span><span class="sxs-lookup"><span data-stu-id="fec71-248">2—Running</span></span>  <br/> <br/><span data-ttu-id="fec71-249">**メモ**: アプリケーション名のレジストリ キーは、DefaultIMApp エントリの値と同一の必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-249">**NOTE**:  The application name registry key must be the same as the value of the DefaultIMApp entry.</span></span>           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a><span data-ttu-id="fec71-250">Office との統合のために必要なインターフェイスを実装する</span><span class="sxs-lookup"><span data-stu-id="fec71-250">Implementing the required interfaces for integration with Office</span></span>
<span data-ttu-id="fec71-251"><a name="off15_IMIntegration_ImplementRequired"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-251"></span></span>

<span data-ttu-id="fec71-p118">**UCCollaborationLib** 名前空間には、Office と統合するために IM クライアント アプリケーションの実行可能ファイル (または COM サーバー) が実装する必要のある 3 つのインターフェイスがあります。これらのインターフェイスが実装されていない場合、Office アプリケーションは初期化プロセス中にバックアウトして、IM クライアント アプリケーションとの接続が確立されていません。</span><span class="sxs-lookup"><span data-stu-id="fec71-p118">There are three interfaces from the **UCCollaborationLib** namespace that the executable (or COM server) of an IM client application must implement so that it can integrate with Office. If these interfaces are not implemented, the Office application backs out during the initialization process and the connection with the IM client application is not established.</span></span> 
  
<span data-ttu-id="fec71-254">必要なインターフェイスは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fec71-254">The required interfaces are as follows:</span></span>
  
- <span data-ttu-id="fec71-255">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)必須ではありませんが、 **_IUCOfficeIntegrationEvents** インターフェイスも同じ派生クラス内に実装される必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-255">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)—Although not required, the **_IUCOfficeIntegrationEvents** interface should also be implemented in the same derived class.</span></span> 
    
- <span data-ttu-id="fec71-256">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)必須ではありませんが、 **_ILyncClientEvents** インターフェイスも同じ派生クラス内に実装される必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-256">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)—Although not required, the **_ILyncClientEvents** interface should also be implemented in the same derived class.</span></span> 
    
- [<span data-ttu-id="fec71-257">IAutomation</span><span class="sxs-lookup"><span data-stu-id="fec71-257">IAutomation</span></span>](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a><span data-ttu-id="fec71-258">IUCOfficeIntegration インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fec71-258">IUCOfficeIntegration interface</span></span>
<span data-ttu-id="fec71-259"><a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-259"></span></span>

<span data-ttu-id="fec71-p119">**IUCOfficeIntegration** インターフェイスは、Office アプリケーションが IM クライアント アプリケーションと接続するためのエントリ ポイントを提供します。このインターフェイスは、IM クライアント アプリケーションとの接続を開始するプロセスの一部として Office アプリケーションが呼び出す 3 つのメソッドを定義します。 **IUCOfficeIntegration** インターフェイスを実装するクラスは、Office がそのインスタンスを共同作成できるように、共同作成可能でなければなりません。さらに、HKEY_LOCAL_MACHINE\Software\IM Providers\  _アプリケーション名_ レジストリ キーで、GUID エントリの値として入力された CLSID を公開する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="fec71-p119">The **IUCOfficeIntegration** interface provides the entry-point for an Office application to connect to the IM client application. The interface defines three methods that an Office application calls as part of the process of initiating a connection with the IM client application. The class that implements the **IUCOfficeIntegration** interface must be co-creatable so that Office can co-create an instance of it. In addition, it must expose the CLSID that is entered as the value for the GUID entry in the HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_ registry key.</span></span> 
  
<span data-ttu-id="fec71-p120">**IUCOfficeIntegration** から継承するクラスも **_IUCOfficeIntegrationEvents** インターフェイスを実装する必要があります。 **_IUCOfficeIntegrationEvents** インターフェイスには、 **IUCOfficeIntegration** インターフェイスのイベント ハンドラーを公開するメンバーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fec71-p120">The class that inherits from **IUCOfficeIntegration** should also implement the **_IUCOfficeIntegrationEvents** interface. The **_IUCOfficeIntegrationEvents** interface contains the members that expose the event handlers of the **IUCOfficeIntegration** interface.</span></span> 
  
<span data-ttu-id="fec71-266">表 2 は、 **IUCOfficeIntegration** と **_IUCOfficeIntegration** から継承するクラスに実装されている必要のあるメンバーを示しています。</span><span class="sxs-lookup"><span data-stu-id="fec71-266">Table 2 shows the members that must be implemented in the class that inherits from **IUCOfficeIntegration** and **_IUCOfficeIntegration**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fec71-267">**IUCOfficeIntegration** と **_IUCOfficeIntegrationEvents** インターフェイス、およびそのメンバーについて詳しくは、 [UCCollaborationLib.IUCOfficeIntegration](https://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) と [UCCollaborationLib._IUCOfficeIntegrationEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec71-267">For more information about the **IUCOfficeIntegration** and **_IUCOfficeIntegrationEvents** interfaces and their members, see [UCCollaborationLib.IUCOfficeIntegration](https://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) and [UCCollaborationLib._IUCOfficeIntegrationEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span></span> 
  
<span data-ttu-id="fec71-268">**表 2. IUCOfficeIntegration と _IUCOfficeIntegrationEvents インターフェイスの実装**</span><span class="sxs-lookup"><span data-stu-id="fec71-268">**Table 2. Implementation of the IUCOfficeIntegration and _IUCOfficeIntegrationEvents interfaces**</span></span>

|<span data-ttu-id="fec71-269">**インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="fec71-269">**Interface**</span></span>|<span data-ttu-id="fec71-270">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="fec71-270">**Member**</span></span>|<span data-ttu-id="fec71-271">**説明**</span><span class="sxs-lookup"><span data-stu-id="fec71-271">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fec71-272">**IUCOfficeIntegration**</span><span class="sxs-lookup"><span data-stu-id="fec71-272">**IUCOfficeIntegration**</span></span> <br/> |<span data-ttu-id="fec71-273">**GetAuthenticationInfo** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-273">**GetAuthenticationInfo** method</span></span>  <br/> |<span data-ttu-id="fec71-274">認証情報の文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-274">Gets the authentication info string.</span></span>  <br/> |
||<span data-ttu-id="fec71-275">**GetInterface** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-275">**GetInterface** method</span></span>  <br/> |<span data-ttu-id="fec71-276">特定のバージョンのインターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-276">Gets the interface of a particular version.</span></span>  <br/> |
||<span data-ttu-id="fec71-277">**GetSupportedFeatures** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-277">**GetSupportedFeatures** method</span></span>  <br/> |<span data-ttu-id="fec71-278">サポートされている Office の統合機能を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-278">Gets the supported Office integration features.</span></span>  <br/> |
|<span data-ttu-id="fec71-279">**_IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="fec71-279">**_IUCOfficeIntegrationEvents**</span></span> <br/> |<span data-ttu-id="fec71-280">**OnShuttingDown** イベント</span><span class="sxs-lookup"><span data-stu-id="fec71-280">**OnShuttingDown** event</span></span>  <br/> |<span data-ttu-id="fec71-281">IM クライアント アプリケーションがシャットダウンしようとするときに発生するイベント。</span><span class="sxs-lookup"><span data-stu-id="fec71-281">The event raised when the IM client application is trying to shut down.</span></span>  <br/> |
   
<span data-ttu-id="fec71-282">次のコードを使用して、IM クライアント アプリケーション内の **IUCOfficeIntegration** と **_IUCOfficeIntegration** インターフェイスから継承するクラスを定義します。</span><span class="sxs-lookup"><span data-stu-id="fec71-282">Use the following code to define a class that inherits from the **IUCOfficeIntegration** and **_IUCOfficeIntegration** interfaces within an IM client application.</span></span> 
  
```cs
// An example of a class that can be co-created and can integrate
// with Office as an IM provider.
[ClassInterface(ClassInterfaceType.None)]
[ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
[Guid("{CLSID value}"), ComVisible(true)]
public class LitwareClientAppObject : IUCOfficeIntegration
{
    // Implementation details omitted.
}

```

<span data-ttu-id="fec71-283">**GetAuthenticationInfo** メソッドは、文字列を  _version_ パラメーターの引数として取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-283">The **GetAuthenticationInfo** method takes a string as an argument for the  _version_ parameter.</span></span> <span data-ttu-id="fec71-284">Office アプリケーションは、このメソッドを呼び出すと、Office のバージョンに応じて引数の 2 つの文字列のいずれかで渡します。</span><span class="sxs-lookup"><span data-stu-id="fec71-284">When the Office application calls this method, it passes in one of two strings for the argument, depending on the version of Office.</span></span> <span data-ttu-id="fec71-285">Office アプリケーションがメソッドに IM クライアント アプリケーションでサポートされる (つまり機能がサポートされる) Office のバージョンを提供すると、**GetAuthenticationInfo** メソッドは、ハード コーディングされた XML 文字列 「`<authenticationinfo>`」を返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-285">When the Office application supplies the method with the version of Office that the IM client application supports (that is, supports the functionality), the **GetAuthenticationInfo** method returns a hard-coded XML string `<authenticationinfo>`.</span></span> 
  
<span data-ttu-id="fec71-286">次のコードを使用して、IM クライアント アプリケーションのコード内で **GetAuthentication** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fec71-286">Use the following code to implement the **GetAuthentication** method within the IM client application code.</span></span> 
  
```cs
public string GetAuthenticationInfo(string _version)
{
    // Define the version of Office that the IM client application supports.
    string supportedOfficeVersion = "15.0.0.0";
    // Do a simple check for equivalency.
    if (supportedOfficeVersion == _version)
    {
        // If the version of Office is supported, this method must 
        // return the string literal "<authenticationinfo>" exactly.
        return "<authenticationinfo>";
    }
    else
    {
        return null;
    }
}

```

<span data-ttu-id="fec71-p122">**GetInterface** メソッドは、  _interface_ パラメーターの引数として渡された内容に応じて、クラスへの参照を呼び出し元コードにシャトルします。Office アプリケーションは、 **GetInterface** メソッドを呼び出すと、インターフェイス パラメーター用に 2 つの値のいずれか、つまり **UCCollaborationLib.OIInterface** 列挙の **oiInterfaceILyncClient** 定数 (1) または [oiInterfaceIAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) 定数 (2) を渡します。Office アプリケーションが **oiInterfaceILyncClient** 定数を渡すと、 **GetInterface** メソッドは **ILyncClient** インターフェースを実装するクラスへの参照を返します。Office アプリケーションが **oiInterfaceIAutomation** 定数を渡すと、 **GetInterface** メソッドは **IAutomation** インターフェースを実装するクラスを返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p122">The **GetInterface** method shuttles references to classes to the calling code, depending on what is passed in as an argument for the  _interface_ parameter. When an Office application calls the **GetInterface** method, it passes in one of two values for the interface parameter: either the **oiInterfaceILyncClient** constant (1) or the **oiInterfaceIAutomation** constant (2) of the [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration. If the Office application passes in the **oiInterfaceILyncClient** constant, the **GetInterface** method returns a reference to a class that implements the **ILyncClient** interface. If the Office application passes in the **oiInterfaceIAutomation** constant, the **GetInterface** method returns a class that implements the **IAutomation** interface.</span></span> 
  
<span data-ttu-id="fec71-291">次のコード例を使用して、IM クライアント アプリケーションのコード内で **GetInterface** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fec71-291">Use the following code example to implement the **GetInterface** method within the IM client application code.</span></span> 
  
```cs
public object GetInterface(string _version, OIInterface _interface)
{
    // These objects implement the ILyncClient or IAutomation 
    // interfaces respectively. There is no restriction on what these
    // classes are named.
    IMClient imClient = new IMClient();
    IMClientAutomation imAutomation = new IMClientAutomation();
    // Return different object references depending on the value passed in
    // for the _interface parameter.
    switch (_interface)
    {
        // The calling code is asking for an object that inherits
        // from ILyncClient, so it returns such an object.
        case OIInterface.oiInterfaceILyncClient:
        {
            return imClient;
        }
        // The calling code is asking for an object that inherits
        // from IAutomation, so it returns such an object.
        case OIInterface.oiInterfaceIAutomation:
        {
            return imAutomation;
        }
        default:
        {
            throw new NotImplementedException();
        }
    }
}

```

<span data-ttu-id="fec71-292">**GetSupportedFeatures**メソッドは、IM クライアント アプリケーションによってサポートされる IM 機能に関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-292">The **GetSupportedFeatures** method returns information about the IM features that the IM client application supports.</span></span> <span data-ttu-id="fec71-293">その唯一のパラメーター  _version_ は、文字列を取ります。</span><span class="sxs-lookup"><span data-stu-id="fec71-293">It takes a string for its only parameter,  _version_.</span></span> <span data-ttu-id="fec71-294">Office アプリケーションが **GetSupportedFeatures** メソッドを呼び出すと、メソッドは [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) 列挙からの値を返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-294">When the Office application calls the **GetSupportFeatures** method, the method returns a value from the [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> <span data-ttu-id="fec71-295">返される値は IM のクライアントの機能を示し、値にフラグを追加することによって、IM クライアント アプリケーションの各機能が Office アプリケーションに対して指定されます。</span><span class="sxs-lookup"><span data-stu-id="fec71-295">The returned value specifies the capabilities of the IM client, where each capability of the IM client application is indicated to the Office application by adding a flag to the value.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="fec71-296">Office 2013 (およびそれ以降) アプリケーションは、**OIFeature** 列挙の以下の定数を無視します。</span><span class="sxs-lookup"><span data-stu-id="fec71-296">Office 2013 applications ignore the following constants in the **OIFeature** enumeration:</span></span> 
> - <span data-ttu-id="fec71-297">**oiFeaturePictures** (2)</span><span class="sxs-lookup"><span data-stu-id="fec71-297">**oiFeaturePictures** (2)</span></span> 
> - <span data-ttu-id="fec71-298">**oiFeatureFreeBusyIntegration**</span><span class="sxs-lookup"><span data-stu-id="fec71-298">**oiFeatureFreeBusyIntegration**</span></span>
> - <span data-ttu-id="fec71-299">**oiFeaturePhoneNormalization**</span><span class="sxs-lookup"><span data-stu-id="fec71-299">**oiFeaturePhoneNormalization**</span></span>
  
<span data-ttu-id="fec71-300">次のコード例を使用して、IM クライアント アプリケーションのコード内で **GetSupportFeatures** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fec71-300">Use the following code example to implement the **GetSupportFeatures** method within the IM client application code.</span></span> 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a><span data-ttu-id="fec71-301">ILyncClient インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fec71-301">ILyncClient interface</span></span>
<span data-ttu-id="fec71-302"><a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-302"></span></span>

<span data-ttu-id="fec71-p124">**ILyncClient** インターフェイスは、IM クライアント アプリケーション自体の機能に対応しています。これは、アプリケーションにサインインしたユーザー ( [UCCollaborationLib.ISelf ](https://msdn.microsoft.com/library/UCCollaborationLib.ISelf)インターフェイスによって表されるローカル ユーザー)、アプリケーションの状態、ローカル ユーザーの連絡先の一覧、および他のいくつかの設定を参照するプロパティを公開します。IM のクライアント アプリケーションに接続しようとするとき、Office アプリケーションは **ILyncClient** インターフェイスを実装するオブジェクトへの参照を取得します。その参照から、Office は IM クライアント アプリケーションの機能の多くにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="fec71-p124">The **ILyncClient** interface maps to the capabilities of the IM client application itself. It exposes properties that refer to the person who is signed into the application (the local user, represented by the [UCCollaborationLib.ISelf](https://msdn.microsoft.com/library/UCCollaborationLib.ISelf) interface), the state of the application, the list of contacts for the local user, and several other settings. When it's trying to connect to the IM client application, the Office application gets a reference to an object that implements the **ILyncClient** interface. From that reference, Office can access much of the functionality of the IM client application.</span></span> 
  
<span data-ttu-id="fec71-p125">さらに、 **ILyncClient** インターフェイスを実装するクラスは、 **_ILyncClientEvents** インターフェイスも実装する必要があります。 **_ILyncClientEvents** インターフェイスは、IM クライアント アプリケーションの状態を監視するために必要ないくつかのイベントを公開します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p125">In addition, the class that implements the **ILyncClient** interface should also implement the **_ILyncClientEvents** interface. The **_ILyncClientEvents** interface exposes several of the events that are required for monitoring the state of the IM client application.</span></span> 
  
<span data-ttu-id="fec71-309">表 3 は、**ILyncClient** と **_ILyncClientEvents** から継承するクラスに実装されている必要のあるメンバーを示しています。</span><span class="sxs-lookup"><span data-stu-id="fec71-309">Table 3 shows the members that must be implemented in the class that inherits from **ILyncClient** and **_ILyncClientEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fec71-310">表に記載されていない **ILyncClient** または **\_ILyncClientEvents** インターフェイスのメンバーは、存在している必要がありますが、実装されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fec71-310">Any member of the **ILyncClient** or **\_ILyncClientEvents** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="fec71-311">存在していても実装されていないメンバーは、**NotImplementedException** または **E\_NOTIMPL** エラーをスローすることがあります。</span><span class="sxs-lookup"><span data-stu-id="fec71-311">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="fec71-312">**ILyncClient** と **_ILyncClientEvents** インターフェイス、およびそのメンバーの詳細については、「[UCCollaborationLib.ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient)」および「[UCCollaborationLib._ILyncClientEvents](https://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec71-312">For more information about the **ILyncClient** and **_ILyncClientEvents** interfaces and their members, see [UCCollaborationLib.ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) and [UCCollaborationLib._ILyncClientEvents](https://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span></span> 
  
<span data-ttu-id="fec71-313">**表 3. ILyncClient と ILyncClientEvents インターフェイスの実装**</span><span class="sxs-lookup"><span data-stu-id="fec71-313">**Table 3. Implementation of ILyncClient and ILyncClientEvents interfaces**</span></span>

|<span data-ttu-id="fec71-314">**インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="fec71-314">**Interface**</span></span>|<span data-ttu-id="fec71-315">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="fec71-315">**Member**</span></span>|<span data-ttu-id="fec71-316">**説明**</span><span class="sxs-lookup"><span data-stu-id="fec71-316">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fec71-317">**ILyncClient**</span><span class="sxs-lookup"><span data-stu-id="fec71-317">**ILyncClient**</span></span> <br/> |<span data-ttu-id="fec71-318">**ContactManager** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-318">**ContactManager** property</span></span>  <br/> |<span data-ttu-id="fec71-319">連絡先グループ マネージャーを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-319">Gets the contact group manager.</span></span>  <br/> |
||<span data-ttu-id="fec71-320">**ConversationManager** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-320">**ConversationManager** property</span></span>  <br/> |<span data-ttu-id="fec71-321">会話マネージャーを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-321">Gets the conversations manager.</span></span>  <br/> |
||<span data-ttu-id="fec71-322">**Self** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-322">**Self** property</span></span>  <br/> |<span data-ttu-id="fec71-323">**Self** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-323">Gets the **Self** object.</span></span>  <br/> |
||<span data-ttu-id="fec71-324">**SignIn** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-324">**SignIn** method</span></span>  <br/> |<span data-ttu-id="fec71-325">特定の可用性を持つ IM クライアント アプリケーションのサインイン プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="fec71-325">Starts the IM client application sign-in process with a specific availability.</span></span>  <br/> |
||<span data-ttu-id="fec71-326">**State** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-326">**State** property</span></span>  <br/> |<span data-ttu-id="fec71-327">現在のプラットフォーム状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-327">Gets the current platform state.</span></span>  <br/> |
||<span data-ttu-id="fec71-328">**Uri** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-328">**Uri** property</span></span>  <br/> |<span data-ttu-id="fec71-329">IM クライアント アプリケーションの URI を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-329">Gets the URI of the IM client application.</span></span>  <br/> |
|<span data-ttu-id="fec71-330">**_ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="fec71-330">**_ILyncClientEvents**</span></span> <br/> |<span data-ttu-id="fec71-331">**OnStateChanged** イベント</span><span class="sxs-lookup"><span data-stu-id="fec71-331">**OnStateChanged** event</span></span>  <br/> |<span data-ttu-id="fec71-p127">IM クライアント アプリケーションの状態が変化したときに発生します。このイベントを処理し、 **eventData.NewState** プロパティを取得する必要があります。アプリケーション内のいずれかのサブシステムで状態の変更が生じたとき、IM クライアント アプリケーションのインスタンスにバインドされているすべてのプロセスに対して、イベントが発生します。  </span><span class="sxs-lookup"><span data-stu-id="fec71-p127">Raised when the IM client application state changes. You should handle this event and get the **eventData.NewState** property. The event is raised for all processes bound to an instance of an IM client application when any subsystem in the application causes the state change.  </span></span><br/> |
   
<span data-ttu-id="fec71-p128">初期化の処理中に、Office は **ILyncClient.State** プロパティにアクセスします。このプロパティは、 [UCCollaborationLib.ClientState](https://msdn.microsoft.com/library/UCCollaborationLib.ClientState) 列挙からの値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-p128">During the initialization process, Office accesses the **ILyncClient.State** property. This property needs to return a value from the [UCCollaborationLib.ClientState](https://msdn.microsoft.com/library/UCCollaborationLib.ClientState) enumeration.</span></span> 
  
```cs
private ClientState _clientState;
public ClientState State
{
    get
    {
        return this._clientState;
    }
}

```

<span data-ttu-id="fec71-p129">**State** プロパティは、IM クライアント アプリケーションの現在の状態を保管します。これは、IM アプリケーションのセッション全体で設定され、更新されている必要があります。IM クライアント アプリケーションは、サインイン、サインアウト、またはシャット ダウンするときに、 **State** プロパティを設定する必要があります。次の例で示すように、このプロパティは **ILyncClient.SignIn** と **ILyncClient.SignOut** メソッド内に設定することが最善です。</span><span class="sxs-lookup"><span data-stu-id="fec71-p129">The **State** property stores the current status of the IM client application. It must be set and updated throughout the IM client application session. When the IM client application signs in, signs out, or shuts down, it should set the **State** property. It is best to set this property within the **ILyncClient.SignIn** and **ILyncClient.SignOut** methods, as the following example demonstrates.</span></span> 
  
```cs
// This field is of a type that implements the 
// IAsynchronousOperation interface.
private IMClientAsyncOperation _asyncOperation = new IMClientAsyncOperation();
// This field is of a type that implements the ISelf interface.
private IMClientSelf _self;
public IMClientAsyncOperation SignIn(string _userUri, string _domainAndUser, 
    string _password, object _IMClientCallback, object _state)
{
    ClientState _previousClientState = this._clientState;
    this._clientState = ClientState.ucClientStateSignedIn;
    // The IMClientStateChangedEventData class implements the 
    // IClientStateChangedEventData interface.
    IMClientStateChangedEventData eventData = 
        new IMClientStateChangedEventData(_previousClientState, 
        this._clientState);
    if (_userUri != null)
    {
        // During the sign-in process, create a new contact with
        // the contact information of the currently signed-in user.
        this._self = new IMClientSelf(IMContact.BuildContact(_userUri));
    }
    // Raise the _ILyncClientEvents.OnStateChanged event.
    OnStateChanged(this, eventData as UC.ClientStateChangedEventData);
    
    return this._asyncOperation;
    }
}

```

<span data-ttu-id="fec71-341">次のコード例は、_ **ILyncClientEvents** インターフェイスと _ **IUCOfficeIntegrationEvents** インターフェイスを使用してイベント リスナーをセットアップする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="fec71-341">The following code example demonstrates how to set up the event listener using the _ **ILyncClientEvents** and _ **IUCOfficeIntegrationEvents** interfaces.</span></span> 
  
```cs
using Microsoft.Office.Uc;
using System;
using System.Runtime.CompilerServices;
using System.Runtime.InteropServices;
namespace SampleImplementation
{
    // Note: UCOfficeIntegration inherits from both IUCOfficeIntegration and _IUCOfficeIntegrationEvents_Event
    [ClassInterface(ClassInterfaceType.None), Guid("13c41ef9-eb90-4e94-8a7c-1e9d686bc019"), ComVisible(true)]
    [ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
    public class MyInstantMessengerOfficeIntegration : UCOfficeIntegration
    {
        #region IUCOfficeIntegration implementation
        public string GetAuthenticationInfo(string _version)
        {
            return "";
        }
        public object GetInterface(string _version, OIInterface _interface)
        {
            return null;
        }
        public OIFeature GetSupportedFeatures(string _version)
        {
            return OIFeature.oiFeatureAddOneNoteToConversation;
        }
        #endregion
        #region _IUCOfficeIntegrationEvents support
        // This event implements void _IUCOfficeIntegrationEvents.OnShuttingDown();
        public event _IUCOfficeIntegrationEvents_OnShuttingDownEventHandler OnShuttingDown;
        // This method is called by the IM application when it is beginning to shut down.
        // The method will raise the OnShuttingDown event which is translated by .NET COM interop layer
        // into a call to _IUCOfficeIntegrationEvents.OnShuttingDown.
        // This notifies Office applications that the IM application is going away.
        internal void RaiseOnShuttingDownEvent()
        {
            if (this.OnShuttingDown != null)
            {
                this.OnShuttingDown();
            }
        }
        #endregion
    }
    // Note: LyncClient inherits from both ILyncClient and _ILyncClientEvents_Event
    // You must implement LyncClient because the event handlers in _ILyncClientEvents expect you to pass a LyncClient interface.
    [ComVisible(true)]
    [ComSourceInterfaces(typeof(_ILyncClientEvents))]
    public class MyInstantMessengerOfficeIntegration2 :
        Client,
        Client2,
        LyncClient
    {
        #region Interfaces
        public LyncClientCapabilityTypes Capabilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConferenceScheduler ConferenceScheduler
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager ContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConversationManager ConversationManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DelegatorClient[] DelegatorClients
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DeviceManager DeviceManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public bool InSuppressedMode
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager PrivateContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public RoomManager RoomManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Self Self
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientSettings Settings
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public SignInConfiguration SignInConfiguration
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientState State
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientType Type
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public string Uri
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Utilities Utilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ApplicationRegistration CreateApplicationRegistration(string _appGuid, string _appName)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Initialize(string _clientName, string _version = "0", string _clientShortName = "0", string _clientNameAbbreviation = "0", string _clientLongName = "0", SupportedFeatures _supportedFeatures = SupportedFeatures.ucAllFeatures, [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Shutdown([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignIn(string _userUri = "0", string _domainAndUsername = "0", string _password = "0", [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignOut([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        #endregion
        #region _ILyncClientEvents support
        public event _ILyncClientEvents_OnStateChangedEventHandler OnStateChanged;
        public event _ILyncClientEvents_OnNotificationReceivedEventHandler OnNotificationReceived;
        public event _ILyncClientEvents_OnCredentialRequestedEventHandler OnCredentialRequested;
        public event _ILyncClientEvents_OnSignInDelayedEventHandler OnSignInDelayed;
        public event _ILyncClientEvents_OnCapabilitiesChangedEventHandler OnCapabilitiesChanged;
        public event _ILyncClientEvents_OnDelegatorClientAddedEventHandler OnDelegatorClientAdded;
        public event _ILyncClientEvents_OnDelegatorClientRemovedEventHandler OnDelegatorClientRemoved;
        // Notifies Office apps that the IM client state (signed out, signing in, singed in, signing out, etc) has changed.
        internal void RaiseOnStateChangedEvent(ClientStateChangedEventData eventData)
        {
            if (this.OnStateChanged != null)
            {
                this.OnStateChanged(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a notification event from MAPI (e.g. autodiscover has finished)
        internal void RaiseOnNotificationReceivedEvent(LyncClientNotificationReceivedEventData eventData)
        {
            if (this.OnNotificationReceived != null)
            {
                this.OnNotificationReceived(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a request for credentials for some operation (e.g. sign in, web search)
        internal void RaiseOnCredentialRequestedEvent(CredentialRequestedEventData eventData)
        {
            if (this.OnCredentialRequested != null)
            {
                this.OnCredentialRequested(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has been delayed from signing in and gives an estimated delay time.
        internal void RaiseOnSignInDelayedEvent(SignInDelayedEventData eventData)
        {
            if (this.OnSignInDelayed != null)
            {
                this.OnSignInDelayed(this, eventData);
            }
        }
        // Notifies Office apps that the capabilities of this IM client have changed.
        internal void RaiseOnCapabilitiesChangedEvent(PreferredCapabilitiesChangedEventData eventData)
        {
            if (this.OnCapabilitiesChanged != null)
            {
                this.OnCapabilitiesChanged(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been added to the IM client object.
        internal void RaiseOnDelegatorClientAdded(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientAdded != null)
            {
                this.OnDelegatorClientAdded(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been removed from the IM client object.
        internal void RaiseOnDelegatorClientRemoved(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientRemoved != null)
            {
                this.OnDelegatorClientRemoved(this, eventData);
            }
        }
        #endregion
    }
}
```

### <a name="iautomation-interface"></a><span data-ttu-id="fec71-342">IAutomation インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fec71-342">IAutomation interface</span></span>
<span data-ttu-id="fec71-343"><a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-343"></span></span>

<span data-ttu-id="fec71-p130">**IAutomation** インターフェイスは、IM クライアント アプリケーションの機能を自動化します。これを使用して、会話を開始すること、会議に参加すること、および拡張機能ウィンドウのコンテキストを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="fec71-p130">The **IAutomation** interface automates features of the IM client application. It can be used to start conversations, join conferences, and provide extensibility window context.</span></span> 
  
<span data-ttu-id="fec71-346">表 4 は、 **IAutomation** から継承するクラスに実装されている必要のあるメンバーを示しています。</span><span class="sxs-lookup"><span data-stu-id="fec71-346">Table 4 shows the members that must be implemented in the class that inherits from **IAutomation**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fec71-347">表に記載されていない **IAutomation** インターフェイスのメンバーは、存在している必要がありますが、実装されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fec71-347">Any member of the **IAutomation** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="fec71-348">存在していても実装されていないメンバーは、**NotImplementedException** または **E_NOTIMPL** エラーをスローすることがあります。</span><span class="sxs-lookup"><span data-stu-id="fec71-348">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="fec71-349">**IAutomation** インターフェイスとそのメンバーの詳細については、「[UCCollaborationLib.IAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.IAutomation)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec71-349">For more information about the **IAutomation** interface and its members, see [UCCollaborationLib.IAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span></span> 
  
<span data-ttu-id="fec71-350">**表 4. IAutomation インターフェイスの実装**</span><span class="sxs-lookup"><span data-stu-id="fec71-350">**Table 4. Implementation of IAutomation interface**</span></span>

|<span data-ttu-id="fec71-351">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="fec71-351">**Member**</span></span>|<span data-ttu-id="fec71-352">**説明**</span><span class="sxs-lookup"><span data-stu-id="fec71-352">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fec71-353">**StartConversation** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-353">**StartConversation** method</span></span>  <br/> |<span data-ttu-id="fec71-p132">指定された会話モダリティを使用して会話を開始します。 **IConversationWindow** のインスタンスが返されます。  </span><span class="sxs-lookup"><span data-stu-id="fec71-p132">Starts a conversation using the specified conversation modality. An instance of **IConversationWindow** is returned.  </span></span><br/> |
   
## <a name="implementing-contact-presence-integration"></a><span data-ttu-id="fec71-356">連絡先プレゼンス統合の実装</span><span class="sxs-lookup"><span data-stu-id="fec71-356">Implementing contact presence integration</span></span>
<span data-ttu-id="fec71-357"><a name="off15_IMIntegration_ImplementIMFeatures"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-357"></span></span>

<span data-ttu-id="fec71-p133">前述の 3 つの必須インターフェイスに加えて、Office での連絡先プレゼンス機能を有効にするために必要な他のいくつかのインターフェイスがあります。これらには、以下のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fec71-p133">In addition to the three required interfaces discussed previously, there are several other interfaces that are important for enabling contact presence functionality in Office. These include the following:</span></span>
  
- <span data-ttu-id="fec71-360">[IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) や **IContact2** インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="fec71-360">The [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) or **IContact2** interface.</span></span> 
    
- <span data-ttu-id="fec71-361">[ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="fec71-361">The [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) interface.</span></span> 
    
- <span data-ttu-id="fec71-362">[IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) と [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="fec71-362">The [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) and [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) interfaces.</span></span> 
    
- <span data-ttu-id="fec71-363">[IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) と [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="fec71-363">The [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) and [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) interfaces.</span></span> 
    
- <span data-ttu-id="fec71-364">[IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="fec71-364">The [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) interface.</span></span> 
    
- <span data-ttu-id="fec71-365">[IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="fec71-365">The [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) interface.</span></span> 
    
- <span data-ttu-id="fec71-366">[ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fec71-366">The [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) interface</span></span> 
    
### <a name="icontact-interface"></a><span data-ttu-id="fec71-367">IContact インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fec71-367">IContact interface</span></span>
<span data-ttu-id="fec71-368"><a name="off15_IMIntegration_ImplementRequired_IContact"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-368"></span></span>

<span data-ttu-id="fec71-p134">**IContact** インターフェイスは、IM クライアント アプリケーションのユーザーを表します。このインターフェイスは、ユーザーのプレゼンス、使用可能なモダリティ、グループ メンバーシップ、および連絡先の種類のプロパティを公開します。別のユーザーとの会話を開始するには、そのユーザーに **IContact** のインスタンスを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-p134">The **IContact** interface represents an IM client application user. The interface exposes presence, available modalities, group membership, and contact type properties for a user. To start a conversation with another user, you must provide that user instance of **IContact**.</span></span>
  
<span data-ttu-id="fec71-372">表 5 は、 **IContact** から継承するクラスに実装されている必要のあるメンバーを示しています。</span><span class="sxs-lookup"><span data-stu-id="fec71-372">Table 5 shows the members that must be implemented in the class that inherits from **IContact**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fec71-373">表に記載されていない **IContact** インターフェイスのメンバーは、存在している必要がありますが、実装されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fec71-373">Any member of the **IContact** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="fec71-374">存在していても実装されていないメンバーは、**NotImplementedException** または **E_NOTIMPL** エラーをスローすることがあります。</span><span class="sxs-lookup"><span data-stu-id="fec71-374">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="fec71-375">**IContact** インターフェイスとそのメンバーの詳細については、「[UCCollaborationLib.IContact](https://msdn.microsoft.com/library/UCCollaborationLib.IContact)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec71-375">For more information about the **IContact** interface and its members, see [UCCollaborationLib.IContact](https://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span></span> 
  
<span data-ttu-id="fec71-376">**表 5. IContact インターフェイスの実装**</span><span class="sxs-lookup"><span data-stu-id="fec71-376">**Table 5. Implementation of the IContact interface**</span></span>

|<span data-ttu-id="fec71-377">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="fec71-377">**Member**</span></span>|<span data-ttu-id="fec71-378">**説明**</span><span class="sxs-lookup"><span data-stu-id="fec71-378">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fec71-379">**CanStart** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-379">**CanStart** method</span></span>  <br/> |<span data-ttu-id="fec71-380">指定の種類のモダリティを連絡先で開始できる場合は、 **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-380">Returns **true** if a given type of modality can be started on the contact.</span></span>  <br/> |
|<span data-ttu-id="fec71-381">**GetContactInformation** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-381">**GetContactInformation** method</span></span>  <br/> |<span data-ttu-id="fec71-382">発行連絡先から 1 つのプレゼンス アイテムを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-382">Gets one presence item from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="fec71-383">**BatchGetContactInformation** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-383">**BatchGetContactInformation** method</span></span>  <br/> |<span data-ttu-id="fec71-384">発行連絡先から複数のプレゼンス アイテムを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-384">Gets multiple presence items from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="fec71-385">**Settings** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-385">**Settings** property</span></span>  <br/> |<span data-ttu-id="fec71-386">連絡先プロパティのコレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-386">Gets a collection of contact properties.</span></span>  <br/> |
|<span data-ttu-id="fec71-387">**CustomGroups** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-387">**CustomGroups** property</span></span>  <br/> |<span data-ttu-id="fec71-388">連絡先がメンバーとなっているグループのコレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-388">Gets a collection of groups that the contact is a member of.</span></span>  <br/> |
   
<span data-ttu-id="fec71-p136">初期化プロセス中に、Office アプリケーションは **IContact.CanStart** メソッドを呼び出して、ローカル ユーザーの IM 機能を判別します。 **CanStart** メソッドは、 [UCCollaborationLib.ModalityTypes](https://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) 列挙から  __modalityTypes_ パラメーターの引数としてフラグを取得します。現在のユーザーが要求されたモダリティに関わることができる場合 (つまり、ユーザーにインスタント メッセージング、音声とビデオのメッセージング、またはアプリケーション共有の能力がある場合)、 **CanStart** メソッドは **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p136">During the initialization process, the Office application calls the **IContact.CanStart** method to determine the IM capabilities for the local user. The **CanStart** method takes a flag from the [UCCollaborationLib.ModalityTypes](https://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) enumeration as an argument for the  __modalityTypes_ parameter. If the current user can engage in the requested modality (that is, the user is capable of instant messaging, audio and video messaging, or application sharing), the **CanStart** method returns **true**.</span></span>
  
```cs
public bool CanStart(ModalityTypes _modalityTypes)
{
    // Define the capabilities of the current IM client application
    // user by using flags from the ModalityTypes enumeration.
    ModalityTypes userCapabilities = 
        ModalityTypes.ucModalityInstantMessage | 
        ModalityTypes.ucModalityAudioVideo | 
        ModalityTypes.ucModalityAppSharing;
    // Perform a simple test for equivalency.
    if (_modalityType == userCapabilities) 
    {
        return true;
    }
    else 
    {
        return false;
    }
}

```

<span data-ttu-id="fec71-p137">**GetContactInformation** メソッドは、連絡先に関する情報を **IContact** オブジェクトから取得します。呼び出し元のコードは [UCCollaborationLib.ContactInformationType](https://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) 列挙からの値を、取得するデータを示す  __contactInformationType_ パラメーターに渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-p137">The **GetContactInformation** method retrieves information about the contact from the **IContact** object. The calling code needs to pass in a value from the [UCCollaborationLib.ContactInformationType](https://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) enumeration for the  __contactInformationType_ parameter, which indicates the data to be retrieved.</span></span> 
  
```cs
public object GetContactInformation(
    ContactInformationType _contactInformationType)
{
    // Determine the information to return from the contact's data based
    // on the value passed in for the _contactInformationType parameter.
    switch (_contactInformationType)
    {
        case ContactInformationType.ucPresenceEmailAddresses:
        {
            // Return the URI associated with the contact.
            string returnValue = this.Uri.ToLower().Replace("sip:", String.Empty);
            return returnValue;
        }
        case ContactInformationType.ucPresenceDisplayName:
        {
            // Return the display name associated with the contact.
            string returnValue = this._DisplayName;
            return returnValue;
        }
        default:
        {
            throw new NotImplementedException;
        }
        // Additional implementation details omitted.
    }
}
```

<span data-ttu-id="fec71-p138">**GetContactInformation** と同様に、 **BatchGetContactInformation** メソッドは、連絡先に関する複数のプレゼンス アイテムを **IContact** オブジェクトから取得します。呼び出し元のコードは、値の配列を **ContactInformationType** 列挙から  __contactInformationTypes_ パラメーターに渡す必要があります。メソッドは、要求されたデータを含む [UCCollaborationLib.IContactInformationDictionary](https://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p138">Similar to the **GetContactInformation**, the **BatchGetContactInformation** method retrieves multiple presence items about the contact from the **IContact** object. The calling code needs to pass in an array of values from the **ContactInformationType** enumeration for the  __contactInformationTypes_ parameter. The method returns an [UCCollaborationLib.IContactInformationDictionary](https://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) object that contains the requested data.</span></span> 
  
```cs
public IMClientContactInformationDictionary BatchGetContactInformation(
    ContactInformationType[] _contactInformationTypes)
{
    // The IMClientContactInformationDictionary class implements the
    // IContactInformationDictionary interface.
    IMClientContactInformationDictionary contactDictionary = 
        new IMClientContactInformationDictionary();
    foreach (ContactInformationType type in _contactInformationTypes)
    {
        // Call GetContactInformation for each type of contact 
        // information to retrieve. This code adds a new entry to
        // a Dictionary object exposed by the
        // ContactInformationDictionary property.
        contactDictionary.ContactInformationDictionary.Add(
            type, this.GetContactInformation(type));
    }
    return contactDictionary;
}
```

<span data-ttu-id="fec71-397">**IContact.Settings** プロパティは、連絡先についてのカスタム プロパティが含まれる **IContactSettingDictionary** オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-397">The **IContact.Settings** property returns an **IContactSettingDictionary** object that contains custom properties about the contact.</span></span> 
  
```cs
public IMClientContactSettingDictionary Settings
{
    get
    {
       // The IMClientContactSettingDictionary class implements
       // the IContactSettingDictionary interface.
       return new IMClientContactSettingDictionary();
    }
}
```

<span data-ttu-id="fec71-398">**IContact.CustomGroups** プロパティは、連絡先がメンバーとなっているすべてのグループを含む **IGroupCollection** オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-398">The **IContact.CustomGroups** property returns an **IGroupCollection** object that includes all of the groups of which the contact is a member.</span></span> 
  
```cs
public IMClientGroupCollection CustomGroups
{
    get {
       // The IMClientGroupCollection class implements
       // the IGroupCollection interface.
        return new IMClientGroupCollection();
    }
}
```

### <a name="iself-interface"></a><span data-ttu-id="fec71-399">ISelf インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fec71-399">ISelf interface</span></span>
<span data-ttu-id="fec71-400"><a name="off15_IMIntegration_ImplementRequired_ISelf"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-400"></span></span>

<span data-ttu-id="fec71-p139">初期化プロセス中に、Office アプリケーションは **ILyncClient.Self** プロパティにアクセスして、現在のユーザーのためのデータを取得します。その結果、 **ISelf** オブジェクトが必ず返されます。 **ISelf** インターフェイスは、ローカルの、サインインしている IM クライアント アプリケーションのユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p139">During the initialization process, the Office application gets the data for the current user by accessing the **ILyncClient.Self** property, which must return an **ISelf** object. The **ISelf** interface represents the local, signed-in IM client application user.</span></span> 
  
<span data-ttu-id="fec71-403">表 6 は、 **ISelf** から継承するクラスに実装されている必要のあるメンバーを示しています。</span><span class="sxs-lookup"><span data-stu-id="fec71-403">Table 6 shows the members that must be implemented in the class that inherits from **ISelf**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fec71-p140">表に記載されていない **ISelf** インターフェイスのメンバーは、存在している必要がありますが、実装されている必要はありません。存在していても実装されていないメンバーは、 **NotImplementedException** または **E_NOTIMPL** エラーをスローすることがあります。</span><span class="sxs-lookup"><span data-stu-id="fec71-p140">Any member of the **ISelf** interface not listed in the table must be present but does not need to be implemented. Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
  
<span data-ttu-id="fec71-406">**表 6. ISelf インターフェイスの実装**</span><span class="sxs-lookup"><span data-stu-id="fec71-406">**Table 6. Implementation of the ISelf interface**</span></span>

|<span data-ttu-id="fec71-407">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="fec71-407">**Member**</span></span>|<span data-ttu-id="fec71-408">**説明**</span><span class="sxs-lookup"><span data-stu-id="fec71-408">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fec71-409">**Contact** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-409">**Contact** property</span></span>  <br/> |<span data-ttu-id="fec71-410">ローカル ユーザーに関連付けられた **IContact** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-410">Gets the **IContact** object associated with the local user.</span></span>  <br/> |
   
<span data-ttu-id="fec71-p141">ローカル ユーザーのプレゼンス、使用可能なモダリティ、グループ メンバーシップ、および連絡先の種類のプロパティは、( **IContact** オブジェクトを返す) **ISelf.Contact** プロパティによって公開されます。初期化プロセス中に、Office アプリケーションは **ISelf.Contact** プロパティにアクセスして、ローカル ユーザーの連絡先情報への参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p141">Presence, available modalities, group membership, and contact type properties for the local user are exposed through the **ISelf.Contact** property (which returns an **IContact** object). During the initialization process, the Office application accesses the **ISelf.Contact** property to get a reference to the contact information for the local user.</span></span> 
  
<span data-ttu-id="fec71-413">次のコードを使用して、 **Contact** プロパティを実装する、 **ISelf** インターフェイスから継承するクラスを定義します。</span><span class="sxs-lookup"><span data-stu-id="fec71-413">Use the following code to define a class that inherits from the **ISelf** interface that implements the **Contact** property.</span></span> 
  
```cs
[ComVisible(true)]
public class IMClientSelf : ISelf
{
    // Declare a private field to store contact data for local user.
    private IMClientContact _contactData;
    // In the constructor for the ISelf object, the calling code 
    // must supply contact data.
    public IMClientSelf (IMClientContact _selfContactData)
    {
        this._contactData = _selfContactData;
    }
    // When accessed, the Contact property returns a reference
    // to the IContact object that represents the local user.
    public IMClientContact Contact
    {
        get
        {
            return this._contactData as IMClientContact;
        }
    }
    // Additional implementation details omitted.
}
```

### <a name="icontactmanager-and-_icontactmanagerevents-interfaces"></a><span data-ttu-id="fec71-414">IContactManager と _IContactManagerEvents インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fec71-414">IContactManager and _IContactManagerEvents interfaces</span></span>
<span data-ttu-id="fec71-415"><a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-415"></span></span>

<span data-ttu-id="fec71-p142">**IContactManager** オブジェクトは、ローカル ユーザー自身の連絡先情報を含む、ローカル ユーザーの連絡先を管理します。Office アプリケーションは、 **IContactManager** オブジェクトを使用して、ローカル ユーザーの連絡先に対応する **IContact** オブジェクトにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="fec71-p142">The **IContactManager** object manages the contacts for the local user, including the local user's own contact information. The Office application uses an **IContactManager** object to access **IContact** objects that correspond to the local user's contacts.</span></span> 
  
<span data-ttu-id="fec71-418">表 7 は、 **IContactManager** と **_IContactManagerEvents** から継承するクラスに実装されている必要のあるメンバーを示しています。</span><span class="sxs-lookup"><span data-stu-id="fec71-418">Table 7 shows the members that must be implemented in the class that inherits from **IContactManager** and **_IContactManagerEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fec71-419">表に記載されていない **IContactManager** インターフェイスのメンバーは、存在している必要がありますが、実装されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fec71-419">Any member of the **IContactManager** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="fec71-420">存在していても実装されていないメンバーは、**NotImplementedException** または **E\_NOTIMPL** エラーをスローすることがあります。</span><span class="sxs-lookup"><span data-stu-id="fec71-420">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="fec71-421">**IContactManager** と **_IContactManagerEvents** インターフェイス、およびそのメンバーの詳細については、「[UCCollaborationLib.IContactManager](https://msdn.microsoft.com/library/UCCollaborationLib.IContactManager)」および「[UCCollaborationLib._IContactManagerEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec71-421">For more information about the **IContactManager** and **_IContactManagerEvents** interfaces and their members, see [UCCollaborationLib.IContactManager](https://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) and [UCCollaborationLib._IContactManagerEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span></span> 
  
<span data-ttu-id="fec71-422">**表 7. IContactManager と _IContactManagerEvents インターフェイスの実装**</span><span class="sxs-lookup"><span data-stu-id="fec71-422">**Table 7. Implementation of the IContactManager and _IContactManagerEvents interfaces**</span></span>

|<span data-ttu-id="fec71-423">**インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="fec71-423">**Interface**</span></span>|<span data-ttu-id="fec71-424">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="fec71-424">**Member**</span></span>|<span data-ttu-id="fec71-425">**説明**</span><span class="sxs-lookup"><span data-stu-id="fec71-425">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fec71-426">**IContactManager**</span><span class="sxs-lookup"><span data-stu-id="fec71-426">**IContactManager**</span></span> <br/> |<span data-ttu-id="fec71-427">**GetContactByUri** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-427">**GetContactByUri** method</span></span>  <br/> |<span data-ttu-id="fec71-428">連絡先 URI を使用して、新しい連絡先インスタンスを検索または作成します。</span><span class="sxs-lookup"><span data-stu-id="fec71-428">Finds or creates a new contact instance by using the contact URI.</span></span>  <br/> |
||<span data-ttu-id="fec71-429">**CreateSubscription** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-429">**CreateSubscription** method</span></span>  <br/> |<span data-ttu-id="fec71-430">サブスクリプションやクエリのバッチ処理に使用できる **ISubscription** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="fec71-430">Creates an **ISubscription** object that can be used for batching subscriptions or queries.</span></span>  <br/> |
||<span data-ttu-id="fec71-431">**Lookup** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-431">**Lookup** method</span></span>  <br/> |<span data-ttu-id="fec71-432">連絡先または配布グループを検索します。</span><span class="sxs-lookup"><span data-stu-id="fec71-432">Looks up a contact or distribution group.</span></span>  <br/> |
|<span data-ttu-id="fec71-433">**_IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="fec71-433">**_IContactManagerEvents**</span></span> <br/> |<span data-ttu-id="fec71-434">**OnGroupAdded** イベント</span><span class="sxs-lookup"><span data-stu-id="fec71-434">**OnGroupAdded** event</span></span>  <br/> |<span data-ttu-id="fec71-p144">グループがグループ コレクションに追加されると発生します。更新されたグループ コレクションは、 **IContactManager.Groups** プロパティから取得できます。  </span><span class="sxs-lookup"><span data-stu-id="fec71-p144">Raised when a group is added to a group collection. The updated group collection can be obtained from the **IContactManager.Groups** property.  </span></span><br/> |
||<span data-ttu-id="fec71-437">**OnGroupRemoved** イベント</span><span class="sxs-lookup"><span data-stu-id="fec71-437">**OnGroupRemoved** event</span></span>  <br/> |<span data-ttu-id="fec71-p145">グループがグループ コレクションから除去されると発生します。更新されたグループ コレクションは、 **IContactManager.Groups** プロパティから取得できます。  </span><span class="sxs-lookup"><span data-stu-id="fec71-p145">Raised when a group is removed from a group collection. The updated group collection can be obtained from the **IContactManager.Groups** property.  </span></span><br/> |
||<span data-ttu-id="fec71-440">**OnSearchProviderStateChanged** イベント</span><span class="sxs-lookup"><span data-stu-id="fec71-440">**OnSearchProviderStateChanged** event</span></span>  <br/> |<span data-ttu-id="fec71-441">検索プロバイダーの状態が変化したときに発生します。</span><span class="sxs-lookup"><span data-stu-id="fec71-441">Raised when a search provider's status changes.</span></span>  <br/> |
   
<span data-ttu-id="fec71-p146">Office は **IContactManager.GetContactByUri** を呼び出して、連絡先の SIP アドレスを使用することにより、連絡先プレゼンス情報を取得します。Active Directory で連絡先が SIP アドレス用に構成されると、Office は連絡先用にこのアドレスを判別して、 **GetContactByUri** を呼び出し、連絡先の SIP アドレスを  __contactUri_ パラメーターに渡します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p146">Office calls **IContactManager.GetContactByUri** to get a contact's presence information, by using the SIP address of the contact. When a contact is configured for an SIP address in the Active Directory, Office determines this address for a contact and calls **GetContactByUri**, passing the SIP address of the contact in for the  __contactUri_ parameter.</span></span> 
  
<span data-ttu-id="fec71-p147">Office は、連絡先の SIP アドレスを判別できないとき、 **IContactManager.Lookup** メソッドを呼び出して、IM サービスを使用することにより SIP を検索します。ここで、Office は検索できた最良のデータを連絡先に渡します (たとえば、連絡先のメール アドレスだけなど)。 **Lookup** メソッドは、非同期で **AsynchronousOperation** オブジェクトを返します。コールバックを呼び出すときに、 **Lookup** メソッドは連絡先の URI に加えて操作の成否も返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p147">When Office cannot determine the SIP address for the contact, it calls the **IContactManager.Lookup** method to find the SIP by using the IM service. Here Office passes in the best data that it can find for the contact (for example, just the email address for the contact). The **Lookup** method asynchronously returns an **AsynchronousOperation** object. When it invokes the callback, the **Lookup** method should return the success or failure of the operation in addition to the URI of the contact.</span></span> 
  
```cs
public IMClientContact GetContactByUri(string _contactUri)
{
    // Declare a Contact variable to contain information about the contact.
    IMClientContact tempContact = null;
    // The _groupCollections field is an IGroupCollection object. Iterate 
    // over each group in collection to see if the 
    // contact is a part of the group.
    foreach (IMClientGroup group in this._groupCollections)
    {
       if (group.TryGetContact(_contactUri, out tempContact))
       {
           break;
       }
    }
    // Check to see that the URI returned a valid contact. If it
    // did not, create a new contact.
    if (tempContact == null)
    {
        tempContact = IMClientContact.BuildContact(_contactUri);
    }
    // Return the contact to the calling code.
    return tempContact;
}
```

<span data-ttu-id="fec71-p148">Office アプリケーションは、個々の連絡先のプレゼンスの変更をサブスクライブする必要があります。したがって、連絡先のプレゼンス状態が変化したとき、IM サーバーは、IM クライアント アプリケーションに警告を出すことにより、Office アプリケーションに警告します。これを行うには、Office アプリケーションが **IContactManager.CreateSubscription** メソッドを呼び出して、この要求に対する新しい **IContactSubscription** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p148">The Office application needs to subscribe to presence changes for an individual contact. Thus, when a contact's presence status changes, the IM server alerts the IM client application—thereby alerting the Office application. To do this, the Office application calls the **IContactManager.CreateSubscription** method to create a new **IContactSubscription** object for this request.</span></span> 
  
```cs
// Declare a private field to contain an IContactSubscription object.
private IMClientContactSubscription _contactSubscription;
// Return the IContactSubscription object associated 
// with the IContactManager object.
public IMClientContactSubscription CreateSubscription()
{
    return this._contactSubscription;
}
```

### <a name="igroup-and-igroupcollection-interfaces"></a><span data-ttu-id="fec71-451">IGroup と IGroupCollection インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fec71-451">IGroup and IGroupCollection interfaces</span></span>
<span data-ttu-id="fec71-452"><a name="off15_IMIntegration_ImplementRequired_IGroup"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-452"></span></span>

<span data-ttu-id="fec71-p149">**IGroup**オブジェクトは、集合的なグループ名によって連絡先のコレクションを特定するために、追加のプロパティを持つ連絡先のコレクションを表します。 **IGroupCollection** オブジェクトは、ローカル ユーザーと IM クライアント アプリケーションで定義されている **IGroup** オブジェクトのコレクションを表します。Office アプリケーションは **IGroupCollection** と **IGroup** オブジェクトを使用して、ローカル ユーザーの連絡先にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="fec71-p149">The **IGroup** object represents a collection of contacts with additional properties for identifying the contact collection by a collective group name. An **IGroupCollection** object represents a collection of **IGroup** objects defined by a local user and the IM client application. The Office application uses the **IGroupCollection** and **IGroup** objects to access the local user's contacts.</span></span> 
  
<span data-ttu-id="fec71-456">表 9 は、以下の表の **IGroup** と **IGroupCollection** から継承するクラスに実装されている必要のあるメンバーを示しています。</span><span class="sxs-lookup"><span data-stu-id="fec71-456">Table 9 shows the members that must be implemented in the classes that inherit from **IGroup** and **IGroupCollection** in the following table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fec71-457">表に記載されていない **IGroup** インターフェイスのメンバーは、存在している必要がありますが、実装されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fec71-457">Any member of the **IGroup** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="fec71-458">存在していても実装されていないメンバーは、**NotImplementedException** または **E_NOTIMPL** エラーをスローすることがあります。</span><span class="sxs-lookup"><span data-stu-id="fec71-458">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="fec71-459">**IGroup** と **IGroupCollection** インターフェイス、およびそのメンバーの詳細については、「[UCCollaborationLib.IGroup](https://msdn.microsoft.com/library/UCCollaborationLib.IGroup)」および「[UCCollaborationLib.IGroupCollection](https://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec71-459">For more information about the **IGroup** and **IGroupCollection** interfaces and their members, see [UCCollaborationLib.IGroup](https://msdn.microsoft.com/library/UCCollaborationLib.IGroup) and [UCCollaborationLib.IGroupCollection](https://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span></span> 
  
<span data-ttu-id="fec71-460">**表 9. IGroup と IGroupCollection インターフェイスの実装**</span><span class="sxs-lookup"><span data-stu-id="fec71-460">**Table 9. Implementation of the IGroup and IGroupCollection interfaces**</span></span>

|<span data-ttu-id="fec71-461">**インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="fec71-461">**Interface**</span></span>|<span data-ttu-id="fec71-462">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="fec71-462">**Member**</span></span>|<span data-ttu-id="fec71-463">**説明**</span><span class="sxs-lookup"><span data-stu-id="fec71-463">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fec71-464">**IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="fec71-464">**IGroupCollection**</span></span> <br/> |<span data-ttu-id="fec71-465">**Count** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-465">**Count** property</span></span>  <br/> |<span data-ttu-id="fec71-466">コレクションに含まれている **IGroup** オブジェクトの数を返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-466">Returns the count of **IGroup** objects in the collection</span></span>  <br/> |
||<span data-ttu-id="fec71-467">**Item** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-467">**Item** property</span></span>  <br/> |<span data-ttu-id="fec71-468">コレクション内の指定のインデックス位置にある **IGroup** オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-468">Returns the **IGroup** object at the specified index in the collection.</span></span>  <br/> |
|<span data-ttu-id="fec71-469">**IGroup**</span><span class="sxs-lookup"><span data-stu-id="fec71-469">**IGroup**</span></span> <br/> |<span data-ttu-id="fec71-470">**Id** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-470">**Id** property</span></span>  <br/> |<span data-ttu-id="fec71-471">グループの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="fec71-471">Returns the ID of the group.</span></span>  <br/> |
   
<span data-ttu-id="fec71-p151">Office アプリケーションは、ローカル ユーザーの情報を取得すると、 **IGroupCollection** オブジェクトを返す **IContact.CustomGroups** プロパティを呼び出すことにより、連絡先 (ローカル ユーザー) のグループ メンバーシップにアクセスします。 **IGroupCollection** には、 **IGroup** オブジェクトの配列 (または **List**) が含まれている必要があります。 **IGroupCollection** から派生するクラスは、コレクション内の項目数を返す **Count** プロパティ、およびコレクションから **IGroup** オブジェクトを返すインデクサー メソッド **this(int)** を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec71-p151">When the Office application gets the information for the local user, it accesses the group memberships of the contact (local user) by calling the **IContact.CustomGroups** property, which returns an **IGroupCollection** object. The **IGroupCollection** must contain an array (or **List**) of **IGroup** objects. The class that derives from **IGroupCollection** must expose a **Count** property, which returns the number of items in the collection, and an indexer method, **this(int)**, which returns an **IGroup** object from the collection.</span></span> 
  
### <a name="icontactsubscription-interface"></a><span data-ttu-id="fec71-475">IContactSubscription インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fec71-475">IContactSubscription interface</span></span>
<span data-ttu-id="fec71-476"><a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-476"></span></span>

<span data-ttu-id="fec71-p152">**IContactSubscription** インターフェイスによって、そのプレゼンス情報の更新を受け取る連絡先と通知をトリガーするプレゼンス情報の種類を指定できます。Office アプリケーションは **IContactSubscription** オブジェクトを使用して、連絡先のプレゼンス ステータスの情報を登録します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p152">The **IContactSubscription** interface allows you to specify the contacts to receive presence information updates for and the types of presence information that trigger a notification. Office applications use an **IContactSubscription** object to register changes to contact's presence status.</span></span> 
  
<span data-ttu-id="fec71-479">表 10 は、 **IContactSubscription** から継承するクラスに実装されている必要のあるメンバーを示しています。</span><span class="sxs-lookup"><span data-stu-id="fec71-479">Table 10 shows the members that must be implemented in the classes that inherit from **IContactSubscription**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fec71-480">表に記載されていない **IContactSubscription** インターフェイスのメンバーは、存在している必要がありますが、実装されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fec71-480">Any member of the **IContactSubscription** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="fec71-481">存在していても実装されていないメンバーは、**NotImplementedException** または **E_NOTIMPL** エラーをスローすることがあります。</span><span class="sxs-lookup"><span data-stu-id="fec71-481">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="fec71-482">**IContactSubscription** インターフェイスとそのメンバーの詳細については、「[UCCollaborationLib.IContactSubscription](https://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec71-482">For more information about the **IContactSubscription** interface and its members, see [UCCollaborationLib.IContactSubscription](https://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span></span> 
  
<span data-ttu-id="fec71-483">**表 10. IContactSubscription インターフェイスの実装**</span><span class="sxs-lookup"><span data-stu-id="fec71-483">**Table 10. Implementation of the IContactSubscription interface**</span></span>

|<span data-ttu-id="fec71-484">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="fec71-484">**Member**</span></span>|<span data-ttu-id="fec71-485">**説明**</span><span class="sxs-lookup"><span data-stu-id="fec71-485">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fec71-486">**AddContact** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-486">**AddContact** method</span></span>  <br/> |<span data-ttu-id="fec71-487">サブスクリプション オブジェクトに連絡先を追加します。</span><span class="sxs-lookup"><span data-stu-id="fec71-487">Adds a contact to the subscription object.</span></span>  <br/> |
|<span data-ttu-id="fec71-488">**Subscribe** メソッド</span><span class="sxs-lookup"><span data-stu-id="fec71-488">**Subscribe** method</span></span>  <br/> |<span data-ttu-id="fec71-489">IM クライアント アプリケーションが連絡先についてプレゼンスを監視するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="fec71-489">Helps the IM client application to monitor presence for a contact.</span></span>  <br/> |
   
<span data-ttu-id="fec71-p154">**IContactSubscription** インターフェイスには、配列または **List** を使用して、監視するすべての **IContact** オブジェクトへの参照を含める必要があります。 **IContactSubscription.AddContact** メソッドは、 **IContactSubscription** オブジェクトの基礎となるデータ構造のために **IContact** オブジェクトを追加することによって、プレゼンスの変更を監視する新しい連絡先を追加します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p154">The **IContactSubscription** interface must contain a reference to all the **IContact** objects that it monitors, using an array or a **List**. The **IContactSubscription.AddContact** method adds an **IContact** object for the to the underlying data structure of the **IContactSubscription** object, thereby adding a new contact to monitor for presence changes.</span></span> 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

<span data-ttu-id="fec71-p155">**IContactSubscription.Subscribe** メソッドにより、IM クライアント アプリケーションは、連絡先のプレゼンス オブザーバーにアクセスできます。それはポーリング戦略を使用して、IM クライアント アプリケーションがサブスクライブした連絡先について、サーバーからのプレゼンスを取得できます。 **Subscribe** メソッドは、ユーザーの連絡先リストの外部から (たとえば、大規模なパブリック ネットワークから) プレゼンスが要求されている状況で役立ちます。</span><span class="sxs-lookup"><span data-stu-id="fec71-p155">The **IContactSubscription.Subscribe** method allows an IM client application to access presence observers for the contact. It can use a polling strategy to get the presence from the server for the contacts for that the IM client application has subscribed to. The **Subscribe** method is helpful in situations where presence is requested for someone outside of a user's contact list (for example, from a larger public network).</span></span> 
  
### <a name="icontactendpoint-interface"></a><span data-ttu-id="fec71-495">IContactEndPoint インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fec71-495">IContactEndPoint interface</span></span>
<span data-ttu-id="fec71-496"><a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-496"></span></span>

<span data-ttu-id="fec71-497">**IContactEndPoint** は、連絡先の電話番号コレクションからの電話番号を表します。</span><span class="sxs-lookup"><span data-stu-id="fec71-497">The **IContactEndPoint** represents a telephone number from a contact's collection of telephone numbers.</span></span> 
  
<span data-ttu-id="fec71-498">表 11 は、 **IContactEndPoint** から継承するクラスに実装されている必要のあるメンバーを示しています。</span><span class="sxs-lookup"><span data-stu-id="fec71-498">Table 11 shows the members that must be implemented in the classes that inherit from **IContactEndPoint**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fec71-499">表に記載されていない **IContactEndPoint** インターフェイスのメンバーは、存在している必要がありますが、実装されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fec71-499">Any member of the **IContactEndPoint** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="fec71-500">存在していても実装されていないメンバーは、**NotImplementedException** または **E_NOTIMPL** エラーをスローすることがあります。</span><span class="sxs-lookup"><span data-stu-id="fec71-500">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="fec71-501">**IContactEndPoint** インターフェイスとそのメンバーの詳細については、「[UCCollaborationLib.IContactEndpoint](https://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec71-501">For more information about the **IContactEndPoint** interface and its members, see [UCCollaborationLib.IContactEndpoint](https://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span></span> 
  
<span data-ttu-id="fec71-502">**表 11. IContactEndPoint インターフェイスの実装**</span><span class="sxs-lookup"><span data-stu-id="fec71-502">**Table 11. Implementation of the IContactEndPoint interface**</span></span>

|<span data-ttu-id="fec71-503">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="fec71-503">**Member**</span></span>|<span data-ttu-id="fec71-504">**説明**</span><span class="sxs-lookup"><span data-stu-id="fec71-504">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fec71-505">**DisplayName** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-505">**DisplayName** property</span></span>  <br/> |<span data-ttu-id="fec71-506">表示文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-506">Gets the display string.</span></span>  <br/> |
|<span data-ttu-id="fec71-507">**Type** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-507">**Type** property</span></span>  <br/> |<span data-ttu-id="fec71-508">連絡先のエンドポイントの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-508">Gets the contact endpoint type</span></span>  <br/> |
|<span data-ttu-id="fec71-509">**Uri** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-509">**Uri** property</span></span>  <br/> |<span data-ttu-id="fec71-510">連絡先の URI を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-510">Gets the contact URI.</span></span>  <br/> |
   
### <a name="ilocalestring-interface"></a><span data-ttu-id="fec71-511">ILocaleString インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fec71-511">ILocaleString interface</span></span>
<span data-ttu-id="fec71-512"><a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a></span><span class="sxs-lookup"><span data-stu-id="fec71-512"></span></span>

<span data-ttu-id="fec71-p157">**ILocaleString** は、ローカライズされた文字列とローカリゼーションのロケール ID の両方を含む、ローカライズされた文字列構造です。 **ILocaleString** インターフェイスを使用して、連絡先カードのカスタム ステータスの文字列を書式設定します。</span><span class="sxs-lookup"><span data-stu-id="fec71-p157">The **ILocaleString** is a localized string structure that contains both a localized string and the locale ID of the localization. The **ILocaleString** interface is used to format the custom status string on the contact card.</span></span> 
  
<span data-ttu-id="fec71-515">表 12 は、 **ILocaleString** から継承するクラスに実装されている必要のあるメンバーを示しています。</span><span class="sxs-lookup"><span data-stu-id="fec71-515">Table 12 shows the members that must be implemented in the classes that inherit from **ILocaleString**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fec71-516">表に記載されていない **ILocaleString** インターフェイスのメンバーは、存在している必要がありますが、実装されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fec71-516">Any member of the **ILocaleString** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="fec71-517">存在していても実装されていないメンバーは、**NotImplementedException** または **E_NOTIMPL** エラーをスローすることがあります。</span><span class="sxs-lookup"><span data-stu-id="fec71-517">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="fec71-518">**ILocalString** インターフェイスとそのメンバーの詳細については、「[UCCollaborationLib.ILocaleString](https://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec71-518">For more information about the **ILocalString** interface and its members, see [UCCollaborationLib.ILocaleString](https://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span></span> 
  
<span data-ttu-id="fec71-519">**表 12. ILocaleString インターフェイスの実装**</span><span class="sxs-lookup"><span data-stu-id="fec71-519">**Table 12. Implementation of the ILocaleString interface**</span></span>

|<span data-ttu-id="fec71-520">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="fec71-520">**Member**</span></span>|<span data-ttu-id="fec71-521">**説明**</span><span class="sxs-lookup"><span data-stu-id="fec71-521">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fec71-522">**LocaleId** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-522">**LocaleId** property</span></span>  <br/> |<span data-ttu-id="fec71-523">ロケール ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-523">Gets the locale ID.</span></span>  <br/> |
|<span data-ttu-id="fec71-524">**Value** プロパティ</span><span class="sxs-lookup"><span data-stu-id="fec71-524">**Value** property</span></span>  <br/> |<span data-ttu-id="fec71-525">文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="fec71-525">Gets the string.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fec71-526">関連項目</span><span class="sxs-lookup"><span data-stu-id="fec71-526">See also</span></span>

- <span data-ttu-id="fec71-527">[UCCollaborationLib](https://msdn.microsoft.com/library/UCCollaborationLib) 名前空間</span><span class="sxs-lookup"><span data-stu-id="fec71-527">[UCCollaborationLib](https://msdn.microsoft.com/library/UCCollaborationLib) namespace</span></span> 
    

