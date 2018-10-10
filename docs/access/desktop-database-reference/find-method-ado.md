---
title: メソッドを検索するには、ActiveX データ オブジェクト (ADO)
TOCTitle: Find Method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc78503008daa733e747923697f21917ada8c106
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477514"
---
# <a name="find-method-ado"></a><span data-ttu-id="e53d7-102">Find メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="e53d7-102">Find Method (ADO)</span></span>


<span data-ttu-id="e53d7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e53d7-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="e53d7-p101">[Recordset](recordset-object-ado.md) から、指定した条件を満たす行を検索します。必要に応じて、検索の方向、開始行、および開始行からのオフセットを指定できます。条件が一致すると、カレント行の位置は、検出されたレコードに設定され、条件を満たす行がない場合は、 **Recordset** の最後 (または最初) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e53d7-p101">Searches a [Recordset](recordset-object-ado.md) for the row that satisfies the specified criteria. Optionally, the direction of the search, starting row, and offset from the starting row may be specified. If the criteria is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e53d7-107">構文</span><span class="sxs-lookup"><span data-stu-id="e53d7-107">Syntax</span></span>

<span data-ttu-id="e53d7-108">(*条件*、 *SkipRows*、 *SearchDirection*、*開始*) を検索します。</span><span class="sxs-lookup"><span data-stu-id="e53d7-108">Find (*Criteria*, *SkipRows*, *SearchDirection*, *Start*)</span></span>

## <a name="parameters"></a><span data-ttu-id="e53d7-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e53d7-109">Parameters</span></span>

  - <span data-ttu-id="e53d7-110">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="e53d7-110">*Criteria*</span></span>

  - <span data-ttu-id="e53d7-111">検索に使用する列の名前、比較演算子、および値を指定するステートメントを含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e53d7-111">A **String** value that contains a statement specifying the column name, comparison operator, and value to use in the search.</span></span>

  - <span data-ttu-id="e53d7-112">*SkipRows*</span><span class="sxs-lookup"><span data-stu-id="e53d7-112">*SkipRows*</span></span>

  - <span data-ttu-id="e53d7-113">省略可能な *.*</span><span class="sxs-lookup"><span data-stu-id="e53d7-113">Optional *.*</span></span> <span data-ttu-id="e53d7-114">既定値が 0 で、現在の行または検索を開始するのにはブックマークの*開始*から行のオフセットを指定する**Long**値。</span><span class="sxs-lookup"><span data-stu-id="e53d7-114">A **Long** value, whose default value is zero, that specifies the row offset from the current row or *Start* bookmark to begin the search.</span></span> <span data-ttu-id="e53d7-115">既定では、現在の行で、検索を開始します。</span><span class="sxs-lookup"><span data-stu-id="e53d7-115">By default, the search will start on the current row.</span></span>

  - <span data-ttu-id="e53d7-116">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="e53d7-116">*SearchDirection*</span></span>

  - <span data-ttu-id="e53d7-117">省略可能な *.*</span><span class="sxs-lookup"><span data-stu-id="e53d7-117">Optional *.*</span></span> <span data-ttu-id="e53d7-118">現在の行、または、検索の方向の次の使用可能な行の検索を開始するかどうかを指定する[SearchDirectionEnum](searchdirectionenum.md)の値です。</span><span class="sxs-lookup"><span data-stu-id="e53d7-118">A [SearchDirectionEnum](searchdirectionenum.md) value that specifies whether the search should begin on the current row or the next available row in the direction of the search.</span></span> <span data-ttu-id="e53d7-119">検索が失敗したは、値が**adSearchForward**である場合、**レコード セット**の最後で停止します。</span><span class="sxs-lookup"><span data-stu-id="e53d7-119">An unsuccessful search stops at the end of the **Recordset** if the value is **adSearchForward**.</span></span> <span data-ttu-id="e53d7-120">検索が失敗したは、値が**adSearchBackward**である場合、**レコード セット**の先頭で停止します。</span><span class="sxs-lookup"><span data-stu-id="e53d7-120">An unsuccessful search stops at the start of the **Recordset** if the value is **adSearchBackward**.</span></span>

  - <span data-ttu-id="e53d7-121">*Start*</span><span class="sxs-lookup"><span data-stu-id="e53d7-121">*Start*</span></span>

  - <span data-ttu-id="e53d7-p104">省略可能です。検索の開始位置として使用する、バリアント型 ( **Variant** ) のブックマークを指定します。</span><span class="sxs-lookup"><span data-stu-id="e53d7-p104">Optional. A **Variant** bookmark that functions as the starting position for the search.</span></span>

## <a name="remarks"></a><span data-ttu-id="e53d7-124">解説</span><span class="sxs-lookup"><span data-stu-id="e53d7-124">Remarks</span></span>

<span data-ttu-id="e53d7-p105">*criteria* には、列の名前を 1 つだけ指定できます。このメソッドでは、複数列の検索はサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="e53d7-p105">Only a single-column name may be specified in *criteria*. This method does not support multi-column searches.</span></span>

<span data-ttu-id="e53d7-127">*条件*で比較演算子があります」**\>**」(より大きい)、「**\<**(より小さい)、「=」(等号) にした場合は、「\>=」(より大きいか等しい)、"\<=」(以上)、"\<\>」(等しくない)、"like"(パターン マッチング)、または。</span><span class="sxs-lookup"><span data-stu-id="e53d7-127">The comparison operator in *Criteria* may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="e53d7-128">文字列、浮動小数点数、または日付の*抽出条件*の値があります。</span><span class="sxs-lookup"><span data-stu-id="e53d7-128">The value in *Criteria* may be a string, floating-point number, or date.</span></span> <span data-ttu-id="e53d7-129">文字列値は単一引用符で区切られたまたは」\#」(シャープ記号) のマークを付けます (など、"状態 = 'WA'」または」状態 = \#WA\#」)。</span><span class="sxs-lookup"><span data-stu-id="e53d7-129">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="e53d7-130">区切られた日付の値"\#」(シャープ記号) のマークを付けます (などの"開始\_日\> \#7/22/97\#」) 時間を含めることができます、分および秒を示すには、タイム ・ スタンプが、ミリ秒が含まれていない必要がありますか、エラーが発生して.</span><span class="sxs-lookup"><span data-stu-id="e53d7-130">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#") and can contain hours, minutes and seconds to indicate time stamps but should not contain milliseconds or errors will occur.</span></span>

<span data-ttu-id="e53d7-p107">比較演算子に "like"を使用する場合、文字列値にアスタリスク (\*) を含めると、1 つまたは複数の文字、または部分文字列を検索することができます。たとえば、「state like 'M\*'」と指定すると、Maine や Massachusetts が該当します。また、文字列の先頭と末尾にアスタリスクを使用して、その間に含まれる部分文字列を検索対象として指定することもできます。たとえば、「state like '\*as\*'」と指定すると、Alaska、Arkansas、および Massachusetts が該当します。</span><span class="sxs-lookup"><span data-stu-id="e53d7-p107">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring. For example, "state like 'M\*'" matches Maine and Massachusetts. You can also use leading and trailing asterisks to find a substring contained within the values. For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="e53d7-p108">上の例のように、アスタリスクは、検索文字列の末尾のみに使用するか、または検索文字列の先頭と末尾の両方で使用することができます。ただし、先頭のみのワイルドカード ('\*str') または文字列中のワイルドカード ('s\*r') としてアスタリスクを使用することはできません。この場合はエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e53d7-p108">Asterisks can be used only at the end of a criteria string, or together at both the beginning and end of a criteria string, as shown above. You cannot use the asterisk as a leading wildcard ('\*str'), or embedded wildcard ('s\*r'). This will cause an error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e53d7-p109">[!メモ] <STRONG>Find</STRONG> メソッドを呼び出す前にカレント行の位置が設定されていない場合は、エラーが発生します。 <A href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Find</A> メソッドを呼び出す前に、 <STRONG>MoveFirst</STRONG> などの、行の位置を設定するメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e53d7-p109">An error will occur if a current row position is not set before calling <STRONG>Find</STRONG>. Any method that sets row position, such as <A href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</A>, should be called before calling <STRONG>Find</STRONG>.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="e53d7-p110">[!メモ] レコードセットに対して <STRONG>Find</STRONG> メソッドを呼び出す場合で、レコードセット内の現在の位置が最後のレコードまたはファイルの最後 (EOF) の場合、何も検索されません。あらかじめ <STRONG>MoveFirst</STRONG> メソッドを呼び出して、現在の位置またはカーソルをレコードセットの先頭に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e53d7-p110">If you call the <STRONG>Find</STRONG> method on a recordset, and the current position in the recordset is at the last record or end of file (EOF), you will not find anything. You need to call the <STRONG>MoveFirst</STRONG> method to set the current position/cursor to the beginning of the recordset.</span></span></P>


