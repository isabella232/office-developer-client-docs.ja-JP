---
title: カスタマイズ ファイルの SQL セクション
TOCTitle: Customization File SQL section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ae259589cc8d4945068901c59105425599edc64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295136"
---
# <a name="customization-file-sql-section"></a><span data-ttu-id="113c6-102">カスタマイズ ファイルの SQL セクション</span><span class="sxs-lookup"><span data-stu-id="113c6-102">Customization File SQL section</span></span>


<span data-ttu-id="113c6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="113c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="113c6-p101">**sql** セクションには、クライアントのコマンド文字列を置き換える新規 SQL 文字列を含めることができます。このセクションに SQL 文字列がない場合、このセクションは無視されます。</span><span class="sxs-lookup"><span data-stu-id="113c6-p101">The **sql** section can contain a new SQL string that replaces the client command string. If there is no SQL string in the section, the section will be ignored.</span></span>

<span data-ttu-id="113c6-106">新しい SQL 文字列を*パラメーター化*することができます。</span><span class="sxs-lookup"><span data-stu-id="113c6-106">The new SQL string may be *parameterized*.</span></span> <span data-ttu-id="113c6-107">つまり、 **sql**セクションの sql 文字列 (' ? ' 文字で示される) のパラメーターは、クライアントのコマンド文字列 (かっこで囲まれたコンマ区切りのリストで指定されています) の*識別子*で、対応する引数によって置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="113c6-107">That is, parameters in the **sql** section SQL string (designated by the '?' character) can be replaced by corresponding arguments in an *identifier* in the client command string (designated by a comma-delimited list in parentheses).</span></span> <span data-ttu-id="113c6-108">The identifier and argument list behave like a function call.</span><span class="sxs-lookup"><span data-stu-id="113c6-108">The identifier and argument list behave like a function call.</span></span>

<span data-ttu-id="113c6-109">たとえば、クライアントのコマンド文字列が "CustomerByID (4)" で、sql セクションヘッダーが\[sql CustomerByID\]で、新しい SQL セクション文字列が "CustomerID = ? の\*顧客から選択" であるとします。</span><span class="sxs-lookup"><span data-stu-id="113c6-109">For example, assume the client command string is "CustomerByID(4)" , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="113c6-110">ハンドラーが生成するので、sql セクションヘッダー \[は sql\] CustomerByID で、新しい sql セクション文字列は "CustomerID \* : 得意先から選択してください = ?" です。</span><span class="sxs-lookup"><span data-stu-id="113c6-110">The Handler will generate , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="113c6-111">ハンドラーは、[CustomerID = \* 4 の顧客から選択] を生成し、その文字列を使用してデータソースに対してクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="113c6-111">The Handler will generate "SELECT \* FROM Customers WHERE CustomerID = 4" and use that string to query the data source.</span></span>

<span data-ttu-id="113c6-112">新規 SQL ステートメントが Null 文字列 ("") の場合、このセクションは無視されます。</span><span class="sxs-lookup"><span data-stu-id="113c6-112">If the new SQL statement is the null string (""), then the section is ignored.</span></span>

<span data-ttu-id="113c6-p104">新規 SQL ステートメント文字列が有効なステートメントでない場合、ステートメントの実行は失敗します。また、クライアント パラメーターは無視されます。このことを利用して、すべてのクライアント SQL コマンドを意図的に "無効" にするために次のような指定を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="113c6-p104">If the new SQL statement string is not valid, then the execution of the statement will fail. The client parameter is effectively ignored. You can do this intentionally to "turn off" all client SQL commands by specifying:</span></span>

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a><span data-ttu-id="113c6-116">構文</span><span class="sxs-lookup"><span data-stu-id="113c6-116">Syntax</span></span>

<span data-ttu-id="113c6-117">置き換える SQL 文字列エントリの形式は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="113c6-117">A replacement SQL string entry is of the form:</span></span>

<span data-ttu-id="113c6-118">**SQL = \* sqlString**\*</span><span class="sxs-lookup"><span data-stu-id="113c6-118">**SQL=\*sqlString**\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="113c6-119">パーツ</span><span class="sxs-lookup"><span data-stu-id="113c6-119">Part</span></span></p></th>
<th><p><span data-ttu-id="113c6-120">説明</span><span class="sxs-lookup"><span data-stu-id="113c6-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="113c6-121"><strong>SQL</strong></span><span class="sxs-lookup"><span data-stu-id="113c6-121"><strong>SQL</strong></span></span></p></td>
<td><p><span data-ttu-id="113c6-122">これが SQL セクション エントリであることを示すリテラル文字列。</span><span class="sxs-lookup"><span data-stu-id="113c6-122">A literal string that indicates this is an SQL section entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="113c6-123"><strong><em>sqlString</em></strong></span><span class="sxs-lookup"><span data-stu-id="113c6-123"><strong><em>sqlString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="113c6-124">クライアント文字列を置き換える SQL 文字列。</span><span class="sxs-lookup"><span data-stu-id="113c6-124">An SQL string that replaces the client string.</span></span></p></td>
</tr>
</tbody>
</table>

