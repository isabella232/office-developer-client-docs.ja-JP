---
title: QuitAccess マクロ アクション
TOCTitle: QuitAccess macro action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 793e6c2e57f50b5086780d8632952c45f3d4442d
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997986"
---
# <a name="quitaccess-macro-action"></a><span data-ttu-id="2a96b-102">QuitAccess マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="2a96b-102">QuitAccess macro action</span></span>

<span data-ttu-id="2a96b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2a96b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a96b-104">**QuitAccess**アクションを使用すると、Microsoft Access を終了します。</span><span class="sxs-lookup"><span data-stu-id="2a96b-104">You can use the **QuitAccess** action to exit Microsoft Access.</span></span> <span data-ttu-id="2a96b-105">**QuitAccess**アクションでは、Access の終了時にデータベース オブジェクトを保存するためのいくつかのオプションのいずれかの指定もできます。</span><span class="sxs-lookup"><span data-stu-id="2a96b-105">The **QuitAccess** action can also specify one of several options for saving database objects prior to exiting Access.</span></span>

> [!NOTE]
> <span data-ttu-id="2a96b-106">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="2a96b-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="2a96b-107">設定値</span><span class="sxs-lookup"><span data-stu-id="2a96b-107">Setting</span></span>

<span data-ttu-id="2a96b-108">**QuitAccess**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="2a96b-108">The **QuitAccess** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a96b-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="2a96b-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2a96b-110">説明</span><span class="sxs-lookup"><span data-stu-id="2a96b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a96b-111"><strong>Options</strong></span><span class="sxs-lookup"><span data-stu-id="2a96b-111"><strong>Options</strong></span></span></p></td>
<td><p><span data-ttu-id="2a96b-p102">Access の終了時の未保存のオブジェクトに対する処理を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オプション</strong>] ボックスで、ダイアログ ボックスを表示してオブジェクトごとに保存するかどうかを指定する場合は [<strong>確認</strong>]、ダイアログ ボックスを表示せずにすべてのオブジェクトを保存する場合は [<strong>すべて保存</strong>]、オブジェクトを保存せずに終了する場合は [<strong>終了</strong>] をクリックします。既定値は [<strong>すべて保存</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="2a96b-p102">Specifies what happens to unsaved objects when you quit Access. Click <strong>Prompt</strong> (to display dialog boxes that ask whether to save each object), <strong>Save All</strong> (to save all objects without prompting by dialog boxes), or <strong>Exit</strong> (to quit without saving any objects) in the <strong>Options</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Save All</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2a96b-115">解説</span><span class="sxs-lookup"><span data-stu-id="2a96b-115">Remarks</span></span>

<span data-ttu-id="2a96b-116">**QuitAccess**アクション マクロで、次のすべてのアクションは実行されません。</span><span class="sxs-lookup"><span data-stu-id="2a96b-116">Access doesn't run any actions that follow the **QuitAccess** action in a macro.</span></span>

<span data-ttu-id="2a96b-117">このアクションを使用すると、フォームのカスタム メニュー コマンドまたはボタンを使用して**保存**] ダイアログ ボックスを表示しないで Access を終了します。</span><span class="sxs-lookup"><span data-stu-id="2a96b-117">You can use this action to quit Access without prompts from **Save** dialog boxes by using a custom menu command or a button on a form.</span></span> <span data-ttu-id="2a96b-118">たとえば、マスター フォーム、ユーザー設定のワークスペースにオブジェクトを表示するために使用される場合もあります。</span><span class="sxs-lookup"><span data-stu-id="2a96b-118">For example, you might have a master form that you use to display the objects in your custom workspace.</span></span> <span data-ttu-id="2a96b-119">このフォームには、 **Quit**ボタン**すべてを保存**する設定**オプション**の引数を指定して**QuitAccess**アクションを含むマクロを実行する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2a96b-119">This form could have a **Quit** button that runs a macro containing the **QuitAccess** action with the **Options** argument set to **Save All**.</span></span>

<span data-ttu-id="2a96b-120">/System オプションは、[**ファイル**] タブをクリックして、[**終了**] をクリックと同じ効果。</span><span class="sxs-lookup"><span data-stu-id="2a96b-120">This action has the same effect as clicking the **File** tab and then clicking **Exit**.</span></span> <span data-ttu-id="2a96b-121">このコマンドをクリックすると、保存されていないオブジェクトがある場合、ダイアログ ボックスが表示か**QuitAccess**アクションの引数**のオプション**の**プロンプト**を使用する場合に表示されるものと同じです。</span><span class="sxs-lookup"><span data-stu-id="2a96b-121">If you have any unsaved objects when you click this command, the dialog boxes that appear are the same as those displayed when you use **Prompt** for the **Options** argument of the **QuitAccess** action.</span></span>

<span data-ttu-id="2a96b-122">Access を終了したりオブジェクトを閉じたりするのにことがなく、指定したオブジェクトを保存するのには、マクロで**SaveObject**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a96b-122">You can use the **SaveObject** action in a macro to save a specified object without having to quit Access or close the object.</span></span>

<span data-ttu-id="2a96b-123">Visual Basic for Applications (VBA) モジュールに**QuitAccess**アクションを実行するには、 **DoCmd**オブジェクトの**Quit**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2a96b-123">To run the **QuitAccess** action in a Visual Basic for Applications (VBA) module, use the **Quit** method of the **DoCmd** object.</span></span>

