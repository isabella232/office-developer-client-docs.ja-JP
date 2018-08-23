---
title: COM アドインを作成し、InfoPath にカスタム機能を追加する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007 では、com アドインを作成する InfoPath 2007 では、独自の機能では、COM アドインが [InfoPath 2007] を追加します。
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath には、ユーザー エクスペリエンスの編集フォームを拡張するための COM アドインがサポートされています。 COM アドインが最初に追加した InfoPath では、他の Office アプリケーションなど、Microsoft Office Word と Microsoft Office Excel サポートされている COM アドインが Office 2000 以降をサポートします。
ms.openlocfilehash: 4c70dfb71cf7b15a0978b4567ffac02a8ba524c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799013"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a><span data-ttu-id="9188d-105">COM アドインを作成し、InfoPath にカスタム機能を追加する</span><span class="sxs-lookup"><span data-stu-id="9188d-105">Create a COM Add-in to Add Custom Features to InfoPath</span></span>

<span data-ttu-id="9188d-106">Microsoft InfoPath には、ユーザー エクスペリエンスの編集フォームを拡張するための COM アドインがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="9188d-106">Microsoft InfoPath supports COM Add-ins for extending the form editing user experience.</span></span> <span data-ttu-id="9188d-107">COM アドインが最初に追加した InfoPath では、他の Office アプリケーションなど、Microsoft Office Word と Microsoft Office Excel サポートされている COM アドインが Office 2000 以降をサポートします。</span><span class="sxs-lookup"><span data-stu-id="9188d-107">Although support for COM Add-ins was first added in InfoPath, other Office applications such as Microsoft Office Word and Microsoft Office Excel have supported COM add-ins since Office 2000.</span></span>
  
<span data-ttu-id="9188d-p103">InfoPath での COM アドイン サポートはフォーム編集環境用に使用できます。COM アドインを使用してもフォーム デザイン環境は拡張できません。</span><span class="sxs-lookup"><span data-stu-id="9188d-p103">COM Add-in support in InfoPath is available for the form editing environment. The form design environment cannot be extended by using COM Add-ins.</span></span>
  
## <a name="the-idtextensibility2-interface"></a><span data-ttu-id="9188d-110">IDTExtensibility2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9188d-110">The IDTExtensibility2 Interface</span></span>

<span data-ttu-id="9188d-p104">InfoPath 編集環境は、**IDTExtensibility2** インターフェイスをサポートしますが、その実装は COM アドイン開発者が行う必要があります。**IDTExtensibility2** はデュアル インターフェイス オブジェクトで、編集環境内でイベントとして動作する 5 つのメソッドを提供します。これらのメソッドにより、次の表に記載されている環境のスタートアップおよびシャットダウン条件に COM アドインが対応できます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p104">The InfoPath editing environment provides support for the **IDTExtensibility2** interface, which must be implemented by developers of COM Add-ins. **IDTExtensibility2** is a dual-interface object that provides five methods which act as events within the editing environment. These methods allow the COM add-in to respond to environment startup and shutdown conditions, listed in the following table.</span></span> 
  
|<span data-ttu-id="9188d-113">**インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="9188d-113">**Interface**</span></span>|<span data-ttu-id="9188d-114">**説明**</span><span class="sxs-lookup"><span data-stu-id="9188d-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9188d-115">**OnAddInsUpdate (バリアントとして ByVal custom())**</span><span class="sxs-lookup"><span data-stu-id="9188d-115">**OnAddInsUpdate (ByVal custom() As Variant)**</span></span> <br/> |<span data-ttu-id="9188d-116">環境内でのアドインの読み込み時、またはアンロード時に発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-116">Occurs when an add-in is loaded or unloaded in the environment.</span></span>  <br/> |
|<span data-ttu-id="9188d-117">**OnBeginShutdown (バリアントとして ByVal custom())**</span><span class="sxs-lookup"><span data-stu-id="9188d-117">**OnBeginShutdown (ByVal custom() As Variant)**</span></span> <br/> |<span data-ttu-id="9188d-118">環境のシャット ダウン中に発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-118">Occurs when the environment is being shut down.</span></span>  <br/> |
|<span data-ttu-id="9188d-119">**OnConnection (ByVal アプリケーションのオブジェクトとして、ByVal ConnectMode として ext_ConnectMode、ByVal AddInInst のオブジェクトとして、ByVal custom() バリアントとして)**</span><span class="sxs-lookup"><span data-stu-id="9188d-119">**OnConnection(ByVal Application As Object, ByVal ConnectMode As ext_ConnectMode, ByVal AddInInst As Object, ByVal custom() As Variant)**</span></span> <br/> |<span data-ttu-id="9188d-120">アドインが環境に読み込まれると発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-120">Occurs when an add-in is loaded in the environment.</span></span>  <br/> |
|<span data-ttu-id="9188d-121">**OnDisconnection (ByVal の RemoveMode と ext_DisconnectMode、ByVal custom() のバリアントとして)**</span><span class="sxs-lookup"><span data-stu-id="9188d-121">**OnDisconnection (ByVal RemoveMode As ext_DisconnectMode, ByVal custom() As Variant)**</span></span> <br/> |<span data-ttu-id="9188d-122">アドインが環境からアンロードされると発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-122">Occurs when an add-in is unloaded from the environment.</span></span>  <br/> |
|<span data-ttu-id="9188d-123">**OnStartupComplete (バリアントとして ByVal custom())**</span><span class="sxs-lookup"><span data-stu-id="9188d-123">**OnStartupComplete (ByVal custom() As Variant)**</span></span> <br/> |<span data-ttu-id="9188d-124">環境の起動が完了すると発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-124">Occurs when the environment has completed starting.</span></span>  <br/> |
   
## <a name="registering-com-add-ins"></a><span data-ttu-id="9188d-125">COM アドインの登録</span><span class="sxs-lookup"><span data-stu-id="9188d-125">Registering COM Add-ins</span></span>

<span data-ttu-id="9188d-p105">InfoPath を含め、すべての Office アプリケーションはレジストリを使用して、COM アドイン コレクション内のアドインの一覧表示、接続状態の格納、ブートやデマンド読み込み情報の格納を行います。InfoPath COM アドインの場合、次のキーの下に、各アドインの名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p105">All Office applications, including InfoPath, use the registry to list add-ins in the COM Add-Ins collection, to store the connect state, and to store the boot or demand load information. For InfoPath COM Add-ins, the name of each add-in appears under the following key:</span></span>
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
<span data-ttu-id="9188d-128">クライアント コンピューターのすべてのユーザーが使用できる COM アドインがインストールされている場合は、HKLM レジストリ ハイブにレジストリ キーがあります。</span><span class="sxs-lookup"><span data-stu-id="9188d-128">For COM Add-ins installed for use by every user of the client computer, the registry key is located in the HKLM registry hive:</span></span>
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
<span data-ttu-id="9188d-129">レジストリ キー名はアドインの **ProgIdAttribute** に対応し、次の値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9188d-129">The registry key name corresponds to the **ProgIdAttribute** of the add-in, and contains the following values.</span></span> 
  
|<span data-ttu-id="9188d-130">**名前**</span><span class="sxs-lookup"><span data-stu-id="9188d-130">**Name**</span></span>|<span data-ttu-id="9188d-131">**型**</span><span class="sxs-lookup"><span data-stu-id="9188d-131">**Type**</span></span>|<span data-ttu-id="9188d-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="9188d-132">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9188d-133">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="9188d-133">**FriendlyName**</span></span> <br/> |<span data-ttu-id="9188d-134">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="9188d-134">**String**</span></span> <br/> |<span data-ttu-id="9188d-135">**[COM アドイン]** ダイアログ ボックスに表示され、**[セキュリティ センター]** の **[アドイン]** ページに 一覧表示される名前。</span><span class="sxs-lookup"><span data-stu-id="9188d-135">The name that is displayed in the **COM Add-ins** dialog box and listed in the **Add-ins** page of the **Trust Center**.</span></span>  <br/> |
|<span data-ttu-id="9188d-136">**説明**</span><span class="sxs-lookup"><span data-stu-id="9188d-136">**Description**</span></span> <br/> |<span data-ttu-id="9188d-137">**String**</span><span class="sxs-lookup"><span data-stu-id="9188d-137">**String**</span></span> <br/> |<span data-ttu-id="9188d-138">**[セキュリティ センター]** でアドインが選択されている場合に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="9188d-138">The string that is displayed when the add-in is selected in the **Trust Center**.</span></span>  <br/> |
|<span data-ttu-id="9188d-139">**LoadBehavior**</span><span class="sxs-lookup"><span data-stu-id="9188d-139">**LoadBehavior**</span></span> <br/> |<span data-ttu-id="9188d-140">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="9188d-140">**DWORD**</span></span> <br/> |<span data-ttu-id="9188d-p106">COM アドインの読み込み方法を指定します。値は 0、1、2、8、および 16 を組み合わせたものです。詳細については、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9188d-p106">Specifies the way the COM Add-in is loaded. The value can be a combination of 0, 1, 2, 8, and 16. See the table below for more information.</span></span>  <br/> |
   
<span data-ttu-id="9188d-p107">**LoadBehavior** の **DWORD** 値には、編集環境での COM アドインの読み込み方法を示す値が含まれている必要があります。次の表の値、または表中の値の組み合わせを指定できます。たとえば、Visual Studio 2005 で作成される COM アドインには、アプリケーションの起動時に読み込まれた "3" の **LoadBehavior** が含まれ、接続されます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p107">The **DWORD** value for **LoadBehavior** should contain a value describing how the COM Add-in loads in the editing environment. The value can be from the table below, or a combination of values from the table. For example, a COM Add-in created in Visual Studio 2005 will have a **LoadBehavior** of "3" loaded at application startup and be connected.</span></span> 
  
|<span data-ttu-id="9188d-147">**値**</span><span class="sxs-lookup"><span data-stu-id="9188d-147">**Value**</span></span>|<span data-ttu-id="9188d-148">**説明**</span><span class="sxs-lookup"><span data-stu-id="9188d-148">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9188d-149">0</span><span class="sxs-lookup"><span data-stu-id="9188d-149">0</span></span>  <br/> |<span data-ttu-id="9188d-p108">切断済み。アドインを **[COM アドイン]** のダイアログ ボックスに非アクティブとして表示します。</span><span class="sxs-lookup"><span data-stu-id="9188d-p108">Disconnected. The add-in shows as Inactive in the **COM Add-in** dialog box.  </span></span><br/> |
|<span data-ttu-id="9188d-152">1</span><span class="sxs-lookup"><span data-stu-id="9188d-152">1</span></span>  <br/> |<span data-ttu-id="9188d-p109">接続済み。アドインを **[COM アドイン]** のダイアログ ボックスに アクティブとして表示します。</span><span class="sxs-lookup"><span data-stu-id="9188d-p109">Connected. The add-in shows as Active in the **COM Add-in** dialog box.  </span></span><br/> |
|<span data-ttu-id="9188d-155">2</span><span class="sxs-lookup"><span data-stu-id="9188d-155">2</span></span>  <br/> |<span data-ttu-id="9188d-p110">起動時に読み込む。アドインは、ホスト アプリケーションの起動時に読み込まれ、接続されます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p110">Load at Startup. The add-in is loaded and connected when the host application starts.</span></span>  <br/> |
|<span data-ttu-id="9188d-158">8</span><span class="sxs-lookup"><span data-stu-id="9188d-158">8</span></span>  <br/> |<span data-ttu-id="9188d-p111">必要時に読み込む。アドインは、ユーザーがアドインの機能を使用するボタンをクリックした時など、ホスト アプリケーションが要求した場合に読み込まれ、接続されます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p111">Load on Demand. The add-in is loaded and connected when the host application requires it, for example when a user clicks a button that uses functionality in the add-in.</span></span>  <br/> |
|<span data-ttu-id="9188d-161">16</span><span class="sxs-lookup"><span data-stu-id="9188d-161">16</span></span>  <br/> |<span data-ttu-id="9188d-p112">初回に接続する。アドインを登録した後にユーザーがホスト アプリケーションを実行した時に、アドインは初めて読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p112">Connect first time. The add-in will be loaded and connected the first time the user runs the host application after registering the add-in.</span></span>  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a><span data-ttu-id="9188d-164">Visual Studio 2005 または Visual Studio 2008 を利用したマネージ COM アドインの作成</span><span class="sxs-lookup"><span data-stu-id="9188d-164">Creating a Managed COM Add-in with Visual Studio 2005 or Visual Studio 2008</span></span>

<span data-ttu-id="9188d-165">Microsoft Visual Studio 2005 または Visual Studio 2008 を使用してマネージ COM アドインを作成するには、次の手順で共有アドイン プロジェクトを作成します。 </span><span class="sxs-lookup"><span data-stu-id="9188d-165">To create a managed COM add-in using Microsoft Visual Studio 2005 or Visual Studio 2008, create a Shared Add-In project as follows:</span></span> 
  
1. <span data-ttu-id="9188d-166">Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="9188d-166">Start Visual Studio.</span></span>
    
2. <span data-ttu-id="9188d-167">**[ファイル]** メニューの **[新しいプロジェクト]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-167">On the **File** menu, click **New Project**.</span></span>
    
3. <span data-ttu-id="9188d-168">**[新しいプロジェクト]** ダイアログ ボックスの **[プロジェクトの種類]** ウィンドウで、**[その他のプロジェクトの種類]** フォルダーをクリックし、次に **[拡張]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-168">In the **Project Types** pane of the **New Project** dialog box, click the **Other Projects Types** folder, and then click **Extensibility**.</span></span>
    
4. <span data-ttu-id="9188d-169">**[テンプレート]** ウィンドウで、**[共有アドイン]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-169">In the **Templates** pane, click **Shared Add-In**.</span></span>
    
5. <span data-ttu-id="9188d-170">**[名前]** ボックスにプロジェクト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="9188d-170">In the **Name** box, type a name for the project.</span></span> 
    
6. <span data-ttu-id="9188d-p113">**[場所]** ボックスにフォルダーのパスを入力するか、**[参照]** をクリックしてフォルダーのパスを選択し、**[OK]** をクリックします。**共有アドイン ウィザード**が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p113">In the **Location** box, type a folder path or click **Browse** and select a folder path, and then click **OK**. The **Shared Add-in Wizard** appears.</span></span> 
    
7. <span data-ttu-id="9188d-p114">**共有アドイン ウィザード**で **[次へ]** をクリックします。**[プログラミング言語の選択]** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p114">Click **Next** in the **Shared Add-in Wizard**. The **Select a Programming Language** page appears.</span></span> 
    
8. <span data-ttu-id="9188d-p115">**[Visual Basic を使用してアドインを作成]** をクリックし、**[次へ]** をクリックします。**[アプリケーション ホストの選択]** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p115">Click **Create an Add-in using Visual Basic**, then click **Next**. The **Select An Application Host** page appears.</span></span> 
    
9. <span data-ttu-id="9188d-p116">**Microsoft InfoPath** 以外の各アプリケーションの横にあるボックスのチェックを外して、**[次へ]** をクリックする。**[名前と説明の入力]** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p116">Uncheck the boxes next to each application except **Microsoft InfoPath**, and then click **Next**. The **Enter a Name and Description** page appears.</span></span> 
    
10. <span data-ttu-id="9188d-179">**[アドインの名前]** ボックスに、COM アドインの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="9188d-179">In the **What is the name of your Add-In** box, type the name of your COM Add-in.</span></span> 
    
11. <span data-ttu-id="9188d-p117">**[アドインの説明]** ボックスには、COM アドインの説明を入力し、**[次へ]** をクリックします。**[アドイン オプションの選択]** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p117">In the **What is the description of your Add-In** box, type the description for your COM Add-in, and click **Next**. The **Choose Add-In Options** page appears.</span></span> 
    
12. <span data-ttu-id="9188d-182">**[ホスト アプリケーションが読み込む時にマイ アドインを読み込む]** ボックスと **[マイ アドインをインストールするユーザーだけでなく、インストール先のコンピューターの全ユーザーが利用する]** ボックスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-182">Check the **I would like my Add-in to load when the host application loads** and **My Add-in should be available to all users of the computer it was installed on, not just the person who installs it** boxes.</span></span> 
    
13. <span data-ttu-id="9188d-183">**[次ヘ]** をクリックして **[概要]** ページを確認し、**[完了]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-183">Click **Next** to review the **Summary** page, then click **Finish**.</span></span>
    
<span data-ttu-id="9188d-p118">Visual Studio によるプロジェクトの作成後に、2 つのプロジェクトが [ ソリューション エクスプローラー ] ウィンドウに表示されます。最初のプロジェクトは、COM アドイン用のプロジェクトです。2 番目のプロジェクトは、COM アドインを展開するためのセットアップ プロジェクトです。**共有アドイン ウィザード**は **Microsoft Office 14.0 オブジェクト ライブラリ**への参照を挿入するだけであるため、次の手順で InfoPath オブジェクト ライブラリへの参照を挿入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9188d-p118">After the project is created by Visual Studio, you will see two projects in the Solution Explorer window. The first project is the project for the COM Add-in; the second project is a setup project for deploying the COM Add-in. The **Shared Add-in Wizard** only inserts a reference to the **Microsoft Office 14.0 Object Library**, so it is necessary to insert a reference to the InfoPath object library using the following steps:</span></span>
  
1. <span data-ttu-id="9188d-p119">**[マイ プロジェクト]** をダブルクリックして、アドイン プロジェクトのプロパティを表示します。**[参照]** タブをクリックして、プロジェクトに自動的に追加された参照を表示します。</span><span class="sxs-lookup"><span data-stu-id="9188d-p119">Double-click **My Project** to display the add-in project properties. Click the **References** tab to display the references automatically added to the project.</span></span> 
    
2. <span data-ttu-id="9188d-189">**[追加]** ボタンをクリックして、**[参照の追加]** ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="9188d-189">Click the **Add** button to display the **Add Reference** dialog box.</span></span> 
    
3. <span data-ttu-id="9188d-190">**[COM]** タブの **[Microsoft.InfoPath 2.0 タイプ ライブラリ]** をダブルクリックし、**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-190">On the **COM** tab, double-click **Microsoft.InfoPath 2.0 Type Library**, and click **OK**.</span></span>
    
4. <span data-ttu-id="9188d-p120">**[Microsoft InfoPath 3.0 タイプ ライブラリ]** への参照を追加すると、削除する必要のある 3 つのアセンブリ (**ADODB**、**MSHTML**、**MSXML2**) への参照も追加されます。**References** の **Solution Explorer** で、これらの参照を右クリックし、次に **[削除]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-p120">Adding a reference to the **Microsoft InfoPath 3.0 Type Library** also adds references to three assemblies that must be removed: **ADODB**, **MSHTML**, and **MSXML2**. In **Solution Explorer** under **References**, right-click each of these references, and then click **Remove**.</span></span>
    
## <a name="viewing-the-registry-settings"></a><span data-ttu-id="9188d-193">レジストリ設定の表示</span><span class="sxs-lookup"><span data-stu-id="9188d-193">Viewing the Registry Settings</span></span>

<span data-ttu-id="9188d-194">COM アドインのインストール時に作成されるレジストリ設定を表示するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9188d-194">To view the registry settings that will be created when the COM Add-in is installed, follow these steps:</span></span>
  
1. <span data-ttu-id="9188d-195">**[ソリューション エクスプローラー]** にある設定プロジェクトのルート ノードを右クリックし、**[表示]**、**[エディター]**、**[レジストリ]** を順番にクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-195">Right-click the root node of the setup project in the **Solution Explorer**, click **View**, then **Editor**, then click **Registry**.</span></span>
    
2. <span data-ttu-id="9188d-196">左側のウィンドウで、プラス記号をクリックして **[HKEY_LOCAL_MACHINE]**、**[ソフトウェア]**、**[Microsoft]**、**[InfoPath]**、**[アドイン]** を順番にクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-196">In the left-hand pane, click the plus to expand **HKEY_LOCAL_MACHINE**, **Software**, **Microsoft**, **InfoPath**, then **AddIns**.</span></span>
    
3. <span data-ttu-id="9188d-197">共有アドイン プロジェクトの **ProgID** に対応する名前をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-197">Click the name corresponding to your shared add-in project's **ProgID**.</span></span>
    
<span data-ttu-id="9188d-198">これらのプロパティのいずれかを変更するには、プロパティを右クリックし、**[プロパティ ウィンドウ]** をクリックして、**プロパティ ウィンドウ**の **[値]** ボックスを変更します。</span><span class="sxs-lookup"><span data-stu-id="9188d-198">To change any of these properties, right-click the property, click **Properties Window**, and change the **Value** box in the **Properties Window**.</span></span>
  
## <a name="compiling-and-distributing-the-shared-add-in"></a><span data-ttu-id="9188d-199">共有アドインのコンパイルと配布</span><span class="sxs-lookup"><span data-stu-id="9188d-199">Compiling and Distributing the Shared Add-In</span></span>

<span data-ttu-id="9188d-p121">共有アドイン プロジェクトが開発されたコンピューターでテストするためにマネージ COM アドインをコンパイルするには、ソリューション エクスプローラーで共有アドイン プロジェクトのルート ノードを右クリックし、[ビルド] をクリックします。エラーが出ずにプロジェクトがビルドすると、InfoPath 編集環境を起動し、マネージ COM アドインの使用を開始できます。実行中の InfoPath のインスタンスがある場合は、プロジェクトをビルドする前に閉じてください。COM アドインが登録されていることを確認するために、[COM アドイン] ダイアログ ボックスを開く必要がある場合があります。[COM アドイン] ダイアログ ボックスは、次の手順で開きます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p121">To compile the managed COM Add-in for testing on the computer on which the Shared Add-In project was developed, right-click the root node of the Shared Add-In project in the Solution Explorer and click Build. If the project builds with no errors, you can start the InfoPath editing environment and begin using the managed COM Add-in. If you have an instance of InfoPath running, close it before building the project. It may also be necessary to open the COM Add-ins dialog box to verify that the COM Add-in is registered. To open the COM Add-ins dialog box, follow these steps:</span></span>
  
1. <span data-ttu-id="9188d-p122">InfoPath 編集環境を開く最も簡単な方法は、既存のフォーム テンプレートを開きます。すると、そのフォーム テンプレートに基づいて新しいフォームが作成されます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p122">Open the InfoPath editing environment. The easiest way to do this is to open an existing form template, which will create a new form based on that form template.</span></span>
    
2. <span data-ttu-id="9188d-207">**[ツール]** メニューの **[セキュリティ センター]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-207">Click **Trust Center** on the **Tools** menu.</span></span> 
    
3. <span data-ttu-id="9188d-208">左側の **[アドイン]** カテゴリをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-208">Click the **Add-ins** category on the left.</span></span> 
    
4. <span data-ttu-id="9188d-209">**[セキュリティ センター]** ダイアログ ボックスの下部近くにある **[管理]** セクションで、リストから **[COM アドイン]** を選択し、**[移動]** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9188d-209">In the **Manage** section near the bottom of the **Trust Center** dialog box, select **COM Add-ins** from the list and click the **Go** button.</span></span> 
    
5. <span data-ttu-id="9188d-p123">**[COM アドイン]** ダイアログ ボックスに、最近ビルドしたアドインの名前が表示され、その横にチェック ボックスがあります。横にチェック ボックスがない場合は、エラーにより COM アドインの読み込みが失敗しています。この失敗についてはダイアログ ボックスの **[読み込み時の動作]** セクションの一覧に含められます。</span><span class="sxs-lookup"><span data-stu-id="9188d-p123">In the **COM Add-ins** dialog box, you will see the name of your recently-built add-in and there should be a check box next to it. If there is no check box next to it, the COM Add-in failed to load due to an error, which will be listed in the **Load Behavior** section of the dialog box.</span></span> 
    
<span data-ttu-id="9188d-p124">共有アドイン プロジェクトが開発されたコンピューター以外のコンピューターで使用するマネージ COM アドインをコンパイルするには、次の追加手順に従ってコードをセキュリティで保護してください。他のコンピューターで使用する共有アドイン プロジェクトをセキュリティで保護する方法については、次の 3 つの資料を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9188d-p124">To compile the managed COM add-in for use on a computer other than the computer on which the Shared Add-In project was developed, you must follow additional steps to secure your code. For information on securing Shared Add-In projects for use on other computers, see the following three articles:</span></span>
  
- [<span data-ttu-id="9188d-214">マネージ COM アドインが Office XP での展開</span><span class="sxs-lookup"><span data-stu-id="9188d-214">Deployment of Managed COM Add-Ins in Office XP</span></span>](http://go.microsoft.com/fwlink/?LinkID=73473)
  
- [<span data-ttu-id="9188d-215">COM アドイン Shim ソリューションを使用してマネージ COM アドインで Office XP を展開するには</span><span class="sxs-lookup"><span data-stu-id="9188d-215">Using the COM Add-in Shim Solution to Deploy Managed COM Add-ins in Office XP</span></span>](http://go.microsoft.com/fwlink/?LinkID=73474)
  
- [<span data-ttu-id="9188d-216">COM シム ウィザードを使用して Office 拡張機能を分離します。</span><span class="sxs-lookup"><span data-stu-id="9188d-216">Isolating Office Extensions with the COM Shim Wizard</span></span>](http://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> <span data-ttu-id="9188d-217">COM アドインを分離していない場合、メモリ リークが発生し、アプリケーションが不安定になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9188d-217">Not isolating the COM Add-in may cause memory leaks and application instability.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9188d-p125">.NET Framework または設定プロジェクトが要求するその他の必要なアセンブリがターゲット コンピューターにインストールされていないと、.msi ファイルが正しくインストールされない可能性があります。また、.msi ファイルを配布するだけで .msi ファイルをインストールすることはできません。Visual Studio によって生成された元の .msi ファイルと同じフォルダー内の他のサポート ファイルも配布する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9188d-p125">If the .NET Framework or other required assemblies from the setup project are not already installed on target computers, the .msi file may not install properly. Also, you cannot distribute the .msi file and then attempt to install the .msi file. You must also distribute the other support files in the same folder as the original .msi file generated by Visual Studio.</span></span> 
  
## <a name="coding-in-the-com-add-in"></a><span data-ttu-id="9188d-221">COM アドインでのコーディング</span><span class="sxs-lookup"><span data-stu-id="9188d-221">Coding in the COM Add-in</span></span>

<span data-ttu-id="9188d-222">InfoPath のフォーム編集環境で発生したアプリケーション イベントは、COM アドインでキャプチャできます。</span><span class="sxs-lookup"><span data-stu-id="9188d-222">Application events that occur in the InfoPath form editing environment can be captured by a COM Add-in.</span></span> <span data-ttu-id="9188d-223">[ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx)オブジェクトの次のイベントは、ユーザー アクションに応答するのには COM アドインによって使用できます。</span><span class="sxs-lookup"><span data-stu-id="9188d-223">The following events of the [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) object can be used by the COM Add-in to respond to user actions:</span></span> 
  
|<span data-ttu-id="9188d-224">**イベント**</span><span class="sxs-lookup"><span data-stu-id="9188d-224">**Event**</span></span>|<span data-ttu-id="9188d-225">**説明**</span><span class="sxs-lookup"><span data-stu-id="9188d-225">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9188d-226">[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx)イベント</span><span class="sxs-lookup"><span data-stu-id="9188d-226">[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx) Event</span></span>  <br/> |<span data-ttu-id="9188d-227">新しいフォームが作成されるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-227">Occurs when a new form is created.</span></span>  <br/> |
|<span data-ttu-id="9188d-228">[終了](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx)イベント</span><span class="sxs-lookup"><span data-stu-id="9188d-228">[Quit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx) Event</span></span>  <br/> |<span data-ttu-id="9188d-229">ユーザーが InfoPath を終了するときに発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-229">Occurs when the user quits InfoPath.</span></span>  <br/> |
|<span data-ttu-id="9188d-230">[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx)イベント</span><span class="sxs-lookup"><span data-stu-id="9188d-230">[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx) Event</span></span>  <br/> |<span data-ttu-id="9188d-231">任意の文書ウィンドウがアクティブになるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-231">Occurs when any document window is activated.</span></span>  <br/> |
|<span data-ttu-id="9188d-232">[ただし](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx)イベント</span><span class="sxs-lookup"><span data-stu-id="9188d-232">[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx) Event</span></span>  <br/> |<span data-ttu-id="9188d-233">任意の文書ウィンドウが非アクティブになったときに発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-233">Occurs when any document window is deactivated.</span></span>  <br/> |
|<span data-ttu-id="9188d-234">[WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx)イベント</span><span class="sxs-lookup"><span data-stu-id="9188d-234">[WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx) Event</span></span>  <br/> |<span data-ttu-id="9188d-235">ドキュメント ウィンドウのサイズが変更されるとき、または移動されるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-235">Occurs when any document window is resized or moved.</span></span>  <br/> |
|<span data-ttu-id="9188d-236">[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx)イベント</span><span class="sxs-lookup"><span data-stu-id="9188d-236">[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx) Event</span></span>  <br/> |<span data-ttu-id="9188d-237">開いている文書が閉じる直前に発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-237">Occurs immediately before any open document closes.</span></span>  <br/> |
|<span data-ttu-id="9188d-238">[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx)イベント</span><span class="sxs-lookup"><span data-stu-id="9188d-238">[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx) Event</span></span>  <br/> |<span data-ttu-id="9188d-239">開かれているドキュメントが印刷される直前に発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-239">Occurs immediately before any open document is printed.</span></span>  <br/> |
|<span data-ttu-id="9188d-240">[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx)イベント</span><span class="sxs-lookup"><span data-stu-id="9188d-240">[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx) Event</span></span>  <br/> |<span data-ttu-id="9188d-241">開かれているドキュメントが保存される直前に発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-241">Occurs immediately before any open document is saved.</span></span>  <br/> |
|<span data-ttu-id="9188d-242">[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx)イベント</span><span class="sxs-lookup"><span data-stu-id="9188d-242">[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx) Event</span></span>  <br/> |<span data-ttu-id="9188d-243">新しいフォームが作成されるとき、既存のフォームが開かれるとき、または別のフォームがアクティブになるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-243">Occurs when a new form is created, when an existing form is opened, or when another form is made the active form.</span></span>  <br/> |
|<span data-ttu-id="9188d-244">[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx)イベント</span><span class="sxs-lookup"><span data-stu-id="9188d-244">[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx) Event</span></span>  <br/> |<span data-ttu-id="9188d-245">文書が開いたときに発生します。</span><span class="sxs-lookup"><span data-stu-id="9188d-245">Occurs when a document is opened.</span></span>  <br/> |
   
<span data-ttu-id="9188d-246">COM アドインでこれらのイベントをキャプチャするには、**Connect** クラス内のクラス レベル変数を宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9188d-246">To capture these events in the COM Add-in, you must declare the following class-level variables in your **Connect** class:</span></span> 
  
```vb
InfoPathApplication = DirectCast( _
   application, Microsoft.Office.Interop.InfoPath._Application3)
InfoPathApplicationEvents = DirectCast( _
   InfoPathApplication.Events, _
   Microsoft.Office.Interop.InfoPath.ApplicationEvents)
```

```cs
InfoPathApplication =
   (Microsoft.Office.Interop.InfoPath._Application3)application;
InfoPathApplicationEvents =
   (Microsoft.Office.Interop.InfoPath.ApplicationEvents)
   InfoPathApplication.Events;
```

<span data-ttu-id="9188d-247">[_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx)オブジェクトをアドインで、**オブジェクト**が受信した汎用アプリケーションを最初の行にキャストします。</span><span class="sxs-lookup"><span data-stu-id="9188d-247">The first line casts the generic application **Object** received by the add-in to the [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) object.</span></span> <span data-ttu-id="9188d-248">2 行目は、 **_Application3**オブジェクト ( **InfoPathApplication**変数によって表されます) の[イベント](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx)のプロパティを[ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx)オブジェクトにキャストします。</span><span class="sxs-lookup"><span data-stu-id="9188d-248">The second line casts the [Events](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) property of the **_Application3** object (represented by the **InfoPathApplication** variable) to the [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) object.</span></span> 
  
<span data-ttu-id="9188d-p128">イベント ハンドラーを作成するには、Visual Studio のウィンドウの上部にある **[クラス名]** ドロップダウン ボックスから **InfoPathApplicationEvents** を選択し、次に Visual Studio ウィンドウの上部にある **[メソッド名]** ドロップダウン ボックスから処理したいイベントを選択します。たとえば、フォームを保存するタイミングをコントロールするには、**XDocumentBeforeSave** イベントを処理します。**[メソッド名]** ドロップダウンから **XDocumentBeforeSave** を選択すると、次の手順を自動的に挿入します。</span><span class="sxs-lookup"><span data-stu-id="9188d-p128">To create event handlers, select **InfoPathApplicationEvents** from the **Class Name** drop-down box at the top of the Visual Studio window, and then select the event you want to handle in the **Method Name** drop-down box at the top of the Visual Studio window. For example, if you need to control when a form is saved, you handle the **XDocumentBeforeSave** event. Selecting **XDocumentBeforeSave** from the **Method Name** drop-down automatically inserts the following procedure:</span></span> 
  
```vb
Private Sub InfoPathApplicationEvents_XDocumentBeforeSave( _
   ByVal pDocument As Microsoft.Office.Interop.InfoPath._XDocument, _
   ByRef pfCancel As Boolean) _
   Handles InfoPathApplicationEvents.XDocumentBeforeSave
End Sub
```

```cs
private void InfoPathApplicationEvents_XDocumentBeforeSave(
   Microsoft.Office.Interop.InfoPath._XDocument pDocument, ref bool pfCancel)
{
}

```

<span data-ttu-id="9188d-252">**ApplicationEvents** オブジェクトのいずれのイベントも、同じメソッドを使用する COM アドインで処理することができます。</span><span class="sxs-lookup"><span data-stu-id="9188d-252">Any of the events of the **ApplicationEvents** object can be handled by the COM Add-in using the same method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9188d-253">関連項目</span><span class="sxs-lookup"><span data-stu-id="9188d-253">See also</span></span>

- [<span data-ttu-id="9188d-254">Microsoft Office 2000 COM アドインを作成します。</span><span class="sxs-lookup"><span data-stu-id="9188d-254">Creating a Microsoft Office 2000 COM Add-in</span></span>](http://go.microsoft.com/fwlink/?LinkID=73468) 
- [<span data-ttu-id="9188d-255">マネージ COM アドインが Visual Studio .NET での Office を作成します。</span><span class="sxs-lookup"><span data-stu-id="9188d-255">Creating Office Managed COM Add-Ins with Visual Studio .NET</span></span>](http://go.microsoft.com/fwlink/?LinkID=73470)
- [<span data-ttu-id="9188d-256">IDTExtensibility2 のイベント プロシージャの使用</span><span class="sxs-lookup"><span data-stu-id="9188d-256">Working with the IDTExtensibility2 Event Procedures</span></span>](http://go.microsoft.com/fwlink/?LinkID=73471)
- [<span data-ttu-id="9188d-257">Office COM アドインを Visual Basic .NET でビルドします。</span><span class="sxs-lookup"><span data-stu-id="9188d-257">Build an Office COM Add-in With Visual Basic .NET</span></span>](http://go.microsoft.com/fwlink/?LinkID=73469)
- [<span data-ttu-id="9188d-258">Office COM アドインを Visual C# .NET を使用してビルドします。</span><span class="sxs-lookup"><span data-stu-id="9188d-258">Build an Office COM Add-in With Visual C# .NET</span></span>](http://go.microsoft.com/fwlink/?LinkID=73472)
- [<span data-ttu-id="9188d-259">Office システム SE の Visual Studio 2005年のツールを使用して、InfoPath 2007 のアドインを作成します。</span><span class="sxs-lookup"><span data-stu-id="9188d-259">Creating InfoPath 2007 Add-Ins by Using Visual Studio 2005 Tools for the Office System SE</span></span>](http://msdn.microsoft.com/en-us/library/bb968857%28office.12%29.aspx)

