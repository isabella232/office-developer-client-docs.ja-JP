---
title: Excel アドイン (XLL) 開発における既知の問題
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- known issues [excel 2007]
localization_priority: Normal
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34784f6895386efe7e6c3ca7ec213c7d71931058
ms.sourcegitcommit: f139451a43598b59da22775333779df691df460a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/27/2018
ms.locfileid: "26685180"
---
# <a name="known-issues-in-excel-xll-development"></a><span data-ttu-id="f740f-104">Excel アドイン (XLL) 開発における既知の問題</span><span class="sxs-lookup"><span data-stu-id="f740f-104">Known Issues in Excel XLL Development</span></span>

 <span data-ttu-id="f740f-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f740f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f740f-106">このトピックでは、Microsoft Excel での XLL 開発で遭遇する可能性のある既知の問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="f740f-106">This topic describes known issues in Microsoft Excel that you might encounter in XLL development.</span></span>
  
## <a name="unregistering-xll-commands-and-functions"></a><span data-ttu-id="f740f-107">XLL のコマンドおよび関数を登録解除する</span><span class="sxs-lookup"><span data-stu-id="f740f-107">Unregistering XLL Commands and Functions</span></span>

<span data-ttu-id="f740f-108">XLL で関数やコマンドを登録すると、Excel 上で新しいリソース名が作成され、そのリソース名を持つ DLL 関数の参照と関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="f740f-108">When an XLL registers a function or command, Excel creates a new name for the resource and associates a reference to the DLL function with that name.</span></span> <span data-ttu-id="f740f-109">このリソース名は、[xlfRegister](xlfregister-form-1.md) 関数の 4 番目の引数である *pxFunctionText* から取得されます。</span><span class="sxs-lookup"><span data-stu-id="f740f-109">The name is taken from the fourth argument,  *pxFunctionText*  , of the [xlfRegister](xlfregister-form-1.md) function.</span></span> <span data-ttu-id="f740f-110">また、このリソース名は、ワークシート名を管理する標準のダイアログ ボックスからは非表示になっています。</span><span class="sxs-lookup"><span data-stu-id="f740f-110">This name is hidden from the normal dialog boxes for managing worksheet names.</span></span> <span data-ttu-id="f740f-111">関数やコマンドを登録解除するには、[xlfSetName](xlfsetname.md) 関数を使用してリソース名を削除する必要があります。この際、リソース名を渡しますが、定義は渡しません。</span><span class="sxs-lookup"><span data-stu-id="f740f-111">To unregister a function or command, you must delete the name by using the [xlfSetName](xlfsetname.md) function, passing the name but not passing a definition.</span></span> <span data-ttu-id="f740f-112">ただし、バグがあると、この関数ウィザードの一覧からリソース名を削除することができません。</span><span class="sxs-lookup"><span data-stu-id="f740f-112">However, a bug prevents this from removing the name from the Function Wizard lists.</span></span> 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a><span data-ttu-id="f740f-113">関数ウィザードにおける引数の説明文字列の切り捨て</span><span class="sxs-lookup"><span data-stu-id="f740f-113">Argument Description String Truncation in the Function Wizard</span></span>

<span data-ttu-id="f740f-114">*PxArgumentHelp1* パラメーターと、その後の **xlfRegister** 関数のパラメーターはすべて、XLL 関数の引数に相当し、文字列は省略することができます。</span><span class="sxs-lookup"><span data-stu-id="f740f-114">The  *pxArgumentHelp1*  parameter and all subsequent parameters of the **xlfRegister** function are optional strings that correspond to the arguments of the XLL function.</span></span> <span data-ttu-id="f740f-115">引数作成ダイアログ ボックスにヘルプを表示するために、関数ウィザードにはこれらのパラメータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f740f-115">The Function Wizard displays these to provide help in the argument construction dialog box.</span></span> <span data-ttu-id="f740f-116">ダイアログ ボックスに表示する際、最後の引数に相当する文字列が Excel 上で 1 文字または 2 文字切り捨てられる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f740f-116">Sometimes Excel truncates the string that corresponds to the final argument by one or two characters when displaying it in the dialog box.</span></span> <span data-ttu-id="f740f-117">これを回避するために、関数登録の最後の「引数ヘルプ」パラメーターとして付加的な「空の文字列」を追加できます。</span><span class="sxs-lookup"><span data-stu-id="f740f-117">You can avoid this by adding an additional "empty string" as the last "argument help" parameter of your function registration.</span></span>
  
## <a name="binary-name-scope-limitation"></a><span data-ttu-id="f740f-118">バイナリ名のスコープ制限</span><span class="sxs-lookup"><span data-stu-id="f740f-118">Binary Name Scope Limitation</span></span>

<span data-ttu-id="f740f-p103">バイナリ名とそのデータは、作成された時点でアクティブだったワークシートが再度アクティブになったときにのみ取得できます。ワークシート関数では、ワークブック内のワークシートをアクティブにすることはできないため (コマンドでのみ可能)、バイナリ名の適用は非常に制限されています。特定のワークシートからのみ呼び出されるコマンドがあれば、バイナリ名を使用してコマンドに関するデータを格納することもできます。</span><span class="sxs-lookup"><span data-stu-id="f740f-p103">Binary names and their data can be retrieved only when the worksheet that was active at the time they were created is again active. Because worksheet functions cannot activate worksheets within a workbook (only commands can do this), applications of binary names are very limited. If you have a command that is only invoked from a particular worksheet, for example, you could use a binary name to store command-related data.</span></span>
  
## <a name="xlset-and-workbooks-with-array-formulas"></a><span data-ttu-id="f740f-122">xlSet と配列数式を含むワークブック</span><span class="sxs-lookup"><span data-stu-id="f740f-122">xlSet and Workbooks with Array Formulas</span></span>

<span data-ttu-id="f740f-123">Excel 2003 以前のバージョンにおいて、作業中ではないワークシートの範囲に値を割り当てようとすると、[xlSet 関数](xlset.md) はエラーになり、作業中のシート上の同等範囲に配列数式が入ります。</span><span class="sxs-lookup"><span data-stu-id="f740f-123">In Excel 2003 and earlier versions, the [xlSet function](xlset.md) fails if you try to assign values to a range on a worksheet that is not the active worksheet, where the equivalent range on the active sheet contains an array formula.</span></span> <span data-ttu-id="f740f-124">この場合、「配列の一部を変更できません」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f740f-124">In this case, Excel displays the message "You cannot change part of an array."</span></span> <span data-ttu-id="f740f-125">この問題は、Excel 2007 で修正されました。</span><span class="sxs-lookup"><span data-stu-id="f740f-125">This was fixed in Excel 2007.</span></span> 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a><span data-ttu-id="f740f-126">データ テーブルで循環参照が可能</span><span class="sxs-lookup"><span data-stu-id="f740f-126">Circular References are Tolerated in Data Tables</span></span>

<span data-ttu-id="f740f-p105">Excel では現在、データ テーブルのベースとなる計算において、同テーブル上の値を参照している場合でもエラーになりません。このようなシナリオはまれなことですが、データ テーブルの値を計算する数式の作成や変更には注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="f740f-p105">Excel currently does not raise an error if the calculation that a data table is based on refers to something in the table itself. As unlikely as this scenario might be, you should be careful when you are creating or modifying formulas that are used to calculate data table values.</span></span>
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a><span data-ttu-id="f740f-129">整数 XLOPER12 を XLOPER に変換する</span><span class="sxs-lookup"><span data-stu-id="f740f-129">Converting an Integer XLOPER12 to an XLOPER</span></span>

<span data-ttu-id="f740f-p106">整数型 **xltypeInt** は、**XLOPER12** データ型では 32 ビットの符号付き整数ですが、**XLOPER** データ型では 16 ビット符号付き整数であるため、整数 **XLOPER12** の値の中には、整数 **XLOPER** に含められないものがある可能性があります。Excel 内部でこのデータ型を変換する場合は、データ型を浮動小数点 **xltypeNum** **XLOPER** に変換してこの問題を回避します。</span><span class="sxs-lookup"><span data-stu-id="f740f-p106">Because the integer type **xltypeInt** is a 32-bit signed integer in the **XLOPER12** data type, but it is only a 16-bit signed integer in the **XLOPER** data type, it is possible that some integer **XLOPER12** values cannot be contained in an integer **XLOPER**. Where Excel converts this type internally, it gets around this problem by converting the type to a floating-point **xltypeNum** **XLOPER**.</span></span>
  
<span data-ttu-id="f740f-p107">フレームワーク関数 [XLOper12ToXLOper](xloper12toxloper.md) は、この動作を反映して、Excel 内部の動作と一致するようにします。この関数を呼び出す際、返される **XLOPER** が常に **xltypeInt** であると想定しないでください。**my_xloper** 型が **xltypeNum** の場合に **my_xloper.val.w** を読み出すと、false の値が返されます。</span><span class="sxs-lookup"><span data-stu-id="f740f-p107">The Framework [XLOper12ToXLOper](xloper12toxloper.md) function mirrors this behavior to be consistent with Excel internally. When you call this function, you should not assume that the returned **XLOPER** will always be **xltypeInt**; reading **my_xloper.val.w** gives a false value if the **my_xloper** type is **xltypeNum**.</span></span>
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a><span data-ttu-id="f740f-134">引数をインプレースで変更して XLOPER または XLOPER12 を返す</span><span class="sxs-lookup"><span data-stu-id="f740f-134">Returning XLOPER or XLOPER12 by Modifying Arguments in Place</span></span>

<span data-ttu-id="f740f-p108">Excel では引数をインプレースで変更して、**XLOPER** または **XLOPER12** を返すように関数を登録することができます。しかし、**XLOPER**/ **XLOPER12** 引数がメモリをポイントしており、そのポインターが DLL 関数の戻り値で上書きされると、Excel でメモリ リークが発生する可能性があります。Excel でエラーは表示されませんが、結果的にクラッシュする恐れがあります。また、DLL で戻り値用のメモリが割り当てられている場合、Excel はそのメモリを解放しようとするため、すぐにアプリケーションがクラッシュする恐れがあります。そのため、**XLOPER**/ **XLOPER12** 引数はインプレースで変更しないでください。**XLOPER** 引数や **XLOPER12** 引数はすべて、必ず読み取り専用として扱ってください。</span><span class="sxs-lookup"><span data-stu-id="f740f-p108">Excel permits the registration of functions that return an **XLOPER** or **XLOPER12** by modifying an argument in place. However, if an **XLOPER**/ **XLOPER12** argument points to memory, and the pointer is then overwritten by the return value of the DLL function, Excel can leak memory. Excel does not display an error, but it might eventually crash. Also, if the DLL allocated memory for the return value, Excel might try to free that memory, which could cause an immediate application crash. Therefore, you should not modify **XLOPER**/ **XLOPER12** arguments in place. All **XLOPER** or **XLOPER12** arguments should be treated as strictly read-only.</span></span> 
  
<span data-ttu-id="f740f-141">詳細については、「[Excel のメモリ管理](memory-management-in-excel.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f740f-141">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f740f-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="f740f-142">See also</span></span>



[<span data-ttu-id="f740f-143">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="f740f-143">XLOper12ToXLOper</span></span>](xloper12toxloper.md)


[<span data-ttu-id="f740f-144">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="f740f-144">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="f740f-145">Excel XLL SDK API 関数リファレンス</span><span class="sxs-lookup"><span data-stu-id="f740f-145">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)
  
[<span data-ttu-id="f740f-146">Excel のメモリ管理</span><span class="sxs-lookup"><span data-stu-id="f740f-146">Memory Management in Excel</span></span>](memory-management-in-excel.md)

