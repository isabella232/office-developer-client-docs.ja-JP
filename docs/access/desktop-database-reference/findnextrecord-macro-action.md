---
title: "'FindNextRecord/次のレコードを検索' マクロ アクション"
TOCTitle: FindNextRecord Macro Action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 05dec445360d5c42636880982e27e0abd46d048e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883653"
---
# <a name="findnextrecord-macro-action"></a><span data-ttu-id="b85fa-102">"FindNextRecord/次のレコードを検索" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="b85fa-102">FindNextRecord Macro Action</span></span>


<span data-ttu-id="b85fa-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b85fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b85fa-104">前の操作を**行って**または、[**検索し、置換**] ダイアログ ボックスの値で指定された条件を満たす次のレコードを検索する**FindNextRecord**アクションを使用することができます ([**ホーム**] タブの [**検索**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="b85fa-104">You can use the **FindNextRecord** action to find the next record that meets the criteria specified by the previous **FindRecord** action or the value in the **Find and Replace** dialog box (on the **Home** tab, click **Find**).</span></span> <span data-ttu-id="b85fa-105">**FindNextRecord**アクションを使用するにはレコードを繰り返し検索します。</span><span class="sxs-lookup"><span data-stu-id="b85fa-105">You can use the **FindNextRecord** action to search repeatedly for records.</span></span> <span data-ttu-id="b85fa-106">たとえば、すべてのレコードの中から特定の得意先のレコードを連続して検索できます。</span><span class="sxs-lookup"><span data-stu-id="b85fa-106">For example, you can move successively through all the records for a specific customer.</span></span>

## <a name="setting"></a><span data-ttu-id="b85fa-107">設定値</span><span class="sxs-lookup"><span data-stu-id="b85fa-107">Setting</span></span>

<span data-ttu-id="b85fa-108">**FindNextRecord**アクション引数はありません。</span><span class="sxs-lookup"><span data-stu-id="b85fa-108">The **FindNextRecord** action doesn't have any arguments.</span></span> <span data-ttu-id="b85fa-109">**FindNextRecord**アクションは、次の操作を**行って**または、[**検索し、置換**] ダイアログ ボックスで設定した基準を満たすレコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="b85fa-109">The **FindNextRecord** action finds the next record that meets the criteria set either by the **FindRecord** action or in the **Find and Replace** dialog box.</span></span> <span data-ttu-id="b85fa-110">**FindRecord**アクションの引数は、 **[検索し、置換**] ダイアログ ボックスでオプションを使用して共有されます。</span><span class="sxs-lookup"><span data-stu-id="b85fa-110">The arguments for the **FindRecord** action are shared with the options in the **Find and Replace** dialog box.</span></span>

<span data-ttu-id="b85fa-111">検索条件を設定するには、操作を**行って**を使用します。</span><span class="sxs-lookup"><span data-stu-id="b85fa-111">To set the search criteria, use the **FindRecord** action.</span></span> <span data-ttu-id="b85fa-112">通常、マクロで操作を**行って**を入力し、 **FindNextRecord**アクションを使用して同じ条件を満たすレコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="b85fa-112">Typically, you enter a **FindRecord** action in a macro and then use the **FindNextRecord** action to find succeeding records that meet the same criteria.</span></span> <span data-ttu-id="b85fa-113">場合のみ、特定の条件のレコードを検索するのには満たされている、 **FindNextRecord**アクションのアクション行の [**条件**] 列に条件式を入力できます。</span><span class="sxs-lookup"><span data-stu-id="b85fa-113">To search for records only when a certain condition is met, you can enter a conditional expression in the **Condition** column of the action row for the **FindNextRecord** action.</span></span>

## <a name="remarks"></a><span data-ttu-id="b85fa-114">解説</span><span class="sxs-lookup"><span data-stu-id="b85fa-114">Remarks</span></span>

<span data-ttu-id="b85fa-115">このアクションの動作は、[ **検索と置換**] ダイアログ ボックスの [ **次を検索**] をクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="b85fa-115">This action has the same effect as using the **Find Next** button in the **Find and Replace** dialog box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b85fa-116">操作を<STRONG>行って</STRONG>は、テーブル、クエリ、およびフォームの [<STRONG>ホーム</STRONG>] タブの [<STRONG>検索</STRONG>] コマンドに対応しています、[コード] ウィンドウで [<STRONG>編集</STRONG>] メニューの [<STRONG>検索</STRONG>] コマンドに対応していません。</span><span class="sxs-lookup"><span data-stu-id="b85fa-116">Although the <STRONG>FindRecord</STRONG> action corresponds to the <STRONG>Find</STRONG> command on the <STRONG>Home</STRONG> tab for tables, queries, and forms, it doesn't correspond to the <STRONG>Find</STRONG> command on the <STRONG>Edit</STRONG> menu in the Code window.</span></span> <span data-ttu-id="b85fa-117">モジュール内のテキストを検索する操作を<STRONG>行って</STRONG>、 <STRONG>FindNextRecord</STRONG>アクションを使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="b85fa-117">You can't use the <STRONG>FindRecord</STRONG> action or <STRONG>FindNextRecord</STRONG> action to search for text in modules.</span></span></P>




> [!TIP]
> <P><span data-ttu-id="b85fa-118">操作を<STRONG>行って</STRONG>の<STRONG>現在のフィールド</STRONG>の引数を<STRONG>[はい]</STRONG>に設定するとは、検索対象となる、<STRONG>を使用する前にデータを格納しているコントロールにフォーカスを移動するのには<STRONG>フォーカスを移動</STRONG>を使用する必要があります。FindNextRecord</STRONG>アクション。</span><span class="sxs-lookup"><span data-stu-id="b85fa-118">If you've set the <STRONG>Only Current Field</STRONG> argument of the <STRONG>FindRecord</STRONG> action to <STRONG>Yes</STRONG>, you may need to use the <STRONG>GoToControl</STRONG> action to move the focus to the control containing the data you're searching for before you use the <STRONG>FindNextRecord</STRONG> action.</span></span></P>



<span data-ttu-id="b85fa-119">現在選択されているテキストがある場合、検索する文字列と同じ**FindNextRecord**のマクロ アクション実行時に、選択範囲、選択範囲は、同じフィールドで、同じレコードの直後、検索が開始されます。</span><span class="sxs-lookup"><span data-stu-id="b85fa-119">If the currently selected text is the same as the search text at the time the **FindNextRecord** macro action is carried out, the search begins immediately following the selection, in the same field as the selection, and in the same record.</span></span> <span data-ttu-id="b85fa-120">選択されているテキストと検索テキストが異なる場合は、カレント レコードの先頭から検索が開始されます。</span><span class="sxs-lookup"><span data-stu-id="b85fa-120">Otherwise, the search begins at the start of the current record.</span></span> <span data-ttu-id="b85fa-121">このため、1 つのレコードに同じ検索条件を満たすテキストが複数存在する場合の検索が可能です。</span><span class="sxs-lookup"><span data-stu-id="b85fa-121">This enables you to find multiple instances of the same search criteria that might appear in a single record.</span></span>

<span data-ttu-id="b85fa-122">ただし、 **FindNextRecord**アクションを含むマクロを実行するコマンド ボタンを使用する場合、検索条件の最初のインスタンスが見つからないを繰り返しします。</span><span class="sxs-lookup"><span data-stu-id="b85fa-122">However, note that if you use a command button to run a macro containing the **FindNextRecord** action, the first instance of the search criteria will be found repeatedly.</span></span> <span data-ttu-id="b85fa-123">この現象は、一致する値を含むフィールドからフォーカスを削除するコマンド ボタンをクリックするとされるために発生します。</span><span class="sxs-lookup"><span data-stu-id="b85fa-123">This behavior occurs because clicking the command button removes the focus from the field containing the matching value.</span></span> <span data-ttu-id="b85fa-124">**FindNextRecord**アクションは、レコードの先頭から検索し、開始されます。</span><span class="sxs-lookup"><span data-stu-id="b85fa-124">The **FindNextRecord** action will then begin searching from the start of the record.</span></span> <span data-ttu-id="b85fa-125">この問題を避けるためには、カスタム ツールバーのボタンや AutoKeys マクロで定義されているキーの組み合わせなど、フォーカスを変更しない方法を使用してマクロを実行します。</span><span class="sxs-lookup"><span data-stu-id="b85fa-125">To avoid this problem, run the macro by using a technique that doesn't change the focus, such as a custom toolbar button or a key combination defined in an AutoKeys macro.</span></span> <span data-ttu-id="b85fa-126">代わりに、マクロの**FindNextRecord**アクションを実行する前に、検索条件を含むフィールドにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="b85fa-126">Alternatively, set the focus in the macro to the field containing the search criteria before you carry out the **FindNextRecord** action.</span></span>

<span data-ttu-id="b85fa-127">**No**に設定する**最初の検索**引数を指定して操作を**行って**を含むマクロを実行するコマンド ボタンを使用する場合も同じ現象が発生します。</span><span class="sxs-lookup"><span data-stu-id="b85fa-127">The same behavior also occurs if you use a command button to run a macro containing the **FindRecord** action with the **Find First** argument set to **No**.</span></span>

<span data-ttu-id="b85fa-128">モジュールの Visual Basic for Applications の**FindNextRecord**アクションを実行するには、 **DoCmd**オブジェクトの**FindNext**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b85fa-128">To run the **FindNextRecord** action in a Visual Basic for Applications module, use the **FindNext** method of the **DoCmd** object.</span></span>

