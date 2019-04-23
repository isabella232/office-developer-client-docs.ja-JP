---
title: Parameter メンバー (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25eae70d88307331c44983c4e7cbbcce3fe9d309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288113"
---
# <a name="parameter-members-dao"></a><span data-ttu-id="20455-102">Parameter メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="20455-102">Parameter members (DAO)</span></span>

<span data-ttu-id="20455-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="20455-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20455-104">Parameter オブジェクトは、クエリに指定する値を表します。</span><span class="sxs-lookup"><span data-stu-id="20455-104">A Parameter object represents a value supplied to a query.</span></span> <span data-ttu-id="20455-105">パラメーターは、パラメーター クエリを基に作成した QueryDef オブジェクトに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="20455-105">The parameter is associated with a QueryDef object created from a parameter query.</span></span>

## <a name="properties"></a><span data-ttu-id="20455-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="20455-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20455-107">名前</span><span class="sxs-lookup"><span data-stu-id="20455-107">Name</span></span></p></th>
<th><p><span data-ttu-id="20455-108">説明</span><span class="sxs-lookup"><span data-stu-id="20455-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20455-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span><span class="sxs-lookup"><span data-stu-id="20455-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span></span></p></td>
<td><p><span data-ttu-id="20455-110"><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="20455-110"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="20455-111">Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="20455-111">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="20455-112"><strong><a href="parameter-object-dao.md">Parameter</a></strong> オブジェクトが入力パラメーター、出力パラメーター、その両方、またはプロシージャからの戻り値のいずれを表すかを示す値を設定または取得します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="20455-112">Sets or returns a value that indicates whether a <strong><a href="parameter-object-dao.md">Parameter</a></strong> object represents an input parameter, an output parameter, both, or the return value from the procedure (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20455-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="20455-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="20455-114">指定したオブジェクトの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20455-114">Returns the name of the specified object.</span></span> <span data-ttu-id="20455-115">読み取り専用 <strong>文字列</strong> です。</span><span class="sxs-lookup"><span data-stu-id="20455-115">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20455-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="20455-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="20455-p104">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="20455-p104">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20455-119"><strong><a href="parameter-type-property-dao.md">種類</a></strong></span><span class="sxs-lookup"><span data-stu-id="20455-119"><strong><a href="parameter-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="20455-120">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="20455-120">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="20455-121">読み取り/書き込みの <strong>整数</strong> です。</span><span class="sxs-lookup"><span data-stu-id="20455-121">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20455-122"><strong><a href="parameter-value-property-dao.md">Value</a></strong></span><span class="sxs-lookup"><span data-stu-id="20455-122"><strong><a href="parameter-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="20455-p106">オブジェクトの値を設定または取得します。値の取得および設定が可能です。バリアント型 (<strong>Variant</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="20455-p106">Sets or returns the value of an object. Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

