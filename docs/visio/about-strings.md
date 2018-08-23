---
title: 文字列について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251826
localization_priority: Normal
ms.assetid: e1174d8f-70cb-4595-7906-889da15367db
description: 数式は文字列を含めることができます。 プロンプト セル、図形データ項目の値、またはテキスト フィールドなどで文字列の出力を書式設定するには、図の書式設定を指定します。 出力は、数値と単位のペアを文字列として書式設定できます日付と時刻、期間、または通貨です。 などの形式の picture0 と 10 uuformats 数値と単位は、9/10 センチメートル 10.9 cm as10 ペアです。
ms.openlocfilehash: 1fd003ecd5c824042e97a40fa8374aeead254ddc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804735"
---
# <a name="about-strings"></a><span data-ttu-id="23478-106">文字列について</span><span class="sxs-lookup"><span data-stu-id="23478-106">About Strings</span></span>

<span data-ttu-id="23478-p102">数式には文字列を含めることができます。プロンプト セル、図形データ項目値、テキスト フィールドなどで文字列の出力を書式設定するには、書式形式を指定します。出力は、数値と単位の組み合わせ、文字列、日付/時刻、期間、または通貨として書式設定できます。たとえば、書式形式 "0 #/10 uu" を使用すると、10.9 cm を "10 9/10 センチメートル (cm)" という数値と単位の組み合わせで表示します。</span><span class="sxs-lookup"><span data-stu-id="23478-p102">Formulas can contain strings. To format string output, such as in a prompt cell, a shape data item value, or a text field, you specify a format picture. Output can be formatted as a number-unit pair, string, date-time, duration, or currency. For example, the format picture "0 #/10 uu" formats the number-unit pair 10.9cm as "10 9/10 centimeters".</span></span>
  
<span data-ttu-id="23478-111">**形式**または**FORMATEX**関数の引数と、[図形データ] セクションのセルの**書式設定**では、書式形式を使用できます。</span><span class="sxs-lookup"><span data-stu-id="23478-111">You can use format pictures in the **Format** cell of the Shape Data section and as an argument to the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="23478-112">テキスト フィールドを挿入するとき、[**フィールド**] ダイアログ ボックス ([**挿入**] タブ) の形式の一覧で形式の画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="23478-112">When you insert a text field, format pictures appear in the list of formats in the **Field** dialog box (**Insert** tab).</span></span> 
  
## <a name="using-functions-to-format-strings"></a><span data-ttu-id="23478-113">文字列の書式設定に関数を使用する</span><span class="sxs-lookup"><span data-stu-id="23478-113">Using functions to format strings</span></span>

<span data-ttu-id="23478-114">カスタム テキスト フィールドの数式を含む文字列に解決されるすべての数式には、 **FORMAT**または**FORMATEX**関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="23478-114">In any formula that resolves to a string, including custom text field formulas, you can use the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="23478-115">FORMAT 関数は、書式付き出力の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="23478-115">The FORMAT function returns a string of the formatted output.</span></span> <span data-ttu-id="23478-116">**FORMATEX**関数は、型指定されていない入力を変換する単位に書式設定された結果を選択します。</span><span class="sxs-lookup"><span data-stu-id="23478-116">The **FORMATEX** function converts untyped input to the units you choose for the formatted result.</span></span> 
  
## <a name="displaying-formatted-shape-data"></a><span data-ttu-id="23478-117">書式設定された図形データを表示する</span><span class="sxs-lookup"><span data-stu-id="23478-117">Displaying formatted shape data</span></span>

<span data-ttu-id="23478-118">図形データの表示値の書式は、[Format] セルに書式形式を入力することにより設定できます。</span><span class="sxs-lookup"><span data-stu-id="23478-118">You can format the displayed value of a shape data item by entering a format picture in the Format cell.</span></span>
  
<span data-ttu-id="23478-p105">たとえば、プロジェクトのタイムライン図形には、プロセスのコストを見積もるための図形データ項目を含めることができます。既定では、図形データ項目の値は文字列です。文字列 "1200" を書式設定する場合、[Format] セルに "$###,###.00" を指定すると、通貨であることがわかるように表示できます。</span><span class="sxs-lookup"><span data-stu-id="23478-p105">For example, a project timeline shape can have a shape data item that measures the cost of a process. By default, a shape data item value is a string. To format the string "1200", you can enter "$###,###.00" in the Format cell so that the user sees a currency.</span></span>
  
<span data-ttu-id="23478-122">Microsoft Visio では、コントロール パネルの [**地域と言語**の項目の**書式設定のカスタマイズ**] ダイアログ ボックスで [**通貨**] タブで設定を使用して通貨記号と桁を確認する区切り記号を表示します。</span><span class="sxs-lookup"><span data-stu-id="23478-122">Microsoft Visio uses the settings on the **Currency** tab in the **Customize Format** dialog box in the **Region and Language** item in Control Panel to determine the currency symbol and thousands separator to display.</span></span> <span data-ttu-id="23478-123">([**コントロール パネル]**、[**地域と言語**、[**追加設定**] をクリックして)</span><span class="sxs-lookup"><span data-stu-id="23478-123">(In **Control Panel**, click **Region and Language**, and then click **Additional Settings**.)</span></span>
  
<span data-ttu-id="23478-124">文字列を通貨の値に変換して値を計算できるようにするには、CY 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="23478-124">To convert a string to a currency value so that you can perform calculations with the value, use the CY function.</span></span>
  
## <a name="using-functions-to-manipulate-text-strings"></a><span data-ttu-id="23478-125">文字列の操作に関数を使用する</span><span class="sxs-lookup"><span data-stu-id="23478-125">Using functions to manipulate text strings</span></span>

<span data-ttu-id="23478-p107">文字列中の特定の文字を検索または置換するなどの、文字列の操作には関数を使用できます。文字列内の、ある文字の位置に関する情報を取得したり、文字列の最初の文字や最後の文字を識別することもできます。</span><span class="sxs-lookup"><span data-stu-id="23478-p107">You can use functions to manipulate text strings, for example, to locate or replace certain characters in a text string. You can also get information about the position of a character in a string, or identify beginning and ending characters in a text string.</span></span> 
  

