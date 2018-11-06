---
title: SendKeys マクロ アクション
TOCTitle: SendKeys macro action
ms:assetid: 3b06fcfc-ea64-c780-b5fc-6fc72853f524
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192656(v=office.15)
ms:contentKeyID: 48544275
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm183441
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 206c12d324b2b9c11b22357a3262a343bba3c122
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998806"
---
# <a name="sendkeys-macro-action"></a><span data-ttu-id="38797-102">SendKeys マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="38797-102">SendKeys macro action</span></span>

<span data-ttu-id="38797-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="38797-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="セキュリティに関する注意" alt="Security note" /><span data-ttu-id="38797-105"><strong>セキュリティ メモ</strong></span><span class="sxs-lookup"><span data-stu-id="38797-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="38797-p101">
      重要な情報または機密情報には <strong>SendKeys</strong> ステートメントまたは AutoKeys マクロを使用しないでください。悪意のあるユーザーがキー入力を途中で遮り、コンピューターおよびデータのセキュリティを侵害するおそれがあります。
</span><span class="sxs-lookup"><span data-stu-id="38797-p101">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="38797-108">**SendKeys** アクションを使用すると、Microsoft Access やアクティブな Windows ベースのアプリケーションにキー操作を直接送信することができます。</span><span class="sxs-lookup"><span data-stu-id="38797-108">You can use the **SendKeys** action to send keystrokes directly to Microsoft Access or to an active Windows-based application.</span></span>

> [!NOTE]
> <span data-ttu-id="38797-109">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="38797-109">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="38797-110">設定</span><span class="sxs-lookup"><span data-stu-id="38797-110">Setting</span></span>

<span data-ttu-id="38797-111">**SendKeys** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="38797-111">The **SendKeys** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38797-112">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="38797-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="38797-113">説明</span><span class="sxs-lookup"><span data-stu-id="38797-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38797-114"><strong>Keystrokes/キー操作</strong></span><span class="sxs-lookup"><span data-stu-id="38797-114"><strong>Keystrokes</strong></span></span></p></td>
<td><p><span data-ttu-id="38797-p102">Access やアプリケーションで処理するキー操作を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>キー操作</strong>] ボックスに、キー操作を入力します。255 文字まで入力できます。この引数は省略できません。  </span><span class="sxs-lookup"><span data-stu-id="38797-p102">The keystrokes you want Access or the application to process. Enter the keystrokes in the <strong>Keystrokes</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can type up to 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38797-119"><strong>Wait/待機</strong></span><span class="sxs-lookup"><span data-stu-id="38797-119"><strong>Wait</strong></span></span></p></td>
<td><p><span data-ttu-id="38797-p103">キー操作の処理が終わるまでマクロを一時中断するかどうかを指定します。中断する場合は [ <strong>はい</strong>]、中断しない場合は [ <strong>いいえ</strong>] をクリックします。既定値は [ <strong>いいえ</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="38797-p103">Specifies whether the macro should pause until the keystrokes have been processed. Click <strong>Yes</strong> (to pause) or <strong>No</strong> (to not pause). The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="38797-123">解説</span><span class="sxs-lookup"><span data-stu-id="38797-123">Remarks</span></span>

<span data-ttu-id="38797-124">**SendKeys** アクションで Access にキー操作を送信すると、Access ウィンドウに直接キー操作入力したときと同じように処理されます。</span><span class="sxs-lookup"><span data-stu-id="38797-124">Access processes the keystrokes it receives through the **SendKeys** action exactly as if you had typed them directly in an Access window.</span></span>

<span data-ttu-id="38797-125">キー操作を指定するには、 **SendKeys** ステートメントと同じ構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="38797-125">To specify the keystrokes, use the same syntax as you would for the **SendKeys** statement.</span></span>

> [!NOTE]
> <span data-ttu-id="38797-126">[!メモ] **Keystrokes/キー操作** 引数に不適切な構文、スペルを誤った文字列、または送り先のウィンドウにとって不適切な値が含まれる場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="38797-126">An error can occur if the **Keystrokes** argument contains incorrect syntax, misspelled text, or other values that aren't appropriate for the window the keystrokes are sent to.</span></span>

<span data-ttu-id="38797-p104">このアクションは、ダイアログ ボックスに情報を入力する場合 (特にマクロを中断せずにダイアログ ボックスに手動で入力する場合) に使用します。Access のアクションには、よく使用するダイアログ ボックスのオプションを自動的に選択する **PrintOut** アクションや **FindRecord** アクションなどがありますが、それ以外のダイアログ ボックスのオプションを選択するには **SendKeys** アクションを使います。</span><span class="sxs-lookup"><span data-stu-id="38797-p104">You can use this action to enter information in a dialog box, particularly if you don't want to interrupt the macro to respond manually to the dialog box. Some Access actions, such as **PrintOut** and **FindRecord**, automatically select the options in certain frequently used dialog boxes. You can use the **SendKeys** action to select the options in less commonly used dialog boxes.</span></span>

> [!NOTE]
> - <span data-ttu-id="38797-130">[!メモ] ダイアログ ボックスによってマクロが中断されるので、ダイアログ ボックスを開くアクションの前に **SendKeys** アクションを配置し、 **Wait/待機** 引数を [ **いいえ** ] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38797-130">Because the dialog box suspends the macro, you must put the **SendKeys** action before the action that causes the dialog box to open and set the **Wait** argument to **No**.</span></span>
> - <span data-ttu-id="38797-p105">Access やその他のアプリケーションにキー操作が到達するタイミングには注意が必要です。目的の処理を実行するために、**SendKeys** アクションを使わずに他の**FindRecord** アクションなどを使用してダイアログ ボックスのオプションを入力できる場合は、他のアクションを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="38797-p105">The timing of the keystrokes reaching Access or another application can be tricky. As a result, it's recommended that if there's some other method (such as the **FindRecord** action) you can use to achieve a desired task, use that method rather than using the **SendKeys** action to fill in the options in a dialog box.</span></span>

<span data-ttu-id="38797-133">Access やその他の Windows ベースのアプリケーションに 255 文字を超えるキー操作を送る場合は、マクロで **SendKeys** アクションを複数回続けて使用します。</span><span class="sxs-lookup"><span data-stu-id="38797-133">If you want to send more than 255 characters to Access or another Windows-based application, you can use several **SendKeys** actions in succession in a macro.</span></span>

<span data-ttu-id="38797-p106">**SendKeys** アクションを使用してキー操作を送ると、対応する **KeyDown** 、 **KeyUp** 、 **KeyPress** イベントが発生します。ただし、ANSI 以外のキー操作 (ファンクション キーなど) を送っても **KeyPress** イベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="38797-p106">Using the **SendKeys** action to send keystrokes triggers the appropriate **KeyDown**, **KeyUp**, and **KeyPress** events. Sending non-ANSI keystrokes (such as a function key) doesn't trigger the **KeyPress** event.</span></span>

<span data-ttu-id="38797-p107">このアクションは Visual Basic for Applications (VBA) モジュールでは使用できません。 **SendKeys** ステートメントを代わりに使用してください。</span><span class="sxs-lookup"><span data-stu-id="38797-p107">This action isn't available from a Visual Basic for Applications (VBA) module. Use the **SendKeys** statement instead.</span></span>

