---
title: Format 関数 (カスタム web アプリケーションのアクセス) 用のカスタムの数値書式
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 97efe972-d873-47d7-be81-8ae3461870c4
description: ユーザー定義の数値書式を作成して数値の表示方法を制御する方法について説明します。
ms.openlocfilehash: fac128ce13edf89105fbee7319533e1a3f346d05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798601"
---
# <a name="custom-numeric-formats-for-the-format-function-access-custom-web-app"></a><span data-ttu-id="8380c-103">Format 関数 (カスタム web アプリケーションのアクセス) 用のカスタムの数値書式</span><span class="sxs-lookup"><span data-stu-id="8380c-103">Custom numeric formats for the Format function (Access custom web app)</span></span>

<span data-ttu-id="8380c-104">ユーザー定義の数値書式を作成して数値の表示方法を制御する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8380c-104">Learn how to control how a number is displayed by creating a user-defined number format.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8380c-p101">[!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="8380c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 

<span data-ttu-id="8380c-p102">ユーザー定義の数値書式を作成して数値の表示方法を変更できます。ユーザー定義の数値書式は、セミコロン (;) で区切られた 1 ～ 3 つのセクションを持つことができます。[Format 関数 (Access カスタム Web アプリ)](format-function-access-custom-web-app.md) 関数の Style 引数に事前定義されたいずれかの数値書式が含まれる場合、1 つのセクションのみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8380c-p102">You can change the way a number is displayed by creating a user-defined number format. A user-defined number format can have from one to three sections separated by a semicolon (;). If the Style argument of the [Format Function (Access custom web app)](format-function-access-custom-web-app.md) function contains one of the predefined numeric formats, only one section is allowed.</span></span> 
  
## <a name="format-specifications"></a><span data-ttu-id="8380c-110">書式指定</span><span class="sxs-lookup"><span data-stu-id="8380c-110">Format specifications</span></span>
<span data-ttu-id="8380c-111"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="8380c-111"></span></span>

<span data-ttu-id="8380c-112">以下の表は、ユーザー定義数値書式の作成に使用できる文字を示します。</span><span class="sxs-lookup"><span data-stu-id="8380c-112">The following table lists characters you can use to create user-defined number formats.</span></span>
  
|<span data-ttu-id="8380c-113">**形式の仕様**</span><span class="sxs-lookup"><span data-stu-id="8380c-113">**Format specification**</span></span>|<span data-ttu-id="8380c-114">**説明**</span><span class="sxs-lookup"><span data-stu-id="8380c-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8380c-115">なし</span><span class="sxs-lookup"><span data-stu-id="8380c-115">None</span></span>  <br/> |<span data-ttu-id="8380c-116">書式のない数値を表示します。</span><span class="sxs-lookup"><span data-stu-id="8380c-116">Displays the number without formatting.</span></span>  <br/> |
|<span data-ttu-id="8380c-117">**0** (0 文字)</span><span class="sxs-lookup"><span data-stu-id="8380c-117">**0** (zero character)</span></span>  <br/> |<span data-ttu-id="8380c-p103">桁のプレースホルダーです。数字または 0 を表示します。式に、書式指定文字列で 0 が指定されている場所に数字がある場合は、該当する数字がその桁に表示されます。それ以外の場合は、その場所に 0 を表示します。</span><span class="sxs-lookup"><span data-stu-id="8380c-p103">Digit placeholder. Displays a digit or a zero. If the expression has a digit in the position where the zero appears in the format string, displays the digit; otherwise, displays a zero in that position.</span></span>  <br/> <span data-ttu-id="8380c-p104">数値の整数部または小数部の桁数が、書式指定式内の 0 の桁数に満たない場合は、その桁位置には 0 を表示します。数値の小数部の桁数が、書式指定式の小数部で指定されている 0 の数より多い場合は、0 の数と同じ桁数に数値が丸められます。数値の整数部の桁数が、書式指定式の整数部の 0 の数より多い場合は、桁をそのまま表示します。</span><span class="sxs-lookup"><span data-stu-id="8380c-p104">If the number has fewer digits than there are zeros (on either side of the decimal) in the format expression, displays leading or trailing zeros. If the number has more digits to the right side of the decimal separator than there are zeros to the right side of the decimal separator in the format expression, rounds the number to as many decimal places as there are zeros. If the number has more digits to the left of the decimal separator than there are zeros to the left of the decimal separator in the format expression, displays the additional digits without modification.</span></span>  <br/> |
|#  <br/> |<span data-ttu-id="8380c-p105">桁のプレースホルダーです。数字を表示するか、何も表示しません。書式指定文字列で # 文字が指定されている場所に該当する桁が、式の結果にある場合は、該当する数字が表示されます。それ以外の場合は、その場所には何も表示されません。</span><span class="sxs-lookup"><span data-stu-id="8380c-p105">Digit placeholder. Displays a digit or nothing. If the expression has a digit in the position where the # character appears in the format string, displays the digit; otherwise, displays nothing in that position.</span></span>  <br/> <span data-ttu-id="8380c-127">この記号は 0 桁プレースホルダーとまったく同様の機能を持ちます。ただし、数値の桁数が、書式指定式の整数部および小数部にある # 記号よりも少ない場合でも、先頭および末尾に 0 が表示されません。</span><span class="sxs-lookup"><span data-stu-id="8380c-127">This symbol works exactly like the 0 digit placeholder, except that leading and trailing zeros aren't displayed if the number has fewer digits than there are # characters on either side of the decimal separator in the format expression.</span></span>  <br/> |
|<span data-ttu-id="8380c-p106">. (ドット文字)</span><span class="sxs-lookup"><span data-stu-id="8380c-p106">. (dot character)</span></span>  <br/> |<span data-ttu-id="8380c-p107">小数点のプレースホルダーです。小数点のプレースホルダーにより、整数部および小数部に表示する桁数が決まります。書式指定式でこの記号の左に # 記号だけがある場合、1 未満の数値の先頭は小数点区切り記号になります。小数値の先頭に 0 を表示するには、整数部の最初の桁のプレースホルダーとして 0 を使用します。ロケールによっては、桁区切り記号としてコンマが使用されます。書式指定結果で小数点のプレースホルダーとして実際に使用される記号は、システムで認識される数値書式によって異なります。したがって、コンマが桁区切り記号として使用されるロケールのユーザーであっても、書式では桁区切り記号としてピリオドを使用する必要があります。書式設定された文字列はロケールの正しい書式で表示されます。</span><span class="sxs-lookup"><span data-stu-id="8380c-p107">Decimal placeholder. The decimal placeholder determines how many digits are displayed to the left and right of the decimal separator. If the format expression contains only # characters to the left of this symbol; numbers smaller than 1 begin with a decimal separator. To display a leading zero displayed with fractional numbers, use zero as the first digit placeholder to the left of the decimal separator. In some locales, a comma is used as the decimal separator. The actual character that is used as a decimal placeholder in the formatted output depends on the number format recognized by the system. Thus, you should use the period as the decimal placeholder in your formats even if you are in a locale that uses a comma as a decimal placeholder. The formatted string will appear in the format correct for the locale.</span></span>  <br/> |
|%  <br/> |<span data-ttu-id="8380c-p108">パーセントのプレースホルダーです。式を 100 倍します。書式指定文字列の表示位置にパーセント記号 (%) が挿入されます。</span><span class="sxs-lookup"><span data-stu-id="8380c-p108">Percent placeholder. Multiplies the expression by 100. The percent character (%) is inserted in the position where it appears in the format string.</span></span>  <br/> |
|<span data-ttu-id="8380c-141">, (コンマ文字)</span><span class="sxs-lookup"><span data-stu-id="8380c-141">, (comma character)</span></span>  <br/> |<span data-ttu-id="8380c-p109">桁区切り記号です。桁区切り記号は、整数部に 4 桁以上ある数値の百の位と千の位を区切ります。書式にある桁区切り記号が桁のプレースホルダー (0 または #) で囲まれている場合は、桁区切り記号の標準使用が指定されます。</span><span class="sxs-lookup"><span data-stu-id="8380c-p109">Thousand separator. The thousand separator separates thousands from hundreds in a number that has four or more places to the left of the decimal separator. Standard use of the thousand separator is specified if the format contains a thousand separator enclosed in digit placeholders (0 or #).</span></span>  <br/> <span data-ttu-id="8380c-p110">小数部の指定の有無にかかわらず、小数点のすぐ左に桁区切り記号がある、または文字列の右端にある場合は、"数値を 1,000 で割って、必要に応じて丸める" ことを意味します。1,000 より小さく、500 以上の数値は 1 と表示され、500 より小さい数値は 0 と表示されます。この位置に 2 つの隣接する区切り記号がある場合は百万の因数でスケーリングし、桁区切り記号が 1 つ増えるごとにさらに 1,000 の因数でスケーリングします。</span><span class="sxs-lookup"><span data-stu-id="8380c-p110">A thousand separator immediately to the left of the decimal separator (whether a decimal is specified) or as the rightmost character in the string means "scale the number by dividing it by 1,000, rounding as needed." Numbers smaller than 1,000 but greater or equal to 500 are displayed as 1, and numbers smaller than 500 are displayed as 0. Two adjacent thousand separators in this position scale by a factor of 1 million, and an additional factor of 1,000 for each additional separator.</span></span>  <br/> <span data-ttu-id="8380c-p111">小数点のすぐ左以外の位置、または文字列の右端の位置に複数の隣接する区切り記号がある場合は、通常の桁区切り記号を指定したものとして処理されます。ロケールによっては、桁区切り記号としてピリオドが使用されます。書式指定された出力で、実際に桁区切り記号として使用される記号は、システムで認識される数値書式によって異なります。したがって、桁区切り記号としてピリオドが使用されるロケールのユーザーであっても、書式で桁区切り記号としてコンマを使用する必要があります。書式設定された文字列は、ロケールの正しい形式で表示されます。</span><span class="sxs-lookup"><span data-stu-id="8380c-p111">Multiple separators in any position other than immediately to the left of the decimal separator or the rightmost position in the string are treated only as specifying the use of a thousand separator. In some locales, a period is used as a thousand separator. The actual character that is used as the thousand separator in the formatted output depends on the Number Format recognized by the system. Thus, you should use the comma as the thousand separator in your formats even if you are in a locale that uses a period as a thousand separator. The formatted string will appear in the format correct for the locale.</span></span>  <br/> <span data-ttu-id="8380c-153">たとえば、次の 3 つの書式文字列を考えてみます。</span><span class="sxs-lookup"><span data-stu-id="8380c-153">For example, consider the three following format strings:</span></span>  <br/> <span data-ttu-id="8380c-154">"#,0." は、桁区切り記号を使用して、1 億を文字列 "100,000,000" として書式設定します。</span><span class="sxs-lookup"><span data-stu-id="8380c-154">"#,0.", which uses the thousands separator to format the number 100 million as the string "100,000,000".</span></span>  <br/> <span data-ttu-id="8380c-155">"#0,." は、1,000 の因数によるスケーリングを使用して、1 億を文字列 "100000" として書式設定します。</span><span class="sxs-lookup"><span data-stu-id="8380c-155">"#0,.", which uses scaling by a factor of one thousand to format the number 100 million as the string "100000".</span></span>  <br/> <span data-ttu-id="8380c-156">"#,0,." は、桁区切り記号と 1,000 の因数によるスケーリングを使用して、1 億を文字列 "100,000" として書式設定します。</span><span class="sxs-lookup"><span data-stu-id="8380c-156">"#,0,.", which uses the thousands separator and scaling by one thousand to format the number 100 million as the string "100,000".</span></span>  <br/> |
|<span data-ttu-id="8380c-157">: (コロン文字)</span><span class="sxs-lookup"><span data-stu-id="8380c-157">: (colon character)</span></span>  <br/> |<span data-ttu-id="8380c-p112">時刻区切り文字。一部のロケールでは、時刻区切り文字を表す目的で他の文字が使用されることがあります。時刻の値が書式設定されるときに、時刻区切り文字によって時、分、および秒が区切られます。書式設定された出力で時刻区切り文字として使用される実際の文字は、システム設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="8380c-p112">Time separator. In some locales, other characters may be used to represent the time separator. The time separator separates hours, minutes, and seconds when time values are formatted. The actual character that is used as the time separator in formatted output is determined by the system settings.</span></span>  <br/> |
|<span data-ttu-id="8380c-162">/ (スラッシュ)</span><span class="sxs-lookup"><span data-stu-id="8380c-162">/ (forward slash character)</span></span>  <br/> |<span data-ttu-id="8380c-p113">日付の区切り記号。ロケールによっては、他の文字が日付の区切り記号として表示される場合があります。日付値の書式が設定されている場合、日付、月、および年は、日付の区切り記号によって区切られます。書式設定された出力で、日付の区切り文字として実際に使用される文字は、システム設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="8380c-p113">Date separator. In some locales, other characters may be used to represent the date separator. The date separator separates the day, month, and year when date values are formatted. The actual character that is used as the date separator in formatted output is determined by the system settings.</span></span>  <br/> |
|<span data-ttu-id="8380c-167">**E-、E +、e-、e +**</span><span class="sxs-lookup"><span data-stu-id="8380c-167">**E- , E+ , e- , e+**</span></span> <br/> |<span data-ttu-id="8380c-p114">指数形式。書式指定式で、E-、E+、e-、または e+ の左に少なくとも 1 つの桁プレースホルダー (0 または #) がある場合、数値は、数値と指数部の間に E または e を挿入して指数形式で表示されます。左にある桁プレースホルダーの数で、指数の桁数が決まります。負の指数にマイナス記号を挿入するには、E- または e- を使用します。負の指数にマイナス記号を入れて、正の指数にプラス記号を入れるには、E+ または e+ を使用します。正しい書式を得るには、この記号の右に桁プレースホルダーを挿入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8380c-p114">Scientific format. If the format expression contains at least one digit placeholder (0 or #) to the left of E-, E+, e-, or e+, the number is displayed in scientific format and E or e is inserted between the number and its exponent. The number of digit placeholders to the left determines the number of digits in the exponent. Use E- or e- to place a minus sign next to negative exponents. Use E+ or e+ to place a minus sign next to negative exponents and a plus sign next to positive exponents. You must also include digit placeholders to the right side of this symbol to achieve correct formatting.</span></span>  <br/> |
|<span data-ttu-id="8380c-174">**- + $ ( )**</span><span class="sxs-lookup"><span data-stu-id="8380c-174">**- + $ ( )**</span></span> <br/> |<span data-ttu-id="8380c-175">リテラル文字です。</span><span class="sxs-lookup"><span data-stu-id="8380c-175">Literal characters.</span></span> <span data-ttu-id="8380c-176">これらの文字が書式指定文字列で入力したとおりに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8380c-176">These characters are displayed exactly as typed in the format string.</span></span> <span data-ttu-id="8380c-177">表示するには、一覧にない文字の前に円記号 (\)は、二重引用符で囲みます ("")。</span><span class="sxs-lookup"><span data-stu-id="8380c-177">To display a character other than one of those listed, precede it with a backslash (\) or enclose it in double quotation marks (" ").</span></span>  <br/> |
|<span data-ttu-id="8380c-178">\ (円記号)</span><span class="sxs-lookup"><span data-stu-id="8380c-178">\ (backward slash character)</span></span>  <br/> |<span data-ttu-id="8380c-179">書式指定文字列内の次の文字を表示します。</span><span class="sxs-lookup"><span data-stu-id="8380c-179">Displays the next character in the format string.</span></span> <span data-ttu-id="8380c-180">リテラル文字として特別な意味を持つ文字を表示するには、先頭に円記号 (\)。</span><span class="sxs-lookup"><span data-stu-id="8380c-180">To display a character that has special meaning as a literal character, precede it with a backslash (\).</span></span> <span data-ttu-id="8380c-181">円記号自体は表示されません。</span><span class="sxs-lookup"><span data-stu-id="8380c-181">The backslash itself isn't displayed.</span></span> <span data-ttu-id="8380c-182">円記号を使用して、次の文字を二重引用符で囲むことと同じです。</span><span class="sxs-lookup"><span data-stu-id="8380c-182">By using a backslash is the same as enclosing the next character in double quotation marks.</span></span> <span data-ttu-id="8380c-183">円記号を表示するには、2 つの円記号 () を使用 (\\)。</span><span class="sxs-lookup"><span data-stu-id="8380c-183">To display a backslash, use two backslashes (\\).</span></span>  <br/> <span data-ttu-id="8380c-184">日付書式と時刻書式指定文字は、リテラル文字として表示できない文字の例 (、c、d、h、m、n、p、q、s、t、w、y、:)、数値の書式設定文字 (#、0%、E、e、コンマ、ピリオド)、文字列の書式設定と文字 (@、 &amp;、 \<、\>と!)。</span><span class="sxs-lookup"><span data-stu-id="8380c-184">Examples of characters that can't be displayed as literal characters are the date-formatting and time-formatting characters (a, c, d, h, m, n, p, q, s, t, w, y, /, and :), the numeric-formatting characters (#, 0, %, E, e, comma, and period), and the string-formatting characters (@, &amp;, \<, \>, and !).</span></span>  <br/> |
|<span data-ttu-id="8380c-185">"ABC"</span><span class="sxs-lookup"><span data-stu-id="8380c-185">"ABC"</span></span>  <br/> |<span data-ttu-id="8380c-p117">二重引用符 (" ") で囲まれた文字列を表示します。コード内の style 引数に文字列を含めるには、Chr(34) を使ってテキストを囲みます (34 は引用符 (") を表す文字コードです)。</span><span class="sxs-lookup"><span data-stu-id="8380c-p117">Displays the string inside the double quotation marks (" "). To include a string in the style argument within code, you must use Chr(34) to enclose the text (34 is the character code for a quotation mark (")).</span></span>  <br/> |
   
<span data-ttu-id="8380c-p118">次の表には、数値のサンプルの書式指定式が含まれています (これらのすべての例では、システムのロケールが English-U.S. であることを想定しています)。最初の列には Format 関数の書式文字列が含まれています。別の列には、書式設定されたデータに列見出しの値がある場合の結果の出力が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8380c-p118">The following table contains some sample format expressions for numbers. (These examples all assume that your system's locale setting is English-U.S.) The first column contains the format strings for the Format function. The other columns contain the resulting output if the formatted data has the value given in the column headings.</span></span>
  
|<span data-ttu-id="8380c-191">**形式 (スタイル)**</span><span class="sxs-lookup"><span data-stu-id="8380c-191">**Format (Style)**</span></span>|<span data-ttu-id="8380c-192">**として「5」の書式設定**</span><span class="sxs-lookup"><span data-stu-id="8380c-192">**"5" formatted as**</span></span>|<span data-ttu-id="8380c-193">**「-5」として書式設定**</span><span class="sxs-lookup"><span data-stu-id="8380c-193">**"-5" formatted as**</span></span>|<span data-ttu-id="8380c-194">**として書式設定された「0.5」**</span><span class="sxs-lookup"><span data-stu-id="8380c-194">**"0.5" formatted as**</span></span>|<span data-ttu-id="8380c-195">**として「0」の書式設定**</span><span class="sxs-lookup"><span data-stu-id="8380c-195">**"0" formatted as**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8380c-196">長さがゼロの文字列 ("")。</span><span class="sxs-lookup"><span data-stu-id="8380c-196">Zero-length string ("")</span></span>  <br/> |<span data-ttu-id="8380c-197">5</span><span class="sxs-lookup"><span data-stu-id="8380c-197">5</span></span>  <br/> |<span data-ttu-id="8380c-198">-5</span><span class="sxs-lookup"><span data-stu-id="8380c-198">-5</span></span>  <br/> |<span data-ttu-id="8380c-199">0.5</span><span class="sxs-lookup"><span data-stu-id="8380c-199">0.5</span></span>  <br/> |<span data-ttu-id="8380c-200">0</span><span class="sxs-lookup"><span data-stu-id="8380c-200">0</span></span>  <br/> |
|<span data-ttu-id="8380c-201">0</span><span class="sxs-lookup"><span data-stu-id="8380c-201">0</span></span>  <br/> |<span data-ttu-id="8380c-202">5</span><span class="sxs-lookup"><span data-stu-id="8380c-202">5</span></span>  <br/> |<span data-ttu-id="8380c-203">-5</span><span class="sxs-lookup"><span data-stu-id="8380c-203">-5</span></span>  <br/> |<span data-ttu-id="8380c-204">1</span><span class="sxs-lookup"><span data-stu-id="8380c-204">1</span></span>  <br/> |<span data-ttu-id="8380c-205">0</span><span class="sxs-lookup"><span data-stu-id="8380c-205">0</span></span>  <br/> |
|<span data-ttu-id="8380c-206">0.00</span><span class="sxs-lookup"><span data-stu-id="8380c-206">0.00</span></span>  <br/> |<span data-ttu-id="8380c-207">5.00</span><span class="sxs-lookup"><span data-stu-id="8380c-207">5.00</span></span>  <br/> |<span data-ttu-id="8380c-208">-5.00</span><span class="sxs-lookup"><span data-stu-id="8380c-208">-5.00</span></span>  <br/> |<span data-ttu-id="8380c-209">0.50</span><span class="sxs-lookup"><span data-stu-id="8380c-209">0.50</span></span>  <br/> |<span data-ttu-id="8380c-210">0.00</span><span class="sxs-lookup"><span data-stu-id="8380c-210">0.00</span></span>  <br/> |
|<span data-ttu-id="8380c-211">#,##0</span><span class="sxs-lookup"><span data-stu-id="8380c-211">#,##0</span></span>  <br/> |<span data-ttu-id="8380c-212">5</span><span class="sxs-lookup"><span data-stu-id="8380c-212">5</span></span>  <br/> |<span data-ttu-id="8380c-213">-5</span><span class="sxs-lookup"><span data-stu-id="8380c-213">-5</span></span>  <br/> |<span data-ttu-id="8380c-214">1</span><span class="sxs-lookup"><span data-stu-id="8380c-214">1</span></span>  <br/> |<span data-ttu-id="8380c-215">0</span><span class="sxs-lookup"><span data-stu-id="8380c-215">0</span></span>  <br/> |
|<span data-ttu-id="8380c-216">$#,##0;($#,##0)</span><span class="sxs-lookup"><span data-stu-id="8380c-216">$#,##0;($#,##0)</span></span>  <br/> |<span data-ttu-id="8380c-217">$5</span><span class="sxs-lookup"><span data-stu-id="8380c-217">$5</span></span>  <br/> |<span data-ttu-id="8380c-218">($5)</span><span class="sxs-lookup"><span data-stu-id="8380c-218">($5)</span></span>  <br/> |<span data-ttu-id="8380c-219">$1</span><span class="sxs-lookup"><span data-stu-id="8380c-219">$1</span></span>  <br/> |<span data-ttu-id="8380c-220">$0</span><span class="sxs-lookup"><span data-stu-id="8380c-220">$0</span></span>  <br/> |
|<span data-ttu-id="8380c-221">$#,##0.00;($#,##0.00)</span><span class="sxs-lookup"><span data-stu-id="8380c-221">$#,##0.00;($#,##0.00)</span></span>  <br/> |<span data-ttu-id="8380c-222">500 円</span><span class="sxs-lookup"><span data-stu-id="8380c-222">$5.00</span></span>  <br/> |<span data-ttu-id="8380c-223">(500 円)</span><span class="sxs-lookup"><span data-stu-id="8380c-223">($5.00)</span></span>  <br/> |<span data-ttu-id="8380c-224">0.50 ドル</span><span class="sxs-lookup"><span data-stu-id="8380c-224">$0.50</span></span>  <br/> |<span data-ttu-id="8380c-225">0.00 ドル</span><span class="sxs-lookup"><span data-stu-id="8380c-225">$0.00</span></span>  <br/> |
|<span data-ttu-id="8380c-226">0%</span><span class="sxs-lookup"><span data-stu-id="8380c-226">0%</span></span>  <br/> |<span data-ttu-id="8380c-227">500%</span><span class="sxs-lookup"><span data-stu-id="8380c-227">500%</span></span>  <br/> |<span data-ttu-id="8380c-228">-500%</span><span class="sxs-lookup"><span data-stu-id="8380c-228">-500%</span></span>  <br/> |<span data-ttu-id="8380c-229">50%</span><span class="sxs-lookup"><span data-stu-id="8380c-229">50%</span></span>  <br/> |<span data-ttu-id="8380c-230">0%</span><span class="sxs-lookup"><span data-stu-id="8380c-230">0%</span></span>  <br/> |
|<span data-ttu-id="8380c-231">0.00%</span><span class="sxs-lookup"><span data-stu-id="8380c-231">0.00%</span></span>  <br/> |<span data-ttu-id="8380c-232">500.00%</span><span class="sxs-lookup"><span data-stu-id="8380c-232">500.00%</span></span>  <br/> |<span data-ttu-id="8380c-233">-500.00%</span><span class="sxs-lookup"><span data-stu-id="8380c-233">-500.00%</span></span>  <br/> |<span data-ttu-id="8380c-234">50.00%</span><span class="sxs-lookup"><span data-stu-id="8380c-234">50.00%</span></span>  <br/> |<span data-ttu-id="8380c-235">0.00%</span><span class="sxs-lookup"><span data-stu-id="8380c-235">0.00%</span></span>  <br/> |
|<span data-ttu-id="8380c-236">0.00 E + 00</span><span class="sxs-lookup"><span data-stu-id="8380c-236">0.00E+00</span></span>  <br/> |<span data-ttu-id="8380c-237">5.00E + 00</span><span class="sxs-lookup"><span data-stu-id="8380c-237">5.00E+00</span></span>  <br/> |<span data-ttu-id="8380c-238">-5.00E + 00</span><span class="sxs-lookup"><span data-stu-id="8380c-238">-5.00E+00</span></span>  <br/> |<span data-ttu-id="8380c-239">5.00E-01</span><span class="sxs-lookup"><span data-stu-id="8380c-239">5.00E-01</span></span>  <br/> |<span data-ttu-id="8380c-240">0.00 E + 00</span><span class="sxs-lookup"><span data-stu-id="8380c-240">0.00E+00</span></span>  <br/> |
|<span data-ttu-id="8380c-241">0.00E-00</span><span class="sxs-lookup"><span data-stu-id="8380c-241">0.00E-00</span></span>  <br/> |<span data-ttu-id="8380c-242">5.00E00</span><span class="sxs-lookup"><span data-stu-id="8380c-242">5.00E00</span></span>  <br/> |<span data-ttu-id="8380c-243">-5.00E00</span><span class="sxs-lookup"><span data-stu-id="8380c-243">-5.00E00</span></span>  <br/> |<span data-ttu-id="8380c-244">5.00E-01</span><span class="sxs-lookup"><span data-stu-id="8380c-244">5.00E-01</span></span>  <br/> |<span data-ttu-id="8380c-245">0.00E00</span><span class="sxs-lookup"><span data-stu-id="8380c-245">0.00E00</span></span>  <br/> |
|<span data-ttu-id="8380c-246">"$#,##0;;\Z\e\r\o"</span><span class="sxs-lookup"><span data-stu-id="8380c-246">"$#,##0;;\Z\e\r\o"</span></span>  <br/> |<span data-ttu-id="8380c-247">$5</span><span class="sxs-lookup"><span data-stu-id="8380c-247">$5</span></span>  <br/> |<span data-ttu-id="8380c-248">$-5</span><span class="sxs-lookup"><span data-stu-id="8380c-248">$-5</span></span>  <br/> |<span data-ttu-id="8380c-249">$1</span><span class="sxs-lookup"><span data-stu-id="8380c-249">$1</span></span>  <br/> |<span data-ttu-id="8380c-250">ゼロ</span><span class="sxs-lookup"><span data-stu-id="8380c-250">Zero</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8380c-251">解説</span><span class="sxs-lookup"><span data-stu-id="8380c-251">Remarks</span></span>
<span data-ttu-id="8380c-252"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="8380c-252"></span></span>

<span data-ttu-id="8380c-253">間に何も入れずに複数のセミコロンを含めた場合、欠けているセクションは、正の値の書式を使用して表示されます。</span><span class="sxs-lookup"><span data-stu-id="8380c-253">If you include semicolons with nothing between them, the missing section is displayed by using the format of the positive value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8380c-254">関連項目</span><span class="sxs-lookup"><span data-stu-id="8380c-254">See also</span></span>

- [<span data-ttu-id="8380c-255">Format 関数 (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="8380c-255">Format Function (Access custom web app)</span></span>](format-function-access-custom-web-app.md) 
- [<span data-ttu-id="8380c-256">Format 関数 (カスタム web アプリケーションのアクセス) のユーザー設定の日付と時刻の書式を設定します。</span><span class="sxs-lookup"><span data-stu-id="8380c-256">Custom date and time formats for the Format function (Access custom web app)</span></span>](custom-date-and-time-formats-for-the-format-function-access-custom-web-app.md)
  
