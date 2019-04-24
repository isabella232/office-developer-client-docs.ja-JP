---
title: Find メソッド-ActiveX データオブジェクト (ADO)
TOCTitle: Find method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32f14e4aeed669e68d976559932306c3cb76c696
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292413"
---
# <a name="find-method-ado"></a><span data-ttu-id="c4c24-102">Find メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="c4c24-102">Find method (ADO)</span></span>

<span data-ttu-id="c4c24-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4c24-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4c24-p101">[Recordset](recordset-object-ado.md) から、指定した条件を満たす行を検索します。必要に応じて、検索の方向、開始行、および開始行からのオフセットを指定できます。条件が一致すると、カレント行の位置は、検出されたレコードに設定され、条件を満たす行がない場合は、 **Recordset** の最後 (または最初) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c4c24-p101">Searches a [Recordset](recordset-object-ado.md) for the row that satisfies the specified criteria. Optionally, the direction of the search, starting row, and offset from the starting row may be specified. If the criteria is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c24-107">構文</span><span class="sxs-lookup"><span data-stu-id="c4c24-107">Syntax</span></span>

<span data-ttu-id="c4c24-108">Find (*Criteria*、 *SkipRows*、 *searchdirection*、 *Start*)</span><span class="sxs-lookup"><span data-stu-id="c4c24-108">Find (*Criteria*, *SkipRows*, *SearchDirection*, *Start*)</span></span>

## <a name="parameters"></a><span data-ttu-id="c4c24-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c4c24-109">Parameters</span></span>

|<span data-ttu-id="c4c24-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c4c24-110">Parameter</span></span>|<span data-ttu-id="c4c24-111">説明</span><span class="sxs-lookup"><span data-stu-id="c4c24-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c4c24-112">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="c4c24-112">*Criteria*</span></span> |<span data-ttu-id="c4c24-113">検索に使用する列の名前、比較演算子、および値を指定するステートメントを含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4c24-113">A **String** value that contains a statement specifying the column name, comparison operator, and value to use in the search.</span></span>|
|<span data-ttu-id="c4c24-114">*SkipRows*</span><span class="sxs-lookup"><span data-stu-id="c4c24-114">*SkipRows*</span></span> |<span data-ttu-id="c4c24-115">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="c4c24-115">Optional.</span></span> <span data-ttu-id="c4c24-116">既定値が0で、検索を開始するために現在の行または*開始*ブックマークからの行のオフセットを指定する**長整数型 (Long)** の値です。</span><span class="sxs-lookup"><span data-stu-id="c4c24-116">A **Long** value, whose default value is zero, that specifies the row offset from the current row or *Start* bookmark to begin the search.</span></span> <span data-ttu-id="c4c24-117">By default, the search will start on the current row.</span><span class="sxs-lookup"><span data-stu-id="c4c24-117">By default, the search will start on the current row.</span></span>|
|<span data-ttu-id="c4c24-118">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="c4c24-118">*SearchDirection*</span></span> |<span data-ttu-id="c4c24-119">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="c4c24-119">Optional.</span></span> <span data-ttu-id="c4c24-120">A [SearchDirectionEnum](searchdirectionenum.md) value that specifies whether the search should begin on the current row or the next available row in the direction of the search.</span><span class="sxs-lookup"><span data-stu-id="c4c24-120">A [SearchDirectionEnum](searchdirectionenum.md) value that specifies whether the search should begin on the current row or the next available row in the direction of the search.</span></span> <span data-ttu-id="c4c24-121">An unsuccessful search stops at the end of the **Recordset** if the value is **adSearchForward**.</span><span class="sxs-lookup"><span data-stu-id="c4c24-121">An unsuccessful search stops at the end of the **Recordset** if the value is **adSearchForward**.</span></span> <span data-ttu-id="c4c24-122">An unsuccessful search stops at the start of the **Recordset** if the value is **adSearchBackward**.</span><span class="sxs-lookup"><span data-stu-id="c4c24-122">An unsuccessful search stops at the start of the **Recordset** if the value is **adSearchBackward**.</span></span>|
|<span data-ttu-id="c4c24-123">*Start*</span><span class="sxs-lookup"><span data-stu-id="c4c24-123">*Start*</span></span> |<span data-ttu-id="c4c24-p104">省略可能です。検索の開始位置として使用する、バリアント型 ( **Variant** ) のブックマークを指定します。</span><span class="sxs-lookup"><span data-stu-id="c4c24-p104">Optional. A **Variant** bookmark that functions as the starting position for the search.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c4c24-126">注釈</span><span class="sxs-lookup"><span data-stu-id="c4c24-126">Remarks</span></span>

<span data-ttu-id="c4c24-p105">*criteria* には、列の名前を 1 つだけ指定できます。このメソッドでは、複数列の検索はサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c4c24-p105">Only a single-column name may be specified in *criteria*. This method does not support multi-column searches.</span></span>

<span data-ttu-id="c4c24-129">*条件*の比較演算子には、"**\>**" (より大きい)、"**\<**" (より小さい)、"=" (等しい)、"\>=" (より大きいまたは等しい)、\<"=" (以下)、"\<\>" (等しくない)、または "like" (パターンマッチング) のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="c4c24-129">The comparison operator in *Criteria* may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="c4c24-130">*抽出条件*の値には、文字列、浮動小数点数、または日付を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c4c24-130">The value in *Criteria* may be a string, floating-point number, or date.</span></span> <span data-ttu-id="c4c24-131">文字列型 (String) の値は、\#一重引用符または "" (シャープ記号) マークで区切られます (たとえば、"state = \#'\#WA '" または "state = WA")。</span><span class="sxs-lookup"><span data-stu-id="c4c24-131">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="c4c24-132">日付の値は\#、\_ \> \#\#"" (シャープ記号) マークで区切られており、タイムスタンプを示すのに時間、分、および秒を含めることができますが、ミリ秒またはエラーが発生することはありません。.</span><span class="sxs-lookup"><span data-stu-id="c4c24-132">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#") and can contain hours, minutes and seconds to indicate time stamps but should not contain milliseconds or errors will occur.</span></span>

<span data-ttu-id="c4c24-p107">比較演算子に "like"を使用する場合、文字列値にアスタリスク (\*) を含めると、1 つまたは複数の文字、または部分文字列を検索することができます。たとえば、「state like 'M\*'」と指定すると、Maine や Massachusetts が該当します。また、文字列の先頭と末尾にアスタリスクを使用して、その間に含まれる部分文字列を検索対象として指定することもできます。たとえば、「state like '\*as\*'」と指定すると、Alaska、Arkansas、および Massachusetts が該当します。</span><span class="sxs-lookup"><span data-stu-id="c4c24-p107">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring. For example, "state like 'M\*'" matches Maine and Massachusetts. You can also use leading and trailing asterisks to find a substring contained within the values. For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="c4c24-p108">上の例のように、アスタリスクは、検索文字列の末尾のみに使用するか、または検索文字列の先頭と末尾の両方で使用することができます。ただし、先頭のみのワイルドカード ('\*str') または文字列中のワイルドカード ('s\*r') としてアスタリスクを使用することはできません。この場合はエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="c4c24-p108">Asterisks can be used only at the end of a criteria string, or together at both the beginning and end of a criteria string, as shown above. You cannot use the asterisk as a leading wildcard ('\*str'), or embedded wildcard ('s\*r'). This will cause an error.</span></span>

> [!NOTE]
> <span data-ttu-id="c4c24-p109">[!メモ] **Find** メソッドを呼び出す前にカレント行の位置が設定されていない場合は、エラーが発生します。 [Find](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) メソッドを呼び出す前に、 **MoveFirst** などの、行の位置を設定するメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4c24-p109">An error will occur if a current row position is not set before calling **Find**. Any method that sets row position, such as [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), should be called before calling **Find**.</span></span>

> [!NOTE]
> <span data-ttu-id="c4c24-p110">[!メモ] レコードセットに対して **Find** メソッドを呼び出す場合で、レコードセット内の現在の位置が最後のレコードまたはファイルの最後 (EOF) の場合、何も検索されません。あらかじめ **MoveFirst** メソッドを呼び出して、現在の位置またはカーソルをレコードセットの先頭に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4c24-p110">If you call the **Find** method on a recordset, and the current position in the recordset is at the last record or end of file (EOF), you will not find anything. You need to call the **MoveFirst** method to set the current position/cursor to the beginning of the recordset.</span></span>


