---
title: 'HelloData: 単純な ADO アプリケーション'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 359816f828191a8643941a21ac520ba7b3231e6b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998204"
---
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="18d4c-102">HelloData: 単純な ADO アプリケーション</span><span class="sxs-lookup"><span data-stu-id="18d4c-102">HelloData: A simple ADO application</span></span>

<span data-ttu-id="18d4c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="18d4c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18d4c-p101">ADO ライブラリ検索の例として、"HelloData" という単純な ADO アプリケーションを取り上げます。HelloData では、4 つの主な ADO 操作 (データの取得、検査、編集、および更新) のそれぞれを行います。ADO の基本事項に焦点を当て、コードが複雑になりすぎるのを防ぐために、この例ではエラー処理を最小限に押さえています。</span><span class="sxs-lookup"><span data-stu-id="18d4c-p101">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData." HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data). In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="18d4c-107">アプリケーションのクエリには、Microsoft SQL Server 2000 に搭載されている Northwind サンプル データベースを使用しています。</span><span class="sxs-lookup"><span data-stu-id="18d4c-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="18d4c-108">**HelloData を実行するには**</span><span class="sxs-lookup"><span data-stu-id="18d4c-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="18d4c-109">ADO 2.5 ライブラリを参照する Visual Basic の標準的な実行可能ファイルのプロジェクトを新規作成します。</span><span class="sxs-lookup"><span data-stu-id="18d4c-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="18d4c-110">フォームの最上部にコマンド ボタンを 4 つ作成し、 **Name** および **Caption** プロパティを以下の表の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="18d4c-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="18d4c-111">ボタンの下には、 **Microsoft データ グリッド コントロール**(Msdatgrd.ocx) を追加します。</span><span class="sxs-lookup"><span data-stu-id="18d4c-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="18d4c-112">Msdatgrd.ocx ファイルは Visual Basic に付属して、ある、 \\windows\\system32 または\\winnt\\system32 ディレクトリ。</span><span class="sxs-lookup"><span data-stu-id="18d4c-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="18d4c-113">Visual Basic の [ツールボックス] ウィンドウには、DataGrid コントロールを追加するには、**プロジェクト**] メニューの [**コンポーネント]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="18d4c-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="18d4c-114">チェック ボックスを横に"Microsoft データ グリッド コントロール 6.0 (SP3) (ole DB)"[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18d4c-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="18d4c-115">コントロールをプロジェクトに追加するに DataGrid コントロールをツールボックスから Visual Basic フォームにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="18d4c-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="18d4c-p103">グリッドの下のフォームに **TextBox** を作成し、プロパティを以下の表の値に設定します。作業が終了すると、フォームは次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="18d4c-p103">Create a **TextBox** on the form below the grid and set its properties as shown in the table. The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="18d4c-118">最後に、 [HelloData のコード](hellodata-code.md)に記載されているコードをコピーし、フォームのコード エディター ウィンドウに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="18d4c-118">Finally, copy the code listed in [HelloData Code](hellodata-code.md) and paste it into the code editor window of the form.</span></span> <span data-ttu-id="18d4c-119">**F5** キーを押してコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="18d4c-119">Press **F5** to run the code.</span></span>

> [!NOTE]
> <span data-ttu-id="18d4c-p105">[!メモ] 次の例およびこのガイドでは、サーバーでの認証用ユーザー ID は "MyId"、パスワードは "123aBc" を使用します。これらの値は、お使いになるサーバーに合わせて有効なログオン認証に置き換えてください。また、"MyServer" も使用するサーバー名に置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="18d4c-p105">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server. You should substitute these values with valid logon credentials for your server. Also, substitute the "MyServer" value with the name of your server.</span></span>

<span data-ttu-id="18d4c-123">コードの詳細については、 [HelloData の詳細](hellodata-details.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18d4c-123">For a detailed description of the code, see [HelloData Details](hellodata-details.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18d4c-124">コントロールの種類</span><span class="sxs-lookup"><span data-stu-id="18d4c-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="18d4c-125">プロパティ</span><span class="sxs-lookup"><span data-stu-id="18d4c-125">Property</span></span></p></th>
<th><p><span data-ttu-id="18d4c-126">値</span><span class="sxs-lookup"><span data-stu-id="18d4c-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18d4c-127">Form</span><span class="sxs-lookup"><span data-stu-id="18d4c-127">Form</span></span></p></td>
<td><p><span data-ttu-id="18d4c-128">Name</span><span class="sxs-lookup"><span data-stu-id="18d4c-128">Name</span></span></p></td>
<td><p><span data-ttu-id="18d4c-129">Form1</span><span class="sxs-lookup"><span data-stu-id="18d4c-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="18d4c-130">Height</span><span class="sxs-lookup"><span data-stu-id="18d4c-130">Height</span></span></p></td>
<td><p><span data-ttu-id="18d4c-131">6500</span><span class="sxs-lookup"><span data-stu-id="18d4c-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="18d4c-132">Width</span><span class="sxs-lookup"><span data-stu-id="18d4c-132">Width</span></span></p></td>
<td><p><span data-ttu-id="18d4c-133">6500</span><span class="sxs-lookup"><span data-stu-id="18d4c-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18d4c-134">MS DataGrid</span><span class="sxs-lookup"><span data-stu-id="18d4c-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="18d4c-135">Name</span><span class="sxs-lookup"><span data-stu-id="18d4c-135">Name</span></span></p></td>
<td><p><span data-ttu-id="18d4c-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="18d4c-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18d4c-137">テキスト ボックス</span><span class="sxs-lookup"><span data-stu-id="18d4c-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="18d4c-138">Name</span><span class="sxs-lookup"><span data-stu-id="18d4c-138">Name</span></span></p></td>
<td><p><span data-ttu-id="18d4c-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="18d4c-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="18d4c-140">Multiline</span><span class="sxs-lookup"><span data-stu-id="18d4c-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="18d4c-141">true</span><span class="sxs-lookup"><span data-stu-id="18d4c-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18d4c-142">Command Button</span><span class="sxs-lookup"><span data-stu-id="18d4c-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="18d4c-143">Name</span><span class="sxs-lookup"><span data-stu-id="18d4c-143">Name</span></span></p></td>
<td><p><span data-ttu-id="18d4c-144">cmdGetData</span><span class="sxs-lookup"><span data-stu-id="18d4c-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="18d4c-145">Caption</span><span class="sxs-lookup"><span data-stu-id="18d4c-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="18d4c-146">Get Data</span><span class="sxs-lookup"><span data-stu-id="18d4c-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18d4c-147">Command Button</span><span class="sxs-lookup"><span data-stu-id="18d4c-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="18d4c-148">Name</span><span class="sxs-lookup"><span data-stu-id="18d4c-148">Name</span></span></p></td>
<td><p><span data-ttu-id="18d4c-149">cmdExamineData</span><span class="sxs-lookup"><span data-stu-id="18d4c-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="18d4c-150">Caption</span><span class="sxs-lookup"><span data-stu-id="18d4c-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="18d4c-151">Examine Data</span><span class="sxs-lookup"><span data-stu-id="18d4c-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18d4c-152">Command Button</span><span class="sxs-lookup"><span data-stu-id="18d4c-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="18d4c-153">Name</span><span class="sxs-lookup"><span data-stu-id="18d4c-153">Name</span></span></p></td>
<td><p><span data-ttu-id="18d4c-154">cmdEditData</span><span class="sxs-lookup"><span data-stu-id="18d4c-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="18d4c-155">Caption</span><span class="sxs-lookup"><span data-stu-id="18d4c-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="18d4c-156">Edit Data</span><span class="sxs-lookup"><span data-stu-id="18d4c-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18d4c-157">Command Button</span><span class="sxs-lookup"><span data-stu-id="18d4c-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="18d4c-158">Name</span><span class="sxs-lookup"><span data-stu-id="18d4c-158">Name</span></span></p></td>
<td><p><span data-ttu-id="18d4c-159">cmdUpdateData</span><span class="sxs-lookup"><span data-stu-id="18d4c-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="18d4c-160">Caption</span><span class="sxs-lookup"><span data-stu-id="18d4c-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="18d4c-161">Update Data</span><span class="sxs-lookup"><span data-stu-id="18d4c-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>



