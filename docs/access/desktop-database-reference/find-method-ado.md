---
title: メソッドを検索するには、ActiveX データ オブジェクト (ADO)
TOCTitle: Find method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa7dc2361d31a6d18af3c381dd75f8f934e78e05
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949881"
---
# <a name="find-method-ado"></a><span data-ttu-id="6ddd7-102">Find メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="6ddd7-102">Find method (ADO)</span></span>

<span data-ttu-id="6ddd7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ddd7-p101">[Recordset](recordset-object-ado.md) から、指定した条件を満たす行を検索します。必要に応じて、検索の方向、開始行、および開始行からのオフセットを指定できます。条件が一致すると、カレント行の位置は、検出されたレコードに設定され、条件を満たす行がない場合は、 **Recordset** の最後 (または最初) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-p101">Searches a [Recordset](recordset-object-ado.md) for the row that satisfies the specified criteria. Optionally, the direction of the search, starting row, and offset from the starting row may be specified. If the criteria is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ddd7-107">構文</span><span class="sxs-lookup"><span data-stu-id="6ddd7-107">Syntax</span></span>

<span data-ttu-id="6ddd7-108">(*条件*、 *SkipRows*、 *SearchDirection*、*開始*) を検索します。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-108">Find (*Criteria*, *SkipRows*, *SearchDirection*, *Start*)</span></span>

## <a name="parameters"></a><span data-ttu-id="6ddd7-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6ddd7-109">Parameters</span></span>

|<span data-ttu-id="6ddd7-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6ddd7-110">Parameter</span></span>|<span data-ttu-id="6ddd7-111">説明</span><span class="sxs-lookup"><span data-stu-id="6ddd7-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6ddd7-112">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="6ddd7-112">*Criteria*</span></span> |<span data-ttu-id="6ddd7-113">検索に使用する列の名前、比較演算子、および値を指定するステートメントを含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-113">A **String** value that contains a statement specifying the column name, comparison operator, and value to use in the search.</span></span>|
|<span data-ttu-id="6ddd7-114">*SkipRows*</span><span class="sxs-lookup"><span data-stu-id="6ddd7-114">*SkipRows*</span></span> |<span data-ttu-id="6ddd7-115">省略可能。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-115">Optional.</span></span> <span data-ttu-id="6ddd7-116">既定値が 0 で、現在の行または検索を開始するのにはブックマークの*開始*から行のオフセットを指定する**Long**値。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-116">A **Long** value, whose default value is zero, that specifies the row offset from the current row or *Start* bookmark to begin the search.</span></span> <span data-ttu-id="6ddd7-117">既定では、現在の行で、検索を開始します。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-117">By default, the search will start on the current row.</span></span>|
|<span data-ttu-id="6ddd7-118">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="6ddd7-118">*SearchDirection*</span></span> |<span data-ttu-id="6ddd7-119">省略可能。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-119">Optional.</span></span> <span data-ttu-id="6ddd7-120">現在の行、または、検索の方向の次の使用可能な行の検索を開始するかどうかを指定する[SearchDirectionEnum](searchdirectionenum.md)の値です。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-120">A [SearchDirectionEnum](searchdirectionenum.md) value that specifies whether the search should begin on the current row or the next available row in the direction of the search.</span></span> <span data-ttu-id="6ddd7-121">検索が失敗したは、値が**adSearchForward**である場合、**レコード セット**の最後で停止します。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-121">An unsuccessful search stops at the end of the **Recordset** if the value is **adSearchForward**.</span></span> <span data-ttu-id="6ddd7-122">検索が失敗したは、値が**adSearchBackward**である場合、**レコード セット**の先頭で停止します。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-122">An unsuccessful search stops at the start of the **Recordset** if the value is **adSearchBackward**.</span></span>|
|<span data-ttu-id="6ddd7-123">*Start*</span><span class="sxs-lookup"><span data-stu-id="6ddd7-123">*Start*</span></span> |<span data-ttu-id="6ddd7-p104">省略可能です。検索の開始位置として使用する、バリアント型 ( **Variant** ) のブックマークを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-p104">Optional. A **Variant** bookmark that functions as the starting position for the search.</span></span>|

## <a name="remarks"></a><span data-ttu-id="6ddd7-126">解説</span><span class="sxs-lookup"><span data-stu-id="6ddd7-126">Remarks</span></span>

<span data-ttu-id="6ddd7-p105">*criteria* には、列の名前を 1 つだけ指定できます。このメソッドでは、複数列の検索はサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-p105">Only a single-column name may be specified in *criteria*. This method does not support multi-column searches.</span></span>

<span data-ttu-id="6ddd7-129">*条件*で比較演算子があります」**\>**」(より大きい)、「**\<**(より小さい)、「=」(等号) にした場合は、「\>=」(より大きいか等しい)、"\<=」(以上)、"\<\>」(等しくない)、"like"(パターン マッチング)、または。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-129">The comparison operator in *Criteria* may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="6ddd7-130">文字列、浮動小数点数、または日付の*抽出条件*の値があります。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-130">The value in *Criteria* may be a string, floating-point number, or date.</span></span> <span data-ttu-id="6ddd7-131">文字列値は単一引用符で区切られたまたは」\#」(シャープ記号) のマークを付けます (など、"状態 = 'WA'」または」状態 = \#WA\#」)。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-131">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="6ddd7-132">区切られた日付の値"\#」(シャープ記号) のマークを付けます (などの"開始\_日\> \#7/22/97\#」) 時間を含めることができます、分および秒を示すには、タイム ・ スタンプが、ミリ秒が含まれていない必要がありますか、エラーが発生して.</span><span class="sxs-lookup"><span data-stu-id="6ddd7-132">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#") and can contain hours, minutes and seconds to indicate time stamps but should not contain milliseconds or errors will occur.</span></span>

<span data-ttu-id="6ddd7-p107">比較演算子に "like"を使用する場合、文字列値にアスタリスク (\*) を含めると、1 つまたは複数の文字、または部分文字列を検索することができます。たとえば、「state like 'M\*'」と指定すると、Maine や Massachusetts が該当します。また、文字列の先頭と末尾にアスタリスクを使用して、その間に含まれる部分文字列を検索対象として指定することもできます。たとえば、「state like '\*as\*'」と指定すると、Alaska、Arkansas、および Massachusetts が該当します。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-p107">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring. For example, "state like 'M\*'" matches Maine and Massachusetts. You can also use leading and trailing asterisks to find a substring contained within the values. For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="6ddd7-p108">上の例のように、アスタリスクは、検索文字列の末尾のみに使用するか、または検索文字列の先頭と末尾の両方で使用することができます。ただし、先頭のみのワイルドカード ('\*str') または文字列中のワイルドカード ('s\*r') としてアスタリスクを使用することはできません。この場合はエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-p108">Asterisks can be used only at the end of a criteria string, or together at both the beginning and end of a criteria string, as shown above. You cannot use the asterisk as a leading wildcard ('\*str'), or embedded wildcard ('s\*r'). This will cause an error.</span></span>

> [!NOTE]
> <span data-ttu-id="6ddd7-p109">[!メモ] **Find** メソッドを呼び出す前にカレント行の位置が設定されていない場合は、エラーが発生します。 [Find](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) メソッドを呼び出す前に、 **MoveFirst** などの、行の位置を設定するメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-p109">An error will occur if a current row position is not set before calling **Find**. Any method that sets row position, such as [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), should be called before calling **Find**.</span></span>

> [!NOTE]
> <span data-ttu-id="6ddd7-p110">[!メモ] レコードセットに対して **Find** メソッドを呼び出す場合で、レコードセット内の現在の位置が最後のレコードまたはファイルの最後 (EOF) の場合、何も検索されません。あらかじめ **MoveFirst** メソッドを呼び出して、現在の位置またはカーソルをレコードセットの先頭に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ddd7-p110">If you call the **Find** method on a recordset, and the current position in the recordset is at the last record or end of file (EOF), you will not find anything. You need to call the **MoveFirst** method to set the current position/cursor to the beginning of the recordset.</span></span>


