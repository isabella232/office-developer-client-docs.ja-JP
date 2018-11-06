---
title: Connection.CreateQueryDef メソッド (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 681da274ab1f709da2eb614df038e6aa492a224a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997253"
---
# <a name="connectioncreatequerydef-method-dao"></a><span data-ttu-id="55b1a-102">Connection.CreateQueryDef メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="55b1a-102">Connection.CreateQueryDef method (DAO)</span></span>

<span data-ttu-id="55b1a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="55b1a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="55b1a-104">新しい **[QueryDef](querydef-object-dao.md)** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="55b1a-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b1a-105">構文</span><span class="sxs-lookup"><span data-stu-id="55b1a-105">Syntax</span></span>

<span data-ttu-id="55b1a-106">*式*です。CreateQueryDef (***名前***、 ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="55b1a-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="55b1a-107">\*式\***接続**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="55b1a-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="55b1a-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="55b1a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55b1a-109">名前</span><span class="sxs-lookup"><span data-stu-id="55b1a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="55b1a-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="55b1a-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="55b1a-111">データ型</span><span class="sxs-lookup"><span data-stu-id="55b1a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="55b1a-112">説明</span><span class="sxs-lookup"><span data-stu-id="55b1a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55b1a-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="55b1a-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="55b1a-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="55b1a-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="55b1a-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="55b1a-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="55b1a-116">新しい <strong>QueryDef</strong> の一意の名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="55b1a-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55b1a-117"><em>SQLText</em></span><span class="sxs-lookup"><span data-stu-id="55b1a-117"><em>SQLText</em></span></span></p></td>
<td><p><span data-ttu-id="55b1a-118">省略可能</span><span class="sxs-lookup"><span data-stu-id="55b1a-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="55b1a-119"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="55b1a-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="55b1a-p101"><strong>QueryDef</strong> を定義する SQL ステートメントを表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。この引数を省略した場合、コレクションへの追加前または追加後に、<strong><a href="querydef-sql-property-dao.md">SQL</a></strong> プロパティを設定して、<strong>QueryDef</strong> を定義できます。</span><span class="sxs-lookup"><span data-stu-id="55b1a-p101">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>. If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="55b1a-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="55b1a-122">Return value</span></span>

<span data-ttu-id="55b1a-123">QueryDef</span><span class="sxs-lookup"><span data-stu-id="55b1a-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="55b1a-124">注釈</span><span class="sxs-lookup"><span data-stu-id="55b1a-124">Remarks</span></span>

<span data-ttu-id="55b1a-125">Microsoft Access ワークスペースでは、 **QueryDef** の作成時に名前として長さ 0 の文字列以外を指定すると、作成された **QueryDef** オブジェクトが **[QueryDefs](querydefs-collection-dao.md)** コレクションに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="55b1a-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="55b1a-126">Name で指定されたオブジェクトが既に**QueryDefs**コレクションのメンバーである場合、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="55b1a-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="55b1a-127">一時**クエリ定義**を作成するには、 **CreateQueryDef**メソッドを実行すると、引数 name に長さ 0 の文字列を使用します。</span><span class="sxs-lookup"><span data-stu-id="55b1a-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="55b1a-128">新しく作成した [QueryDef](connection-name-property-dao.md) の \*\*\*\*Name\*\*\*\* プロパティを長さ 0 の文字列 ("") に設定することにより、これを行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="55b1a-128">You can also accomplish this by setting the **[Name](connection-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> <span data-ttu-id="55b1a-129">一時的な **QueryDef** オブジェクトは、 **QueryDefs** コレクション内に新しい永続的オブジェクトを作成せずに動的 SQL ステートメントを繰り返し使用する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="55b1a-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="55b1a-130">長さ 0 の文字列は永続的な **QueryDef** オブジェクトの有効な名前ではないので、一時的な **QueryDef** をコレクションに追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="55b1a-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="55b1a-131">新しく作成した **QueryDef** オブジェクトの **Name** プロパティと **SQL** プロパティはいつでも設定が可能であり、設定後に **QueryDef** を **QueryDefs** コレクションに追加できます。</span><span class="sxs-lookup"><span data-stu-id="55b1a-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="55b1a-132">**QueryDef** オブジェクトで SQL ステートメントを実行するには、 **[Execute](connection-execute-method-dao.md)** メソッドまたは **[OpenRecordset](connection-openrecordset-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="55b1a-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](connection-execute-method-dao.md)** or **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="55b1a-133">ODBC データベースを使用して SQL パススルー クエリを実行する場合は、 **QueryDef** オブジェクトの使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="55b1a-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="55b1a-134">Microsoft Access データベース エンジンのデータベースで **QueryDefs** コレクションから **QueryDef** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="55b1a-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

