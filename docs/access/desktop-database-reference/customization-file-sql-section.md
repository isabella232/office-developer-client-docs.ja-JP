---
title: カスタマイズ ファイルの SQL セクション
TOCTitle: Customization File SQL Section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09be671ba15727e3612ade78c5b54af12b1d1c57
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476553"
---
# <a name="customization-file-sql-section"></a><span data-ttu-id="75586-102">カスタマイズ ファイルの SQL セクション</span><span class="sxs-lookup"><span data-stu-id="75586-102">Customization File SQL Section</span></span>


<span data-ttu-id="75586-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="75586-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="75586-p101">**sql** セクションには、クライアントのコマンド文字列を置き換える新規 SQL 文字列を含めることができます。このセクションに SQL 文字列がない場合、このセクションは無視されます。</span><span class="sxs-lookup"><span data-stu-id="75586-p101">The **sql** section can contain a new SQL string that replaces the client command string. If there is no SQL string in the section, the section will be ignored.</span></span>

<span data-ttu-id="75586-106">新規 SQL 文字列は、*パラメーター化された*可能性があります。</span><span class="sxs-lookup"><span data-stu-id="75586-106">The new SQL string may be *parameterized*.</span></span> <span data-ttu-id="75586-107">つまり、(かっこで囲まれたコンマ区切りのリストで指定)、クライアントのコマンド文字列の*識別子*に対応する引数 ('?' の文字で指定)、 **sql**セクションの SQL 文字列内のパラメーターを置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="75586-107">That is, parameters in the **sql** section SQL string (designated by the '?' character) can be replaced by corresponding arguments in an *identifier* in the client command string (designated by a comma-delimited list in parentheses).</span></span> <span data-ttu-id="75586-108">識別子と引数のリストは、関数呼び出しと同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="75586-108">The identifier and argument list behave like a function call.</span></span>

<span data-ttu-id="75586-109">たとえば、SQL セクション ヘッダーは、クライアントのコマンド文字列は、"CustomerByID(4)"を\[SQL CustomerByID\] 、新しい SQL セクションの文字列で、"を選択\*お客様の場所を [得意先コード] から = の ?」です。</span><span class="sxs-lookup"><span data-stu-id="75586-109">For example, assume the client command string is "CustomerByID(4)" , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="75586-110">ハンドラーを生成しますが、SQL セクション ヘッダーは、 \[SQL CustomerByID\] 、新しい SQL セクションの文字列で、"を選択\*お客様の場所を [得意先コード] から = の ?」です。</span><span class="sxs-lookup"><span data-stu-id="75586-110">The Handler will generate , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="75586-111">ハンドラーが生成されます"を選択\*お客様の場所を [得意先コード] から = の 4」と、その文字列を使用して、データ ソースのクエリを実行するのには。</span><span class="sxs-lookup"><span data-stu-id="75586-111">The Handler will generate "SELECT \* FROM Customers WHERE CustomerID = 4" and use that string to query the data source.</span></span>

<span data-ttu-id="75586-112">新規 SQL ステートメントが Null 文字列 ("") の場合、このセクションは無視されます。</span><span class="sxs-lookup"><span data-stu-id="75586-112">If the new SQL statement is the null string (""), then the section is ignored.</span></span>

<span data-ttu-id="75586-p104">新規 SQL ステートメント文字列が有効なステートメントでない場合、ステートメントの実行は失敗します。また、クライアント パラメーターは無視されます。このことを利用して、すべてのクライアント SQL コマンドを意図的に "無効" にするために次のような指定を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="75586-p104">If the new SQL statement string is not valid, then the execution of the statement will fail. The client parameter is effectively ignored. You can do this intentionally to "turn off" all client SQL commands by specifying:</span></span>

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a><span data-ttu-id="75586-116">構文</span><span class="sxs-lookup"><span data-stu-id="75586-116">Syntax</span></span>

<span data-ttu-id="75586-117">置き換える SQL 文字列エントリの形式は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="75586-117">A replacement SQL string entry is of the form:</span></span>

<span data-ttu-id="75586-118">**SQL = \* sqlString**\*</span><span class="sxs-lookup"><span data-stu-id="75586-118">**SQL=\*sqlString**\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75586-119">パーツ</span><span class="sxs-lookup"><span data-stu-id="75586-119">Part</span></span></p></th>
<th><p><span data-ttu-id="75586-120">説明</span><span class="sxs-lookup"><span data-stu-id="75586-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75586-121"><strong>SQL</strong></span><span class="sxs-lookup"><span data-stu-id="75586-121"><strong>SQL</strong></span></span></p></td>
<td><p><span data-ttu-id="75586-122">これが SQL セクション エントリであることを示すリテラル文字列。</span><span class="sxs-lookup"><span data-stu-id="75586-122">A literal string that indicates this is an SQL section entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75586-123"><strong><em>sqlString</em></strong></span><span class="sxs-lookup"><span data-stu-id="75586-123"><strong><em>sqlString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="75586-124">クライアント文字列を置き換える SQL 文字列。</span><span class="sxs-lookup"><span data-stu-id="75586-124">An SQL string that replaces the client string.</span></span></p></td>
</tr>
</tbody>
</table>

